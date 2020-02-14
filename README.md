# Solve Me If You Can

* Route / should redirect to /universal

Make it so that:
* Route /universal is a SSR loaded page (Universal).
* Route /spa should be only rendered on client side (SPA).

On page load (refresh):
* The number in the store should be increased by 1 (see addNumber mutation in count.js).
* Make sure the number is always 1. Both if you refresh the page on /universal and on /spa