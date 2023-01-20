---
sidebar_position: 2
---
# Sprite
extends [GameObject](GameObject)

## Creating 
```js
new Sprite({options})
```

## Options
| Name    | Type                                | Description                                               |
|---------|-------------------------------------|-----------------------------------------------------------|
| texture | string \| [PIXI.Texture](https://pixijs.download/dev/docs/PIXI.Texture.html) \| undefined | A texture url or a texture resource from Engine.resources |

### Example
```js
new Sprite({texture: Engine.instance.resources.textureName})
```

## Properties
| Name      | Type        | Additional details                                                                                                                        |
|-----------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| container | [PIXI.Sprite](https://pixijs.download/dev/docs/PIXI.Sprite.html) |                                                                                                                                           |
| tint      | number      | Applies a tint to the Sprite. The number is a hexadecimal value. For example, a value of 0xFF0000 will apply the color red to the Sprite. |