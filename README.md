# SameBoy MacOS Build Instructions.

Building the SameBoy out-of-the-box for MacOS

Motivation : I DL'd the SameBoy app but it wouldn't run due to signing. I'm a dev so I got it going from source

# Instructions

* Make sure you have Brew installed
* XCode too
* Clone SameBoy -> https://github.com/LIJI32/SameBoy.git
* Clone RGBDS -> https://github.com/gbdev/rgbds
* Next, ensure that Bison is install `brew install bison`
* Next, FORCE the Brew version of Bison is acccessible `brew link bison --force `
  * This is necessary as MacOS will pick an older version of Bison shipped with XCode
  * THIS MAY NOT WORK in which case manually add `/usr/local/opt/bison/bin` to you PATH
* Build RGBDS (this requires version 3+ of Bison)
* Add the RGBS binaries to your PATH
* Now head back to SameBoy and use `make -j $SOMEBIGNUMBER` to build SameBoy
* Now use `open $BLAH/SameBot.app`

That's probably it. Now you can write code with rgasm to make a cart and then open it in SameBoy.

There's a very useful "hello world" toot here -> https://gbdev.io/gb-asm-tutorial/part1/hello_world.html
