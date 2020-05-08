# creating-mCourser-sites
This repository contains information how to create site for embeding into mCourser.

## Requirements
Custom Table Of Content is not just not only a simple static page. It gives a possibility to embed any site of any complexity into mCourser.
Because of it, a site creator should be familiar with the following technologies:
 * HTML 5
 * JS
 * CSS
 
Each site should be created by a web developer because of the complexity of ToC. 
Even simple redirection to a lesson requires a communication with mCourser by a library provided by us.

Additional skills, which would be useful while site creation are:
 * Typescript
 * React
 * Angular
 
## mCourser communication
For communication from your site to mCourser additional repository have been maintained: [mCourser communication](https://github.com/icplayer/mCourser-iframe-communication). That repository contains simple util for sending messages between the sites.

## Creating site
mCourser contains only few requirement and limitations: 
* All paths must be relative: styles, JS or images.
* A package must be zip file with index.html file in root.
* The site sends information about site height, see: [Site height](./pages/page-height.md)
* Not all APIs between the sites are available. It depends of usage context.


## Faq
* React application resolves paths as absolute: In `package.json` set `"homepage": "."`. See [React example](https://github.com/icplayer/mCourser-iframe-communication/blob/master/examples/react/package.json).
* Unpacking package takes too long, how to test it faster?: See [How to test site](./pages/test-site.md).
* Is there any example of ready site?: [mCourser communication examples](https://github.com/icplayer/mCourser-iframe-communication/tree/master/examples) contains examples.
