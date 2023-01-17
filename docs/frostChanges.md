# Changes

This is a list of all cahnges to this package, it'll help you:

 - Know what's changed
 - Know how to use changes

## Changed node-fetch to @replit/node-fetch

Why was this a change?
 - It allows the package to be used in common javascript

How to use: `none`

## Add custom data field

Why was this a change?
 - Allows custom data to be sent to themes, good if you dont want other users to edit themes manually in some spots

How to use: 
### Client side

set the `customData` field when you make your dashboard client

*Data in data field may vary between themes*
```js
client.dashboard = new Dashboard(client, {
    customData:{
        all:{
            footer:{
                text: "hallo"
                color: "#ff0000"
            }
        }
    }
});
```

### Theme side

use `dashboardDetails.customData` to get data
