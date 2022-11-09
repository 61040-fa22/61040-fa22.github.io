---
title: Final project deployment guidance
layout: page
parent: Resources
---

For the final project you will have the freedom to choose where your application will be deployed. We'll give a few options here, but you may choose any provider that allows your application to be publicly accessible.

## Vercel (recommended)
We recommend continuing to use Vercel since you all have experience with it from the individual assignments. We'll also only be able to guarantee staff support for this option. However, it has a few limitations you may want to take into account:
*  First, each server execution is limited to 10 seconds, so it may be difficult to implement real-time functionality that requires persistent connections (e.g. WebSockets).
*  Additionally, the free plan only allows one user from each team to deploy.
    *  To work around this, we recommend creating a shared GitHub and Vercel account for your team, so that all team members will be able to deploy. We recommend that you make your own Moira mailing list for your team.

### Making a mailing list
* Navigate to this [site](https://listmaker.mit.edu/lc/) and click Moira for "Choose the type of list you desire:"
* Fill out Name of list, Description, and List owner (you can use the MIT username of any of your teammates). Leave the default options, and click next.
* Confirm selections and click next.
* Congrats, you have made a mailing list!
### Making accounts for your team
* Now using the address associated with this list, [sign up](https://vercel.com/signup/email?) for a new Vercel account.
* Sign up with your mailing list email, e.g. 61040-utas-test@mit.edu.
* Similarly, [sign up](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home) for a new Github account.


## Heroku (difficulty: medium)
Heroku is more flexible than Vercel. So if your team is trying to utilize something that Vercel does not provide (e.g., WebSocket), then deploying with Heroku can be useful. 

### Getting the Student Offer
The student offer is only needed after Nov 28 when the free plan expires, but since it takes several days to get approval, we suggest you do it earlier.

**Step 1. Sign up for [GitHub Student Developer Pack](https://education.github.com/discount_requests/pack_application)**
This might take 1~3 days for approval from GitHub.


**Step 2. Once you get approval from GitHub, apply for [Heroku Student Offer](https://www.heroku.com/github-students/signup)**
It takes up to 24 hours for the credits to be applied to your account.

### Deploying your website

**Step 3. Modify api/index.ts in your code**

Please modify your `api/index.ts` file as below. You can copy and paste these text!

```typescript=
// Add this line at the top
import path from "path";

…

// Add the following lines
const isProduction = process.env.NODE_ENV === 'production';
const vuePath = path.resolve(__dirname, "..", "client", isProduction ? "dist" : "public");
app.use(express.static(vuePath));
app.get("*", (req, res) => {
  res.sendFile(path.join(vuePath, "index.html"));
});

// Comment out the following lines
// app.all('*', (req: Request, res: Response) => {
//   res.status(404).json({
//     error: 'Page not found'
//   });
// });
```

**Step 4. [Create a new app](https://dashboard.heroku.com/apps) on Heroku**

Press the button “New” at the top right corner of the dashboard, and click on “Create a new app.” Name your app and choose US as the region.


**Step 5. Add a remote to your local repository**

Git remotes are versions of your repository that live on other servers. You deploy your app by pushing its code to a special Heroku-hosted remote that’s associated with your app. 

First, log in to Heroku.

```shell=
$ heroku login
```

Then add a remote using the following command.

```shell=
$ heroku git:remote -a your-app-name
```

**Step 6. Deploy your code**

First, change the NPM config mode. This makes sure that Heroku also installs devDependencies, not just dependencies in your `package.json`

```shell=
$ heroku config:set NPM_CONFIG_PRODUCTION=false
```

Then you can use the following command to deploy your code

```shell
$ git push heroku main
```

Or if you want to deploy from a non-main branch of your local repository, use this command instead.

```shell
$ git push heroku branch-name:main
```

**Step 7. Go to the settings tab of your app, and set the config variables**
All the variables you had in your .env file should be updated here such as MONGO_SRV.

![config](https://i.imgur.com/7gAZRrm.png)


### Upgrading the dyno type

Go to the resources tab to change the dyno type. You don’t need to change the dyno type until Nov 28. But starting Nov 28, the free plan will no longer be available, so you need to upgrade it using your student offer.

To upgrade the plan, go to the resources tab and click on “change dyno type.” Then you will see a modal as below.

![modal](https://i.imgur.com/3hF7qDp.png)

You will receive credits worth $13 USD per month for 12 months (for a total value of $156 USD). This is enough to cover one month of the Eco Dynos plan ($5/month) or the Hobby Dynos plan ($7/month). 

![plan](https://i.imgur.com/OVh8pjd.png)




## AWS (difficulty: hard)
This option will require the most setup work but will also give you complete control over the environment your app is running in. You will need to start up an EC2 instance and install any software necessary to run your app. The [free tier](https://aws.amazon.com/free/) will be sufficient for this project.

## Personal VPS (difficulty: advanced)

NOTE: I can delete this if this is too big brain -cynthia
maybe this can be merged with the AWS section -zach

If one of your team members manages their own virtual private server (VPS), consider asking them to host your group project there, as VPSes offer the most flexibility in supporting all sorts of server-side technologies. **However, you must have extensive system administration experience (Unix, Nginx/Apache, daemons) to proceed with this option**; most of the staff do not have experience hosting on VPSes and thus may not be able to fully support you. If you decide to proceed with this option, [pm2](https://pm2.keymetrics.io/) is a great tool for maintaining the uptime on the process running your webserver. 