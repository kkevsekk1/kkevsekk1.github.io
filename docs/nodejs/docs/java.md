# java

## Functions

### invokeDefault()

```ts
function invokeDefault<T>(
   javaobj: any, 
   methodName: string, 
args?: any[]): Promise<T>
```

**`Alpha`**

采用默认的计算线程池异步调用java方法，返回Promise接受结果

#### Type Parameters

| Type Parameter |
| ------ |
| `T` |

#### Parameters

| Parameter | Type | Description |
| ------ | ------ | ------ |
| `javaobj` | `any` | java对象，不能是js对象 |
| `methodName` | `string` | 要调用的方法名 |
| `args`? | `any`[] | 传递的参数 |

#### Returns

`Promise`\<`T`\>

调用结果

#### Defined in

[src/java/index.ts:11](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/java/index.ts#L11)

***

### invokeIo()

```ts
function invokeIo<T>(
   javaobj: any, 
   methodName: string, 
args?: any[]): Promise<T>
```

**`Alpha`**

和[invokeDefault](java.md#invokedefault)类似，采用io线程池

#### Type Parameters

| Type Parameter |
| ------ |
| `T` |

#### Parameters

| Parameter | Type | Description |
| ------ | ------ | ------ |
| `javaobj` | `any` |  |
| `methodName` | `string` |  |
| `args`? | `any`[] |  |

#### Returns

`Promise`\<`T`\>

#### Defined in

[src/java/index.ts:33](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/java/index.ts#L33)

***

### invokeUi()

```ts
function invokeUi<T>(
   javaobj: any, 
   methodName: string, 
args?: any[]): Promise<T>
```

**`Alpha`**

和[invokeDefault](java.md#invokedefault)类似，采用ui线程

#### Type Parameters

| Type Parameter |
| ------ |
| `T` |

#### Parameters

| Parameter | Type | Description |
| ------ | ------ | ------ |
| `javaobj` | `any` |  |
| `methodName` | `string` |  |
| `args`? | `any`[] |  |

#### Returns

`Promise`\<`T`\>

#### Defined in

[src/java/index.ts:47](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/java/index.ts#L47)

***

### loadClass()

```ts
function loadClass(className: string): JavaClass
```

**`Alpha`**

加载并返回一个java类

#### Parameters

| Parameter | Type | Description |
| ------ | ------ | ------ |
| `className` | `string` | java全类名 |

#### Returns

`JavaClass`

#### Defined in

[src/java/index.ts:22](https://github.com/aiselp/AutoX/blob/fef14132f01d123d8ccfc0937f3f37dc42567abf/autojs/src/js-api/src/java/index.ts#L22)
