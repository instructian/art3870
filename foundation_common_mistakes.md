# Common Mistakes
## Zurb Foundation

Don't do this

    <body class="large-12 medium-12 small-12 row">
       <header class="row">
         <h1 class="columns small-12 medium-6 large-4">Discover</h1>

Do this 

    <body class="row">
           <header class="columns small-12 medium-6 large-4">
             <h1>Discover</h1>

The .row class creates a width and the frame for the site the columns subdivide the frame and small-12 is the measure of the subdivision.

