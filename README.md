# Simple Dropdown
[![Build status][travis-badge]][travis-url] [![Bower dependencies][bowerdeps-badge]][bowerdeps-url] ![Version][bower-badge] ![Size][size-badge]<br/>[![Cross browser test status][browser-badges]][travis-url]

Simple callout-style dropdown menu

### Installation & usage

Install simple-dropdown with Bower

```sh
$ bower install simple-dropdown-menu --save
```

Import it into the `<head>` of your page

```html
<link rel="import" href="/bower_components/simple-dropdown/simple-dropdown.html">
```

Then use simple-dropdown in your project, and add simple-dropdown-item children for menu items

```html
<simple-dropdown>
  <a href="/settings">user settings</a>
</simple-dropdown>
```

Note for cross-browser support you should also include the [Web Components Polyfill][webcomponents].

## Options

Property    | Type    | Default               | Description                                                                                                                                                               
----------- | ------- | -----------------     | ------------                                                                                                                                                              
`active`    | Boolean | `false`               | Whether the dropdown is open or not                                                                                                                                       
`origin`    | String  | `''`                  | Position the menu should open from. Can be any combination of `'top'`, `'bottom'`, `'left'`, `'center`, or `'right'`.                                                                
`noTap`     | Boolean | `false`               | Disable openeing menu on tap/click                                                                                                                                        
`noIcon`    | Boolean | `false`               | Disable icon in toggle button                                                                                                                                             
`arrow`     | Boolean | `false`               | Add a callout-style arrow to the dropdown menu    

```html
<simple-dropdown position="top left" arrow no-icon></simple-dropdown> 
```

## Methods

Method     | Arguments | Description                                          
---------- | --------- | ------------                                         
`toggle()` | `none`    | Utility method to that toggles the `active` property

## Styling
Style simple-dropdown with custom CSS properties and mixins

Property                        | Default   | Description                            
-----------------------------   | --------- | ------------                           
`--simple-dropdown-icon-size`   | `18px`    | Size of the toggle icon           
`--simple-dropdown-gutter`      | `0`       | Spacing between the toggle and the menu when open
`--simple-dropdown-offset`      | `-5px`    | Left/right offset of the dropdown menu when open, relative to the toggle



Apply properties on simple-dropdown

```css
simple-dropdown {
  --simple-dropdown-icon-size: 1rem;
}
```

--

MIT © [Simpla](friends@simpla.io)

[webcomponents]: https://github.com/webcomponents/webcomponentsjs

[bower-badge]: https://img.shields.io/bower/v/simple-dropdown.svg
[bowerlicense-badge]: https://img.shields.io/bower/l/simple-dropdown.svg
[travis-badge]: https://img.shields.io/travis/SimpleElements/simple-dropdown.svg
[travis-url]: https://travis-ci.org/SimpleElements/simple-dropdown
[bowerdeps-badge]: https://img.shields.io/gemnasium/SimpleElements/simple-dropdown.svg
[bowerdeps-url]: https://gemnasium.com/bower/simple-dropdown
[size-badge]: https://badges.herokuapp.com/size/github/SimpleElements/simple-dropdown/master/simple-dropdown.html?gzip=true&color=blue
[browser-badges]: https://badges.herokuapp.com/travis/SimpleElements/simple-dropdown/sauce/SimpleElements?labels=none
