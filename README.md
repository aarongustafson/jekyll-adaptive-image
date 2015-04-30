# Jekyll Adaptive Images

An implementation of Adaptive Images with `srcset` and `sizes` using [Google’s open image resizing service](https://carlo.zottmann.org/2013/04/14/google-image-resizer/).

The tag is simple:

	{% adaptive_image /path/to/image.jpg [attr="value"] %}

You can add as many attributes as you want.

## Global Configuration

To keep things simple and consistant, you can set up the standard sizes of your adaptive images in variables in `_config.yml`:

	adaptive_image:
	  cache: 2592000
	  srcset: 
	    - 1920
	    - 600
	    - 320
	  sizes:
	  	- "(min-width:60em) 42.5em"
	    - 100vw
	
* `cache` is for the length of time you want to cache it (in seconds)
* `srcset` is a list of sizes (in unitless pixel widths) you want to offer
* `sizes` is the size configurations for layout purposes