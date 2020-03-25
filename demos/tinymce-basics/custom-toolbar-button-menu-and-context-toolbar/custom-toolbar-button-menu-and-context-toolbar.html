<!--
    In this demo we use a callout block to demonstrate creating
    a custom toolbar button, a custom menu item and a custom
    context toolbar.
-->

<!doctype html>
<html>
<head>
    <meta charset="utf-8">
    <title>TinyMCE Demos – Custom Toolbar Buttons, Menus and Context Toolbars</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <script src="https://cdn.tiny.cloud/1/qagffr3pkuv17a8on1afax661irst1hbr4e6tbv888sz91jc/tinymce/5-dev/tinymce.min.js" referrerpolicy="origin"></script>

    <script>
        // An iconpack holds our custom button's SVG icons.
        // Tip! A custom icon pack does not have to be a separate file
        tinymce.IconManager.add('customIcons', {
          icons: {
            'callout': '<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24"><g><path d="M20 7a2 2 0 0 1 2 2v6a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V9a2 2 0 0 1 2-2h16zm0 2H4v6h16V9z"/><path d="M7 10.5a1.5 1.5 0 1 1 0 3 1.5 1.5 0 0 1 0-3z"/></g></svg>',
            'swatch-blue': '<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24"><rect width="18" height="18" x="3" y="3" fill="#76B8E4" fill-rule="evenodd" rx="2"/></svg>',
            'swatch-yellow': '<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24"><rect width="18" height="18" x="3" y="3" fill="#FAD281" fill-rule="evenodd" rx="2"/></svg>',
            'swatch-red': '<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24"><rect width="18" height="18" x="3" y="3" fill="#FF8686" fill-rule="evenodd" rx="2"/></svg>',
          }
        });

        tinymce.init({
            selector: "#editor",

            // Tip! To make TinyMCE leaner, only include the plugins you actually need
            plugins: "link lists code noneditable",

            // We have put our custom callout button last.
            toolbar: "undo redo | formatselect | bold italic strikethrough backcolor | bullist link callout",

            // Tip! The height option accepts any valid CSS for height
            height: 'calc(100vh - 4rem)',

            // The Callout contains multiple HTML elements, some we
            // don't want to be editable. First we make the root
            // Callout element non-editable, then we define the
            // parts of the Callout that is editable.
            // https://www.tiny.cloud/docs/plugins/noneditable/
            noneditable_noneditable_class: 'callout',
            noneditable_editable_class: 'content',

            // Hide the right click context menus
            // https://www.tiny.cloud/docs/configure/editor-appearance/#contextmenu
            contextmenu: false,

            // Make the custom icon pack available in TinyMCE. A custom icon pack
            // extends the default icon pack.
            // https://www.tiny.cloud/docs/configure/editor-appearance/#icons
            icons: 'customIcons',

            // We use the menu option to define custom menu items
            // In this case, we want to put our custom callout menu item
            // in the Insert menu. Therefore we need to override the
            // default Insert menu. Keep in mind that you have to define
            // all menu items in the whole menu, you cannot simply append
            // a menu item to an existing menu.
            // For a list of in which menu the default menu items goes, see
            // https://www.tiny.cloud/docs/configure/editor-appearance/#menu
            // https://www.tiny.cloud/docs/ui-components/menuitems/
            menu: {
                insert: {title: 'Insert', items: 'link callout'}
            },

            setup: (editor) => {
                // Register a custom toolbar button which inserts a callout
                // https://www.tiny.cloud/docs/ui-components/toolbarbuttons/
                editor.ui.registry.addButton('callout', {
                    icon: 'callout',
                    tooltip: 'Insert callout',
                    onAction: function () {
                        // Insert content at the location of the cursor.
                        // It is wise to include an empty paragraph to
                        // avoid having text be inserted directly under
                        // the div.
                        // https://www.tiny.cloud/docs/api/tinymce/tinymce.editor/#insertcontent
                        tinymce.activeEditor.insertContent(`
                            <div class="callout">
                                <div class="content"><p>Callout</p></div>
                            </div>
                        `);
                    }
                });

                // Below we register our three callout colors that we will
                // put into the context toolbar. To better illustrate how
                // the code works, we repeaded every button. In a real world
                // scenario you would make a loop to create all the variants.
                // and make the toggling of the classes more elegant.
                editor.ui.registry.addButton('calloutyellow', {
                    icon: 'swatch-yellow',
                    tooltip: 'Yellow callout',
                    onAction: function () {
                        // First we get the selected element. It can be either the
                        // callout itself or any child element within it.
                        // https://www.tiny.cloud/docs/api/tinymce.dom/tinymce.dom.selection/#getnode
                        const node = tinymce.activeEditor.selection.getNode();

                        // Then we traverse up the DOM tree to make sure we target
                        // the callout element if it wasn't the selected node.
                        // https://www.tiny.cloud/docs/api/tinymce.dom/tinymce.dom.domutils/#getparent
                        const callout = tinymce.activeEditor.dom.getParent(node, '.callout');

                        // Then we remove and add the neccesseary classes.
                        // https://www.tiny.cloud/docs/api/tinymce.dom/tinymce.dom.domutils/#removeclass
                        // https://www.tiny.cloud/docs/api/tinymce.dom/tinymce.dom.domutils/#addclass
                        tinymce.DOM.removeClass(callout, 'red');
                        tinymce.DOM.addClass(callout, 'yellow');
                    }
                });

                // See the `calloutyellow` example above
                editor.ui.registry.addButton('calloutred', {
                    icon: 'swatch-red',
                    tooltip: 'Red callout',
                    onAction: function () {
                        const node = tinymce.activeEditor.selection.getNode();
                        const callout = tinymce.activeEditor.dom.getParent(node, '.callout');
                        tinymce.DOM.removeClass(callout, 'yellow');
                        tinymce.DOM.addClass(callout, 'red');
                    }
                });

                // See the `calloutyellow` example above
                editor.ui.registry.addButton('calloutblue', {
                    icon: 'swatch-blue',
                    tooltip: 'Blue callout',
                    onAction: function () {
                        const node = tinymce.activeEditor.selection.getNode();
                        const callout = tinymce.activeEditor.dom.getParent(node, '.callout');
                        tinymce.DOM.removeClass(callout, 'yellow');
                        tinymce.DOM.removeClass(callout, 'red');
                    }
                });

                // Register a custom remove callout button which we will
                // put in the context toolbar
                // https://www.tiny.cloud/docs/ui-components/toolbarbuttons/
                editor.ui.registry.addButton('removecallout', {
                    icon: 'remove',
                    tooltip: 'Remove callout',
                    onAction: function () {
                        // First we get the selected element. It can be either the
                        // callout itself or any child element within it.
                        // https://www.tiny.cloud/docs/api/tinymce.dom/tinymce.dom.selection/#getnode
                        const node = tinymce.activeEditor.selection.getNode();

                        // Then we traverse up the DOM tree to make sure we target
                        // the callout element if it wasn't the selected node.
                        // https://www.tiny.cloud/docs/api/tinymce.dom/tinymce.dom.domutils/#getparent
                        const callout = tinymce.activeEditor.dom.getParent(node, '.callout');

                        // Make the callout the selected element
                        // https://www.tiny.cloud/docs/api/tinymce.dom/tinymce.dom.selection/#select
                        tinymce.activeEditor.selection.select(callout);

                        // Finally we issue a delete command to remove the selected callout
                        // https://www.tiny.cloud/docs/api/tinymce/tinymce.editor/#execcommand
                        tinymce.activeEditor.execCommand('delete');
                    }
                });

                // Register a custom context toolbar
                // QUESTION: Is there a better way? Also, the classlist doesn't work on an empty error
                // https://www.tiny.cloud/docs/ui-components/contexttoolbar/#registeringacontexttoolbar
                editor.ui.registry.addContextToolbar('callout', {
                    predicate: function (node) {
                        // Return true if the node has the callout class. Due to a bug in
                        // TinyMCE (TINY-4751) we must also make sure the node is an element node
                        return node.nodeType === 1 && node.classList.contains('callout');
                    },
                    items: 'calloutblue calloutyellow calloutred | removecallout',
                    position: 'node',
                    scope: 'node'
                });

                // Register a custom menu item which contains sub menu items for each
                // callout color. We deliberately repeaded ourself to make it easier
                // to understand what is going on. In a real world scenario, you would
                // probably use a loop to create the menu items
                editor.ui.registry.addNestedMenuItem('callout', {
                    text: 'Callout',
                    icon: 'callout',
                    getSubmenuItems: () => {
                        return [
                            {
                                type: 'menuitem',
                                text: 'Blue',
                                icon: 'swatch-blue',
                                onAction: () => {
                                    tinymce.activeEditor.insertContent(`
                                        <div class="callout">
                                            <div class="content"><p>Callout</p></div>
                                        </div>
                                    `);
                                }
                            }, {
                                type: 'menuitem',
                                text: 'Yellow',
                                icon: 'swatch-yellow',
                                onAction: () => {
                                    tinymce.activeEditor.insertContent(`
                                        <div class="callout yellow">
                                            <div class="content"><p>Callout</p></div>
                                        </div>
                                    `);
                                }
                            }, {
                                type: 'menuitem',
                                text: 'Red',
                                icon: 'swatch-red',
                                onAction: () => {
                                    tinymce.activeEditor.insertContent(`
                                        <div class="callout red">
                                            <div class="content"><p>Callout</p></div>
                                        </div>
                                    `);
                                }
                            }
                        ];
                    }
                });
            },

            // The following css will be injected into the editor, extending
            // the default styles.
            // In a real world scenario, with much more custom styles for headings
            // links, tables, images etc, it's recommended to use the content_css
            // option to load a separate CSS file. Makes editing easier too.
            // https://www.tiny.cloud/docs/configure/content-appearance/#content_style
            // https://www.tiny.cloud/docs/configure/content-appearance/#content_css
            content_style: `
                .callout {
                    margin: 1rem 0;
                    padding: .5rem 1rem .5rem 1.5rem;
                    background: #EEF4F8;
                    border-left: 3px solid #9FCCE9;
                    color: #5D7F95;
                    font-size: 14px;
                }

                .callout.yellow {
                    background: #FCF8F0;
                    border-left-color: #F9DDA4;
                    color: #B49A64;
                }

                .callout.red {
                    background: #FCF0F0;
                    border-left-color: #FFABAB;
                    color: #AA6464;
                }

                .callout p {
                    margin: 0;
                }

                /* The default styles has an outline around editable
                 * content inside a non-editable container to make it
                 * more apparent what is editable and not. In our case
                 * we don't need that so we override this using the
                 * following styles
                 */
                .mce-content-body [contentEditable=false] [contentEditable=true]:hover,
                .mce-content-body [contentEditable=false] [contentEditable=true]:focus {
                    outline: none;
                }
            `,
        });
    </script>
    <style>
        body {
            margin: 2rem .5rem;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', Helvetica, Arial, sans-serif;
        }

        main {
            max-width: 800px;
            margin: auto;
        }
    </style>
</head>
<body>
<main>
    <textarea id="editor">
        <h1>About this demo</h1>
        <p>In this demo we use a callout block to demonstrate creating a <span style="background-color: #fbeeb8;">custom toolbar button</span>, a <span style="background-color: #c2e0f4;">custom menu item</span> and a <span style="background-color: #bfedd2;">custom context toolbar</span>. Insert a callout by pressing the <strong>last toolbar button</strong> or through the <strong>Insert menu</strong>.</p>
        <h3>Remove below</h3>
        <div class="callout">
            <div class="content">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum a molestie nisl, at sodales diam. Vivamus ullamcorper convallis odio, ut lacinia sem.</div>
        </div>
    </textarea>
</main>
</body>
</html>
