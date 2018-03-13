CKEditor 5 decoupled document build
========================================

[![Join the chat at https://gitter.im/ckeditor/ckeditor5](https://badges.gitter.im/ckeditor/ckeditor5.svg)](https://gitter.im/ckeditor/ckeditor5?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![npm version](https://badge.fury.io/js/%40ckeditor%2Fckeditor5-build-decoupled-document.svg)](https://www.npmjs.com/package/@ckeditor/ckeditor5-build-decoupled-document)
[![Dependency Status](https://david-dm.org/ckeditor/ckeditor5-build-decoupled-document/status.svg)](https://david-dm.org/ckeditor/ckeditor5-build-decoupled-document)
[![devDependency Status](https://david-dm.org/ckeditor/ckeditor5-build-decoupled-document/dev-status.svg)](https://david-dm.org/ckeditor/ckeditor5-build-decoupled-document?type=dev)

The decoupled document build for CKEditor 5. Read more about the [decoupled document build]((https://ckeditor5.github.io/docs/nightly/ckeditor5/latest/builds/guides/overview.html#document-editor) and see the [demo](https://ckeditor5.github.io/docs/nightly/ckeditor5/latest/examples/builds/document-editor.html).

## Documentation

See:

* [Installation](https://ckeditor5.github.io/docs/nightly/ckeditor5/latest/builds/guides/integration/installation.html) for how to install this package and what it contains.
* [Basic API](https://ckeditor5.github.io/docs/nightly/ckeditor5/latest/builds/guides/integration/basic-api.html) for how to create an editor and interact with it.
* [Configuration](https://ckeditor5.github.io/docs/nightly/ckeditor5/latest/builds/guides/integration/configuration.html) for how to configure the editor.
* [Creating custom builds](https://ckeditor5.github.io/docs/nightly/ckeditor5/latest/builds/guides/development/custom-builds.html) for how to customize the build (configure and rebuild the editor bundle).

## Quick start

First, install the build from npm:

```
npm install --save @ckeditor/ckeditor5-build-decoupled-document
```

And use it in your website:

```html
<div id="editor">
	<p>This is the editor content.</p>
</div>
<script src="./node_modules/@ckeditor/ckeditor5-build-decoupled-document/build/ckeditor.js"></script>
<script>
	DecoupledDocumentEditor
		.create( '<h2>Hello world!</h2>', {
			toolbarContainer: '.toolbar-container',
			editableContainer: '.editable-container'
		} )
		.then( editor => {
			window.editor = editor;
		} )
		.catch( err => {
			console.error( err.stack );
		} );
</script>
```

Or in your JavaScript application:

```js
import DecoupledDocumentEditor from '@ckeditor/ckeditor5-build-decoupled-document';

// Or using CommonJS verion:
// const DecoupledDocumentEditor = require( '@ckeditor/ckeditor5-build-decoupled-document' );

DecoupledDocumentEditor
	.create( '<h2>Hello world!</h2>', {
			toolbarContainer: '.toolbar-container',
			editableContainer: '.editable-container'
		} )
	.then( editor => {
		window.editor = editor;
	} )
	.catch( err => {
		console.error( err.stack );
	} );
```

**Note:** If you are planning to integrate CKEditor 5 deep into your application, it is actually more convenient and recommended to install and import the source modules directly (like it happens in `ckeditor.js`). Read more in the [Advanced setup guide](https://ckeditor5.github.io/docs/nightly/ckeditor5/latest/builds/guides/integration/advanced-setup.html).

## License

Licensed under the GPL, LGPL and MPL licenses, at your choice. For full details about the license, please check the `LICENSE.md` file.