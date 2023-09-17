# React Component ChartWidget

The Chart Widget component extending the [Chart](function.Chart.md) component to support advanced BI
capabilities such as drilldown.

## Example

Example of using the `ChartWidget` component to
plot a bar chart of the `Sample ECommerce` data source hosted in a Sisense instance.
Drill-down capability is enabled.

```tsx
<ChartWidget
  dataSource={DM.DataSource}
  chartType="bar"
  dataOptions={{
    category: [DM.Category.Category],
    value: [measures.sum(DM.Commerce.Revenue)],
    breakBy: [],
  }}
  drilldownOptions={{
    drilldownCategories: [DM.Commerce.AgeRange, DM.Commerce.Gender, DM.Commerce.Condition],
  }}
/>
```
