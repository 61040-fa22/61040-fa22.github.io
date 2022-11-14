---
title: Notes on Data Modeling
layout: page
parent: Resources
---

**Rationale**. Data modeling is a fundamental skill in software design. The idea is to be able to describe state without committing to a particular representation. This is important for the following reasons:

- When you’re designing software you want to separate essential and non-essential features. Details of representation don’t matter in the early stages of design, and they add clutter and potential confusion.

- When it comes to choosing a representation, you want to have a basic form that is free of any commitments as the starting point. If you started with a form that included representation details, you may not be able to transform it into other valid representations because they wouldn’t preserve some detail that is not in fact relevant.
- Being able to think about state in abstract terms helps you think clearly about design and convey your ideas succinctly. 

**History**. Data modeling has a long history. The key innovation was the invention of the entity relationship diagram, which was introduced to help in database design by expressing the data that needed to be stored from the particular schema devised to store it. Data modeling is central to all approaches to formal methods (such as Alloy, B, VDM and Z) and is central to the idea of abstract data types (in which values of a type are viewed not in terms of their representation but in terms of an abstract data model).

**A kind of rep**. One way to understand data models is that they’re a kind of representation themselves—but a very abstract one in which the only data types you have are primitives (eg, ints and strings), unspecified reference types (eg, User), and two constructors, sets and relations. 

**Sets are relations**. I use the term *relation model* for the kind of model I’m going to describe here, since you can think of the relation as the only constructor. A set is just a relation with one column. (Or, thinking of a relation as a set of tuples, a set is a relation whose tuples have just one element.)

**Using programming language constructors.** Some programmers get very comfortable with the constructors of particular programming languages and then they use those constructors for their data modeling. For example, you could build data models with the cons cells of Scheme, or the objects of JavaScript, or the hash maps of Java. But all of these contain implementation details that are avoided in sets and relations. For example, if you use cons cells to make a collection as a linked list, you’re implying that the order matters: you can’t describe a simple set of items in which the order is irrelevant.

**Example**. As a simple example of a data model, consider a *Label* concept in which labels are attached to items and can be either system or user labels. (The distinction might matter because system labels can be added but not removed, for example.) Here is a suitable data model:

	labels: Item -> set Label
	SystemLabel, UserLabel: set Label

The first line say that labels is a relation that maps items to labels; the set multiplicity says that each item can map to any number of labels. The second line says that SystemLabel and UserLabel are sets of labels. Our intent is that these sets are disjoint (a label can’t be both) and exhaustive (a label is one or the other), but the data model doesn’t say that. We can add that constraint as a comment (or it can be expressed formally in a language like Alloy).

**Meaning of relations**. The meaning of a relation declaration is very simple. It just introduces a state variable whose value is a binary relation, which is just a set of pairs (or if both sides have the same type, a directed graph). So a value of the labels variable might be

	{(i1, x1), (i2, x1), (i2, x2),}

in which item i1 has label x1, and item i2 has labels x1 and x2. Or you can think of this as a table:

| *Item* | *labels* | 
| ----- | ----- |
| i1 | x1 |
| i2 | x1 |
| i2 | x2 |

Either way, the key point is that this is an *explicit* but *abstract* way to view the state. Contrast this with a typical programming representation such as

	labels: Map [Item, Set[Label]]

which introduces a much more complicated structure (with map and set objects) and involves opaque rather than explicit structures. A mapping, for example, doesn’t have an explicit, visible structure as implied by a relation, but instead gives you an abstract data type on which you can apply various methods (such as *get*). 

Because a relation is an explicit, mathematical structure, you don’t need to be restricted by any methods that happen to be defined; you can use any of the standard mathematical operators to obtain new values by combining the relation with old values. In Alloy’s notation, for example, you can write the following expressions

	i.labels // the labels for item i
	S.labels // the labels of all items in set S
	labels.x // the items with label x
	labels.SystemLabel // the items that have system labels
	S - labels.SystemLabel // the items in S that don't have system labels

In this class, you don’t need to know how to use these operators.

**Other multiplicities**. In addition to *set* (meaning zero or more), you can also write *some* (one or more), *one* (exactly one) or *lone* (less than or equal to one). So 

	labels: Item -> one Label

