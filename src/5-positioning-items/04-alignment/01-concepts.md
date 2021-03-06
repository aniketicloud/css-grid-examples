# Alignment & Justification Concepts

You can only align an item when it's inside a container that
has extra space than the item needs.
(The reason why there is a `height: 100%` on particular tags or classes like html,body,container-1. So that we can use the extra space below the 4em boxes. Look how I need to add height to tags or classes(first htl, then body then container-1). if we remove heiht from any of these, vertical effect will not be visible)

There are 2 types alignments we can set.

| Item                 | Container |
| -------------------- | --------- |
| Grid                 | Webpage   |
| Content of grid cell | Grid cell |

<!-- <table>
  <tr style="color:brown;">
    <th style="border-right: 1px solid brown">Item</th>
    <th>Container</th>
  </tr>
  <tbody>
    <tr>
      <td style="border-right: 1px solid brown">Grid</td>
      <td>Webpage</td>
    </tr>
    <tr>
      <td style="border-right: 1px solid brown">Contents of grid cell</td>
      <td>Grid cell</td>
    </tr>
  </tbody>
</table> -->

In above table,

1. We can align 'Grid' on a 'Webpage'
2. We can align the 'Content of the grid cell' _within_ the cell
3. In the example the 'Grid' is the _box_, and 'Content' is the _number_ inside the box

---

## Alignment & Justification Properties

|     | justify         | align         |
| --- | --------------- | ------------- |
| 1   | justify-content | align-content |
| 2   | justify-items   | align-items   |
| 3   | justify-self    | align-self    |

- In simple terms,
  - → justify means left to right ( x axis ) ( Horizontal )
  - ↓ align means top to bottom ( y axis ) ( Vertical )

> Checkout [CSS Box Alignment docs](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Alignment)

---

## justify-content & align-content

Both 'justify-content' and 'align-content' properties has the same possible values as shown in the table below.

|     | property value  | alignment                                                   |
| --- | --------------- | ----------------------------------------------------------- |
| 1   | start (default) | start position                                              |
| 2   | center          | at the center                                               |
| 3   | end             | at the end                                                  |
| 4   | space-between   | leave the tracks flush against the edges. No outside space. |
| 5   | space-evenly    | same space outside as between the tracks                    |
| 6   | space-around    | just half-space on the outside, as it between the tracks    |

- 4,5,6 will separate in space and distribute space between them. Difference is with what space leaves on the outside (or extreme ends)
- Applying these properties to justify means the effect is on horizontal axis
- Applying these properties to align means the effect is on vertical axis

---

---

## justify-items & align-items

- justify still means from left to right
- align still means from top to bottom
- First difference here is that, these two properties will change _items_ that are inside the the content, that is _items inside **ALL** grid cells_
- Second difference is the default value.
  - Default value **is NOT start**. Default value is **stretch** other
  - So if one sets value of justify-items & align-items to _start_, the items inside the content(grid-cell), will no longer fill up the space

Both 'justify-items' and 'align-items' properties has the same possible values as shown in the table below.

|     | property value        | alignment      |
| --- | --------------------- | -------------- |
| 1   | **stretch** (default) | start position |
| 2   | start                 | start position |
| 3   | center                | at the center  |
| 4   | end                   | at the end     |

---

## justify-self & align-self (related to items inside the grid-cell)

- These two properties will change _items_ that are inside the the content, that is _items inside **ONE** grid cell_

|     | property value        | alignment      |
| --- | --------------------- | -------------- |
| 1   | **stretch** (default) | start position |
| 2   | start                 | start position |
| 3   | center                | at the center  |
| 4   | end                   | at the end     |
