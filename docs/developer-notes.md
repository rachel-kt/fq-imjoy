# Development notes
## Documentation
Documentation is written with mkdocs using the Material style.

* [mkdocs website](https://www.mkdocs.org/)
  
### Installation

Install mkdocs:  `pip install mkdocs`

### Preview and deployment

* Launch dev-server: `mkdocs serve`
* Building the site: `mkdocs build`
* Deploy to GitHub pages: `mkdocs gh-deploy` 
    **Note**:  if this does not work, force commit with `mkdocs gh-deploy --clean --force`

### Some options

#### PyMdown Extensions
https://squidfunk.github.io/mkdocs-material/extensions/pymdown/

https://facelessuser.github.io/pymdown-extensions/#extensions

allows to create block-styled side conten

```
!!! note "This is a note"
    Lorem ipsum dolor sit amet
```

!!! note "This is a note"
    Lorem ipsum dolor sit amet

#### Resize images
Includes the  [attr_list extension](https://python-markdown.github.io/extensions/attr_list/), which allows for resizing (among other things):

```
![imjoy-connect-jupyter.gif](img/imjoy-connect-jupyter.gif){: style="width:300px"}
```
![imjoy-connect-jupyter.gif](img/imjoy-connect-jupyter.gif){: style="width:300px"}

```
![imjoy-connect-jupyter.gif](img/imjoy-connect-jupyter.gif){: style="width:100px"}
```
![imjoy-connect-jupyter.gif](img/imjoy-connect-jupyter.gif){: style="width:100px"}


## Update imjoy manifest
After changes in ImJoy plugins, update the plugin manifest.

Install `node.js` with conda

``` bash
conda install -c conda-forge nodejs
```

Run this command in project root directory
``` bash
node update_manifest.js
```