[**React Zustand Toolkit API v0.1.1**](../README.md)

***

[React Zustand Toolkit API](../README.md) / StoreProviderProps

# Interface: StoreProviderProps\<TState\>

Defined in: [types/index.ts:46](https://github.com/okyrychenko-dev/react-zustand-toolkit/blob/main/src/types/index.ts#L46)

Props for generated provider component

## Extends

- [`StoreProviderConfig`](StoreProviderConfig.md)\<`TState`\>

## Type Parameters

### TState

`TState` = `unknown`

## Properties

### enableDevtools?

> `optional` **enableDevtools**: `boolean`

Defined in: [types/index.ts:30](https://github.com/okyrychenko-dev/react-zustand-toolkit/blob/main/src/types/index.ts#L30)

Enable Redux DevTools integration

#### Default

```ts
process.env.NODE_ENV === 'development'
```

#### Inherited from

[`StoreProviderConfig`](StoreProviderConfig.md).[`enableDevtools`](StoreProviderConfig.md#enabledevtools)

***

### devtoolsName?

> `optional` **devtoolsName**: `string`

Defined in: [types/index.ts:35](https://github.com/okyrychenko-dev/react-zustand-toolkit/blob/main/src/types/index.ts#L35)

Name for the DevTools instance

#### Default

```ts
'Store'
```

#### Inherited from

[`StoreProviderConfig`](StoreProviderConfig.md).[`devtoolsName`](StoreProviderConfig.md#devtoolsname)

***

### onStoreCreate()?

> `optional` **onStoreCreate**: (`store`) => `void`

Defined in: [types/index.ts:40](https://github.com/okyrychenko-dev/react-zustand-toolkit/blob/main/src/types/index.ts#L40)

Callback called after store is created
Use this to initialize the store, register middlewares, etc.

#### Parameters

##### store

`StoreApi`\<`TState`\>

#### Returns

`void`

#### Inherited from

[`StoreProviderConfig`](StoreProviderConfig.md).[`onStoreCreate`](StoreProviderConfig.md#onstorecreate)

***

### children

> **children**: `ReactNode`

Defined in: [types/index.ts:47](https://github.com/okyrychenko-dev/react-zustand-toolkit/blob/main/src/types/index.ts#L47)
