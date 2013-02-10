## &micro;Publish

### about
&micro;Publish is a web publishing engine written in [Go](http://golang.org).


### usage
By default &micro;Publish expects to be executed while in the directory
that you wish to serve.

``` bash
$ upublish
```

#### Required Files
The only file that is required by &micro;Publish is a single template file,
which must contain the token "{{content}}".

Example:

``` HTML
<!DOCTYPE html>
<html>
  <head>
    <title>Example</title>
  </head>
  <body>
    <h1>Example &micro;Publish Template</h1>
    <div class="content">
      {{content}}
    </div>
  </body>
</html>
```

#### Command Line Options

Name      | Default       | Description
----------|---------------|---------------------------------------------------
-addr     | :8080         | The address to listen for incoming connections on
-debug    | false         | Enable debug mode; disables caching of files
-default  | index         | The default file to serve when none is provided
-ext      | md            | The extension of the markdown files
-home     | /             | The directory to server when '/' is requested
-path     | .             | The directory of the files to serve
-public   | public        | Which directory to serve static files from
-tmpl     | template.html | The name of the template file