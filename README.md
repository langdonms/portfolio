# Update: Creating a new Repo
I'm restarted this project on a new Repo to install Material Design Components for the web locally. Hopping over there. https://github.com/langdonms/portfolio-md

# Updating my portfolio
### Why?
I'm recreating my portfolio site from scratch. It's currently hosted at https://langdonsanders.com built with WordPress theme that not require any custom code and has a dated aesthetic.

### Goals
 * refresh the aesthetic design and usability of my site
 * improve web design skills through practice
 * learn new modules for image hosting and galleries

### Requirements
 * responsive
 * easy to read
 * intuitive to navigate
 * expandable for future projects

## Approach

* Diving right in.  
   At first I started with a basic HTML page and tried to recreate my print resume using Bootstrap. This was great to start feeling like I was making progress but quickly realized I needed a more strategic approach.    
* Reading portfolio revision blogs  
* Collecting my thoughts in a sketch pad for. . .   
   layouts, colors, value, audience
* Start exploring frameworks that already established best practices 

### Explore frameworks

* [Bootstrap](https://getbootstrap.com/)  
   I'm familiar with this when creating wedding invitation website. Responsive, easy to use.

* [Material Design](https://material.io/develop/)  
   Great design qualities with emphasis on usability. A great opportunity to try learning a new framework.
   
## Learning Material Design  
Working Through [these tutorials](https://material.io/collections/developer-tutorials/#web)

- [x] [MDC Web101](https://codelabs.developers.google.com/codelabs/mdc-101-web/#0) - learned how to create a dev environment, create input fields, add buttons, add CSS classes and import MDC (Material Components). [*Learn about more components here*](https://material.io/components/web/catalog/)
- [x] [MDC Web102](https://codelabs.developers.google.com/codelabs/mdc-102-web/#0) - looks promising learning "A navigation drawer, An image list full of products". Notes, the Drawer needs the list components, so you install both. 
       `npm install @material/drawer@1.0.1 @material/list@1.0.1`  
    Learning Drawer and Image List. 
   - Install the components needed using NPM Add the HTML. Add CSS (import and style),initiate with JS. Both CSS and JS use import.
   > "Note: We use the standard Navigation Drawer variant in this codelab. The standard variant has no drawer-specific logic, so we instantiate the MDCList inside of it directly. Dismissible and modal variants also exist, which use a dedicated MDCDrawer component for additional features. You can find out more about the MDC Navigation Drawer variants in the [documentation](https://material.io/develop/web/components/drawers/)."  
   - On the image list, note the `product-list` class
- [x] [MDC Web103](https://codelabs.developers.google.com/codelabs/mdc-103-web) Customizing. Color, added a new .scss file with the variables and like `$mdc-theme-on-primary: #442C2E;` which are then imported in`_common.scss`. Important note: 
  >"Any global variables you wish to override (e.g. `$mdc-theme-primary` or `$mdc-theme-secondary`) **must be declared before** importing the components' styles into your `*.scss` files. In this case,` _common.scss` is a partial that is imported before anything else in login.scss and home.scss, so it will apply to both pages' styles."  
  
  For typography, need to install with npm and import in SCSS `@import "@material/typography/mdc-typography";` that as well. Made a line separator in the list. Adjsuted image arrangement and subtitles. Adding "elevation" component for images. [Details on elevation here.](https://material.io/develop/web/components/elevation/) Steps again are... install the component using npm, import it in the `.scss` file, make a element with a class in `.html`, then in the `.scss` file write the stylings for that element with `.class-name {thing-to-change: value;}`  
  Image lists [reference here:](https://github.com/material-components/material-components-web/blob/master/packages/mdc-image-list/README.md#variants)
- [x] [MDC Web111](https://codelabs.developers.google.com/codelabs/mdc-111-web/#1) Changed a button, installed and imported button component, styled, add ripple effect. Changed the `<select>` style (for drop-down lists), also used a select icon. Use MDC classes in html, import and initiate in the JS file with `import {MDC-name} from '@material/mdc-name';` and then initiating as`new variable(document.querySelector('.class-name'));`  On to text fields. Added the textfield component, installed, and made a class in the markup - this careated a subtle but intutive text input field rather than a plain white box. 
  
## Next steps, implementing in my project.
~### Can use CDN of [Material Desgn Lite](https://getmdl.io/started/) MDL
This is probably the easiest way to get started. Just reference the CDN.~
>MDL is being replaced by [Material Components for the web (MDC Web)](https://material.io/develop/web/docs/migrating-from-mdl/)

### Material Components for the Web
[Getting Started](https://material.io/develop/web/docs/getting-started/) however it only is installed through npm, not a CDN. Could go with Material Design Lite but if that's going to be deprecated and/or this might be a good opporunity to learn npm. Can use unpkg to get the sources too. Can load all components or just the ones I need, probably best to be more lightweight and only pull what I use.

### NPM and Node
Note about npm and Node, the examples above start with `npm install` then `npm start` which is activating the dependences and start commands written written in those modudles, see help on [npm start](https://docs.npmjs.com/cli/start.html)
>Install the dependencies in the local node_modules folder. In global mode (ie, with -g or --global appended to the command), it installs the current package context (ie, the current working directory) as a global package. By default, npm install will install all modules listed as dependencies in package.json." [npm install](https://docs.npmjs.com/cli/install.html)  
Look in the `package.json` in the root folder to see the scripts and dependencies.  Now continuing with MDC Web111.


