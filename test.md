We know that it's a good idea to design responsively to provide the best multi-device experience,
but responsive design also yields a win for accessibility.

qwerty

Consider a site like [Udacity](https://udacity.com):

<figure class="w-figure">
  {% Img src="image/admin/5q9dDtEubSM23SzokQNu.jpg", alt="The Udacity site", width="800", height="393", class="w-screenshot" %}
</figure>

A low-vision user who has difficulty reading small print might zoom in the page,
perhaps as much as 400%.
Because the site is designed responsively,
the UI will rearrange itself for the "smaller viewport" (actually for the larger page),
which is great for desktop users who require screen magnification
and for mobile screen reader users as well. It's a win-win.
Here's the same page magnified to 400%:

<figure class="w-figure">
  {% Img src="image/admin/WKHO21uWQz5lJ7Aqej1E.jpg", alt="The Udacity site zoomed to 400%", width="800", height="393" %}
</figure>

In fact, just by designing responsively,
we're meeting rule [1.4.4 of the WebAIM checklist](https://webaim.org/standards/wcag/checklist#sc1.4.4),
which states that a page "… should be readable and functional when the text size is doubled."

Going over all of responsive design is outside the scope of this guide,
but here are a few important takeaways that will benefit your responsive experience
and give your users better access to your content.

## Use the viewport meta tag

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Setting `width=device-width` will match the screen's width in device-independent pixels,
and setting `initial-scale=1` establishes a 1:1 relationship between CSS pixels and device-independent pixels.
Doing this instructs the browser to fit your content to the screen size,
so users don't just see a bunch of scrunched-up text.

See [Size content to viewport](/responsive-web-design-basics/#viewport) to learn more.

## Allow users to zoom

It is possible to use the viewport meta tag to prevent zooming,
by setting `maximum-scale=1` or `user-scaleable=no`.
Avoid doing this, and let your users zoom in if they need to.
