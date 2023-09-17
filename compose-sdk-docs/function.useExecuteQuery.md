# React Hook useExecuteQuery

React hook that executes a data query.
This approach, which offers an alternative to [ExecuteQuery](function.ExecuteQuery.md) component, is similar to React Query's `useQuery` hook.

## Example

```tsx
 const { data, isLoading, isError } = useExecuteQuery({
   dataSource: DM.DataSource,
   dimensions: [DM.Commerce.AgeRange],
   measures: [measures.sum(DM.Commerce.Revenue)],
   filters: [filters.greaterThan(DM.Commerce.Revenue, 1000)],
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
