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
- [ ] [MDC Web102](https://codelabs.developers.google.com/codelabs/mdc-102-web/#0) - looks promising learning "A navigation drawer, An image list full of products". Notes, the Drawer needs the list components, so you install both. 
       `npm install @material/drawer@1.0.1 @material/list@1.0.1`  
    Learning Drawer and Image List. 
   - Install the components needed using NPM Add the HTML. Add CSS (import and style),initiate with JS. Both CSS and JS use import.
   > "Note: We use the standard Navigation Drawer variant in this codelab. The standard variant has no drawer-specific logic, so we instantiate the MDCList inside of it directly. Dismissible and modal variants also exist, which use a dedicated MDCDrawer component for additional features. You can find out more about the MDC Navigation Drawer variants in the [documentation](https://material.io/develop/web/components/drawers/)."  
   - On the image list, note the `product-list` class
- [ ] [MDC Web103](https://codelabs.developers.google.com/codelabs/mdc-103-web) Customizing
