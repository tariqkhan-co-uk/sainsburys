# Sainsbury’s Entertainment Test

### Software Developer Front-End

## Programming Test

> [Link](https://rawgit.com/tariqkhan-co-uk/sainsburys/master/programming.html)

Any problems I've encountered have been noted as comments within the source code. I may have over-commented?

Features implemented:
* Toggle user's favourite photos
* Selected images have a selected class
* De-selection of a selected photo
* Remember selected images on page reload

I have not used any frameworks including jQuery.

I would usually seperate html from css and javascript, but have not for the purpose of this test to enable you to view all relevant code from within one file.

Implemented cross-compatibility for the following browsers:
* Chrome
* Firefox
* IE versions 9+

IE 7 and 8 can be supported by implementing code to 'attachEvent' rather than 'addEventListener' and including code alternative to 'indexOf':

```html
if(!Array.prototype.indexOf) {
	Array.prototype.indexOf = function(obj, fromIndex) {
		if(fromIndex == null) {
			fromIndex = 0;
		} else if(fromIndex < 0) {
			fromIndex = Math.max(0, this.length + fromIndex);
		}
		for(var i = fromIndex; i < this.length; i++) {
			if(this[i] === obj)
				return i;
		}
		return -1;
	};
}
```


## Design Test

> [Link](https://rawgit.com/tariqkhan-co-uk/sainsburys/master/design.html)

Again, I would usually seperate html from css and javascript, but have not for the purpose of this test to enable you to view all relevant code from within one file.

* I have catered for ALL devices by implementing fully responsive.
* Clicking on the menu will display additional menu entries. Although, not implemented, you can have the menu close when clicking anywhere other than the menu by implementing a 'back to top' link, which has height and width set to 100% and positioned below the menu when the navigation target is active.
* I have not used javascript.
* I have not used Bootstrap/Foundation
* I have not applied any attributes to the html tags and have instead creating div elements within. I usually do this, in case, support for an older browser is required.

Implemented cross-compatibility for the following browsers:
* Chrome
* Firefox
* IE versions 9+

IE 8 is supported with the use of respond.js (polyfill for min/max-width)
IE 7 is supported with use of 1 conditional statement to enable relocating the 'More...' section as per mobile design view
