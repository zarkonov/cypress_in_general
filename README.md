# Cypress project setup



## Installation
1. Create a new folder for your project, locally on your machine (for example New cypress project folder).
2. Install git.
3. Use the following link for [node](https://nodejs.org/en/download/)  installation in Windows OS.
4. Open Visual Studio Code.
5. Open the new  folder with new Cypress project.
6. Open the terminal in VSC within the new Cypress project folder.
7. Check you are positioned in the new Cypress project folder, by runing the following command in opened terminal
```bash
pwd
```
9. Run the following command  to setup npm package
```bash
npm init
```
10. Install cypress with the following command
```bash
npm install cypress 
```
12. After it's installation there is a new folder node_modules and a new file package-lock.json, available in your local repositorium cretaed for this project. 

13. Run the following command to install prettier
```bash
npm install prettier
```
and confirm in package.json file, that at its end "prettier" is defined.
14. In the root of  created repository, from VSC, below node_modules folder, create a file
```bash
.prettierrc
```
15. Open the .prettierrc file and add the following content to it:
```bash
{
    "trailingComma": "es5",
    "tabWidth": 2,
    "semi": false,
    "singleQuote": true,
    "useTabs": true,
    "bracketSpacing": true,
    "arrowParens": "avoid"
}
```
## Usage
1. Run  Cypress with the following command:
```bash
npx cypress open
```
2. After the command is executed, folder cypress is created in the new Cypress project repository.
3. Within Cypress folder  a new file - tscongfig.json should be open and edit.
4. Add the following content to the opened file tscongfig.json
```bash
{
    "compilerOptions": {
        "allowJs": true,
        "baseUrl": "../node_modules",
        "types": [
            "cypress"
        ],
        "outDir": "lib"
    },
    "include": [
        "**/*.*"
    ]
}
```
6.Modify the content of the package.json, to look like this:
```bash
{
  "name": "cypress_assignment",
  "version": "1.0.0",
  "description": "cypress automation ",
  "main": "index.js",
  "scripts": {
    "cy:open": "cypress open",
    "cy:run": "cypress run"
  },
  "keywords": [
    "test",
    "automation"
  ],
  "author": "ZN",
  "license": "ISC",
  "dependencies": {
    "cypress": "^9.5.3",
    "prettier": "^2.6.2"
  },
  "devDependencies": {
    "cypress-plugin-tab": "^1.0.5"
  }
}
```
By doing it, Cypress start is enabled with the command:
```bash
npm run cy:open
```
and headless mode is enabled, starting with the command
```bash
npm run cy:run
```
Your Cypress is set and ready to run!!!

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
This is licence free project.

## Appendix GIT porcelain commands (to be further updated)
git bash here

git init

git add .

git commit -m "initial commit"

git remote add origin https://github.com/zarkonov/cypress_in_general  - connects local and remote repo

git pull origin master  - pulls remote master and connect with local master repo

git push origin master  - push local master content to remote master 

git push --force origin master    - if above recalls the errors - only applicable at the project setup, do not force

git branch screenshots_after_test_run  - new branch is created screenshots_after_test_run

git checkout screenshots_after_test_run  - branch chenaged

change the code and tests, again:

git add . - adds changes to the staging area of the branch we checkout to

git commit -m "3 screenshots added after every test run"   - commit changes

git push --set-upstream origin screenshots_after_test_run            - push local branch to remote repo and make them to be aligned

On Bitbucket or Github click Git pull request and merge branch with master

git push --set-upstream origin master                - runs locally from master branch to follow the remote master branch
                               

