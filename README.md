STEP 1) INSTALL REACT
$ npm install -g create-react-app

STEP 2) CREATE PROJECT FOLDER
$ create-react-app robofriends

cd into robofriends and see packages, react and dependencies already created. A robofriends folder is also created in your dir. Now drag the folder to submlime text

$ ls
node_modules/  package.json  package-lock.json  public/  README.md  src/

Open the robofriends or newreact folder in Sublime text. Check json file to see all the dependencies created etc

package-lock.json file has all the version nos of your dependencies and makes sure they are locked in

.gitignore: It has files it has to ignore. It is auto generated

STEP 3)
$ npm start

> newreact@0.1.0 start C:\Users\AbdulRahman Abu\desktop\newreact
> react-scripts start

 Starting the development server...

Compiled with warnings.
......

The browser will be loaded and the react engine and logo shows

If you need to update your version of React, you go to the package.json file to edit the versions to the latest versions. Once you finish editing the react script, save and run 
npm install 
while in the folder eg robofriends dir. That will install latest version of create-react-app.
Then to confirm it is working, run
npm start

Now lets create a project, run
$ create-react-app newreact
Then check the package.json file to see it is the latest version of react. Then run
$ npm start

NOW LETS CREATE OUR OWN COMPONENT CALLED HELLO(from robofriends folfolder in sublime text)
Go to index.js file and edit 
ReactDOM.render(<App/>, document.getElementById('root'));

TO

ReactDOM.render(<hello/>, document.getElementById('root'));.

then replace
import App from './App';   WITH

import Hello from './Hello.js';

NOTE: Every component is capitalised
Now go to src and create hello.js file

NOTE:
ReactNative is for mobile phones
React is a View Library. It does the Dom manipulation
ReactDOM is used for the DOM website
Import './index.css'; means ./ it is in the same dir
reisterServiceWorker makes our   app work faster offline
import App from './App'; same as App.js. Putting js refers to same file

class App extends Component {
  render() {...
Remember Component must always render something

NEXT STEP
Open hello.js, import react and component.
NB: You can copy this from App.js
import React, { Component } from 'react';

Now if we want another file to use this, we have to export it
export default Hello;
NOTE: 
To start our server, do npm start
