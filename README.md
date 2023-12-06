# Redis Hugo site template

## Files and folders

* **/archetypes**: A Markdown file needs to have some front matter. An archetype defines which front matter is used when using `hugo new content`. Right now, the only supported archetype is the default one. **Note:** We might want to add additional archetypes in the future because most of our pages contain additional meta data properties like `linkTitle`. 
* **/content**: This folder contains the markdown files. We will have the subfolders `docs/develop`, `docs/integrate`, and `docs/operate``
* **/assets**: CSS files, site-wide icons and images
* **/data**: Data files that are accessed by Hugo. The data is then rendered with the help of short codes or partials.
* **/layouts/partials**: HTML templates that are used across sites. Examples are TOC-s, breadcrumps, or headers. 
* **/layouts/$type**: Each page type has at least the following templates to implement `single.html` and `list.html`. The `single` template is used to render a concrete page. The `list` template is used to render a collection (e.g., all sub-pages).
* **/layouts/home.html**: The home page of the site. So the page that is entered when you open the root path
* **/layouts/404.html**: The default 404 page.
* **/layouts/shortcodes** HTML template snippets that you want to leverage within Markdown files. Examples are tabbed code examples or notification blocks.
* **/public**: This is the folder that is generated by Hugo. This content needs to be published by you.
* **/static**: Any static files that need to be accessed by the site, e.g., CSS or JavaScript.
* **/package.json**: Node.js dependencies. Tailwind, for instance, is installed via the Node package manager (`npm`).
* **/config.toml**: Hugo's site configuration, like the root path and menu items. Hugo can access configuration elements when rendering the site. So you can define custom configuration settings here.
* **/syntax.css**: Hugo supports syntax highlighting via shortcodes. The highligher is configured via this CSS file.
* **/Makefile**: We use make to wrap some Hugo commands and to add addtional build steps.
* **/tailwind.config.js**: This is the Tailwind CSS framwork's configuration file.
* **/postcss.config.js**: Needed to make Tailwind statically accessible to the site.

## Build script and data files

> TODO

## How to build

1. Use `make` to clean and build everything `make all`
2. Then run Hugo in debug mode to build the site `make build`
3. The build result can be found within the folder **/public**



