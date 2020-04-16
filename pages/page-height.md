# Setting custom page height of iFrame
Page embeded in mCourser is available via iFrame. Because of it, mCourser do not know how long provided site is.
Sometimes page may be too short or multiple scrollbars appears. In these cases, provided page should send own height.

For sending new height to mCourser, use [mCourser communication](https://github.com/icplayer/mCourser-iframe-communication).
After initialization, send height of document: `communication.updateIFrameHeight(documentHeight);`. Example:

    communication.init().then((isAuth) => {
      // ...
      var siteHeight = getSiteHeight(); // It should be implemented
      communication.updateIFrameHeight(siteHeight);
    });
    
That method can be called more than once.


It's good practice to send height at least one per site initialization.
mCourser site does not set always the same iframe size and size may be changed in the future (e.g. UI changes).
