# GameObject

GameObject is the base class for all objects in Migu. 

## Creating
```js
new GameObject({options})
```

## Automatically called methods

### start

Called when the GameObject is created unless ``ignoreStart`` is set to true on its options.

### update(delta: number)

Called every frame. ``delta`` contains the time elapsed in milliseconds from last frame to this frame, usually used to compensate frame time variation.

## Options
| Name                 | Type       | Optional? | Description                                                                                                                                                                                                       |
|----------------------|------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| anchor               | Vector     | optional  | Center of the GameObject. It is relative to the GameObject's size, usually going from Vector(-1, -1) to Vector(1, 1).                                                                                             |
| parent               | GameObject | optional  | When set, the created GameObject will automatically turn into a child of this property, being affect by its local space.                                                                                          |
| ignoreEmptyContainer | boolean    | optional  | Most times you won't set this property. When true, this will make the GameObject not create an empty PIXI Container. It is automatically set to true when creating a Sprite, an AnimatedSprite or a TilingSprite. |
| ignoreStart          | boolean    | optional  | When set to true, the GameObject will not call start() after its creation.                                                                                                                                        |
| zIndex               | number     | optional  | This will make the GameObject appear on front of objects with smaller zIndex values.                                                                                                                              |
| tag                  | string     | optional  | This will make the tag variable to be set to the value of this property.                                                                                                                                          |
| engine               | Engine     | optional  | Completely optional, unless you want to use multiple engine instances.                                                                                                                                            |

## Properties

| Name | Type |
|-----------|----------------|
| container | PIXI.Container |
| engine    | Engine         |
| parent    | GameObject     |
| children  | GameObject[]   |
| tag       | string         |
| position  | Vector         |
| x         | number         |
| y         | number         |
| rotation  | number         |
| angle     | number         |
| scale     | number         |
| scaleX    | number         |
| scaleY    | number         |
| visible   | boolean        |
| zIndex    | number         |

## Methods

| Usage | Return type |
|-----------------------------|------|
| addChild(child: GameObject) | null |
| lookAt(point: Vector)       | null |
| destroy()                   | null |