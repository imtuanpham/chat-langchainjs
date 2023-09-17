# React Component BarChart

A React component representing categorical data with horizontal rectangular bars,
whose lengths are proportional to the values that they represent.
See [Bar Chart](https://docs.sisense.com/main/SisenseLinux/bar-chart.htm) for more information.

## Example

An example of using the component to visualize the `Sample ECommerce` data source:
```tsx
<BarChart
  dataSet={DM.DataSource}
  dataOptions={{
    category: [DM.Commerce.AgeRange],
    value: [measures.sum(DM.Commerce.Revenue)],
    breakBy: [DM.Commerce.Gender],
  }}
  filters={[filters.greaterThan(DM.Commerce.Revenue, 1000)]}
  onDataPointClick={(point, nativeEvent) => {
    console.log('clicked', point, nativeEvent);
  }}
/>
```
