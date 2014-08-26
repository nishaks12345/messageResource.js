#messageResource.js
**messageResource.js** is a simple JavaScript library for reading message resource property files of following format.
```
#example.properties

home.title = My Tile
home.welcome = Welcome Message
description = This is a brief description message.
```
##Basic Usage
[Clik here](dist/messageResource.min.js) to download messageResource.min.js.
###HTML
```html
<!-- Include messageResource.min.js in the html -->
<script src="messageResource.min.js"></script>
```
###JavaScript
```js

// initialize messageResource.js with settings
messageResource.init({
  // path to directory containing message resource files(.properties file),
  // give empty string or discard this configuration if files are in the
  // same directory as that of html file.
  filePath : 'path/messageresource/'
});

// will load the file moduleName.properties
// and callbackFunction will be executed when loading is complete.
messageResource.load('moduleName', callbackFunction);

// use messageResource.get function to get values from loaded file. 
var value = messageResource.get('sample.key', 'moduleName');

```