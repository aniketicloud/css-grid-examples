# Grid Accessibility

accessibility means the quality of being easily understood

---

## The visual layout of your page should mirror the source order of your HTML elements

- _Visual order_ should be same as _Source order_.
- Test with keyboard navigation on a page.
- Users excpect the tab-order in natural reading order.
- Avoid code that moves items out of the flow.
- In CSS Grid, the problem arises when you explicitly tell the source order.
- Default value of _order_ property of CSS Grid is 0. It can be negative and positive number.

```
grid-item {
  order: 0;
}
```

### Causes when Source order and Visual order is out of sync

1. Explicitly positioning an element (grid-row, grid-column, grid-area).

- this might get overlapping of grid items too.

2. Using `grid-auto-flow: dense;`.
3. Setting the `order` property (`order: 1;`).

> ! Important: Try not to set the positions explicitly. There will be other way.
