<svg width="112" height="96" xmlns="http://www.w3.org/2000/svg"><g><path d="M45 31L67 31 67 36 45 36z"/><path d="M45 61L67 61 67 66 45 66z"/><path d="M37 51L74 51 74 56 37 56z"/><path d="M37 41L74 41 74 46 37 46z"/><path d="M55.747 0l44.9 43.24 6.506-6.069 4.677 4.234-55.915 54.412L10.42 51.651l-6.022 5.813L0 53.2 55.747 0zM14.912 47.315L55.93 87.131 96.918 47.31 55.93 7.469 14.912 47.315z"/></g></svg>

# TinyMCE Demos
TinyMCE is a versatile tool that can be used for a wide variety of text editing tasks. This repository aims to inspire you and demonstrate different approaches to common use cases.

Every demo has a thorougly documented html file explaining the TinyMCE config as well as links to relevant documentation to make it easy to use these demos as basis for your own projects.

## Build and serve the demos locally

You can download and run these demos locally. Some demos uses premium plugins so we have included an API key that works for `localhost`.

- Check out this repository to your local computer.
- Install dependencies using the command `yarn`
- Start the web server to view the demos using the command `yarn run start`
- To just build the project, use `yarn run build`

## TinyMCE Basics

The following demos showcase common how-tos like creating toolbar buttons, menu items, formattingS etc.

### Creating custom toolbar buttons, menus and context toolbars.

This demo uses a custom callout block to demonstrate how to create toolbar buttons, customizing the menu and showing a context toolbar when selecting the callout. It also shows how to add a custom icon pack for our custom toolbar button.

[Custom Toolbar Button, menu and Context Toolbar](demos/tinymce-basics/custom-toolbar-button-menu-and-context-toolbar/custom-toolbar-button-menu-and-context-toolbar.html)

## Tokens (or mail-merge variables)

Tokens – or mail merge variables such as {{name.first}} – are often found in document automation applications. Here are three ways you can implement them in TinyMCE

### Text-based tokens

Transform any text based tokens such as {{name.first}} into spans that we can style and make noneditable – and transform back to pure text when storing the content. Perfect for existing systems as this approach is non-destructive to your content.

### Web component tokens

With the january 2020 release of Microsoft Edge, all major browsers now supports web components. Here we  create a custom element called `<inline-token>` that becomes our token.

### Span-based tokens

Here we use a span with a class to wrap our token. A simple but powerful approach.

## Cool demos

Sometimes you just want to show off right? Here are a couple of demos showcasing just how versatile TinyMCE is

### Expand and show toolbar

A truly minimal and elegant example of an editor that starts out like a unintrusive textarea and grows into a rich text editor upon focus. Demonstrates an interesting use of the inline mode and features like inline placeholder, toolbar groups as well as our new premium thin icon pack.
