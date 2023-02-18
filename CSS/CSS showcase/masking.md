Masking is used to apply a background to particular regions of a div.

### Text masking
```css
.firey-text {
	/* Set the background to be a picture of fire */
	background-image: url(https://fireimages.com/example-1.jpg);
	/* Create a mask so that the background only appears around the text */
	background-clip: text;
	/* Create the same mask a second time, since otherwise it doesn't work
	 * on Chrome or something. Just web standards things */
	-webkit-background-clip: text;
	/* Finally, set the text to transparent so we can see the background 
	 *  through it */
	color: transparent;
}
```

### Clipping
```css
/* clip in a circle */
.circle {
	clip-path: circle(32px at 94px 75px);
}

/* clip in a polygon */
.poly {
	/* literally just a polygon from a series of points */
	clip-path: polygon(75px 50px, 90px 55px, 120px 50px);
}

/* clip in a custom shape. Only supported on Firefox */
.path {
	/* literal demon shit - the lecturer DID NOT explain this. I have no 
	 * idea what's going on. I think I'll have an aneurism if I think 
	 * about this for too much longer AAAAAAAAAAAAAAAAAAAAAAAAAAAAA */
	clip-path: path('M 75 66 C 70.2 74 73 86.6667 75 92 C 77.8 89.6 103.5 91 116 92 C 118 87.6 116.167 75.8333 115 70.5L123 52.5 L 108 58.5 C 104 56.1 89.6667 56.5 83 57 L 69 50 L 75 66');
}
```

### Image masking
Use a URL for a mask image. Mask images have black meaning fully visible, and white as fully transparent.

```css
.image-mask {
  mask-image: url(https://image-url.com/image.png);
  /* Chrome has lets be diferent syndrome I guess */
  -webkit-mask-image: url(https://image-url.com/image.png);
}
```