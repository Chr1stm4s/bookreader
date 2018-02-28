# 3.0.0 Major Release

Version 3.0.0 is an effort to make BookReader more modular, extensible, and easier to use.

Changes include:

- Make BookReader easier to use, by adding `options` to the constructor, and adding new `options.data` option. The old way of overriding properties should still work, but it is deprecated. With `options.data`, all BookReader needs is the image URLs and dimensions. To have dynamic image URLs (eg for scaling), omit the URL from `options.data`, and include `options.getPageURI`.
- Factor out extra features into plugins. See `plugins` directory. Example plugins include:  
    - plugins.chapters.js - render chapter markers  
    - plugins.search.js - add search ui, and callbacks  
    - plugins.tts.js - add tts (read aloud) ui, sound library, and callbacks  
    - plugins.url.js - automatically updates the browser url  
    - plugins.resume.js - uses cookies to remember the current page  
    - plugins.mobile_nav.js - adds responsive mobile nav to BookReader  
Note that there is minor overhead added when loading multiple script tags. If this is a concern, a build step, can be used to concatenate the files into a single JS file.
- Clean up code: Remove a lot of commented-out code. Remove some unused methods.  
- Change some, but not all, CSS ids to classes.  
- DEPRECATED: Use options to configure BookReader. It is now deprecated to change properties directly.
- DEPRECATED: CSS ids are being removed, (eg #BookReader is now .BookReader), with the goal to entirely use classes instead. This is in progress, but it is considered deprecated to use the ids directly. We would like to remove all ids for the next major release.
- BREAKING: If features that are now in plugins were used, the plugin's JS file will need to be included as well. Note, we would also like to separate the CSS into a separate file for the next major release.

# 2.1.0
- Add auto mode to 1up autosize (in addition to height and width)  
- Remove the old responsiveAutofit (which is not needed anymore)  

# 2.0.2
- Fix regex issue when searching  
- Make the search api endpoint configurable  

# 2.0.1
- Add package.json and CHANGELOG  
- Remove more IA-specific code  

# 2.0.0
- Major release  
- Many changes from updated Archive.org bookreader brought back to this open source project.  
