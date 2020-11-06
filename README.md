# Developing

## Running the document website in local

1.  `cd website` & `npm install`
1.  From within the `website` directory, run the local web server using `yarn start` or `npm start`.
1.  Load the example site at http://localhost:3000 if it did not already open automatically. If port 3000 has already been taken, another port will be used. Look at the console messages to see which.

    You should see the example site loaded in your web browser. There's also a LiveReload server running and any changes made to the docs and files in the `website` directory will cause the page to refresh. A randomly generated primary and secondary theme color will be picked for you.

## More

See [this document](https://docusaurus.io/docs/en/site-creation) for more info.

# Publishing

## Building Static HTML Pages

To create a static build of your website, run the following script from the `website` directory:

```bash
yarn run build # or `npm run build`
```

This will generate a `build` directory inside the `website` directory containing the `.html` files from all of your docs and other pages included in `pages`.

## Hosting Static HTML Pages

At this point, you can grab all of the files inside the `website/build` directory and copy them over to your favorite web server's `html` directory.

> For example, both Apache and Nginx serve content from `/var/www/html` by default. That said, choosing a web server or provider is outside the scope of Docusaurus.

> When serving the site from your own web server, ensure the web server is serving the asset files with the proper HTTP headers. CSS files should be served with the `content-type` header of `text/css`. In the case of Nginx, this would mean setting `include /etc/nginx/mime.types;` in your `nginx.conf` file. See [this issue](https://github.com/facebook/docusaurus/issues/602) for more info.

## More

See [this document](https://docusaurus.io/docs/en/publishing) for more info.
