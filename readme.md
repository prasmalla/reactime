<p align="center">
  <img src ="./assets/readme-logo-svg.svg" width="300"/>
</p>

<h1 align="center">State Debugger for React</h1>

[![GitHub](https://img.shields.io/github/license/oslabs-beta/reactime)](https://github.com/oslabs-beta/reactime)
[![Build Status](https://travis-ci.com/oslabs-beta/reactime.svg?branch=master)](https://travis-ci.com/oslabs-beta/reactime)
[![npm version](https://badge.fury.io/js/reactime.svg)](http://badge.fury.io/js/reactime)
[![Dependencies](https://david-dm.org/oslabs-beta/reactime.svg)](https://david-dm.org/oslabs-beta/reactime#info=dependencies)
[![DevDependencies](https://david-dm.org/oslabs-beta/reactime/dev-status.svg)](https://david-dm.org/oslabs-beta/reactime?type=dev)
[![Vulnerabilities](https://snyk.io/test/github/oslabs-beta/reactime/badge.svg)](https://snyk.io/test/github/oslabs-beta/reactime)
<p align="center">
<a href="https://nodei.co/npm/reactime/"><img src="https://nodei.co/npm/reactime.png"></a>

  <img src="demo.gif" alt="Demo of Reactime" style="width: 55%">
</p>

Reactime is a debugging tool for React developers. It records state whenever it is changed and allows the user to jump to any previously recorded state.

This dev tool is for React apps using stateful components and prop drilling, and has beta support for Context API, conditional state routing, Hooks (useState, useEffect) and functional components. 

One thing to note is that this library does not work well when mixing React with direct DOM manipulation.

Two parts are needed for this tool to function. The <a href="https://chrome.google.com/webstore/detail/react-time-travel/cgibknllccemdnfhfpmjhffpjfeidjga"><strong>chrome extension</strong></a> must be installed, and the <a href="https://www.npmjs.com/package/reactime"><strong>NPM package</strong></a> must be installed and used in the React code.

After successfully installing the chrome extension, you can test Reactime functionalities in the demo repositories below.

- <a href="http://reactime-demo1.us-east-1.elasticbeanstalk.com/">Calculator</a>
- <a href="http://reactime-demo2.us-east-1.elasticbeanstalk.com/">Bitcoin Price Index</a>

## Installing

1. Download the [extension](https://chrome.google.com/webstore/detail/reactime/cgibknllccemdnfhfpmjhffpjfeidjga) from Chrome Web Store.

2. Install the [npm package](https://www.npmjs.com/package/reactime) in your code.

```
npm i reactime
```

3. Call the library method on your root container after rendering your App.

```
const reactime = require('reactime');

const rootContainer = document.getElementById('root');
ReactDOM.render(<App />, rootContainer);

reactime(rootContainer);
```

4. Done! That's all you have to do to link your React project to our library.

## How to Use

After installing both the Chrome extension and the npm package, just open up your project in the browser.

Then open up your Chrome DevTools. There'll be a new tab called Reactime.

## Features

### Recording

Whenever state is changed (whenever setState or useState is called), this extension will create a snapshot of the current state tree and record it. Each snapshot will be displayed in Chrome DevTools under the Reactime panel.

### Viewing

You can click on a snapshot to view your app's state. State can be visualized in a JSON or a tree. Also, snapshots can be diffed with the previous snapshot, which can be viewed under the Diff tab.

### Jumping

Jumping is the most important feature of all. It allows you to jump to any previous recorded snapshots. Hitting the jump button on any snapshot will change the DOM by setting their state.

### And Much More

- multiple tree graph branches depicting state changes
- tree graph hover functionality to view state changes 
- ability to pan and zoom tree graph
- multiple tabs support
- a slider to move through snapshots quickly
- a play button to move through snapshots automatically
- a pause button, which stops recording each snapshot
- a lock button to freeze the DOM in place. setState will lose all functionality while the extension is locked
- a persist button to keep snapshots upon refresh (handy when changing code and debugging)
- export/import the current snapshots in memory

## Authors

- **Ryan Dang** - [@rydang](https://github.com/rydang)
- **Bryan Lee** - [@mylee1995](https://github.com/mylee1995)
- **Josh Kim** - [@joshua0308](https://github.com/joshua0308)
- **Sierra Swaby** - [@starkspark](https://github.com/starkspark)
- **Ruth Anam** - [@peachiecodes](https://github.com/peachiecodes)
- **David Chai** - [@davidchaidev](https://github.com/davidchaidev)
- **Yujin Kang** - [@yujinkay](https://github.com/yujinkay)
- **Andy Wong** - [@andywongdev](https://github.com/andywongdev)
- **Chris Flannery** - [@chriswillsflannery](https://github.com/chriswillsflannery)
- **Rajeeb Banstola** - [@rajeebthegreat](https://github.com/rajeebthegreat)
- **Prasanna Malla** - [@prasmalla](https://github.com/prasmalla)
- **Rocky Lin** - [@rocky9413](https://github.com/rocky9413)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
