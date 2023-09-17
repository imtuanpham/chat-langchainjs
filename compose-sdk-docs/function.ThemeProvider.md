# React Component ThemeProvider

Theme provider, which allows you to adjust the look and feel of child components.

A Theme Provider component

## Example

Example of a theme provider, which changes the colors and font of the nested indicator chart:

```tsx
<ThemeProvider
  theme={{
    chart: {
      backgroundColor: '#333333',
      textColor: 'orange',
      secondaryTextColor: 'purple',
    },
    typography: {
      fontFamily: 'impact',
    },
  }}
>
  <IndicatorChart {...chartOptions} />
</ThemeProvider>
```
