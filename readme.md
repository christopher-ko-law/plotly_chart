# Belly Button Biodiversity Dashboard.

## Overview
This project combines plotly, html, css and github pages to create a dashboard that displays data regarding bacteria species in a volunteer's belly button.

This dashboard can be accessed through github pages at:
https://christopher-ko-law.github.io/plotly_chart/

The following charts will be displayed:
* Top Ten Bacteria Cultures Found
* Belly Button Washing Frequency
* Bacteria Cultures per Sample

The full page should load as below:<br>
![Full Page](/readme_images/webpage_full.png)

The mobile page should load as below:<br>
![Mobile Page](/readme_images/webpage_mobile.png)


## Deliverable 4 - Customizations
This project was futher customized as below:

### Adding an image to the jumbotron.
A new style.css file located in the css folder was added. New classses and IDs were added into the html file and a background image added as per below:
```
.header-bg {
    background-image: url("../images/petri_header.jpeg");
    background-size: cover;
    background-position: 50%;
    color: black;
}
#header-wrapper{
    background-color: rgba(160, 160, 160, 0.6);
    border-radius: 6px;
}
#header-wrapper h1, #header-wrapper p{
    opacity: 1;
}
```

### Add background color or a variety of compatible colors to the webpage.
The style.css was further modified to change the background colors to the webpage. These are all shades of grey.
```
body {
    background-color:rgb(160, 160, 160);
}
.panel-body{
    background-color:#f5f5f5;
}
.project-info{
    background-color:#f5f5f5;
    border-radius: 4px;
    padding: 10px 15px;
}
```
Additional padding was added between the rows to ensure that the data is well spaced out.


### Add more information about the project as a paragraph on the page.
Additional information was added to the top of the page to ensure the user would know how to use this dashboard.
```
<div class="row">
    <div class="col-md-12 row-margin">
    <div class="project-info">
        <p>This dashboard contains data collected from the belly button of volunteers for Improbable Beef's research.</p>
        <p>Select a Test Subject ID from the dropdown list below. Information about the volunteer will be displayed in the Demographic Info Panel. The following charts will also be displayed:
        <ul>
            <li>Top Ten Bacteria Cultures Found</li>
            <li>Belly Button Washing Frequency</li>
            <li>Bacteria Cultures per Sample</li>
        </ul>
        </p>
    </div>
    </div>
</div>
```

### Make the webpage mobile-responsive.
The Plotly.newPlot is able to take an additional parameter. In this config variable, we can set responsive:true. This will ensure that the graphs are mobile-responsive.
```
var config = {responsive: true}
Plotly.newPlot('gauge', gaugeData, gaugeLayout, config);
```
