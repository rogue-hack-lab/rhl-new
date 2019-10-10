[![Netlify Status](https://api.netlify.com/api/v1/badges/ff6c6c0f-72e6-4722-8718-8833901ab3fa/deploy-status)](https://app.netlify.com/sites/rhl/deploys)

This is the RHL Website.

## Running the site locally

The site is generated using [Hugo](https://gohugo.io) and can be easily generated locally.

- [Install hugo](https://gohugo.io/getting-started/quick-start/)
- Clone this repo
- run `hugo server -D`
- open a browser 

### General Content Updates

General content lived in the `content` folder and is formatted as [markdown](https://daringfireball.net/projects/markdown/)

### Style Updates

Styles and JS are auto generated by hugo (and later compressed by Netlify). To edit css/js edit the files in `assets` and observe changes with `hugo`

### Template updates

Templates are in the `layouts` directory.

- `_default` holds the initial layout
- `partials` holds things that are included across multiple default files
- `shortcodes` are emendable in the content files

### Functions

To make our integration with meetup work we use [Netlify Functions](https://www.netlify.com/docs/functions/#tools-for-building-javascript-functions) to proxy requests to the meetup API. Hugo does not currently offer a mechanism to proxy requests to local dev so if you want to work on functions on the frontend you need to mock api responses with files in the `static` folder. To run development of functions locally do the following:

- endure you have node/npm installed
- `npm i`
- `npm run start:functions`
- function will be available at `localhost:9000/.netlify/functions/{name}`

## Credits

This theme was partially designed with the inspiration from
- [Nathan Randecker](https://github.com/nrandecker/particle)
- [Willian Justen](https://github.com/willianjusten/will-jekyll-template)
- [Vincent Garreau](https://github.com/VincentGarreau/particles.js/)
