# DID WG Resolutions Checker

[View it here](https://rhiaro.github.io/did-wg-resolutions-playground).

Takes [DID WG resolutions](https://www.w3.org/2019/did-wg/Meetings/Minutes/resolutions) and lets you sort by tag, or mark them off when they're done.

Update the data with PRs to this repo.

When new resolutions are made:

* Copy the list item html from the automatically generated resolutions list (linked above) and paste it on top of the list in `index.html`
* Take the URL of the resolution in the minutes and create a new object in `resolutions.js`, like:

```
{
    "uri": "https://...#resolution1",
    "tags": ["one tag", "another tag"],
    "done": false
}
```

When a resolution is actioned:

* Update `resolutions.js` to set `"done": true`

Use the `tags` property to group topically related resolutions together for easy filtering.