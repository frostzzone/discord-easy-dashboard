# Changes

This is a list of all cahnges to this package, it'll help you:

 - Know what's changed
 - Know how to use changes

## Changed node-fetch to cjs format

### Why was this a change?
 - It allows the package to be used in common javascript

### How to use

`none`

## Add custom data field

### Why was this a change?
 - Allows custom data to be sent to themes, good if you dont want other users to edit themes manually in some spots

### How to use

#### Client side

set the `customData` field when you make your dashboard client

*Data in data field may vary between themes*
```js
client.dashboard = new Dashboard(client, {
    customData:{
        all:{
            footer:{
                text: "hallo",
                color: "#ff0000"
            }
        }
    }
});
```

#### Theme side

use `dashboardDetails.customData` to get data

## Host files

### Why was this a change?

 - maybe you want to host an image, or css file idk

### How to use

set the `dir` field to `__dirname` when you make your dashboard client

```js
client.dashboard = new Dashboard(client, {
    dir: __dirname
});
```

![image](assets/public%20folder.png)

Anything in your `public` folder will be hosted

*public folder must be in the same dir as your .js file*

### Why not set it automatically?
well... it kinda does, but it hosts the public folder in the **package**