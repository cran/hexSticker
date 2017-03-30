<!-- README.md is generated from README.Rmd. Please edit that file -->
hexSticker: create hexagon sticker in R
=======================================

Author
------

Guangchuang YU <https://guangchuangyu.github.io>

School of Public Health, The University of Hong Kong

------------------------------------------------------------------------

Examples
--------

> `sticker` function will produce a file with dimension exactly for printing according to <http://hexb.in/sticker.html>

### base plot

``` r
library(hexSticker)
sticker(expression(plot(cars, cex=.5, cex.axis=.5, mgp=c(0,.3,0), xlab="", ylab="")), package="hexSticker",
        p_size=8, s_x=1, s_y=.8, s_width=1.2, s_height=1, filename="inst/figures/baseplot.png")
```

<img src="inst/figures/baseplot.png" height="300"/>

### lattice

``` r
library(lattice)

counts <- c(18,17,15,20,10,20,25,13,12)
outcome <- gl(3,1,9)
treatment <- gl(3,3)
bwplot <- bwplot(counts ~ outcome | treatment, xlab=NULL, ylab=NULL, cex=.5,
                 scales=list(cex=.5), par.strip.text=list(cex=.5))
sticker(bwplot, package="hexSticker", p_size=8, s_x=1.05, s_y=.75, s_width=2, s_height=1.5,
        h_fill="#f9690e", h_color="#f39c12", filename="inst/figures/lattice.png")
```

<img src="inst/figures/lattice.png" height="300"/>

### ggplot2

``` r
library(ggplot2)

p <- ggplot(aes(x = mpg, y = wt), data = mtcars) + geom_point()
p <- p + theme_void() + theme_transparent()

sticker(p, package="hexSticker", p_size=8, s_x=1, s_y=.75, s_width=1.3, s_height=1,
        filename="inst/figures/ggplot2.png")
```

<img src="inst/figures/ggplot2.png" height="300"/>

### image file

``` r
imgurl <- "http://www.belleamibengals.com/bengal_cat_2.png"
sticker(imgurl, package="hexSticker", p_size=8, s_x=1, s_y=.75, s_width=.6,
        filename="inst/figures/imgfile.png")
```

<img src="inst/figures/imgfile.png" height="300"/>

Stickers produced by `hexSticker`
---------------------------------

> If you use `hexSticker` and want your sticker to be listed here, please feel free to edit [README.Rmd](https://github.com/GuangchuangYu/hexSticker/edit/master/README.Rmd).

-   [AnnotationFilter](https://github.com/Bioconductor/BiocStickers/tree/master/AnnotationFilter)
-   [FamAgg](https://github.com/Bioconductor/BiocStickers/tree/master/FamAgg)
-   [ggtree](https://github.com/Bioconductor/BiocStickers/tree/master/ggtree)
-   [MSnbase](https://github.com/Bioconductor/BiocStickers/tree/master/MSnbase)
-   [mzR](https://github.com/Bioconductor/BiocStickers/tree/master/mzR)
-   [treeio](https://github.com/Bioconductor/BiocStickers/tree/master/treeio)
-   [xcms](https://github.com/Bioconductor/BiocStickers/tree/master/xcms)

<img src="https://raw.githubusercontent.com/Bioconductor/BiocStickers/master/AnnotationFilter/AnnotationFilter.png" height="120"/> <img src="https://raw.githubusercontent.com/Bioconductor/BiocStickers/master/FamAgg/FamAgg.png" height="120"/> <img src="https://raw.githubusercontent.com/Bioconductor/BiocStickers/master/ggtree/ggtree.png" height="120"/> <img src="https://raw.githubusercontent.com/Bioconductor/BiocStickers/master/MSnbase/MSnbase.png" height="120"/> <img src="https://raw.githubusercontent.com/Bioconductor/BiocStickers/master/mzR/mzR.png" height="120"/> <img src="https://raw.githubusercontent.com/Bioconductor/BiocStickers/master/treeio/treeio.png" height="120"/> <img src="https://raw.githubusercontent.com/Bioconductor/BiocStickers/master/xcms/xcms.png" height="120"/>
