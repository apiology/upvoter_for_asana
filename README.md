# Upvoter for Asana

[![CircleCI](https://circleci.com/gh/apiology/upvoter_for_asana.svg?style=svg)](https://circleci.com/gh/apiology/upvoter_for_asana)

Chrome extension which quickly finds and increments integer custom
fields in Asana tasks from the Chrome Omnibox.

This is useful if you're trying to track pain points in a backlog -
just throw a backlog feature task a quick upvote in real time as you
suffer through missing the feature, then go back later and take on the
most upvoted tasks!

## Installing

This isn't in the Chrome App Store and doesn't have any cool config,
so welcome to the Chrome Extension development experience!

1. Create a config.js in this directory with a variable named
   'asanaAccessToken' with a new
   [Asana Personal Access Token](https://app.asana.com/0/developer-console)
   assigned to it.
2. Add the name of your Asana workspace to config.js under the name
   'workspaceName'
3. Add the name of the custom field you want to increment to config.js
   under the name 'customFieldName'
4. Add a boolean value indicating whether you want upvoter to
   increment values or decrement values to config.js under the name
   'increment'.  Note that Asana doesn't let you sort an integer
   custom with the highest values on top, so you may find it more
   helpful to set 'increment' to 'false' and use negative values so
   your most important thing show up at top by default.
5. Run `npm install && node_modules/.bin/webpack`
6. Go to [chrome://extensions/](chrome://extensions/)
7. Make sure 'Developer mode' is flipped on in the upper right.
8. Click the 'Load unpacked' button.
9. Choose the directory containing this code.

## Using

Go to the URL bar ("Chrome Omnibox"), and type 'uv', a space, then
search for an Asana task.  You should see them pop up as suggestions.
Pick one, and your custom field will be uploaded!
