# React Component DashboardWidget

The Dashboard Widget component, which is a thin wrapper on the [ChartWidget](function.ChartWidget.md) component,
used to render a widget created in the Sisense instance.

## Example

The example below renders a dashboard widget with the specified widget and dashboard OIDs.
```tsx
<DashboardWidget
  widgetOid={'64473e07dac1920034bce77f'}
  dashboardOid={'6441e728dac1920034bce737'}
/>
```
