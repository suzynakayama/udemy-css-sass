# Advanced CSS and Sass - Udemy

## By [Jonas Schmedtmann](https://www.udemy.com/course/advanced-css-and-sass/)

<h3 id='summary'>Summary</h3>

- [Advanced CSS and Sass - Udemy](#advanced-css-and-sass---udemy)
  - [By Jonas Schmedtmann](#by-jonas-schmedtmann)
    - [Normalize CSS](#normalize-css)
    - [Basic CSS](#basic-css)
          - [Background-image](#background-image)
          - [Clip-path](#clip-path)
          - [Keyframes Animations](#keyframes-animations)

### Normalize CSS

[Summary](#summary)

Reset the css to make every browser to have the same basic css as you want. Nowadays, the browsers are much better, so a simple reset is enough.

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

Note. Never put font related css into the universal selector `*`. Put it on the body.

### Basic CSS

[Summary](#summary)

###### Background-image

[Summary](#summary)

You can add multiple background images, for example an image on the bottom and a gradient on top. To do this use the `background-image` property and define from the top to the bottom. Ex: `background-image: linear-gradient(to right bottom, rgba(126, 213, 111, 0.8), rgba(40, 180, 133, 0.8)), url('../images/hero.jpg');`.

###### Clip-path

[Summary](#summary)

With `clip-path` you can create a geometrical form to clip your image with.
```
                    1    2    3    4
clip-path: polygon(x y, x y, x y, x y);
where: 
1 = top left corner
2 = top right corner
3 = bottom right corner
4 = bottom left corner
Ex. triangle => clip-path: polygon(50% 0, 100% 100%, 0 100%);
Ex2. clip-path: polygon(0 0, 100% 0, 100% 75vh , 0 100%);
```
You can check this website [Clippy](https://bennettfeely.com/clippy/) to play with some forms and get the proper numbers.

###### Keyframes Animations

[Summary](#summary)

For browser perfomance is best to animate only 2 properties: `opacity` and `translate`, because the browsers are optimized for.

*Hack*: use `backface-visibility: hidden;` to fix the shaking at the end of the animation. Also, this is used for not showing the back of the element when animating it.