---
title: "Plotly Assignment"
author: "Sandra Cuffee"
date: "January 1, 2018"
output: 
  ioslides_presentation: 
    keep_md: yes
---



## Airquality Data


```r
data(airquality)
str(airquality)
```

```
## 'data.frame':	153 obs. of  6 variables:
##  $ Ozone  : int  41 36 12 18 NA 28 23 19 8 NA ...
##  $ Solar.R: int  190 118 149 313 NA NA 299 99 19 194 ...
##  $ Wind   : num  7.4 8 12.6 11.5 14.3 14.9 8.6 13.8 20.1 8.6 ...
##  $ Temp   : int  67 72 74 62 56 66 65 59 61 69 ...
##  $ Month  : int  5 5 5 5 5 5 5 5 5 5 ...
##  $ Day    : int  1 2 3 4 5 6 7 8 9 10 ...
```

## Airquality 3D Scatterplot


Ozone, Temp(Temperature), and Wind are represented in the 3D scatter plot by Month. Note: the NAs have been removed.


<!--html_preserve--><div id="34402c5478e0" style="width:720px;height:432px;" class="plotly html-widget"></div>
<script type="application/json" data-for="34402c5478e0">{"x":{"visdat":{"3440231f3dd9":["function () ","plotlyVisDat"]},"cur_data":"3440231f3dd9","attrs":{"3440231f3dd9":{"x":{},"y":{},"z":{},"mode":"markers","color":{},"alpha":1,"sizes":[10,100],"type":"scatter3d"}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"scene":{"xaxis":{"title":"Ozone"},"yaxis":{"title":"Temp"},"zaxis":{"title":"Wind"}},"xaxis":{"domain":[0,1]},"yaxis":{"domain":[0,1]},"hovermode":"closest","showlegend":false,"legend":{"y":0.5,"yanchor":"top"}},"source":"A","config":{"modeBarButtonsToAdd":[{"name":"Collaborate","icon":{"width":1000,"ascent":500,"descent":-50,"path":"M487 375c7-10 9-23 5-36l-79-259c-3-12-11-23-22-31-11-8-22-12-35-12l-263 0c-15 0-29 5-43 15-13 10-23 23-28 37-5 13-5 25-1 37 0 0 0 3 1 7 1 5 1 8 1 11 0 2 0 4-1 6 0 3-1 5-1 6 1 2 2 4 3 6 1 2 2 4 4 6 2 3 4 5 5 7 5 7 9 16 13 26 4 10 7 19 9 26 0 2 0 5 0 9-1 4-1 6 0 8 0 2 2 5 4 8 3 3 5 5 5 7 4 6 8 15 12 26 4 11 7 19 7 26 1 1 0 4 0 9-1 4-1 7 0 8 1 2 3 5 6 8 4 4 6 6 6 7 4 5 8 13 13 24 4 11 7 20 7 28 1 1 0 4 0 7-1 3-1 6-1 7 0 2 1 4 3 6 1 1 3 4 5 6 2 3 3 5 5 6 1 2 3 5 4 9 2 3 3 7 5 10 1 3 2 6 4 10 2 4 4 7 6 9 2 3 4 5 7 7 3 2 7 3 11 3 3 0 8 0 13-1l0-1c7 2 12 2 14 2l218 0c14 0 25-5 32-16 8-10 10-23 6-37l-79-259c-7-22-13-37-20-43-7-7-19-10-37-10l-248 0c-5 0-9-2-11-5-2-3-2-7 0-12 4-13 18-20 41-20l264 0c5 0 10 2 16 5 5 3 8 6 10 11l85 282c2 5 2 10 2 17 7-3 13-7 17-13z m-304 0c-1-3-1-5 0-7 1-1 3-2 6-2l174 0c2 0 4 1 7 2 2 2 4 4 5 7l6 18c0 3 0 5-1 7-1 1-3 2-6 2l-173 0c-3 0-5-1-8-2-2-2-4-4-4-7z m-24-73c-1-3-1-5 0-7 2-2 3-2 6-2l174 0c2 0 5 0 7 2 3 2 4 4 5 7l6 18c1 2 0 5-1 6-1 2-3 3-5 3l-174 0c-3 0-5-1-7-3-3-1-4-4-5-6z"},"click":"function(gd) { \n        // is this being viewed in RStudio?\n        if (location.search == '?viewer_pane=1') {\n          alert('To learn about plotly for collaboration, visit:\\n https://cpsievert.github.io/plotly_book/plot-ly-for-collaboration.html');\n        } else {\n          window.open('https://cpsievert.github.io/plotly_book/plot-ly-for-collaboration.html', '_blank');\n        }\n      }"}],"cloud":false},"data":[{"x":[41,36,12,18,23,19,8,16,11,14,18,14,34,6,30,11,1,11,4,32,23,45,115,37,29,71,39,23,21,37,20,12,13,135,49,32,64,40,77,97,97,85,10,27,7,48,35,61,79,63,16,80,108,20,52,82,50,64,59,39,9,16,122,89,110,44,28,65,22,59,23,31,44,21,9,45,168,73,76,118,84,85,96,78,73,91,47,32,20,23,21,24,44,21,28,9,13,46,18,13,24,16,13,23,36,7,14,30,14,18,20],"y":[67,72,74,62,65,59,61,69,66,68,58,64,66,57,68,62,59,73,61,61,67,81,79,76,82,90,87,82,77,72,65,73,76,84,85,81,83,83,88,92,92,89,73,81,80,81,82,84,87,85,74,86,85,82,86,88,86,83,81,81,81,82,89,90,90,86,82,80,77,79,76,78,78,77,72,79,81,86,97,94,96,94,91,92,93,93,87,84,80,78,75,73,81,76,77,71,71,78,67,76,68,82,64,71,81,69,63,70,75,76,68],"z":[7.4,8,12.6,11.5,8.6,13.8,20.1,9.7,9.2,10.9,13.2,11.5,12,18.4,11.5,9.7,9.7,16.6,9.7,12,12,14.9,5.7,7.4,9.7,13.8,11.5,8,14.9,20.7,9.2,11.5,10.3,4.1,9.2,9.2,4.6,10.9,5.1,6.3,5.7,7.4,14.3,14.9,14.3,6.9,10.3,6.3,5.1,11.5,6.9,8.6,8,8.6,12,7.4,7.4,7.4,9.2,6.9,13.8,7.4,4,10.3,8,11.5,11.5,9.7,10.3,6.3,7.4,10.9,10.3,15.5,14.3,9.7,3.4,8,9.7,2.3,6.3,6.3,6.9,5.1,2.8,4.6,7.4,15.5,10.9,10.3,10.9,9.7,14.9,15.5,6.3,10.9,11.5,6.9,13.8,10.3,10.3,8,12.6,9.2,10.3,10.3,16.6,6.9,14.3,8,11.5],"mode":"markers","type":"scatter3d","marker":{"colorbar":{"title":"Month","ticklen":2},"cmin":5,"cmax":9,"colorscale":[["0","rgba(68,1,84,1)"],["0.25","rgba(60,82,138,1)"],["0.270833333333332","rgba(58,87,139,1)"],["0.5","rgba(37,144,140,1)"],["0.75","rgba(98,199,98,1)"],["1","rgba(253,231,37,1)"]],"showscale":false,"color":[5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,6,6,6,6,6,6,6,6,6,7,7,7,7,7,7,7,7,7,7,7,7,7,7,7,7,7,7,7,7,7,7,7,7,7,7,8,8,8,8,8,8,8,8,8,8,8,8,8,8,8,8,8,8,8,8,8,8,8,9,9,9,9,9,9,9,9,9,9,9,9,9,9,9,9,9,9,9,9,9,9,9,9,9,9,9,9,9],"line":{"color":"transparent"}},"frame":null},{"x":[1,168],"y":[57,97],"type":"scatter3d","mode":"markers","opacity":0,"hoverinfo":"none","showlegend":false,"marker":{"colorbar":{"title":"Month","ticklen":2,"len":0.5,"y":1,"lenmode":"fraction","yanchor":"top"},"cmin":5,"cmax":9,"colorscale":[["0","rgba(68,1,84,1)"],["0.25","rgba(60,82,138,1)"],["0.270833333333332","rgba(58,87,139,1)"],["0.5","rgba(37,144,140,1)"],["0.75","rgba(98,199,98,1)"],["1","rgba(253,231,37,1)"]],"showscale":true,"color":[5,9]},"z":[2.3,20.7],"frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1}},"base_url":"https://plot.ly"},"evals":["config.modeBarButtonsToAdd.0.click"],"jsHooks":{"render":[{"code":"function(el, x) { var ctConfig = crosstalk.var('plotlyCrosstalkOpts').set({\"on\":\"plotly_click\",\"persistent\":false,\"dynamic\":false,\"selectize\":false,\"opacityDim\":0.2,\"selected\":{\"opacity\":1}}); }","data":null}]}}</script><!--/html_preserve-->