says each item has exactly one label. And you can write multiplicities on both sides of an arrow, so 

	labels: Item lone -> set Label

says that each item has zero or more labels, and each label is associated with at most one item. You can use multiplicities for sets, so 

	SystemLabels: some Label

says that SystemLabels is a non-empty set.

By convention, if there is no multiplicity then, for relations, *set* is implied, so 

	labels: Item -> Label

is equivalent to 

	labels: Item -> set Label

For sets, the implied multiplicity is *one*, so 

	Root: Label

is equivalent to

	Root: one Label

**Defining updates**. In a programming language, you might be able to implement these declarations very directly using abstract types. If you had constructors Relation and Set, you could write:

	labels: Relation[Item, Label]
	SystemLabels, UserLabels: Set[Label]

and then you might even use object-oriented notation for describing state changes. For example, the action that adds a label to an item might be written like this:

	add (i: Item, x: Label)
	  labels.add_tuple (i, x)
	
But that’s pretty clunky, and since we already have the language of sets and relations and all their operators from discrete math, we can write the action like this

	add (i: Item, x: Label)
	  labels’ = labels U {(i, x)}
	
where labels’ is the value of the labels relation after. If you like you can use this conventional mathematical syntax. I prefer the operators of the Alloy modeling language which would let you write

	add (i: Item, x: Label)
	  labels’ = labels + i -> x

or, using a C-style shorthand

	add (i: Item, x: Label)
	  labels += i -> x

In your concept definitions in 6.1040, you don’t need to specify actions formally; you can just describe the update to the state variables informally:

	add (i: Item, x: Label)
	  add the tuple (i, x) to labels

**Relational databases**. It may be helpful to compare relational data models to the schemas of relational databases. In that context, each tables is a relation with multiple columns. Suppose we have some items, each with an owner and some labels. In a relational database, you might have a table like this

| *Item* | *Owner* | *Created* | 
| ----- | ----- |----- |
| i1 | u1 | d1 |
| i2 | u1 | d2 |

which says that item i1 is owned by user u1 and was created on date d1, and so on. Note that in this schema there is no relationship between owner and created, and it could be split into two separate tables:

| *Item* | *Owner* |
| ----- | ----- |
| i1 | u1 |
| i2 | u1 |

| *Item* | *Created* | 
| ----- | ----- |
| i1 | d1 |
| i2 | d2 |

That would be called a “fully normalized schema,” and corresponds to the data model

	owner: Item -> one User
	created: Item -> one Date

Here’s another table:

| *Item* | *Owner* | *Labels* | 
| ----- | ----- |----- |----- |
| i1 | u1 | x1 |
| i1 | u1 | x2 |

This says that item i1 has owner u1 and carries two labels x1 and x2. Here you can see that the lack of normalization is worse, because it leads to redundancy. In summary: a data model is like a relational schema that has been fully normalized. 

## Common mistakes

Here are some examples of common mistakes in data modeling.

**Booleans**. Booleans aren’t usually needed. Instead of

	isSystemLabel: Label -> one Bool
	
you should write 

	SystemLabel: set Label

Using sets rather than boolean functions lets you draw the state with a classification hierarchy, and it also makes expressions easier to write: for example,

	i.labels - SystemLabel
	
is the set of non-system labels of i (that is, the set of labels that you get by finding the labels of item i and then removing the system labels).

**Null values**. Sometimes components with a multiplicity of *lone* suggest that a subset should be introduced. Suppose you have this data model

	name: User -> one String
	password: User -> lone String
	email: User -> lone Email

saying that all users have a name, but only some have passwords and email. Dealing with the cases in which such values are missing can bring needless complexity. Instead, you might define a subset like this:

	name: User -> one String
	RegisteredUser: set User
	password: RegisteredUser -> one String
	email: RegisteredUser -> one Email

which says that registered users always have a password and email, so now you can just check whether a user is registered, and if they are, you know they have those values. This can be helpful in an implementation too: for example, in Mongo, you could create a collection for just registered users in which no fields are null.

**Needless classes**. Don’t introduce sets to model programming-language like classes (or Mongo-like collections). For example, these declarations introduce a set of labeling objects and then give each of them an item and a label:

	labelings: set Labelings
	item: Labeling -> one Item
	label: Labeling -> one Label

