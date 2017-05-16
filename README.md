# Simple Dropdown
 ![Version][bower-badge] [![Build status][travis-badge]][travis-url] ![Size][size-badge] [![Published][webcomponents-badge]][webcomponents-url]

Performant, lightweight, style-agnostic popout/dropdown menu

<!---
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="simple-dropdown.html">
    <style>
      body {
      min-height: 100px
      }
      simple-dropdown {
        margin-left: 20px;
        font-family: sans-serif;
        font-size: 14px;
      }
      simple-dropdown div {
        padding: 10px 16px;
        font-size: 12px
      }
    </style>
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<simple-dropdown origin="top right" label="menu" arrow>
  <div>item</div>
</simple-dropdown>
```

### Installation & usage

Install simple-dropdown with Bower (Yarn support coming soon)

```sh
$ bower i SimpleElements/simple-dropdown --save
```

Import it into the `<head>` of your page

```html
<link rel="import" href="/bower_components/simple-dropdown/simple-dropdown.html">
```

Then use simple-dropdown in your project, and toggle the `active` property to open/close the dropdown

```html
<simple-dropdown id="dropdown">
  <a href="/settings">user settings</a>
</simple-dropdown>

<script>
  // Open the dropdown
  document.querySelector('#dropdown').active = true;
</script>
```

#### Polyfills for cross-browser support
Simple dropdown relies on emerging standards, for full cross-browser support include the [Web Components Lite][webcomponents] polyfill.

```html
<script src="https://unpkg.com/webcomponents.js@^0.7.24/web-components-lite.min.js" async></script>
```


## Options

Property    | Type    | Default               | Description                                                                                                                                                               
----------- | ------- | -----------------     | ------------                                                                                                                                                              
`active`    | Boolean | `false`               | Whether the dropdown is open or not                                                                                                                                       
`origin`    | String  | `''`                  | Position the menu should open from. Can be any combination of `'top'`, `'bottom'`, `'left'`, `'center`, or `'right'`.                                                                
`label`     | String  | `''`                  | Optional label to display in toggle button
`noTap`     | Boolean | `false`               | Disable openeing menu on tap/click                                                                                                                                        
`noIcon`    | Boolean | `false`               | Disable icon in toggle button                                                                                                                                             
`arrow`     | Boolean | `false`               | Add a callout-style arrow to the dropdown menu    

Properties can either be set as attributes on the element, or imperitively with Javascript
```html
<simple-dropdown position="top left" arrow no-icon></simple-dropdown> 

<script>
    document.querySelector('simple-dropdown').noTap = true;
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

MIT © [Simpla](friends@simpla.io)

[webcomponents]: https://github.com/webcomponents/webcomponentsjs

[bower-badge]: https://img.shields.io/bower/v/simple-dropdown-menu.svg
[travis-badge]: https://img.shields.io/travis/SimpleElements/simple-dropdown.svg
[travis-url]: https://travis-ci.org/SimpleElements/simple-dropdown
[size-badge]: https://badges.herokuapp.com/size/github/SimpleElements/simple-dropdown/master/simple-dropdown.html?gzip=true
[webcomponents-badge]: https://img.shields.io/badge/webcomponents.org-published-blue.svg
[webcomponents-url]: https://www.webcomponents.org/element/SimpleElements/simple-dropdown
