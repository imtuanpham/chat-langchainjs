# React Component PolarChart

A React component comparing multiple categories/variables with a spacial perspective in a radial chart.
See [Polar Chart](https://docs.sisense.com/main/SisenseLinux/polar-chart.htm) for more information.

## Example

An example of using the component to visualize the `Sample ECommerce` data source:
```tsx
<PolarChart
  dataSet={DM.DataSource}
  dataOptions={{
    category: [DM.Commerce.AgeRange],
    value: [measures.sum(DM.Commerce.Revenue)],
    breakBy: [DM.Commerce.Gender],
  }}
  filters={[filters.greaterThan(DM.Commerce.Revenue, 1000)]}
  onDataPointClick= {(point, nativeEvent) => {
    console.log('clicked', point, nativeEvent);
  }}
/>
```
