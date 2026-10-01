# Inline figs explode

**problem**  
If you have an inline figure like this one ![](smiley.png) it just blows up in the pdf.

**issue**  
https://github.com/jupyter-book/mystmd/issues/2820

**solution**  
Check whether it is an inline figure and set a max height in px comparable with fontsize.