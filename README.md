# wantsVideo

This is a script that enhances static images with autoplaying video in browsers that support it.

## Latest CDN version

https://interactive.guim.co.uk/libs/wants-video/wantsVideo.js

# Usage

Include the library within your page or application via `<script>`.

(that's all for now, and the below is just a plan for how it will work in the future…)

Add a data-wants-video attribute to `<img>` tags, pointing to the video version of the image. For example:

```html
<img data-wants-video="https://uploads.guim.co.uk/2016/11/11/VR_Richlink_abr400.mp4"
      src="https://uploads.guim.co.uk/2016/11/11/vr-kit@1x.jpg">
```

When you call the wantsVideo() method, the script will test the browser for autoplaying video support, and inject a `<video>` tag immediately before the `<img>` tag. In the above example, the result would be:

```html
<div class="video">
  <video poster="https://uploads.guim.co.uk/2016/11/11/vr-kit@1x.jpg" loop="true">
    <source src="https://uploads.guim.co.uk/2016/11/11/VR_Richlink_abr400.mp4" type="video/mp4">
  </video>
</div>
<img data-wants-video="https://uploads.guim.co.uk/2016/11/11/VR_Richlink_abr400.mp4"
      src="https://uploads.guim.co.uk/2016/11/11/vr-kit@1x.jpg">
```
