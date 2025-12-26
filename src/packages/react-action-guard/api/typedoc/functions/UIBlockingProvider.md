[**React Action Guard API v0.6.0**](../README.md)

***

[React Action Guard API](../README.md) / UIBlockingProvider

# Function: UIBlockingProvider()

> **UIBlockingProvider**(`props`): `ReactNode`

Defined in: [src/context/UIBlockingContext.tsx:136](https://github.com/okyrychenko-dev/react-action-guard/blob/main/src/context/UIBlockingContext.tsx#L136)

Provider component for isolated UI blocking state management.

Creates an independent store instance for a subtree of your application.
Each provider has its own isolated blocking state, separate from the global
store and other provider instances.

**Use cases:**
- Server-Side Rendering (SSR) - Avoid state sharing between requests
- Testing - Isolated state for each test
- Micro-frontends - Independent blocking state per micro-app
- Modals/Dialogs - Scoped blocking within a dialog

Uses `createStoreProvider` from `@okyrychenko-dev/react-zustand-toolkit` with
built-in DevTools support and middleware registration.

## Parameters

### props

[`UIBlockingProviderProps`](../interfaces/UIBlockingProviderProps.md)

Provider configuration

## Returns

`ReactNode`

## Examples

Basic SSR setup
```tsx
import { UIBlockingProvider } from '@okyrychenko-dev/react-action-guard';

function App() {
  return (
    <UIBlockingProvider>
      <MyApplication />
    </UIBlockingProvider>
  );
}
```

With middleware and custom DevTools name
```tsx
import { UIBlockingProvider, loggerMiddleware } from '@okyrychenko-dev/react-action-guard';

function App() {
  return (
    <UIBlockingProvider
      enableDevtools={true}
      devtoolsName="MyApp-UIBlocking"
      middlewares={[loggerMiddleware]}
    >
      <MyApplication />
    </UIBlockingProvider>
  );
}
```

Multiple providers for micro-frontends
```tsx
function MicroFrontendApp() {
  return (
    <div>
      <UIBlockingProvider devtoolsName="MicroApp1">
        <MicroApp1 />
      </UIBlockingProvider>
      
      <UIBlockingProvider devtoolsName="MicroApp2">
        <MicroApp2 />
      </UIBlockingProvider>
    </div>
  );
}
```

Testing with isolated state
```tsx
// In your test file
import { render } from '@testing-library/react';
import { UIBlockingProvider } from '@okyrychenko-dev/react-action-guard';

test('blocker behavior', () => {
  render(
    <UIBlockingProvider enableDevtools={false}>
      <ComponentUnderTest />
    </UIBlockingProvider>
  );
  // Each test gets isolated state
});
```

## See

 - [useUIBlockingContext](../variables/useUIBlockingContext.md) to access the store from context
 - [useIsInsideUIBlockingProvider](../variables/useIsInsideUIBlockingProvider.md) to check if inside a provider
 - [UIBlockingProviderProps](../interfaces/UIBlockingProviderProps.md) for prop details

## Since

0.6.0
