#### Quick Access
id:: 6567d1cd-f170-4872-a017-fcb428285f78
collapsed:: true
	- Projects:
	  collapsed:: true
		- The Collective
		- Latent Arcana
		-
	- Framework:
	  collapsed:: true
		- Notes:
			- Properties:
			  collapsed:: true
				- Built-in
				  {{embed ((656a373c-3c3b-4aa5-ba98-040bdc62e30c))}}
				- Mine:
					- TODO this
- # Personal Process
  collapsed:: true
	- ## Notes
		- ---
		  desc: Where I note how I note
		  ---
		-
	-
- # Logseq
  collapsed:: true
	- ### Links
		- https://docs.logseq.com/#/page/macros
	- ## Properties
	  collapsed:: true
		- ### Mine
		- ### Built-In
		  collapsed:: true
			- There are built-in in properties that control Logseq functionality. Most of the these properties are hidden from the user but a few are user editable. These property names are reserved for Logseq and thus *must* not be used as a user property.
			- Legend for properties below:
				- (1) and (N) indicate how many values you may define, one and multiple values respectively.
				- (page) and (block) indicates a property is a page property or block property only. Otherwise a property can be both a page property and block property.
			- Editable properties
			  id:: 656a373c-3c3b-4aa5-ba98-040bdc62e30c
				- `icon` (1) (page) - define icon identifier for a page.
				  `title` (1) (page) - overrides the title of a page to be different from the file name.
				  `tags` (N) - get listed in their own section "Pages tagged with X" below a page.
				  `template` (1) - designates a page/block as a template.
				  `template-including-parent` (1) - specifies whether the parent level content of the selected block should be included when using a template. previously called `include-parent`
				  `alias` (N) - define synonyms for a page.
				  `filters` (N) (page) - store selected filters for linked references on page-level. object with booleans
				  `public` (1) (page) - defines whether a page should be included in an export. boolean
				  `exclude-from-graph-view` (1) (page) - defines whether a page should be excluded in global graph view. boolean
			- See [Props](https://docs.logseq.com/#/page/built-in%20properties:~:text=TablesFunctionality-,Props,-1) for table related properties
			- Hidden properties
				- `collapsed` (1) (block) - specifies whether a block is collapsed.
				  `id` (1) (block) - specifies a block id.
				  `created-at` (1) (block) - deprecated property that defines the created date/time stamps in [Unix time](https://en.wikipedia.org/wiki/Unix_time)
				  `updated-at` (1) (block) - deprecated property that defines the updated date/time stamps in [Unix time](https://en.wikipedia.org/wiki/Unix_time). previously `last-modified-at`
				  `query-table` (1) (block) - marks a query to be shown as the table view.
				  `query-properties` (N) (block) - properties user has chosen to see in query table.
				  `query-sort-by` (1) (block) - property by which to sort query table
				  `query-sort-desc` (1) (block) - property sort direction. boolean where true is descending
				- See `hidden-built-in-properties` in [https://github.com/logseq/logseq/blob/master/deps/graph-parser/src/logseq/graph_parser/property.cljs](https://github.com/logseq/logseq/blob/master/deps/graph-parser/src/logseq/graph_parser/property.cljs) for the full list.
		- ### More
		  collapsed:: true
			- ### Props
			  collapsed:: true
				- Logseq tables now render differently depending on the block-level props. The default values for these props can also be set in your `config.edn` as top level keys.
				- #### logseq.table.version
					- The `logseq.table.version` prop determines the version of the table. It can take one of two possible values:
						- `1` (default) - version 1 displays the standard table with no customizations
						- `2` - version 2 displays a table with dynamic widths to better fit content, with customizations available via props
				- #### logseq.table.hover
					- The `logseq.table.hover` prop configures the hover effect of the table. It accepts the following values:
						- `cell` (default) - hovering over a cell will highlight just the cell you are interacting with
						- `row` - hovering over a cell will highlight the entire row of the cell you are interacting with
						- `col` - hovering over a cell will highlight the entire column of the cell you are interacting with
						- `both` - hovering over a cell will highlight the entire row and the entire column of the cell you are interacting with
						- `none` - hovering over a cell will not cause a change in visual appearance
				- #### logseq.table.compact
					- The `logseq.table.compact` prop decides whether to show a compact version of the data. The possible values are:
						- `false` (default) - table data will be shown with standard padding for laid back consumption
						- `true` - table data will be shown with minimal padding to fit as much information on the screen as densely as possible
				- ### logseq.table.headers
					- The `logseq.table.headers` prop adjusts the casing that should be applied to the header columns. You can set it to one of the following options:
						- `none` (default) - use the name of the column exactly as found in the source data
						  collapsed:: true
							- `exAMpLE header` becomes `exAMpLE header`
						- `uppercase` - transform the entire name of the column to uppercase letters
						  collapsed:: true
							- `exAMpLE header` becomes `EXAMPLE HEADER`
						- `capitalize` - transform the entire name of the column to have each word capitalized
						  collapsed:: true
							- `exAMpLE header` becomes `Example Header`
						- `capitalize-first` - transform the entire name of the column to lowercase letters, and capitalize only the first letter of the column name
						  collapsed:: true
							- `exAMpLE header` becomes `Example header`
						- `lowercase` - transform the entire name of the column to lowercase letters
						  collapsed:: true
							- `exAMpLE header` becomes `example header`
				- #### logseq.table.borders
					- The `logseq.table.borders` prop allows you to define whether or not the table should have borders between all cells and rows. It can be either:
						- `true` (default) - show borders between all of the cells
						- `false` - do not show borders between any of the cells
				- #### logseq.table.stripes
					- The `logseq.table.stripes` prop decides whether or not the table should have alternately colored table rows. The available options are:
						- `false` (default) - all rows will have a uniform background color
						- `true` - rows will have alternating background colors
				- #### logseq.table.max-width
					- The `logseq.table.max-width` prop specifies the maximum width (in rems) that should be applied to each column. It accepts any number, with a default value of `30`.
						- `30` (default) - do not allow table columns to exceed 30 rems
						- `any number` - limit the maximum size of table columns to this many rems
				- #### logseq.color
					- The `logseq.color` prop sets the color accent of the table. The following colors are available:
						- `crimson`
						- `red`
						- `tomato`
						- `orange`
						- `amber`
						- `green`
						- `grass`
						- `teal`
						- `blue`
						- `purple`
						- `indigo`
						- `violet`
						- `plum`
						- `pink`
	- ## Graphical explanation of pages, blocks and reference
	  collapsed:: true
		- Imagine the pages as nodes organized on a circle:
		  ![image](https://discuss.logseq.com/uploads/default/original/2X/0/00089bd2f37a17c98da216a2b8e4ab9c2e1e6cbf.png)
		- ---
		- The `[[references]]` are links (arrows with a direction). This is a **graph/network** and it can be displayed in *Graph View*:
		- ![image](https://discuss.logseq.com/uploads/default/original/2X/9/966c74da7827866d1fc5120e72d7ef86e1bcc174.png)
		- ---
		- Each page has a **tree** of blocks:
		- ![image](https://discuss.logseq.com/uploads/default/original/2X/a/ab52f613b7c89fa32107ee52ace8baf64003de56.png)
		- ---
		- The `[[references]]` are links that actually start from a *block* and target a *page*.
		- ![image](https://discuss.logseq.com/uploads/default/original/2X/9/924457ba04bd9e7769a37bb9a5bbf11f69c073a9.png)
		- Imagine that the circle represents a room, the “hall of pages”. The pages are doors and the links can be represented as people entering the room from one door and exiting from another. The *Graph View* available in Logseq displays the paths they took in the hall of pages, with no information of blocks that are behind each door.
		- In a geometric sense, the connections you see in *Graph View* are the projections of the actual links that go from *blocks* to *pages*. If you are not familiar with a projection, think of it as a shadow:
		- #+BEGIN_EXPORT hiccup
		  [:a {:href "https://discuss.logseq.com/uploads/default/original/2X/e/e5e5d1ac7e416ee6852dbcb7aa5b47e0af10b90b.png", :title "image"} [:img {:srcset "https://discuss.logseq.com/uploads/default/optimized/2X/e/e5e5d1ac7e416ee6852dbcb7aa5b47e0af10b90b_2_517x317.png, https://discuss.logseq.com/uploads/default/original/2X/e/e5e5d1ac7e416ee6852dbcb7aa5b47e0af10b90b.png 1.5x, https://discuss.logseq.com/uploads/default/original/2X/e/e5e5d1ac7e416ee6852dbcb7aa5b47e0af10b90b.png 2x", :alt "image", :width "517", :src "https://discuss.logseq.com/uploads/default/optimized/2X/e/e5e5d1ac7e416ee6852dbcb7aa5b47e0af10b90b_2_517x317.png", :loading "lazy", :height "317"}] [:div {} [:svg {:aria-hidden "true"} [:use {:href "#far-image"}]] [:span {} "image"] [:span {} "706×433 61.2 KB"] [:svg {:aria-hidden "true"} [:use {:href "#discourse-expand"}]]]]
		  #+END_EXPORT
		- The *page references* can be traversed in the opposite direction thanks to the section *Linked references* available at the bottom of each page.
		- ---
		- Instead a connection between *pages* can be made using *Page properties*. A special property is *Tags*, because the same link can be traversed in the reverse direction thanks to a section that appears at the bottom of pages, named *“Pages tagged with (current page)”*.
		- #+BEGIN_EXPORT hiccup
		  [:a {:href "https://discuss.logseq.com/uploads/default/original/2X/6/6f73866e5f6573625250c2e38182121ab5b366e9.png", :title "image"} [:img {:srcset "https://discuss.logseq.com/uploads/default/optimized/2X/6/6f73866e5f6573625250c2e38182121ab5b366e9_2_517x281.png, https://discuss.logseq.com/uploads/default/optimized/2X/6/6f73866e5f6573625250c2e38182121ab5b366e9_2_775x421.png 1.5x, https://discuss.logseq.com/uploads/default/original/2X/6/6f73866e5f6573625250c2e38182121ab5b366e9.png 2x", :alt "image", :width "517", :src "https://discuss.logseq.com/uploads/default/optimized/2X/6/6f73866e5f6573625250c2e38182121ab5b366e9_2_517x281.png", :loading "lazy", :height "281"}] [:div {} [:svg {:aria-hidden "true"} [:use {:href "#far-image"}]] [:span {} "image"] [:span {} "829×451 55.9 KB"] [:svg {:aria-hidden "true"} [:use {:href "#discourse-expand"}]]]]
		  #+END_EXPORT
		- ---
		- In general, *properties* have a *key::* and a *value*, so basically those links are *triples* like *subject* + *verb* + *object*. Compared to the previous links (those made with `[[references]]` from a block to a page), these links made with *properties* are relations **with a name**.
		- ![image](https://discuss.logseq.com/uploads/default/original/2X/1/114478bbfa8119007a4551a176a692a122d946f8.png)
		- Even if you, as a user, can’t see it, everything in Logseq is stored as *triples* in a so called *graph database*. Then Logseq UI displays only a small portion of that graph i.e. the one where *nodes* are *pages* and the *links* are the `[[references]]`.
		- ---
		- Since blocks can have *properties* too, it is possible to turn a normal `[[reference]]` in one where the name of the relation is specified. For example, a block could represent a book, a page an author and the *property* `author::` their relation:
		- #+BEGIN_EXPORT hiccup
		  [:a {:href "https://discuss.logseq.com/uploads/default/original/2X/0/06ea69ed5949e1b87e0b6e0a01c4fcc85e3e1d09.png", :title "image"} [:img {:srcset "https://discuss.logseq.com/uploads/default/optimized/2X/0/06ea69ed5949e1b87e0b6e0a01c4fcc85e3e1d09_2_690x323.png, https://discuss.logseq.com/uploads/default/original/2X/0/06ea69ed5949e1b87e0b6e0a01c4fcc85e3e1d09.png 1.5x, https://discuss.logseq.com/uploads/default/original/2X/0/06ea69ed5949e1b87e0b6e0a01c4fcc85e3e1d09.png 2x", :alt "image", :width "690", :src "https://discuss.logseq.com/uploads/default/optimized/2X/0/06ea69ed5949e1b87e0b6e0a01c4fcc85e3e1d09_2_690x323.png", :loading "lazy", :height "323"}] [:div {} [:svg {:aria-hidden "true"} [:use {:href "#far-image"}]] [:span {} "image"] [:span {} "907×425 58.7 KB"] [:svg {:aria-hidden "true"} [:use {:href "#discourse-expand"}]]]]
		  #+END_EXPORT
		- ---
		- It is also possible to use *block references* as *values* of *properties*. Since *pages* are not involved, no connection is displayed in *Graph view*. In the example below, the pages *Books* and *Authors* gather all books and authors (maybe organized in a hierarchy of blocks) and the *property* `author::` links them:
		- #+BEGIN_EXPORT hiccup
		  [:a {:href "https://discuss.logseq.com/uploads/default/original/2X/1/1276a77ea9410ae44fd4cdd4377658e80d5562e1.png", :title "image"} [:img {:srcset "https://discuss.logseq.com/uploads/default/optimized/2X/1/1276a77ea9410ae44fd4cdd4377658e80d5562e1_2_690x271.png, https://discuss.logseq.com/uploads/default/original/2X/1/1276a77ea9410ae44fd4cdd4377658e80d5562e1.png 1.5x, https://discuss.logseq.com/uploads/default/original/2X/1/1276a77ea9410ae44fd4cdd4377658e80d5562e1.png 2x", :alt "image", :width "690", :src "https://discuss.logseq.com/uploads/default/optimized/2X/1/1276a77ea9410ae44fd4cdd4377658e80d5562e1_2_690x271.png", :loading "lazy", :height "271"}] [:div {} [:svg {:aria-hidden "true"} [:use {:href "#far-image"}]] [:span {} "image"] [:span {} "987×389 68 KB"] [:svg {:aria-hidden "true"} [:use {:href "#discourse-expand"}]]]]
		  #+END_EXPORT
		- The image above also represent the same link traversed in the opposite direction thanks to the button that appears at the right of a block when it has been referenced somewhere else. In the example above it let you see all the books by an author and where that author is mentioned in general. This feature is available in latest Logseq release (0.8.18) thanks to [this change 18](https://github.com/logseq/logseq/pull/8695) by [@cldwalker](https://discuss.logseq.com/u/cldwalker) (many thanks!).
		- It’s up to the user to choose what should be a page and what a block. Using *queries* it is possible to retrieve content using both *page references* and *block references*. It is also possible to specify the name of the relation in case *properties* were used and even retrieve everything that has a given *property key* like `author::`.
- # Obsidian
  collapsed:: true
	- Links:
		- https://docs.logseq.com/#/page/macros