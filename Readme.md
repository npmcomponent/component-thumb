*This repository is a mirror of the [component](http://component.io) module [component/thumb](http://github.com/component/thumb). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/component-thumb`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# Thumb

  Scale an image or data uri within the given dimensions.

  ![canvas thumbnail image generator](http://f.cl.ly/items/3V2X113N01042G1H0A1u/Screen%20Shot%202012-08-09%20at%2011.35.20%20AM.png)

## Installation

```
$ npm install thumb-component
```

## Example

```js
var thumb = require('thumb');
var input = document.querySelector('input');

input.onchange = function(e){
  var reader = new FileReader;

  reader.onload = function(){
    thumb(reader.result, 200, 200, function(err, img, datauri){
      document.body.appendChild(img);
    });
  };

  reader.readAsDataURL(input.files[0]);
};
```

## License

  MIT