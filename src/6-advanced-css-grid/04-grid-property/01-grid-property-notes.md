# grid property uses and precautions

### **grid** is a shorthand for lot of properties

- grid-template-rows
- grid-template-columns
- grid-auto-rows
- grid-auto-columns
- grid-auto-flow
- grid-template-areas

- You can fill as many or few values in grid property as you like.
- But if you don't define a value of grid property, grid will set it to it's default value

```css
body {
  display: grid;

  /* code section 1 */
  grid-template-areas:
    'header header header'
    'nav    main   aside'
    'footer footer footer';
  grid-template-rows: minmax(min-content, 5em) auto minmax(min-content, 5em);
  grid-template-columns: 10em 2fr 1fr;

  /* code section 2 */
  grid:
    'hhh hhh hhh' minmax(min-content, 5em)
    'nnn mmm aaa' auto
    'fft fft fft' minmax(min-content, 5em) /
    10em 2fr 1fr;
}
```

- In above example, header will be replaced with hhh, nav will be replaced with nnn and so on.
- In above example, header will be replaced with nothing (default value of grid-area is nothing), nav will be replaced with nothing and so on.
  - Because grid property will over-ride grid-template-areas.
  - In _code section 3_ we are saying area names as header, nav etc.
  - In _code section 4_ we are saying that there are no area names.
  - Because of how CSS works, grid will wipe out the area names

```css
body {
  display: grid;

  /* code section 3 */
  grid-template-areas:
    'header header header'
    'nav    main   aside'
    'footer footer footer';
  grid-template-rows: minmax(min-content, 5em) auto minmax(min-content, 5em);
  grid-template-columns: 10em 2fr 1fr;

  /* code section 4 */
  grid:
    minmax(min-content, 5em)
    auto
    minmax(min-content, 5em) /
    10em 2fr 1fr;
}
```

## Golden Rule while using **grid** property
- If you want to use grid, define grid property first, probably after defining the container as `display: grid;`. This way, there are no surprises.
```css
[grid-container] {
  display: grid;
  grid: < whatever values and names you want >

  /* then you can add other properties, that is properties 
  grid shorthand can be used for (which was written at Start of this file) */
}
```