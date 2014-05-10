# What's this

Now you can use a simple and pure javascript lib to mask html elements. Fuck jQuery, Zepto and any others javascript frameworks!

Let's live now in a lightweight client-side world using VanillaMasker.  
This is a cross-browser and cross-device lib for desktop and responsible sites.

The [demo page](http://bankfacil.github.io/vanilla-masker/demo.html).

# How to use

Download the lib: [development version](https://raw.githubusercontent.com/BankFacil/vanilla-masker/master/build/vanilla-masker.js) (3.33 Kbytes), [minified version](https://raw.githubusercontent.com/BankFacil/vanilla-masker/master/build/vanilla-masker.min.js) (1.87 Kbytes) or [gzipped version](https://raw.githubusercontent.com/BankFacil/vanilla-masker/master/build/vanilla-masker.min.gz.js) (711 bytes).

Include it into your html page:
``` html
<script src="vanilla-masker.min.js"></script>
```

And given these simple inputs tag:
``` html
<input type="text">
<input type="text">
<input type="text">
```

You can use the code below...
``` javascript
// Instancing the VanillaMasker object
var masker = new VanillaMasker({
  precision: 2, // Decimal precision
  separator: ',', // Decimal separator
  delimiter: '.', // Number delimiter
  unit: 'R$', // Money unit (default is a blank string)
  zeroCents: true // Fill decimals with zero value
});

// Masking an input element to money.
masker.maskMoney(document.querySelector("input"));

// Masking an input element to accept only positive numbers without decimal precision.
masker.maskNumber(document.querySelector("input"));

// Or masking an all input elements to money.
masker.maskMoney(document.querySelectorAll("input"));
```

# How to run localhost

* Install node.js - http://nodejs.org/download
* Clone this repository - `git clone git@github.com:BankFacil/vanilla-masker.git`
* Install Grunt - `npm install -g grunt-cli`
* Install Grunt dependencies - `cd vanilla-masker && npm install`
* Running development mode - `grunt dev`
* Open the browser - http://localhost:4500

# Run test

* Run the command: `grunt test`

# Build project

* Run the command: `grunt build`

# TODO

* Mask custom inputs methods, like maskPhone, maskZipCode, etc;
* Bower compatibility;
* AMD support;
* JSHint task;

# Compatibility

Desktop browsers:

* Chrome
* Firefox
* Safari
* Opera
* Internet Explorer 9+ (coming soon IE8 support)

Mobile browsers:

* Android (2.2+) native browsers
* Chrome mobile
* Dolphin
* Opera mobile (not tested yet)
* iOS (not tested yet)

# Contributors

Caio Ribeiro Pereira - caio.ribeiro.pereira@gmail.com  
Leandro Alvares da Costa - leandroadacosta@gmail.com

# License

MIT License: http://bankfacil.mit-license.org

# Powered by

Bankfacil: http://www.bankfacil.com.br  
