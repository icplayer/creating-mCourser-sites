# creating-mCourser-sites
This repository contains information how to create site for embeding into mCourser.

## mCourser communication
For communication from your site to mCourser additional repository have been maintained: [mCourser communication](https://github.com/icplayer/mCourser-iframe-communication). This repository contains simple util for sending messages between the sites.

## Creating site
mCourser contains only few requirement and limitations: 
* All paths must be relative: styles, JS or images.
* Package must be zip file with index.html file in root.
* Provided package sends information about site height, see: [Site height](./pages/page-height.md)
* Not all APIs between the sites are available. It depends of usage context.


## Faq
* React application resolves paths as absolute: In `package.json` set `"homepage": "."`. See [React example](https://github.com/icplayer/mCourser-iframe-communication/blob/master/examples/react/package.json).
* Unpacking package takes too long, how to test it faster?: See [How to test site](./pages/test-site.md).
* Is there any example of ready site?: [mCourser communication examples](https://github.com/icplayer/mCourser-iframe-communication/tree/master/examples) contains examples.
