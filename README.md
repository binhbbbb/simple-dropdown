# Simple Dropdown
[![Build status][travis-badge]][travis-url] ![Size][size-badge] [![Version][tag-badge]][releases-url] [![Published][webcomponents-badge]][webcomponents-url]

Performant, featherweight, style-agnostic dropdown UI component, built on Web Components.

<!---
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="simple-dropdown.html">
    <style>
      body {
        font-family: sans-serif;
        color: #303c46;
      }
      
      simple-dropdown {
        margin-bottom: 50px;
      }

      simple-dropdown a {
        text-decoration: none;
        color: inherit;
        font-size: 0.85em;
        display: inline-block;
        text-decoration: none;
        padding: 0.5em 1em;
      }
    </style>
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<simple-dropdown origin="top right" label="menu" arrow>
  <a href="#">settings</span>
</simple-dropdown>
```

### Contents

- [Installation & usage](#installation--usage)
  - [Polyfills for cross-browser support](#polyfills-for-cross-browser-support)
  - [Transpiling for IE11 support](#transpiling-for-ie11-support)
- [Options](#options)
- [Styling](#styling)


## Installation & usage

Install simple-dropdown with Bower

```sh
$ bower i SimpleElements/simple-dropdown --save
```

Import it into the `<head>` of your page

```html
<link rel="import" href="/bower_components/simple-dropdown/simple-dropdown.html">
```

Then use simple-dropdown in your project

```html
<simple-dropdown></simple-dropdown>
```

### Polyfills for cross-browser support

simple-dropdown relies on emerging standards, for full cross-browser support include the [WebComponentsJS](https://github.com/webcomponents/webcomponentsjs) polyfill on your page.

```html
<script src="https://unpkg.com/@webcomponents/webcomponentsjs@^1.0.0/webcomponents-loader.js"></script>
```

### Transpiling for IE11 support

Web Components like simple-dropdown are distributed as ES6 classes, which are supported in all evergreen browsers. To support Internet Explorer 11 you should transpile simple-dropdown to ES5 and use the `webcomponentsjs` `custom-elements-es5-adapter.js` shim. 

The easiest way to do this is by including [polymer-build][polymer-build] in your buildstep of choice. Then just include the ES5 adapter on your page

```html
<script src="https://unpkg.com/@webcomponents/webcomponentsjs@^1.0.0/custom-elements-es5-adapter.js"></script>
```

## Options

Property       | Type    | Default                       | Description                                                                                                           
-----------    | ------- | -----------------             | ------------                                                                                                          
`active`       | Boolean | `false`                       | Whether the dropdown is open or not                                                                                   
`origin`       | String  | `''`                          | Position the menu should open from. Can be any combination of `'top'`, `'bottom'`, `'left'`, `'center`, or `'right'`. 
`label`        | String  | `''`                          | Optional label to display in toggle button                                                                            
`icon`         | String  | `simple-dropdown:expand-more` | Icon definition, from `iron-iconset`, set to empty string to hide icon                                                
`noTap`        | Boolean | `false`                       | Disable openeing menu on tap/click                                                                                    
`noIconRotate` | Boolean | `false`                       | Whether icon should flip when dropdown is open                                                                        
`arrow`        | Boolean | `false`                       | Add a callout-style arrow to the dropdown menu                                                                        

Properties can either be set as attributes on the element, or imperitively with Javascript
```html
<simple-dropdown position="top left" arrow></simple-dropdown> 

<script>
  document.querySelector('simple-dropdown').active = true;
</script>
```

## Styling
Style simple-dropdown with custom CSS properties and mixins

Property                          | Default   | Description                            
--------------------------------- | --------- | ------------                           
`--simple-dropdown-icon-size`     | `18px`    | Size of the toggle icon           
`--simple-dropdown-gutter`        | `0`       | Spacing between the toggle and the menu when open
`--simple-dropdown-offset`        | `-5px`    | Left/right offset of the dropdown menu when open, relative to the toggle
`--simple-dropdown-border-radius` | `3px`     | Border radius applied to menu


Apply properties on simple-dropdown

```css
simple-dropdown {
  --simple-dropdown-icon-size: 1rem;
}
```


Mixin                      |  Description                            
---------------------------| ------------                           
`--simple-dropdown-toggle` | Mixin applied to the toggle button
`--simple-dropdown-menu`   | Mixin applied to the menu

Define mixins on simple-dropdown

```css
simple-dropdown {
  --simple-dropdown-menu: {
    background: blue;
    color: white;
    padding: 12px 18px;
  }
}
```

***

MIT © [Sean King](https://www.twitter.com/seaneking)

[tag-badge]: https://img.shields.io/github/tag/SimpleElements/simple-dropdown.svg
[releases-url]: https://github.com/SimpleElements/simple-dropdown/releases
[travis-badge]: https://img.shields.io/travis/SimpleElements/simple-dropdown.svg
[travis-url]: https://travis-ci.org/SimpleElements/simple-dropdown
[size-badge]: http://img.badgesize.io/SimpleElements/simple-dropdown/master/simple-dropdown.html?compression=gzip&label=size%20%28unminified%29
[webcomponents-badge]: https://img.shields.io/badge/webcomponents.org-published-blue.svg
[webcomponents-url]: https://www.webcomponents.org/element/SimpleElements/simple-dropdown
[polymer-build]: https://github.com/Polymer/polymer-build
