the navigation between the pages is done using the client side navigation (using JS not the browser)

whenever Link components appear in the browser’s viewport, Next.js automatically prefetches the code for the linked page in the background

Next.js has support for Image Optimization by default.

CSS modules allow you to locally scope CSS at the component-level

The default export of _app.js is a top-level React component that wraps all the pages in your application. You can use this component to keep state when navigating between pages, or to add global styles 

next.js pre render each page means it generate each html in the server  in advance instead of having it all done on the client side (the browser)

hydration process : associate eachgenerated page with miinimum js code necessaery to make it interactive 

Static Generation is the pre-rendering method that generates the HTML at build time. The pre-rendered HTML is then reused on each request.
Server-side Rendering is the pre-rendering method that generates the HTML on each request.

In development mode (when you run npm run dev or yarn dev), pages are pre-rendered on every request. This also applies to Static Generation to make it easier to develop. When going to production, Static Generation will happen once, at build time, and not on every request.

you can choose which pre rendering to use in each page 

We recommend using Static Generation (with and without data) whenever possible because your page can be built once and served by CDN, which makes it much faster than having a server render the page on every request.

in the client side rendering: 
Statically generate (pre-render) parts of the page that do not require external data.
When the page loads, fetch external data from the client using JavaScript and populate the remaining parts.

 SWR : We highly recommend it if you’re fetching data on the client side. It handles caching, revalidation, focus tracking, refetching on interval, and more. 

  Pages that begin with [ and end with ] are dynamic routes in Next.js.