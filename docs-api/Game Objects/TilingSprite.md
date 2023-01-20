---
sidebar_position: 4
---

# TilingSprite
extends [GameObject](GameObject)

A Sprite that can be divided in tiles and cropped to a specific position. It is useful for parallax effect and tilemaps.

## Creating 
```js
new TilingSprite({options})
```

## Options
| Name    | Type                                | Description                                               |
|---------|-------------------------------------|-----------------------------------------------------------|
| texture | string \| [PIXI.Texture](https://pixijs.download/dev/docs/PIXI.Texture.html) | A texture url or a texture resource from Engine.resources |
| tilingSize | {width: number, height: number} | The size of the tile |

### Example
```js
new TilingSprite({
    texture: Engine.instance.resources.textureName,
    tilingSize: {
        width: 100,
        height: 100
    }
})
```

## Properties
| Name      | Type        | Additional details                                                                                                                        |
|-----------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| container | [PIXI.TilingSprite](https://pixijs.download/dev/docs/PIXI.TilingSprite.html) |                                                                                                                                           |
| offset      | [Vector](http://victorjs.org/#constructors-new)      | The offset off the tile. For example, an offset of ``new Vector(100, 200)`` will "move" the view 100 pixels to the right and 200 pixels to the bottom |