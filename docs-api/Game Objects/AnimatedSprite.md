---
sidebar_position: 3
---
# AnimatedSprite
extends [GameObject](GameObject)

## Creating 
```js
new AnimatedSprite({options})
```

## Options
| Name    | Type                                | Description                                               |
|---------|-------------------------------------|-----------------------------------------------------------|
| textures | string[] \| [PIXI.Texture](https://pixijs.download/dev/docs/PIXI.Texture.html)[] \| undefined | An array of texture urls or texture resources from Engine.resources |
| autoPlay | boolean | States if the animation will play automatically |
| loop | boolean | States if the animation will restart after reaching its end |
| animationSpeed | number |  The speed of the animation, the higher the value, the faster it will play|

### Example
```js
new AnimatedSprite({
    textures: [
        Engine.instance.resources.frame1, 
        Engine.instance.resources.frame2
    ],
    autoPlay: true,
    loop: true,
    animationSpeed: 1
})
```

## Properties
| Name      | Type        | Additional details                                                                                                                        |
|-----------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| container | [PIXI.AnimatedSprite](https://pixijs.download/dev/docs/PIXI.AnimatedSprite.html) |                                                                                                                                           |
| animationSpeed     | number      | The speed of the animation, the higher the value, the faster it will play |