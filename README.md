# Development Reminders

## Branches
Use the `writing` branch to make edits and only push to master when youre ready to make changes live. this will prevent the GitLab CI from running too frequently.

## Publishing
To prepare for publishing, set the main tab to `Open`, use the publish icon in the top right corner of the tiddlywiki, hide the extra tabs, unset creating links to nonexistent tiddlers, and save as `index.html` in the `public`directory. Also be sure to compress images and files as much as possible when placing them in the `public` folder.

When merged to master and pushed, all files in `public` will be served.