The Labeling object is just the tuple of our binary relation, and it’s better and easier to write instead

	labels: Item -> Label

Sometimes you do actually need to introduce a set that models a set of tuples. This happens when you want a relation over more than two things. For example, suppose you want the state to include the data that a label was added to an item. You could write

	labelings: set Labelings
	item: Labeling -> one Item
	label: Labeling -> one Label
	date: Labeling -> one Date

Even here you could just use a relation with three columns

	labels: Item -> Label -> Date

but that’s a more advanced form of modeling that can be avoided (and also has the disadvantage of not having a graphical correspondence, since if you stick to binary relations the data model can be drawn as a graph with a labeled edge for each relation).

The problem of needless classes becomes more acute when it implies a relationship that doesn’t exist. Suppose you wrote 

	infos: set ItemInfo
	item: ItemInfo -> one Item
	labels: ItemInfo -> set Label
	owner: ItemInfo -> one Owner

because you were thinking of a collection in Mongo in which each member of the collection is a document that has an item as its key and also carries the labels of the item and the item’s owner.

This is really bad, because it suggests a bogus relationship between the owner and the labels. But of course you could represent this in an implementation with two separate collections, one with items/labels and one with items/owners. The correct data model 

	labels: Item -> Label
	owner: Item -> one Owner

makes it clear you can do that, but this confused model doesn’t.

**Redundant relations**. The beauty of relations is that (unlike programming language types like maps) they don’t imply any particular navigation direction. If you declare

	labels: Item -> Label
	
then you can refer to the items with a particular label x, or the labels of a particular item i (which would be written in Alloy as labels.x and i.labels). You don’t need to include another relation

	items: Label -> Item

just because an action might need to navigate from labels to items.

**Being too concrete**. In your implementation, every type is ultimately built from primitive types. Don’t feel you need to include these in your data model when they’re not essential for describing functionality. For example, if you want to store when an item was created, it’s sufficient to assume an abstract set of Date objects, and just write

	created: Item -> one Date

rather than

	created_unix_seconds: Item -> one Double
	
or even worse

	created_DD, created_MM, created_YY: Item -> one String

which not only introduces implementation choices, but bad ones.

## Some Tips on MongoDB Schema Design

Database design is a big topic that we don’t have time to cover in this class, but here are a few tips for thinking about translating data models into MongoDB schemas.

**Concept modularity**. The division of your app into concepts already gives you a head start on the schema design. Build separate collections for each concept, using views and query joins if you need to navigate across concepts.

**Documents as entities**. Suppose you have some state components like this 

	username: User -> one String
	displayname: User -> one String
	password: User -> one String
		
that map a single type to one or at most one value of some other types. These can be see as an “entity class” and represented easily as a collection of documents with the right hand sides of the relations as fields.

**Many-to-many relations**. A relation such as

	tickets: User -> set Ticket
	
can be represented in a document for *User* by an array field (of Tickets). One problem with this representation is that querying by ticket won’t be very efficient, as it will require a scan of all the user records, and then a traversal through each array. To mitigate this, you can create an index to speedup the lookup.

Alternatively, if the relation is one-to-many (and not many-to-many), you can instead take the transpose
	
	owner: Ticket -> one User
	
and represent that as a field of a document for *Ticket*, so that lookups by Ticket no longer require any searching. For more advanced advice on representing relations that map to many things, see [this article](https://www.mongodb.com/blog/post/6-rules-of-thumb-for-mongodb-schema-design-part-1).
	
**Preserving invariants**. If there are invariants that cover your state components, it’s good to put all the components relevant to an invariant in a single document. For example, if your data model included

	region: User -> one Region
	address: User -> one Address

and a user’s region is based on their address, you’d want to put them in the same document so they could be updated together. Otherwise you’ll have to ensure that two documents are updated in concert, and that’s harder to do.

**Read-only components**. If some components are read-only, you may want to factor them into their own document. Then you won’t need to lock them needlessly when other state components are being updated, potentially damaging performance. For example, if you had

	username: User -> one String
	role: User -> one Role
	password: User -> one Password

and a user can change their password but not their role or username, you could create two separate document types, one with a password field and one with the username and role fields.

