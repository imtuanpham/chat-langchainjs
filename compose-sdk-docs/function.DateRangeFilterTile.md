# React Component DateRangeFilterTile

Date Range Filter Tile component for filtering data by date range.

## Example

React example of configuring the date min max values and handling onChange event.
```tsx
const [dateRangeFilter, setDateRangeFilter] = useState<Filter>(
  filters.dateRange(DM.Commerce.Date.Years),
);

return (
  <DateRangeFilterTile
    title="Date Range"
    attribute={DM.Commerce.Date.Years}
    filter={dateRangeFilter}
    onChange={(filter: Filter) => {
      setDateRangeFilter(filter);
    }}
  />
);
```
