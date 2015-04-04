ofxFontAwesome
===



Simple list of constants to use [FontAwesome](http://fortawesome.github.io/Font-Awesome/icons/) in OpenFrameworks. 
Includes FontAwesome version 4. 



Install Instruction
----

1. Clone this repo into your addons folder
2. Drag ofxFontAwsome to your project
3. Make sure fontawesome-webfont.ttf is copied during the build stage. 
    a. OSX: Click on your target, go to Build-Phases, add this to the Run Script phase:<br>
    `cp -rf ../../../addons/ofxFontAwesome/bin/data/ "$TARGET_BUILD_DIR/$PRODUCT_NAME.app/Contents/Resources"`
    b. Windows: ??
    c. Linux: ??
    d. Alternative: Just drop the ttf in your bin/data folder


Usage
---

Only works with [ofxFontStash](https://github.com/armadillu/ofxFontStash)

	#include "ofxFontAwesome.h"
	#include "ofxFontStash.h"

	ofxFontStash font = NULL;
	
	void ofApp::setup(){
			font.loadFont("fontawesome-webfont.ttf", 100);
	}
	
	void ofApp::draw(){
		ofBackground(0); 
		
		ofSetColor(255);
		font.drawString( ofxFontAwesome::compress + "    " + ofxFontAwesome::expand, 50, 100);
	}

Produces the following output: 

![Preview image](preview.png =100x)



Licensing
---

The font itself (fontawesome-webfont.ttf) is licensed under the [SIL OFL1.1](http://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&id=OFL), the "code" is under the [WTFPL](http://www.wtfpl.net/txt/copying/)