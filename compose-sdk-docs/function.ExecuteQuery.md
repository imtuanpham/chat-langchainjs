# React Component ExecuteQuery

Executes a query and renders a function as child component. The child
component is passed the results of the query.

This component takes the Children Prop Pattern and
offers an alternative approach to the [useExecuteQuery](function.useExecuteQuery.md) hook.

## Example

Example of using the component to query the `Sample ECommerce` data source:
```tsx
<ExecuteQuery
  dataSource={DM.DataSource}
  dimensions={[DM.Commerce.AgeRange]}
  measures={[measures.sum(DM.Commerce.Revenue)]}
  filters={[filters.greaterThan(DM.Commerce.Revenue, 1000)]}
>
{
  (data) => {
    if (data) {
      console.log(data);
      return <div>{`Total Rows: ${data.rows.length}`}</div>;
    }
  }
}
</ExecuteQuery>
```
