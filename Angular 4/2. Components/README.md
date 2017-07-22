# Components


## Introduction
#### What is component ?
 
- The bulk of an Angular application.
- Pieces of UI.
- Include a clas and templete.
- Bind from class -> template and class <- template
<img src="AppComponent.png" style=""/>
 
#### Why use components ?
- Code organization.
- Break up the UI.
- Contain properties & methods.
- Promotes reusability.
- Better teamwork.

#### Application Lifecycle
<p>Angular creates, updates, and destorys components as the user moves through the application. Your app can take action at each moment in this lifecycle through optional lifecycle hooks, like <strong>ngOnInit</strong></p>

## Angular main files

### app.module.ts (default)
It is something like a registry for rest of the application
```TypeScript
import { BrowserModule } from '@angular/platform-browser'; //<- it takes care of display contents on the browser
import { NgModule } from '@angular/core';

import { AppComponent } from './app.component';

@NgModule({
  declarations: //<-- To import components
  [
    AppComponent,
  ],
  imports: //<- For modules
  [
    BrowserModule,
  ],
  providers: [], //<-For service
  bootstrap: [AppComponent]
})
export class AppModule { }

```

### app.component.ts (default)
- It is something like a registry for rest of the application.
- consturctor
```TypeScript
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: [./app.component.css]

})
export class AppComponent { 
  
```
### Data Binding and String Interpolation
- We can take data and bind them dynamically to the template by using 
- {{  }} called string interplation
- Make sure to use backticks (` `) to if you want to use your template inside the component

```TypeScript
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: 
  `
    <h1>{{ name }} is {{  }} years old</h1>
    <h2>My name is {{ person.firstName }} {{person.lastName}}</h2>
  `

})
export class AppComponent { 
  name = 'John Doe!';
  age = 35;
  person = {
    firstName: 'Steve',
    lastName: 'Smith'
  }
}

constructor() {
      
    } //<- baiscally a function run when a component is initialize

    hasBirthday(){
      this.age += 1; //<- it is not going to run becasue we have not called it in the constructor 
    }
}

```

### Adding types to properties