# Testing custom site
There are two options for the site testing:
* Upload new site and click "preview" button.
* Edit the iFrame URL.

Because first option for larger sites takes some time, it's possible to test it by changing the iFrame URL. 
It can be done by browser utils. All of them requires at least one custom site and localhost server. 

## Editing iFrame URL
### Providing localhost server
For changing iFrame URL there is required to open the site by any server (http/https protocol is required).

If the site is developed by "create-react-app", "angular-cli" or any other framework, it should provide own reloading server.
An IP of that server can be used.

If the site is developed manually, there is required to provide any server. Example server:
 * [Nodejs HTTP Server](https://www.npmjs.com/package/http-server)
 * [Python HTTP Server](https://docs.python.org/2/library/simplehttpserver.html)
 * [Apache](https://httpd.apache.org/)

### Changing URL
* Chrome:
    * Click on the preview button.
    * Click by right mouse button on opened site.
    * Click "inspect". Now there should appears new window.
    * In the new window find "iframe" tag with your site.
    * Double click on the "src" attribute.
    * Enter the address of your server. 
* Firefox:
    * Click on the preview button
    * Click by right mouse button on opened site.
    * Click "inspect element". There should appear new window.
    * In the new window find "iframe" tag with your site.
    * Double click on "src" attribute.
    * Enter the address of your server. 
