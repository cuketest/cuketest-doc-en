# NPM Package Downloads

### Download Packages
After a project is created, packages need to be downloaded before you can run the test script. You can download NPM packages using external NPM command.

If you are familiar with Node.js development, the concept will be familiar to you, and this is equivalent to running `"npm install"` command in console window.

You can download dependencies packages with the command line `npm install`

   1. In CukeTest, right-click in the blank area of the file browser and select [Show in Cmd Window]. The command line window will open and the current directory is the project root directory.  
   
   2. Run `npm install` command. You should run this command under the project root directory.

## Update Packages
Some browsers are updated very often, for example, Chrome and Firefox, and there need also an updated webdriver to work with them.

For example, it is a good practice to always have most recent chromedriver available with your test script. This can be done by update corresponding NPM packages to the latest version.

For example, when a web project is created, you have the following in package.json:

```json
   "dependencies": {
       "selenium-webdriver": "^3.6.0"
   }
```

After running "npm install" from command prompt, the version will be updated to "^3.6.0" (may be even higher when you read this). And 3.6.0 package is downloaded to the node_modules folder.

Occasionally, you want to stick to a certain version, to avoid problems in newer version, you can write the version as "3.6.0", which has no "^" with the version, then downloading will only download exact the same version, even there are newer version exists.

This is consistent with NPM, and for more information, please refer to [NPM docs](https://docs.npmjs.com/getting-started/using-a-package.json).
