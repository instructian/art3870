# Common Mistakes

## CSS
Don't do this. Don't load fonts after calling them.

    <link rel="stylesheet" href="css/foundation.css">
    <link rel="stylesheet" href="css/app.css">
    <link href="https://fonts.googleapis.com/css?family=Bitter|Cabin|Padauk|PT+Sans|Rubik|Frank+Ruhl+Libre" rel="stylesheet">

Do this instead:

    <link href="https://fonts.googleapis.com/css?family=Bitter|Cabin|Padauk|PT+Sans|Rubik|Frank+Ruhl+Libre" rel="stylesheet">
    <link rel="stylesheet" href="css/foundation.css">
    <link rel="stylesheet" href="css/app.css">

First load fonts, then frameworks, then your project specific css.

