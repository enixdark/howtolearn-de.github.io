# Source of howtolearn.de

## To Run:

1. Clone/download this repository.
2. `cd` into the cloned/downloaded repository and run the command `bundle`.
3. Run the command `jekyll serve`.

## To run server in Docker

    docker run -p 4000:4000 howtolearn-de:latest server --host=0.0.0.0

## To run build in Docker

    docker image build -t howtolearn-de .
    docker run -v $(pwd)/dist:/src/dist howtolearn-de:latest

## Package.json?

The package.json is for deploying to Netlify. It tells Netlify to install the Pug-CLI NPM package which is needed in order to run Jekyll-Pug.

## Deploy

Run `bundle exec jekyll build --source src --destination dist && cp -r dist/* .` and then add all and push to github.
