You can use keyframes to animate CSS features.

```css
.animated {
	background: repeating-linear-gradient(
	  90deg,
	  blue 0px,
	  blue 10px,
	  purple 10px,
	  purple 20px
	);
	animation: slider  /* name of keyframe to use */
	           1s  /* duration of the animation */
             linear  /* timing function of the animation, eg cubic-bezier */
             0s  /* delay before animation starts */
             infinite  /* how many times the animation should play */
	           normal  /* direction of animation, eg reverse or alternmate */
	           forwards
	           running;
}

@keyframes slider {
	0% { background-position: -28px -28px; }
	100% { background-position: 0px 0px; }
}
```