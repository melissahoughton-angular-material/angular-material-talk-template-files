/\* Before strating, run ng new, setup styles in app.component.scss, remove default html text, add in

```
<div class="container">
  <h1>Hello world!</h1>
</div>
```

commit, then add angular material and show diff at start of demo
\*/

## Differences in files after adding angular mat

- I have already run the new angular app command and add material
- On adding material it asked if I wanted typography and animations and I said yes to both
- It will also ask you want to use one of the default themes - talk about default themes

## Need to add in material module

[Ang Mat Form Field Doc to copy](https://material.angular.io/components/form-field/overview)

- Add in first material module, copying from the docs but it will fail, this because we are not yet importing them
- Can import into individual compontents or import into the overarching app
- We will copy all for this demo as it makes the modules available from all components without having to import individul, easier for learning
- Does increase your bundle size and you are importing more than you need, if its a production app only import what you need
- To further simplify I have setup a page with all of the material modules that you can copy into your project
- Lets do that now
- // Copy and paste material module folder from other project
- // import into app, and build
- Part of the theme is also to have a background color, to have the apply globally, we also want to add in the class `mat-app-background` to the `index.html`

## Look at angular material components

- While that is building lets take a look at the material components themsleves.
- We copied over the from field component which looks like this
- Using the component tags starting with `mat-` are telling angular to use the material component
- Behind the scenes these are components and directives defined by Angular Material, similar to the components and directives you would use in your regular angular code
- Input is an attribute directive, that allows native `<input>` and `<textarea>` elements to work with `<mat-form-field>`.
- These add the `style` templates to tell the browser what to display
- The material component have property inputs to allow you some flexiblity to change how it functions
- Such as the buttons can take inputs to define colors, we will look at that in a second
- `mat-icon` is using the material icon pack, all you need is the tag and the icon name in the middle

## Look at built form

- // Show the fields, click around, talk aobut it, only styles I added were to center iton the page
- // Talk about the flex layout situation

## Add in toolbar header

- Add in toolbar header
  ```
  <mat-toolbar class="mat-elevation-z6" color="primary"></mat-toolbar>
  ```
- Discuss the elevation and color, change the color to accent

## More component examples

- I'm going to copy over a bunch of Material components I put together earlier in this [Example file](example.component.html)
  to give you an idea of whats available

## Custom theme

- But say we wanted to be like orange bank and use a custom theme
- Luckily I have a theme I created earlier here [example theme file](theme.scss)
- // Go to the `angular.json` file and change material styles to: `"src/theme.scss"`
- Restart build because changed the angular build file
- // Explain how can also import to a scss file using `@import`
