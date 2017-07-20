# react-google-maps-docs

documentation for [react-google-maps](https://github.com/tomchentw/react-google-maps)

You may have to put your Google Maps script tag in the head of your HTML.  This allows Google to load to the window before the HTML renders.  Loading a script tag in the head is unconventional, and it is not required when not using React.  If you get your app to work without doing this, please feel free to make a PR with a code example.

```html
<!DOCTYPE html>
<html>
  <head>
    <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY_HERE&libraries=visualization,places"></script>
  </head>
  <body>
    <div id='main'></div>

    <script src='bundle.js'></script>
  </body>
</html>
```