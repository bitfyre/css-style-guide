CSS Naming Conventions
======================

## Table of Contents

1. [Component Naming Conventions](#component-naming-conventions)
  1. [Component Name](#component-name)
  2. [Component Child](#component-child)
  3. [Extending a Component](#extending-a-component)
    1. [Root Extended Component](#root-extended-component)
    2. [Extended Component Children](#extended-component-children)
2. [State Naming Convention](#state-naming-convention)
3. [General Utility Naming Convention](#general-utility-naming-convention)
4. [Naming Usage in Action](#naming-usage-in-action)

## Component Naming Conventions

The following is the basic formula for building class names for usage to apply styling to html.

```css
.{ComponentName}_{modifierName}-{childName}
```

These should be used in combination with semantic markup, as mentioned in “Important Terms” of the Design Goals & Principles Document.

### Component Name

```css
{ComponentName}
```

The Component Name is the root item of the component. It is the starting point for the names of all following children items of the component, modifier components, and the modifier components’ children. The name should be formatted using upper camel case.

```css
.NavList {…}
```

### Component Child

```css
-{childName}
```

Children of the component should be prefixed by the component name plus a dash to symbolize that it is an child of the component. The name should be formatted using lower camel case.

```css
.NavList-anchor {…}
```

### Extending a Component

```css
_{modifierName}
```

When extending a component, the name should include the name of the component it is extending, followed by an underscore, then followed by the more specific instance name.

```css
.NavList_userNav {…}
.NavList_settingsNav {…}
```
#### Root Extended Component

The preceding example would be at the root of the extended component. This will generally be the same as the original, but could be a child of the original component. When building the HTML of the extended component, it should have both the originating component class and the extending component class applied to the element.

#### Extended Component Children

Children of the extending component should use the base component name, followed by an underscore, followed by the extending component name, then followed by the standard child naming convention.

```css
.NavList_userNav-item {…}
.NavList_userNav-anchor {…}
```

The component children should also include the child classes of the originating component along with the child class of the extending component.

**[⬆ back to top](#table-of-contents)**

## State Naming Convention

All state oriented class names should be prefixed with `.is-` or `.has-`.

```css
.is-active {…}
.is-empty {…}
.has-errors {…}
```

This is also one of the few instances where class names can be chained together to achieve specific styling.

```css
.NavList-item.is-active {…}
```

Depending on the circumstance the state classes can be applied to the root or the child element of a component.

**[⬆ back to top](#table-of-contents)**

## General Utility Naming Convention

All general utility classes should be prefixed with `.u-` followed by lower camel case.

```css
.u-clearfix
.u-inlineBlock
```

Utility classes are small self contained components that have no children and have a small limited scope of properties it applies. They are useful for things like a clear fix, changing floats, or overriding font weight when all other properties match an already defined style.

## Naming Usage in Action

- [ ] Include code sample

**[⬆ back to top](#table-of-contents)**
