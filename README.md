# aws-favs-to-pins
Chrome extension to convert favorites in AWS console to pins on the navigation header (as it was before the UI update).

Find it [here](https://chrome.google.com/webstore/detail/aws-favorites-to-pins/ncldghmgebieadpbefcmhicjepidmnhc/related) on the Chrome Web Store!

# How does it work?
- All favorites in AWS Console are within a div that has a property called `data-testid="favorites-container"`
- Fetches first 7 of these favorites, clones them into new divs and adds on to the nav header element

# Limitations
- Sometimes, fetching the `favorites-container` does not work (e.g., when page is refreshed sometimes/services that take time to load; Try going to CodePipeline and then to CodeDeploy) and hence pins don't show up (not sure why)
- Favorites menu is alphabetically ordered and only the top 7 of them are picked to be pins. Can't pick and choose to our liking
- Service name label and icon are both shown always. Not configurable to show just the icon/label

