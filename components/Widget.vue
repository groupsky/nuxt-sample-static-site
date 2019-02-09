<template>
  <div>
    <div id="medium-widget" />
    <script src="https://medium-widget.pixelpoint.io/widget.js" />
    <script>
      function init () {
        MediumWidget.Init({
          renderTo: '#medium-widget',
          params: {
            'resource': 'https://medium.com/@erin.l.schumaker',
            'postsPerLine': 2,
            'limit': 4,
            'picture': 'big',
            'fields': ['description', 'author', 'claps', 'publishAt'],
            'ratio': 'landscape'
          }
        })
      }

      function check () {
        console.log('checking for medium loaded', window.MediumWidget)
        setTimeout(window.MediumWidget ? init : check, 50)
      }

      check()
    </script>
  </div>
</template>
