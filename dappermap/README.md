# Deployment

If deployment isn't working:

* Check that `index.html` uses `./Package` instead of `./build/<...>/Package`.
* Check that `index.html` contains `<script src="coi-serviceworker.min.js></script>` in `<head>`.
* GitHub Pages doesn't support the `Content-Encoding` header that we use to decompress the bundles. There is now manual decompression, but this is something to keep in mind if running from other servers (`Content-Encoding: gzip` is probably more efficient).
