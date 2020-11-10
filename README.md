# CookieHub Theme Customizer

This project is used to create custom themes for CookieHub. In the src folder you will find the source code for sample themes and common SCSS code that can be used to speed up the development.

## Requirements

* [ParcelJS](https://parceljs.org/)
* [Node.js](https://nodejs.org/en/) 10+

The project uses ParcelJS to run a local web server with hot reloading and SCSS compilation.

## Getting started

Follow these steps to get started:
**Install Node.js**
**Clone the git repository**
**Install Parcel using Yarn or NPM:**
`
yarn global add parcel-bundler
`
or
`
npm install -g parcel-bundler
`

**Install required packages using Yarn or NPM:**
`
yarn install
`
or
`
npm install
`

**Start parcel:**
`
parcel src/index.html
`

**Open up the site in a web browser: http://localhost:1234**


## Files and folders

* dist **Production build**
* src **Source code**
  * common **Common SCSS files shared between different themes**
    * _block.scss
    * _button.scss **Button styling**
    * _container.scss **Intended for container specific code**
    * _dark.scss **Dark color scheme**
    * _declaration.scss **Cookie declaration tab**
    * _dialog.scss **Initial cookie consent dialog**
    * _icon.scss **Floating settings icon**
    * _light.scss **Light color scheme**
    * _reset.scss **Browser reset**
    * _settings.scss **Settings dialog**
    * _typography.scss **Typography**
    * _variables.scss **SCSS variables**
  * themes **Available themes**
    * bar
      * theme.scss **The theme SCSS file**
  * index.html **Test html file**
  * index.js **Used to load the SCSS into the compiler**
  * index.scss **Primary SCSS file importing common SCSS files and themes**

## DOM hierarchy

* .ch2 **Root container**
  * .ch2-container **Container and overlay**
    * .ch2-dialog **Initial dialog**
      * p
      * .ch2-dialog-actions
        * button.ch2-allow-all-btn
        * button.ch2-open-settings-btn
    * .ch2-settings **Settings dialog**
      * .ch2-settings-header
        * a.ch2-close-settings-btn
        * p
      * .ch2-settings-tabs **Tab toggler**
        * ul
          * li.active
          * li
      * .ch2-settings-content **Tabs**
        * .ch2-settings-tab-container **Settings tab content**
          * p
          * p
          * button.ch2-allow-all-btn
          * button.ch2-deny-all-btn
          * .ch2-settings-options **One for each cookie category**
            * .ch2-settings-option
              * .ch2-switch
                * .ch2-settings-option-details
        * .ch2-settings-tab-container **Declaration tab content**
          * .ch2-settings-declaration
            * p
            * p
            * .ch2-declaration-category **One for each cookie category**
              * p.ch2-header
              * p
              * table
      * .ch2-settings-actions **Action button in the settings dialog**
        * p
        * button.ch2-save-settings-btn
    * .ch2-icon **Floating settings icon**
      * a.ch2-open-settings-btn
        * svg
        * span