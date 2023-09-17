# React Hook useExecuteQueryByWidgetId

React hook that executes a data query extracted from an existing widget in the Sisense instance.

This approach, which offers an alternative to [ExecuteQueryByWidgetId](function.ExecuteQueryByWidgetId.md) component, is similar to React Query's `useQuery` hook.

## Example

The example below executes a query over the existing dashboard widget with the specified widget and dashboard OIDs.
```tsx
 const { data, isLoading, isError } = useExecuteQueryByWidgetId({
   widgetOid: '64473e07dac1920034bce77f'
   dashboardOid: '6441e728dac1920034bce737'
 });
 if (isLoading) {
   return <div>Loading...</div>;
 }
 if (isError) {
   return <div>Error</div>;
 }
 if (data) {
   return <div>{`Total Rows: ${data.rows.length}`}</div>;
 }
 return null;
```
