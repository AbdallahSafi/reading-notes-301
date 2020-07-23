# Heroku

The use case is simple: You developed an application with your favorite front framework, and you want to test it in production and show it to your users and your mom without bothering with technicalities. Heroku allows you to serve your app directly from your remote repo in just seven steps, which are as follows.

1. Create the App on Heroku

Make sure everything is pushed to your GitHub or other remote repo before you begin. Run the command:

`$ heroku create`

This will create your app on Heroku (which prepares Heroku to receive your source code) and generates two links:

```
Creating app... done, ⬢ fakestuff-farboo-84560
https://fakestuff-farboo-84560.herokuapp.com/ | https://git.heroku.com/fakestuff-farboo-84560.git
```

2. Set the Node Server Configuration

`$ heroku config:set NPM_CONFIG_PRODUCTION=false`

This command will tell Heroku to install the devDependencies. More precisely, this skips the pruning step and accesses the packages declared under devDependencies at runtime. This enables Heroku to launch npm run build.

3. Listen to the Host 0.0.0.0

`$ heroku config:set HOST=0.0.0.0`

4. Run Node in Production Mode

`$ heroku config:set NODE_ENV=production`

5. Tell Heroku to Run “npm run build"

Then we need to add a script in our package.json file to tell Heroku to run npm run build. Just add the line "heroku-postbuild": "npm run build” to your "script" object in your package.json:

```
"scripts": {
  "dev": "nuxt",
  "build": "nuxt build",
  "start": "nuxt start",
  "generate": "nuxt generate",
  "lint": "eslint --ext .js,.vue --ignore-path .gitignore .",
  "heroku-postbuild": "npm run build"
}
```

6. Create a Procfile for Heroku

Heroku needs a Profile to execute and run our application. We just have to create a file with no extension at the root of our app folder, name it Procfile, and add the following line inside:

`web: npm run start`

npm run start is the script that fires the application, and web directs HTTP traffic to it.

7. Push Your GitHub Repo to Heroku to Deploy

Finally all that’s left to do is stage, commit, and push our configured app to Heroku:

```
$ git add Procfile
$ git commit -a -m "Configuration to deploy to heroku"
$ git push heroku master
```

And it’s live. The push-and-deploy process takes a few minutes, and then Heroku gives you the URL where you can see your app.
