# media

## Classes

### MediaPlayer

#### Constructors

##### new MediaPlayer()

```ts
new MediaPlayer(): MediaPlayer
```

###### Returns

[`MediaPlayer`](media.md#mediaplayer)

#### Accessors

##### androidMediaPlayer

```ts
get androidMediaPlayer(): any
```

###### Returns

`any`

###### Defined in

[src/media/index.ts:5](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L5)

##### currentPosition

```ts
get currentPosition(): number
```

###### Returns

`number`

当前播放位置。单位毫秒。

###### Defined in

[src/media/index.ts:11](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L11)

##### duration

```ts
get duration(): number
```

###### Returns

`number`

音乐时长。单位毫秒。

###### Defined in

[src/media/index.ts:17](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L17)

##### isPlaying

```ts
get isPlaying(): boolean
```

###### Returns

`boolean`

###### Defined in

[src/media/index.ts:20](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L20)

#### Methods

##### pause()

```ts
pause(): void
```

###### Returns

`void`

###### Defined in

[src/media/index.ts:30](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L30)

##### play()

```ts
play(
   uri: string, 
   volume?: number, 
looping?: boolean): Promise<void>
```

###### Parameters

| Parameter | Type |
| ------ | ------ |
| `uri` | `string` |
| `volume`? | `number` |
| `looping`? | `boolean` |

###### Returns

`Promise`\<`void`\>

###### Defined in

[src/media/index.ts:23](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L23)

##### prepare()

```ts
prepare(): Promise<void>
```

###### Returns

`Promise`\<`void`\>

###### Defined in

[src/media/index.ts:33](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L33)

##### prepareSync()

```ts
prepareSync(): void
```

###### Returns

`void`

###### Defined in

[src/media/index.ts:36](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L36)

##### release()

```ts
release(): void
```

###### Returns

`void`

###### Defined in

[src/media/index.ts:39](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L39)

##### reset()

```ts
reset(): void
```

###### Returns

`void`

###### Defined in

[src/media/index.ts:42](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L42)

##### seekTo()

```ts
seekTo(msec: number): Promise<void>
```

###### Parameters

| Parameter | Type |
| ------ | ------ |
| `msec` | `number` |

###### Returns

`Promise`\<`void`\>

###### Defined in

[src/media/index.ts:45](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L45)

##### setDataSource()

```ts
setDataSource(path: string): void
```

###### Parameters

| Parameter | Type |
| ------ | ------ |
| `path` | `string` |

###### Returns

`void`

###### Defined in

[src/media/index.ts:48](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L48)

##### setLooping()

```ts
setLooping(looping: boolean): void
```

###### Parameters

| Parameter | Type |
| ------ | ------ |
| `looping` | `boolean` |

###### Returns

`void`

###### Defined in

[src/media/index.ts:51](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L51)

##### setScreenOnWhilePlaying()

```ts
setScreenOnWhilePlaying(keep: boolean): void
```

###### Parameters

| Parameter | Type |
| ------ | ------ |
| `keep` | `boolean` |

###### Returns

`void`

###### Defined in

[src/media/index.ts:54](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L54)

##### setVolume()

```ts
setVolume(leftVolume: number, rightVolume?: number): void
```

###### Parameters

| Parameter | Type |
| ------ | ------ |
| `leftVolume` | `number` |
| `rightVolume`? | `number` |

###### Returns

`void`

###### Defined in

[src/media/index.ts:57](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L57)

##### start()

```ts
start(): void
```

###### Returns

`void`

###### Defined in

[src/media/index.ts:61](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L61)

##### stop()

```ts
stop(): void
```

###### Returns

`void`

###### Defined in

[src/media/index.ts:64](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L64)

## Functions

### playMusic()

```ts
function playMusic(
   uri: string, 
   volume?: number, 
looping?: boolean): Promise<MediaPlayer>
```

#### Parameters

| Parameter | Type |
| ------ | ------ |
| `uri` | `string` |
| `volume`? | `number` |
| `looping`? | `boolean` |

#### Returns

`Promise`\<[`MediaPlayer`](media.md#mediaplayer)\>

#### Defined in

[src/media/index.ts:69](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L69)

***

### scanFile()

```ts
function scanFile(file: string): void
```

#### Parameters

| Parameter | Type |
| ------ | ------ |
| `file` | `string` |

#### Returns

`void`

#### Defined in

[src/media/index.ts:75](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/media/index.ts#L75)
