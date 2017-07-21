# Components


## Introduction
#### What is component ?
 
- The bulk of an Angular application.
- Pieces of UI.
- Include a clas and templete.
- Bind from class -> template and class <- template
<img src="AppComponent.png" />
 
#### Why use components ?
- Code organization.
- Break up the UI.
- Contain properties & methods.
- Promotes reusability.
- Better teamwork.

#### Application Lifecycle
<p>Angular creates, updates, and destorys components as the user moves through the application. Your app can take action at each moment in this lifecycle through optional lifecycle hooks, like <strong>ngOnInit</strong></p>

## Code

### app.module.ts (default)
It is something like a registry for rest of the application
```TypeScript
import { BrowserModule } from '@angular/platform-browser'; //<- it takes care of display contents on the browser
import { NgModule } from '@angular/core';

import { AppComponent } from './app.component';

@NgModule({
  declarations: [
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
### Generating Components, Directives, Pipes and Services
Scaffold  | Usage
---       | ---
Component | `ng g component my-new-component`
Directive | `ng g directive my-new-directive`
Pipe | `ng g pipe my-new-pipe`
Service | `ng g service my-new-service`
Class  | `ng g class my-new-class`
Guard  | `ng g guard my-new-guard`
Interface | `ng g interface my-new-interface`
Enum   | `ng g enum my-new-enum`
Module | `ng g module my-module`

### Updating Angular CLI

```bash
npm uninstall -g angular-cli
npm uninstall --save-dev angular-cli
```

Global package:
```bash
npm uninstall -g @angular/cli
npm cache clean
npm install -g @angular/cli@latest
```

