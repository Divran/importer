# importer
Just a simple javascript/jQuery thingy which can import/include other html files

# how to use

```HTML
  <!-- first import jquery and this file (order doesn't matter) -->
  <script type="text/javascript" src="js/importer.js"></script>
  <script type="text/javascript" src="js/jquery.min.js"></script>
  
  <script>
    // Next, initialize importer
    $(document).ready(function() {
      importer.initialize(
        "#container",
        {
          "index":"index.html",
          "about":"about.html",
          "contact":"contact.html",
        },
        function(){console.log("I'm alive!");},
        "index"
      );
  	});
  
    // Next, when the user clicks a button, load a page
    $("#someButton").click(function() {
      importer.load(
        ".container",
        "about.html",
        function(){console.log("the about page just loaded!");},
        "about"
      );
    });
  
    // And we're done.
  </script>
```
