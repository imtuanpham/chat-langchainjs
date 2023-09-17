# React Component LineChart

A React component displaying data as a series of points connected by a line. Used to show trends or changes over time.
See [Line Chart](https://docs.sisense.com/main/SisenseLinux/line-chart.htm) for more information.

## Example

An example of using the component to visualize the `Sample ECommerce` data source:
```tsx
<LineChart
  dataSet={DM.DataSource}
  dataOptions={{
    category: [DM.Commerce.Date.Years],
    value: [measures.sum(DM.Commerce.Revenue)],
    breakBy: [DM.Commerce.Gender],
  }}
  filters={[filters.greaterThan(DM.Commerce.Revenue, 1000)]}
  onDataPointClick= {(point, nativeEvent) => {
    console.log('clicked', point, nativeEvent);
  }}
/>
```
