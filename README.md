# MDP-SASS

A super simple, quick and dirty approximation of a material palette that matches the [@angular/material](https://github.com/angular/material2) signature of a Material Design palette. Designed to work well with [@angular/material](https://github.com/angular/material2).

[StackBlitz Demo](https://stackblitz.com/edit/mdp-sass-demo)

## Usage

To use, simple install, include where necessary, and call the function:

```scss
@import '~@angular/material/theming';
@include mat-core();
@import '~mdp-sass/mdp-sass';

$my-base-color: #0e5ab2;
$my-accent-color: #b389d7;
$my-warn-color: #f7377b;

$my-mat-primary-palette: mat-palette(get-mat-palette($my-base-color));
$my-mat-accent-palette: mat-palette(get-mat-palette($my-accent-color));
$my-mat-warn-palette: mat-palette(get-mat-palette($my-warn-color));

$my-app-theme: mat-light-theme($my-mat-primary-palette, $my-mat-accent-palette, $my-mat-warn-palette);

@include angular-material-theme($my-app-theme);
```

### `get-mat-palette()`

`get-mat-palette($hex-value, $light-text: false)` Given a base hex value, will return a map formatted to match @angular/material's mat-color signature with contrast values.

#### Optional Light Text Argument

As of v1.0.4, you may now force a light text for colors that are on the cusp of being dark enough to warrant white/light text.

```scss
@import '~@angular/material/theming';
@include mat-core();
@import 'node_modules/mdp-sass';

$my-base-color: #0e5ab2;
$my-accent-color: #b389d7;
$my-warn-color: #f7377b;

$my-mat-primary-palette: mat-palette(get-mat-palette($my-base-color));
$my-mat-accent-palette-light-text: mat-palette(get-mat-palette($my-accent-color, true));
$my-mat-warn-palette: mat-palette(get-mat-palette($my-warn-color));

$my-app-theme: mat-light-theme($my-mat-primary-palette, $my-mat-accent-palette, $my-mat-warn-palette);
```

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

None, however it is designed to work w/ @angular/material.

### Installing

It's just a SASS helper function. So however you see fit for now.

## Running the tests

Coming Soon.

### Pre-Commit linting tests / CI Tests


### And coding style tests

Linter rules.

## Deployment

PRs will be auto-deployed via CI/CI pipeline.

## Contributing

Please submit a PR and add me as a reviewer.

## Authors

* **Taylor Buckner** - *Initial work* - [tabuckner](https://github.com/tabuckner)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* [mbitson](https://github.com/mbitson) - For his [MCG](https://github.com/mbitson/mcg) project
