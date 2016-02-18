<a name="differences"></a>
Like all web apps, the user interface for our sample app is built from an HTML file, (`index.html`), which you can see in the following:

``` html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8" />
	<title>Converter</title>
    <script src="converter.js"></script>
</head>
<body>
	<p>
		<label for="meters">Meters:</label>
		<input type="text" id="meters">
	</p><p>
		<label for="feet">Feet:</label>
		<input type="text" id="feet" readonly>
	</p><p>
		<button id="convert">Convert</button>
	</p>
</body>
</html>
```
The <`script`> tag brings in the following JavaScript, which is in the file `converter.js`:

```javascript
"use strict";
window.onload = function () {
	document.querySelector("#convert").addEventListener("click",
		function () {
			var meters = document.querySelector("#meters");
			var feet = document.querySelector("#feet");
			feet.value = meters.value * 3.28084;
			console.log(feet.value);
		}
	);
};
```
The code executes in the `window.onload` event handler to ensure that all of the HTML elements are loaded before they’re referenced. Another event handler is set up to do the actual work when you click the `convert` button. Both handlers are passed anonymous functions that execute when the corresponding event fires.

Two more small files turn this web app into a Chrome App. The first, `manifest.json`, identifies the web app as a Chrome App. The manifest is coded in JavaScript Object Notation (JSON) to define values for at least four required properties, like this:

```javascript
{
	"app": {
		"background": {
			"scripts": [ "background.js" ]
		}
	},
	"icons": {
    "16": "assets/icon_16.png",
    "128": "assets/icon_128.png"
  },
	"manifest_version": 2,
	"name": "Converter",
	"version": "1.0.0"
}
```
