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

APRIL 8TH 2019
Still on robofriends app.
Tachyons works like bootstraps, having predefined templates.
Fro the dir of robofriends, do
npm install tachyons.
Next go to package.json file to confirm a new version of tachyons was installed.
NEXT
In index.js, do
import 'tachyons';
NEXT
we want to center the Hello world using tachyons. Go to hello.js and type
<div class='f1 tc'>
 f1 means Font 1 and tc means TEXT Center
 Now do npm start and Hello World will be centred.
 React uses JSX as virtual DOM
 Now if you check console, you will see 
 <div class='f1 tc'> gave an error on class.
  It should be ClassName as Class is a reserved word though the code ran.
  Now change it to
  <div className='f1 tc'>
   
   NEXT
   We can add prop or properties within the Hello component. Go to index.js and change 
   
   
   ReactDOM.render(<Hello />, document.getElementById('root'));
   
   
   TO
   
   
   ReactDOM.render(<Hello greeting = {'Hello' + 'React Ninja'} />, document.getElementById('root'));
   
   
Now we have given it a "greeting" prop to  "Hello", we now have access to use props in "Hello.js". so we can edit as follow;

<p>Welcome to React</p>

TO

<p>{this.props.greeting}</p>

AND SAVE

this= this object Hello....has props that is greeting
Now, you can see the code as function. Lets make it a function to give same result

class Hello  extends Component {
    render() {
      return (
       <div className='f1 tc'>
           <h1>Hello World</h1> 
           <p>{this.props.greeting}</p>
        </div> 
       );
       
       TO
       
  const Hello  = (props) => {
      return (
       <div className='f1 tc'>
           <h1>Hello World</h1> 
           <p>{props.greeting}</p>
        </div> 
       );
    }

export default Hello;     
       
   
