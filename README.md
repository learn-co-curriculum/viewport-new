<iframe width="640" height="480" src="//www.youtube.com/embed/pbXerw3QKek?rel=0&modestbranding=1" frameborder="0" allowfullscreen></iframe><p><a href="https://www.youtube.com/watch?v=pbXerw3QKek">Viewport</a></p>

Another thing we have to be concerned with when building a responsive layout is something called the `viewport`. The `viewport` is the *viewable* area inside of the device's screen. Some devices are set up to zoom in or zoom out, so that it will scale the content to fit the screen. 

This default functionality doesn't play well to our media queries. You may have taken time to write a lot of media queries to make your content scale, stretch, or fit on various sized screens, but the device itself may ignore those media queries by zooming out and shrinking your website, so that all of your website on the desktop size can be viewable within the tiny screen on your phone. 

We've all visited websites on our phone where it will zoom out and everything on the page is very tiny--then you have to zoom in to read the text and see the content. Instead, what we want to do is use the following meta tag, which has the name set to `viewport` and accepts a content attribute. For the value we're able to specify various widths and scaling.

```
<meta name="viewport" content="width=device-width, initial scale=1.0, minimum-scale=1.0, maximum-scale=1.0">
```

What want to specify that the width of our viewport should only be *exactly* as wide as the device. Set its initial scale to 1.0--indicating that the device's initial scale is set to a normal scale, and not to zoom in or out on this content. Additionally if we would like to prevent the user from being able to zoom in and out on their device, we can also set the `minimum-scale` to be `100%`, so the minimum amount that can be scaled is `1`--the `initial-scale`, and the maximum amount that they can scale with `maximum-amount` is also set to `1`, which limits everything to 1.0. This means that the site will scale to the default size of the device width, and our media queries will respond accordingly. This locks the device to one size and allows our media queries to do what they were designed to do--which is to create a responsive site.

<p class='util--hide'>View <a href='https://learn.co/lessons/viewport-new'>Viewport</a> on Learn.co and start learning to code for free.</p>
<p class='util--hide'>View <a href='https://learn.co/lessons/viewport-new'>Viewport</a> on Learn.co and start learning to code for free.</p>
