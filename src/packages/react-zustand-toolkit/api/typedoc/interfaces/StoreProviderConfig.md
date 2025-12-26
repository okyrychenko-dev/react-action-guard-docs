[**React Zustand Toolkit API v0.1.1**](../README.md)

***

[React Zustand Toolkit API](../README.md) / StoreProviderConfig

# Interface: StoreProviderConfig\<TState\>

Defined in: [types/index.ts:25](https://github.com/okyrychenko-dev/react-zustand-toolkit/blob/main/src/types/index.ts#L25)

Configuration for store provider

## Extended by

- [`StoreProviderProps`](StoreProviderProps.md)

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

***

### devtoolsName?

> `optional` **devtoolsName**: `string`

Defined in: [types/index.ts:35](https://github.com/okyrychenko-dev/react-zustand-toolkit/blob/main/src/types/index.ts#L35)

Name for the DevTools instance

#### Default

```ts
'Store'
```

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
