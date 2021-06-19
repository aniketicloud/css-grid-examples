# Named Grid Areas Notes

- grid-template-areas defines _named areas_ of the grid
- below property will create 3 x 3 matrix grid areas

```css
[grid-container] {
  grid-template-areas:
    'header header header'
    'nav    main   aside'
    'footer footer footer';
}
```

- In CSS terms, it expects the series of strings in single/double quotation marks.
- Each quotation means a single row, each space separated word inside means columns.

## 5 Things to know about 'grid-template-areas'

1. No L-shaped areas. Stick to the areas of rectangular shape. Example below won't work.

```css
[grid-container] {
  grid-template-areas:
    'header header header'
    '**footer**    main   aside'
    '**footer footer footer**';
}
```

2. Each row must have same number of cells. Example below won't work.

````css
[grid-container] {
  grid-template-areas:
    'header'
    'nav    main'
    'footer footer footer';
}

3. Define empty areas with elipses. So,
in previous example one wishes to achieve the result,
this is how it can be done ```css [grid-container] {
  grid-template-areas:
    'header ...    ...'
    'nav    main   ...'
    'footer footer footer';
}
````

4. Named _areas_ implicitly create named _lines_.

- So after defining the grid-area-name, it will automatically create grid-line-names. e.g. for 'header' grid-area-name, it will create 4 grid-line-names:
- For Horizontal : 'header-start' and 'header-end'
- For Vertical : 'header-start' and 'header-end'
  > Check 03-implicit-grid-line-names.html

5. Named _lines_ implicitly create named _areas_.

- It is a compliment of previous statement.
- For this to work, the grid-line-names must end with _-start_ or _-end_. e.g. [footer-start]
- This will not show area names in brwoser devloper tools ( yet ..!)
- Still, this approach seems a little more complicated.
  > Check 04-implicit-grid-area-names.html
