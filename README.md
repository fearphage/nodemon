# nodemon

For use during development of a node.js based application. 

`nodemon` will watch all the files in the directory that nodemon was started, and if they change, it will automatically restart your node application.

`nodemon` does **not** require *any* changes to your code or method of development. `nodemon` simply wraps your node application and keeps an eye on any files that have changed.

# Usage

`nodemon` wraps your application, so you can pass all the arguments you would normally pass to your app:

    nodemon [your node app]
    
For example, if my application accepted a host and port as the arguments, I would start it as so:

    nodemon ./server.js localhost 8080

Any output from this script is prefixed with `[nodemon]`, otherwise all output from your application, errors included, will be echoed out as expected.

# Ignoring files

In some cases you will want to ignore some specific files, directories or file patterns, to prevent nodemon from prematurely restarting your application.  

An example `ignore` file:

    # this is my ignore file with a nice comment at the top
    
    /vendor/*     # ignore all external submodules
    /public/*     # static files
    ./README.md   # a specific file
    *.css         # ignore any CSS files too

The ignore file accepts:

* Comments starting with a `#` symbol
* Blank lines
* Specific files
* File patterns (this is converted to a regex, so you have full control of the pattern)

# Prerequisites

`nodemon` currently depends on the [unix find](http://unixhelp.ed.ac.uk/CGI/man-cgi?find) command (which also is installed on Macs)

# Todo

* Offer a better way to change the monitoring frequency (currently hard coded to 1 second)
* Support windows based users (maybe...)