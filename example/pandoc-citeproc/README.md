#### pandoc and pandoc-citeproc

Render this paper to latex (prints to screen):

    pandoc --filter pandoc-citeproc -s paper.md -t latex

More at [this example](http://pandoc.org/demo/example19/Extension-citations.html)


```
sudo apt-get update 
sudo apt-get install pandoc-citeproc
pandoc --filter pandoc-citeproc -s citeme.md -o citeme.html
```