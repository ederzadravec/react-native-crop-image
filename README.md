# React Native image crop


## Installation

`yarn add @ederzadravec/react-native-image-crop`


This library uses react-native-svg, you must install it too. See https://github.com/react-native-community/react-native-svg for more infos.

#### Android Only

If you do not already have openCV installed in your project, add this line to your `settings.gradle`

```
include ':openCVLibrary310'
project(':openCVLibrary310').projectDir = new File(rootProject.projectDir,'../node_modules/react-native-image-crop/android/openCVLibrary310')
```

## Crop image

```js
const imageCropRef = React.useRef();

const handleOnCrop = () => {
  imageCropRef.current.crop
}

<ImageCrop ref={imageCropRef} />
```


## Props

| Props                  | Type               | Required | Description                                                                             |
| ---------------------- | ------------------ | -------- | --------------------------------------------------------------------------------------- |
| `updateImage`          | `Func`             | Yes      | Returns the cropped image and the coordinates of the cropped image in the initial photo |
| `rectangleCoordinates` | `Object` see usage | No       | Object to predefine an area to crop (an already detected image for example)             |
| `initialImage`         | `String`           | Yes      | Base64 encoded image you want to be cropped                                             |
| `height`               | `Number`           | Yes      | Height of the image (will probably disappear in the future                              |
| `width`                | `Number`           | Yes      | Width of the image (will probably disappear in the future                               |
| `overlayColor`         | `String`           | No       | Color of the cropping area overlay                                                      |
| `overlayStrokeColor`   | `String`           | No       | Color of the cropping area stroke                                                       |
| `overlayStrokeWidth`   | `Number`           | No       | Width of the cropping area stroke                                                       |
| `handlerColor`         | `String`           | No       | Color of the handlers                                                                   |
| `enablePanStrict`      | `Bool`             | No       | Enable pan on X axis, and Y axis                                                        |


## Thank you very much ...

This lib is a customization of [React Native perspective image cropper](https://github.com/Michaelvilleneuve/react-native-perspective-image-cropper)
