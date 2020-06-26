# H1 Fix the IOS Full Screen issue in Framework7
#### H4 Meta Tag in index.html
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, minimum-scale=1, user-scalable=no, minimal-ui, viewport-fit=cover">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black">

#### H4 add this within body tag in index.html
<div class="statusbar-overlay"></div>

#### H4 add a class after view-main
<div class="view view-main ios-edges">

#### H4 Most important is to add a splash in ios platform (config.xml)
Size: 2732x2732
Format: png
Name: default@2x~universal~anyany.png

Example:
<platform name="ios">
    <splash src="Default@2x~universal~anyany.png" />
</platform>
