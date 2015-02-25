CSS Style Guide
===============

## Table of Contents

  1. [Properties Ordering](#property-ordering)
  2. [Selector Depth](#selector-depth)
  3. [Basic Code Formatting](#basic-code-formatting)
  4. [Color values](#color-values)
  5. [Comments](#comments)

## Properties Ordering

The basic rule of thumb is INSIDE OUT. This may be the exact opposite of what you may have down in the past, but the majority of the time this is how properties affect sizing. The font-size will be the first thing to affect the height, followed by they line-height which is directly related to the elements font-size or the inherited font-size of the parent (depending on the unit you use). The next item is the inter-play of the length of content and Width and Height properties. This is followed by padding, then border size, then margins, then finally positioning properties.

  - Text Properties

  ```css
  line-height
  font-* properties
  alphabetize from here
  ```

  - Box model

  ```css
  width
  height
  padding
  border
  margin
  ```

  - Display

  ```css
  display
  overflow (this might belong under box model)
  ```

  - Display

  ```css
  position
  top
  left
  ```

**[⬆ back to top](#table-of-contents)**


## Selector Depth

The only time you should go more than 3 selectors deep is for :hover & :focus states. Alex is finding this is becoming more and more a hard and fast rule. The deeper you nest, the more problems you will have down the road. If you can do it in fewer selectors with more semantic class names, the better off we will be down the road.

**[⬆ back to top](#table-of-contents)**


## Basic Code Formatting

Use two spaces for indentation.

Add a line of white space between each selector + properties block.

  ```css
  // bad
  .header {
    …
  }
  .logo-bar {
    …
    a {…}
  }

  // good
  .header {
    …
  }
  .logo-bar {
    …

    a {
      …
    }
   }
  ```

**[⬆ back to top](#table-of-contents)**


## Color values

All hex color values should use lower case letters.

Colors should be made into variables to be reused.

**[⬆ back to top](#table-of-contents)**

## Comments

Comments related to code that is rendered out directly should use the standard slash star syntax.

  ```css
  /* Headings */
  h1 {…}
  h2 {…}
  ```

Comments related that code or files that are not rendered out directly should use the double slash sytnax. This should be used in places where we might be labeling a group of variables, or a mixin that will be used later, or a file that is a library of such things.

  ```css
  // ===================================================================
  //  Copyright 2015 Org Name. All rights reserved.
  //
  //  Variables
  //
  //  Base set of variables for use with the web project
  //  ==================================================================
  ```

  // colors
  $brandGreen: #20c05c;

**[⬆ back to top](#table-of-contents)**


