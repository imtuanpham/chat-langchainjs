# React Component FunnelChart

A React component representing data progressively decreasing in size or quantity through a conical shape.
See [Funnel Chart](https://docs.sisense.com/main/SisenseLinux/funnel-chart.htm) for more information.

## Example

An example of visualizing sales funnel data:
```tsx
<FunnelChart
  dataSet={{
    columns: [
      { name: 'Stage', type: 'string' },
      { name: 'Unique Users', type: 'number' },
    ],
    rows: [
      ['Website visits', 15654],
      ['Downloads', 4064],
      ['Requested price list', 1987],
      ['Invoice sent', 976],
      ['Finalized', 846],
    ],
  }}
  dataOptions={{
    category: [
      {
        name: 'Stage',
        type: 'string',
      },
    ],
    value: [
      {
        name: 'Unique Users',
        aggregation: 'sum',
      },
    ],
  }}
/>
```
