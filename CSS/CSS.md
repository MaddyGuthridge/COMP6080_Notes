Cascading style sheets

## Cascade
Each element is applied in order. See also: [[inclusion]]
1. External CSS files
2. [[style]] tags in [[HTML]]
3. Inline styles override everything
4. Except for `!important` markers
	- You should probably avoid them though, because they are hacky and make code very unclean

Also consider *specificity*
- If multiple rules provide the same [[properties]], the most specific one is chosen
- [Specifishity](https://specifishity.com) explains it
- This is kinda complicated
- You'll probably never use it
- But it works under the hood

