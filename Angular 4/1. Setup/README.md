#### Components



#### Installation
```bash
npm install -g @angular/cli
```

#### Usage
```bash
ng help
```

#### Generating and serving a project via CLI
```bash
ng new PROJECT-NAME
cd PROJECT-NAME
ng serve
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

