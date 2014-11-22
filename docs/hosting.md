## Hosting MEAN

### Heroku
Before you start make sure you have the [Heroku toolbelt](https://toolbelt.heroku.com/)
installed and an accessible MongoDB instance - you can try [MongoHQ](http://www.mongohq.com/)
which has an easy setup).

Add the db string to the production env in server/config/env/production.js.

```bash
git init
git add .
git commit -m "initial version"
heroku apps:create
heroku config:add NODE_ENV=production
heroku config:add BUILDPACK_URL=https://github.com/mbuchetics/heroku-buildpack-nodejs-grunt.git
git push heroku master
heroku config:set NODE_ENV=production
```

### OpenShift

1. Register for an account on Openshift (http://www.openshift.com).
1. Create an app on Openshift by choosing a 'Node' type site to create. Create the site by making Openshift use Linnovate's Openshift git repo as its source code (https://github.com/linnovate/mean-on-openshift.git)
1. On the second screen after the new application has been created, add a Mongo database
1. When the site has been built, you can visit it on your newly created domain, which will look like my-domain.openshift.com. You may need to restart the instance on Openshift before you can see it. It will look like Mean.io boilerplate.
1. On your new app's console page on Openshift, make a note of the git repo where the code lives. Clone that repo to your local computer where your mean.io app codebase is.
1. Merge your completed local app into this new repo. You will have some conflicts, so merge carefully, line by line.
1. Commit and push the repo with the Openshift code back up to Openshift. Restart your instance on Openshift, you should see your site!
