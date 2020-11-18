## How to set up a new Angular app using Angular Material

1. Run the following commands:
    ```
    ng new my-app
    cd my-app
    ng add @angular/material
    ```

    `ng new my-app` generates the default Angular CLI starter template, you can replace  `my-app` with whatever you want to call your app

    Select `Y` for routing

    Select `SCSS` for styles

    `ng add @angular/material` will install the `@angular/cdk` and `@angular/material` libraries as well as adding setting up fonts and base styles

    In this example you can choose any of the default themes provided

    Select `Y` for animations

2. Remove the default Angular App content

    Remove everything in `app.component.html` except for `<router-outlet></router-outlet>`

3. Create file called `material.module` your `src\app`

    Copy the contents of this file from my [github](https://github.com/melissahoughton/material.module/blob/master/material.module.ts)

4. Add `MaterialModule` to your app imports
    ```
    import { BrowserModule } from '@angular/platform-browser';
    import { NgModule } from '@angular/core';

    import { AppRoutingModule } from './app-routing.module';
    import { AppComponent } from './app.component';
    import { BrowserAnimationsModule } from '@angular/platform-browser/animations';
    import { MaterialModule } from './material.module';

    @NgModule({
    declarations: [
        AppComponent
    ],
    imports: [
        BrowserModule,
        AppRoutingModule,
        BrowserAnimationsModule,
        MaterialModule
    ],
    providers: [],
    bootstrap: [AppComponent]
    })
    export class AppModule { }
    ```
