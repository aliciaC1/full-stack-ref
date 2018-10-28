# React 

## Create a project in Github and deploy to GH pages

1. Run: " yarn create react-app my-app "

2. Go to github pages and create a new repository

3. Copy the address to the repo

4. Run: " git remote add origin <and paste the url from github> "

5. Run: " git remote -v " to check the origin of the fetch and push

6. Run: " git push origin master "

7. Go to the readme and click on "GitHub Pages"

8. Copy and paste 'homepage": "https://myusername.io/myapp" ' to the package.json on the bottom after the ] on the      bottom of the browser list section. Change the username and myapp to appropriate names

9. Install the gh-pages module. Either npm install --save gh-pages || yarn add gh-pages

10. Copy and paste "predeploy": "npm run build",
                   "deploy": "gh-pages -d build"
    * Should be added in the "scripts" section underneath "eject: "react-scripts eject"

11. Run: " yarn run deploy "

12. Make sure the source in the GH settings section is set to gh-pages branch.