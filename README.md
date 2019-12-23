# Grid

Import `grid.sass` to project.<br/>
In `_grid-parameters.sass` all static sizes for each breakpoint.<br/>
In `_variables.sass` add css variables responsive values if necessary.

### Basic usage
In the project must be initialized breakpoints mixins:<br/>
`+xl, +lg, +md, +sm, +xs, +xxs, +xlmin, +lgmin, +mdmin, +smmin, +xsmin, +xxsmin`<br/>
such as

```sass
=xl
  @media (max-width: 1399 + "px")
    @content
=xlmin
  @media (min-width: 1400 + "px")
    @content
```

Grid columns must have `.grid` wrapper and class `.col`<br/>
Columns mods: `.col--xl-1, .col--lg-1, .col--md-1, .col--sm-1, .col--xs-1, .col--xxs-1, .col--1`

```html
<div class="grid {grid--mod}">
  <div class="col {col--mod}"></div>
  <div class="col {col--mod}"></div>
</div>
```