# mnml-crop

Basic image cropping with CSS

Demo: [https://rawksteady.github.io/mnml-crop/](https://rawksteady.github.io/mnml-crop/)

HTML

```html
<!-- As a background image -->
<div class="mnml-crop mnml-crop--16by9">
    <div class="mnml-crop__object" style="background-image: url('url.com/image.jpg');"></div>
</div>
<!-- As an actual image -->
<figure class="mnml-crop mnml-crop--16by9">
    <img class="mnml-crop__object" src="url.com/image.jpg" />
</figure>
```

CSS

````css
.mnml-crop {
    height: 0;
    overflow: hidden;
    position: relative;
}
    .mnml-crop--1by1 {
        padding-bottom: 100%; /* (1/1) * 100% */
    }
    .mnml-crop--4by3 {
        padding-bottom: 75%; /* (3/4) * 100% */
    }
    .mnml-crop--16by10 {
        padding-bottom: 62.5%; /* (10/16) * 100% */
    }
    .mnml-crop--16by9 {
        padding-bottom: 56.25%; /* (9/16) * 100% */
    }
    .mnml-crop--21by9 {
        padding-bottom: 42.85%; /* (9/21) * 100% */
    }
    .mnml-crop__object {
        position: absolute;
    }
    .mnml-crop__object:not(img) {
        background-size: cover;
        background-position: 50%;
        height: 100%;
        width: 100%;

        top: 0;
        left: 0;
        bottom: 0;
        left: 0;
    }
    .mnml-crop__object:not(div) {
        display: block;
        min-height: 100%;
        min-width: 100%;

        top: 50%;
        left: 50%;

        -webkit-transform: translate(-50%, -50%);
                transform: translate(-50%, -50%);
    }
