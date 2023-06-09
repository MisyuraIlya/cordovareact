
1. npx create-react-app .
2. git add .
3. git commit -m "first init"
4. npm run eject
5. edit in config-> paths.js 
change the line
appBuild: resolveApp('www')

6. package.json add new line
"homepage":"./"

7. execute in terminal
cordova create cordovareactapp com.exnaple.cordovareactapp CordovaApp

8. mv config.xml ..
9. change the index.js in react for this

import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';
import reportWebVitals from './reportWebVitals';

const startApp = () => {
  const root = ReactDOM.createRoot(document.getElementById('root'));
  root.render(
    <React.StrictMode>
      <App />
    </React.StrictMode>
  );
}

if(window.cordova) {
  document.addEventListener('deviceready', startApp, false);
} else {
  startApp()
}



10. add from the cordova index.html to react index.html the meta and script below


dependencies  Gradle 7.6
 java 8
 SDK android studio
11. cordova platform add android@9.1.0
12. cordova build android
13. cordova run android --device

