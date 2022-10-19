# Using CSS Grid Layout
## Definition
> CSS Grid is a powerful tool that allows for two-dimensional layouts for columns and rows to be created on the web

## Features of CSS Grid Layout
1. Flexible traction size
>You can use the `fr` unit (Fraction Unit) to assign any specified pixel value to the grid. This will make your grid organized and responsive.

2. Item Placement
>CSS grid has made it much easier to position items in the container in any area you want them to be without having to mess with the HTML markup.

## CSS Grid Properties
1. Grid container

This is a CSS grid property that houses the grid items/elements. We implement the CSS grid container property by setting the container to a display property of `grid` or `in-line grid`.
```
display:grid
```
2. Grid-template-column property
>Used to set each column’s width. It can also define how many columns you want to set to your project.
`grid-template-column`. <br>
<b>Example</b>
`grid-template-column: 100px auto 100px;`

>The code above shows that we have three columns. The width of columns one (the first column) and three (the third column) are set to 100px. The width of column two (the middle column) is set to auto.
>This means that as the size of your screen increases, columns one and three take 100px of the screen width, while column two takes the remaining width of the screen (which is auto).

## Step guide
- Create a div with a class of container
`<div class="container"> </div>` all other div will be nested in the container class.
Check you have created all elements on of the page. 
![](images/our-design-layout.png)
- All other working is going to be completed using CSS.
- In styling:
### a. give our container a display of grid:
We asign a height of 100vh, so that it span the whole device 100%.

    .container{
        display:grid
        height:100vh
        grid-template-column:1fr 1fr 1fr 1fr
    }

#### Output of `height:100vh`, spanning to fit the device viewport
![](images/height-of-100vh.png)

#### Output of `grid-template-column:1fr 1fr 1fr 1fr`
![](images/grid-template-column.png)

### c. We define the Grid-template-row and assign
This determines the number of rows we will have in our design
`grid-template-rows: 0.2fr 1.5fr 1.2fr 0.8fr;`
The output looks as below:
![](images/grid-template-rows.png)

### d. Add  `background-color:` property to every layout, 
```
nav{
    background-color: aqua;
}
main{
    background-color: antiquewhite;
}
#content1{
    background-color: rgb(255, 174, 0);
}
#sidebar{
    background-color: darkkhaki;
}
#content2{
    background-color:chartreuse ;
}
#content3{
    background-color: aquamarine;
}
footer{
    background-color: rgb(24, 200, 209);
}
```
![](images/after-adding-bg.png)

### Grid template area definition
```
grid-template-areas: 
        "nav nav nav nav"
        "sidebar main main main"
        "sidebar content1 content2 content3"
        "sidebar footer footer footer" ;

```
- you have to define each area for reference, 
![](images/grid-template-area-reference.png)
#### Output after grid area definition
![](images/output-grid-tempate-area.png)

### We want to add spaces between each column and rows
- To achieve this we use `grid-gap:` property in our `.container{}` class
![](images/greid-gap-property.png)

#### final `.container:` class style looks like:
```
.container{
    display: grid;
    height: 100vh;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    grid-template-rows: 0.2fr 1.5fr 1.2fr 0.8fr;
    grid-template-areas: 
            "nav nav nav nav"
            "sidebar main main main"
            "sidebar content1 content2 content3"
            "sidebar footer footer footer" ;
    grid-gap: 5px;
}
```

## Responsive Design
In this design, we make everything in one column. Below are sample responsive on various device screen sizes:
### a. Large Screen size- Desktops
![](images/responsive/larg-screen.png)
### a. Medium Screen size- Tablets
![](images/responsive/medium-screen-size.png)
### a. Small screen sizes-Smartphones
![](images/responsive/small-screen-design.png)

## LEARNING RESOURCES ON GRID LAYOUT
- How to Use CSS Grid Layout – Grid Properties Explained with Examples <a href="https://www.freecodecamp.org/news/how-to-use-css-grid-layout/" target="_blank">https://www.freecodecamp.org/news/how-to-use-css-grid-layout/</a>
- A complete guide to Grid Layout: <a href="https://css-tricks.com/snippets/css/complete-guide-grid/" target="_blank">https://css-tricks.com/snippets/css/complete-guide-grid/ </a>
- Learn CSS Grid <a href="https://learncssgrid.com/" target="_blank">https://learncssgrid.com/</a>
- CSS Grid Layout <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout" target="_blank">https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout</a>