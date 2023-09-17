# React Component SisenseContextProvider

Sisense Context Provider Component allowing you to connect to
a Sisense instance and provide that context
to all Compose SDK components in your application.

## Example

Add SisenseContextProvider to the main component of your app as below and then wrap
other SDK components inside this component.

```tsx
import { Chart, SisenseContextProvider } from '@sisense/sdk-ui';
import * as DM from './sample-ecommerce';
import { measures } from '@sisense/sdk-data';

function App() {
  return (
    <>
      <SisenseContextProvider
        url="<instance url>" // replace with the URL of your Sisense instance
        token="<api token>" // replace with the API token of your user account
      >
        <OtherComponent1/>
        <OtherComponent2/>
      </SisenseContextProvider>
    </>
  );
}

export default App;
```
