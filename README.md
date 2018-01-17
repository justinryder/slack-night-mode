Fork of [laCour/slack-night-mode](https://github.com/laCour/slack-night-mode) that adds a Curse Dark theme.

## Usage

Find `C:\Users\{username}\AppData\Local\slack\app-{slackversion}\resources\app.asar.unpacked\src\static\ssb-interop.js` and append the following:

```// Load curse dark theme
document.addEventListener('DOMContentLoaded', function() {
 $.ajax({
   url: 'https://raw.githubusercontent.com/justinryder/slack-night-mode/master/css/themes/build-variants/curse-dark--styles.css',
   success: function(css) {
     $("<style></style>").appendTo('head').html(css);
   }
 });
});```

Save ssb-interop.js and restart Slack or reload it with CTRL+R.
