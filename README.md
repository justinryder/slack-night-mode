Fork of [laCour/slack-night-mode](https://github.com/laCour/slack-night-mode) that adds a Curse Dark theme.

## Desktop Usage

Find `C:\Users\{username}\AppData\Local\slack\app-{slackversion}\resources\app.asar.unpacked\src\static\ssb-interop.js` and append the following:

```
// Load curse dark theme
document.addEventListener('DOMContentLoaded', function() {
 $.ajax({
   url: 'https://raw.githubusercontent.com/justinryder/slack-night-mode/master/css/themes/build-variants/curse-dark--styles.css?_=' + Date.now(),
   success: function(css) {
     $("<style></style>").appendTo('head').text(css);
   }
 });
});
```

Save ssb-interop.js and restart Slack or reload it with CTRL+R.

## Chrome Usage

1) Install the [Stylus Chrome extension](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne?hl=en)
1) Click the Stylus extension icon and select `Manage`
1) Click `Write new style`
1) Name the style
1) Paste the contents of [this CSS](https://raw.githubusercontent.com/justinryder/slack-night-mode/master/css/themes/build-variants/curse-dark--styles.css) into the Code text box
1) Click the plus (+) icon next to "Applied to Everything"
1) Change `URL` to `URLs matching the regexp`
1) Paste this regex into the input beside the dropdown `.*slack\.com\/(messages|threads|unreads).*`
1) Save the style
