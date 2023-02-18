You can specify the font to use on text using the `font-family` property.

There are several ways a font can be used:
### Your user has it installed
```css
.my-text {
	font-family: "Wingdings 2";
}
```

### You provide it yourself
```css
@font-face {
  font-family: 'Wingdings 2';
  src: url("path/to/font.ttf");
  font-weight: normal;
  font-style: normal;
}
/* Now this works! */
.my-text {
	font-family: "Wingdings 2";
}
```

### You load it from somewhere else
You can just link to some other server that has the font, such as [Google Fonts](https://fonts.google.com).

## Font size
Many ways to 
