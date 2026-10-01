# Subfigures

**Problem**  
1. Numbering of subfigures goes wrong when converting. A single figure is numbered 1.1, a subfigure is not adhering to the rules specified in the template - it becomes in the example figure 2 rather than figure 1.2. The reason is that a subfigure is now seen as a grid rather than as a figure:
2. Numbering is hardcode in typst: `This reference should take refer to figure 2a: #link(<fig_tree_2>)[Figure~2a], and this one to figure 2 in general: #link(<fig_trees>)[Figure~2].` where `#link(<fig_tree_2>)[@fig_tree_2]` should be preferred!

Issue 1 might relate to template - have to look it up, no 2 needs a fix.


**Example**  
```{figure} tree_2.png
:width: 80%

A non labeled image of a tree
```


````{figure}
:label: fig_trees
```{figure} tree_2.png
:label: fig_tree_2
:width: 80%

A tree
```
```{figure} tree_3.png
:label: fig_tree_3
:width: 80%

A tree with bg
```
An idea to compare branches with painting with layers
````


This reference should take refer to figure 2a: @fig_tree_2, and this one to figure 2 in general: @fig_trees.