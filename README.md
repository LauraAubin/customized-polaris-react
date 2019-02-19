# Themeable Polaris React

This is an exploration into allowing themes in the [Polaris component library](https://polaris.shopify.com).

### Assigning the theme to a component

Components take an optional prop named `theme` of type `string`. The theme maps back to the custom `styles.scss` file.

i.e,

```
<Card title="foo" theme="dark">
  <p>...</p>
</Card>
```

### Using the components with custom themes

Custom themes are added to [`styles.scss`](https://github.com/LauraAubin/themeable-polaris-react/blob/master/src/Themes/styles.scss) by creating additional map entries.

They take the form,

```css
$themes: (
  default: (
    all-available-elements: color,
  ),
  name-of-theme: (
    element: blue,
  ),
  name-of-another-theme: (
    element: red,
    element-2: green,
  ),
);
```

By omitting an element in the map, the component will automatically use the **default** style.

**All available element styles are listed under [`default`](https://github.com/LauraAubin/themeable-polaris-react/blob/master/src/Themes/styles.scss#L4).**

### Components converted so far

- [Tabs](https://github.com/LauraAubin/themeable-polaris-react/tree/master/src/components/Tabs)
