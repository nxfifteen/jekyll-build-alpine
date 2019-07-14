# Jekyll Build Image, based on Alpine

There are alot of basic Docker containers to build a Jekyll site with, but that doesn't mean I didnt want to create my own.

This image is intended to be used along with your Gitlab or Travis continus integration scripts.

It fires up a instance of Alpine with the baisc Jekyll requirments pre-installed - Jekyll is not installed. Instead I use `bundle install`as part of my CI script. This makes sure the instance installs the right version of Jekyll for any given site. There's no point if this image installs the latest version of Jekyll but I've not updated my site to support it yet, or having to rebuild the image with every Jekyll release. Instead I thought it better to include what is required, everything else can come the the Gemfile.
