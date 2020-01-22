# vue-image-slider


## Install

```bash
npm install --save vue-image-slider
```

## Usage


```HTML
<div id="app">
	<vue-image-slider :images="imageArray" :intervalVal=3000 :height=700 :width=1200 />
</div>
```

```JavaScript
import VueImageSlider from 'vue-image-slider'

export default {
 name: 'app',
 components: {
  VueImageSlider
 },
 data() {
  return {
   imageArray: [
    'https://cdn.pixabay.com/photo/2015/12/12/15/24/amsterdam-1089646_1280.jpg',
    'https://cdn.pixabay.com/photo/2016/02/17/23/03/usa-1206240_1280.jpg',
    'https://cdn.pixabay.com/photo/2015/05/15/14/27/eiffel-tower-768501_1280.jpg',
    'https://cdn.pixabay.com/photo/2016/12/04/19/30/berlin-cathedral-1882397_1280.jpg'
   ],
  }
 },
}
```

## Props



| name            | type                             | default    | description                                                            |
| --------------- | -------------------------------- | ---------- | ---------------------------------------------------------------------- |
| width           | String                           | 700px       | Slider width                                                           |
| height          | String                           | 400px      | Slider height                                                          |
| intervalVal       | Number                           | Undefined       | Delay of autoplay                   |
| images    | Array                         | Undefined | Array of images   |



# License

MIT
