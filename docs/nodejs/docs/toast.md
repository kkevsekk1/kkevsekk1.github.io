# toast

## Functions

### showToast()

```ts
function showToast(message: any, option?: string | ToastOptions): void
```

弹出一条toast

#### Parameters

| Parameter | Type | Description |
| ------ | ------ | ------ |
| `message` | `any` | 要显示的消息 |
| `option`? | `string` \| `ToastOptions` | 可以是"short" | "long"，表示弹出时长 |

#### Returns

`void`

#### Example

```ts
import { showToast } from 'toast'
showToast('hello world')
```

#### Defined in

[src/toast/index.ts:14](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/toast/index.ts#L14)
