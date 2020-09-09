# Sample React App Deploy to gh-pages

Bootstrapped by `create-react-app`

## Install the app using the command
`npx create-react-app yourprojectname`

## Go to your project
`cd yourprojectname`

## Intall gh-pages
`npm install gh-pages`

## Add homepage to `package.json`

`"hompage":"https://yourgithubusername.io/yourprojectname"`

example:
`"homepage":"https://tradecoder.github.io/react-gh-pages"`

## Add below code to the script section of `package.json`

```
"predeploy":"npm run build",
"deploy":"gh-pages -d build"
```

If you do not delete any code from the package.json file from the script,
your code may look like this after adding the above properties

```
 "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject",
    "predeploy":"npm run build",
    "deploy":"gh-pages -d build"
  }
```

## Create a git repo 
`git init`

## Add your github project remote url
`git remote add origin https://github.com/yourgithubusername/yourprojectname.git`

We are adding our own
`git remote add origin https://github.com/tradecoder/react-gh-pages`

## Setup is ok, now deploy your app to github gh-pages
`npm run deploy`

Visit your project using the homepage you set earlier

## Upload the source code to github
`git add --all`
Then `git commit -m 'your message here'`
Then `git push origin master`

Source code uploaded to your github master branch

## Done
