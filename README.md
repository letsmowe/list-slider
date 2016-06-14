# list-slider
Walk through list block and return previous and next item for the active one.

List all ListItem from list block and walk through it (descending, from the last item to first) to find the active item:
+ if find an active item, return its previous and next items;
  + if active item is the first item of the list, return the last item as previous item, and if the active item is the last item of the list, return the first item as next item;
  + if there is no active item on the list, return the first item as previous and next items, and if there is no items on the list, return false.


Examples:

`ul.List>li.ListItem{$}*8`

ListItem: [1] [*2*] [**3**] [*4*] [5] [6] [7] [8]

`ListItem: [1] [2 .is-previous] [3 .is-active] [4 .is-next] [5] [6] [7] [8]`

ListItem: [*1*] [2] [3] [4] [5] [6] [*7*] [**8**]

`ListItem: [1 .is-next] [2] [3] [4] [5] [6] [7 .is-previous] [8 .is-active]`

ListItem: [**1**] [*2*] [3] [4] [5] [6] [7] [*8*]

`ListItem: [1 .is-active] [2 .is-next] [3] [4] [5] [6] [7] [8 .is-previous]`

ListItem: [*1*] [2] [3] [4] [5] [6] [7] [8]

`ListItem: [1 .is-next .is-previous] [2] [3] [4] [5] [6] [7] [8]`
