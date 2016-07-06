Finance-IONIC2
=====================
Ionic v2 study project repo
<br><br>


#### Guess about Ionic 2
------------------------
Start a new project

```bash
    $ ionic start ProjectName blank --v2
```

Run it as server app
-- <cite>now the ionic compile the files and generate the www/build files</cite>

```bash
    $ ionic serve --lab
```
<br><br>


#### Guess TypeScript
---------------------
It first space is for IMPORTs 
-- <cite>include dependencies, just like module did before</cite>

```TypeScript
    import {Component} from '@angular/core';
    import {Platform, ionicBootstrap} from 'ionic-angular';
    import {StatusBar} from 'ionic-native';
    import {HomePage} from './pages/home/home';
```

It second space is the Decorator
-- <cite>indicate what this class is (which type), in that case it is a Component</cite>
```TypeScript
    @Component({
      // use templateUrl to define a complext template (a file), otherwise use just template
      template: '<ion-nav [root]="rootPage"></ion-nav>'
    })
```

It third space is the Class
-- <cite>to set the rootPage, which means the initial page, is necessary to import it</cite>
```TypeScript
    export class MyApp {
      rootPage: any = HomePage;
    
      constructor(platform: Platform) {
        platform.ready().then(() => {
          // Okay, so the platform is ready and our plugins are available.
          // Here you can do any higher level native things you might need.
          StatusBar.styleDefault();
        });
      }
    }
```

Instead $scope we use a class attribute which is called on the HTML
-- <cite>in that case we can use ng-if or N ng-statement with it attribute</cite>
```TypeScript
    export class ListPage {
      selectedItem: any;
    }
```


#### Guess View
---------------
About ./app/app.html
```HTML
    <!-- SideMenu -->
    <ion-menu [content]="content">
```

```HTML
    <!-- Bar on SideMenu -->
    <ion-toolbar>
```

```HTML
    <!-- Content for the SideMenu -->
    <ion-content>
```

```HTML
    <!-- The body Content -->
    <ion-nav>
```