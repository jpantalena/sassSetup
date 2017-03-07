# sassSetup
g41 exercise for setting up sass

Instructions for sass...

- express --git --hbs --css sass
- npm install
- change style.sass extension to scss
- in app.js change line 26 indentedSyntax to false
- add a dev script to start with nodemon


package.json
```javascript
{
  "name": "app",
  "version": "0.0.0",
  "private": true,
  "scripts": {
  "start": "node ./bin/www",
  "dev": "nodemon ./bin/www"
  },
  "dependencies": {
  "body-parser": "~1.15.2",
  "cookie-parser": "~1.4.3",
  "debug": "~2.2.0",
  "express": "~4.14.0",
  "hbs": "~4.0.1",
  "morgan": "~1.7.0",
  "node-sass-middleware": "0.9.8",
  "serve-favicon": "~2.3.0"
  },
  "devDependencies": {
  "nodemon": "^1.11.0"
  }
}
```

- touch public/stylesheets/reset.scss find Eric Meyer reset and paste the entire reset into reset.scss

- touch views/layout.hbs
```javascript
<!DOCTYPE html>
<html>
  <head>
         <title>{{title}}</title>
         <link rel='stylesheet' href='/stylesheets/style.css' />
  </head>

  <body>
  <header>
      <h1>sass setup</h1>
      </header>
  <main>
      {{{body}}}
  </main>
  <footer>
      <small>&copy; g41</small>
  </footer>
  </body>
</html>
```

- touch public/stylesheets/general.scss
```javascript
$dark-grey: #333;
$white: #FFF;

@import url('https://fonts.googleapis.com/css?family=Merriweather:300,400,400i,700');

body {
  font-family: Merriweather;
}

header {
  background-color: $dark-grey;
  color: $white;
  height: 45px;
  padding: 1rem;
  font-weight: 300;
}

main {
  padding: 1rem;
  min-height: calc(100vh - 90px);
}

footer {
  padding: 1rem;
  background-color: $dark-grey;
  color: $white;
  height: 45px;
}
```

- touch public/stylesheets/style.scss
     use style.scss as a container/coordinator
     in your style.scss import general.scss below the reset
```javascript
@import "reset";
@import "general";
```

- touch public/stylesheets/style.css
- find Eric Meyer reset and paste the entire reset into style.css


