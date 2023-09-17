# React Component AreaChart

A React component similar to a [LineChart](function.LineChart.md),
but with filled in areas under each line and an option to display them as stacked.
More info on [Sisense Documentation page](https://docs.sisense.com/main/SisenseLinux/area-chart.htm).

## Example

An example of using the component to visualize the `Sample ECommerce` data source:
```tsx
<AreaChart
  dataSet={DM.DataSource}
  dataOptions={{
    category: [DM.Commerce.Date.Years],
    value: [measures.sum(DM.Commerce.Revenue)],
    breakBy: [DM.Commerce.Gender],
  }}
  styleOptions={{ subtype: 'area/stacked' }}
  filters={[filters.members(DM.Commerce.Gender, ['Female', 'Male'])]}
  onDataPointClick={(point, nativeEvent) => {
    console.log('clicked', point, nativeEvent);
  }}
/>
```
