# graphviz-visual-editor

A web application for interactive visual editing of [Graphviz](http://www.graphviz.org) graphs described in the [DOT](https://www.graphviz.org/doc/info/lang.html) language.

*Disclaimer: This project just started (2018-07-17) and so far contains just some basic features. There's still **no documentation**, to some extent the **UI is horrible** (The author is learning [Material UI](https://material-ui.com/) and [React](https://material-ui.com/) while coding) and **some choices in the UI does nothing***.

That said, it's perfectly possible to use it in its current state :smiley:.

## Installation ##

Until the first npm release has been made, the project must be cloned from GitHub:
```
git clone https://github.com/magjac/graphviz-visual-editor",
cd graphviz-visual-editor
npm install
make
npm run start
```

**NOTE:** The *make* stage emits a few warnings. Ignore them.

## Implemented Features ##

* Render a graph from a textual [DOT](https://www.graphviz.org/doc/info/lang.html) repesentation.
* Pan and zoom of the graph.
* Edit the DOT source in a context sensitive text editor.
* Visually edit the graph through mouse interactions:
  * Insert node shapes by click or drag-and-drop.
  * Select default node style, color and fillcolor.
  * Draw edges between nodes.
  * Select nodes and edges by click or by area drag.
  * Delete selected nodes and edges.
  * Cut/Copy-and-paste a selected node.
* Update the DOT source automatically when the graph is visually edited.
* Update the graph automatically when the DOT source is edited.
* Perform an animated transition of the graph into a new state when changes are made.
* The DOT source and the application state are preserved during page reload by automatic save and retrieve to/from local storage in the browser.
* Options:
  * Automatically fit the graph to the avaible drawing area.
  * Select Graphviz layout engine.
* On-line help:
  * Keyboard shortcuts
  * Mouse interactions

## Currently Known Limitations ##

Apart from the numerous cool features that are missing; here's a list of known limitations in the features that do exist:

* The visual editing capabilities requires the DOT source to be organized with only one node or edge per line since it currently operates by inserting or deleting complete lines.
* Cut/Copy-and-paste of nodes in subgraphs is not yet supported.

## Roadmap ##

* Implement some of the nicest-to-have features, learn from that and rework the UI.
* Make the application available through a web server (it actually already is, but the location is still a secret :stuck_out_tongue:).
* Provide documentation.
* Open up for collaboration.
