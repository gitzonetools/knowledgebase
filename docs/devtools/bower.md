## Bower

### Install Bower
bower is installed using npm:

    $ npm install -g bower

### bower.json and .bowerrc
when running bower in a directory bower looks for two files: `bower.json` and `.bowerrc`.

It starts to look for them in the current working directory of your path and, if it doesn't find them, moves up one folder level at a time.

#### the package config file:`bower.json`
The bower.json file contains information about:
* packagename
* dependencies
* package and dependency versions


### Install Bower Packages

To install bower packages you have to type

    $ bower install [packagename]

So to install jQuery you would type

    $ bower install jquery

### Useful Bower Packages

Name | Description | install command
--- | --- | ---
ajaxchimp | library to easify communication with Mailchimp |
angular | crossbrowser js library |
jquery | crossbrowser js library |
polymer | a library of webcomponents by Google | bower install --save Polymer/polymer#^1.0.0