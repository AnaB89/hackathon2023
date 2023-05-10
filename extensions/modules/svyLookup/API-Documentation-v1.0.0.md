# API Documentation v1.0.0

### Classes

[Lookup](API-Documentation-v1.0.0.md#lookup)\
[LookupField](API-Documentation-v1.0.0.md#lookupfield)

### Functions

[createLookup(dataSource)](API-Documentation-v1.0.0.md#createlookup-datasource-lookup) ⇒ [`Lookup`](API-Documentation-v1.0.0.md#lookup)

Creates a lookup object which can be used to show a pop-up form

### Lookup

* [Lookup](API-Documentation-v1.0.0.md#lookup)
  * [.addField(dataProvider)](API-Documentation-v1.0.0.md#lookup.addfield-dataprovider-lookupfield) ⇒ [`LookupField`](API-Documentation-v1.0.0.md#lookupfield)
  * [.getDataSource()](API-Documentation-v1.0.0.md#lookup.getdatasource-string) ⇒ `String`
  * [.getField(index)](API-Documentation-v1.0.0.md#lookup.getfield-index-lookupfield) ⇒ [`LookupField`](API-Documentation-v1.0.0.md#lookupfield)
  * [.getFieldCount()](API-Documentation-v1.0.0.md#lookup.getfieldcount-number) ⇒ `Number`
  * [.removeField(index)](API-Documentation-v1.0.0.md#lookup.removefield-index)
  * [.showPopUp(callback, target, \[width\], \[height\], \[initialValue\])](API-Documentation-v1.0.0.md#lookup.showpopup-callback-target-width-height-initialvalue)
  * [new Lookup(datasource)](API-Documentation-v1.0.0.md#new-lookup-datasource)

***

#### lookup.addField(dataProvider) ⇒ [`LookupField`](API-Documentation-v1.0.0.md#lookupfield)

Adds a field to the lookup object

| Param        | Type     |
| ------------ | -------- |
| dataProvider | `String` |

***

#### lookup.getDataSource() ⇒ `String`

Gets the data source for this Lookup object

***

#### lookup.getField(index) ⇒ [`LookupField`](API-Documentation-v1.0.0.md#lookupfield)

Gets the field at the specified index

| Param | Type     |
| ----- | -------- |
| index | `Number` |

***

#### lookup.getFieldCount() ⇒ `Number`

Gets the number of fields in the lookup object

***

#### lookup.removeField(index)

Removes a field at the specified index

| Param | Type     |
| ----- | -------- |
| index | `Number` |

***

#### lookup.showPopUp(callback, target, \[width], \[height], \[initialValue])

Shows the lookup

**Suppresswarnings(wrongparameters)**: Fixes illegitmate warning

| Param           | Type               | Description                                                            |
| --------------- | ------------------ | ---------------------------------------------------------------------- |
| callback        | `function`         | The function that will be called when a selection is made              |
| target          | `RuntimeComponent` | The component to show relative to                                      |
| \[width]        | `Number`           | The width of the lookup. Optional. Default is same as target component |
| \[height]       | `Number`           | The height of the lookup. Optional. Default is implementation-specifc. |
| \[initialValue] | `String`           | And initial value to show in the search                                |

***

#### new Lookup(datasource)

| Param      | Type     |
| ---------- | -------- |
| datasource | `String` |

***

### LookupField

* [LookupField](API-Documentation-v1.0.0.md#lookupfield)
  * [.getDataProvider()](API-Documentation-v1.0.0.md#lookupfield.getdataprovider-string) ⇒ `String`
  * [.getFormat()](API-Documentation-v1.0.0.md#lookupfield.getformat-string) ⇒ `String`
  * [.getTitleText()](API-Documentation-v1.0.0.md#lookupfield.gettitletext-string) ⇒ `String`
  * [.getValueListName()](API-Documentation-v1.0.0.md#lookupfield.getvaluelistname-string) ⇒ `String`
  * [.isSearchable()](API-Documentation-v1.0.0.md#lookupfield.issearchable-boolean) ⇒ `Boolean`
  * [.isVisible()](API-Documentation-v1.0.0.md#lookupfield.isvisible-boolean) ⇒ `Boolean`
  * [.setFormat(f)](API-Documentation-v1.0.0.md#lookupfield.setformat-f-lookupfield) ⇒ [`LookupField`](API-Documentation-v1.0.0.md#lookupfield)
  * [.setSearchable(b)](API-Documentation-v1.0.0.md#lookupfield.setsearchable-b-lookupfield) ⇒ [`LookupField`](API-Documentation-v1.0.0.md#lookupfield)
  * [.setTitleText(txt)](API-Documentation-v1.0.0.md#lookupfield.settitletext-txt-lookupfield) ⇒ [`LookupField`](API-Documentation-v1.0.0.md#lookupfield)
  * [.setVisible(b)](API-Documentation-v1.0.0.md#lookupfield.setvisible-b-lookupfield) ⇒ [`LookupField`](API-Documentation-v1.0.0.md#lookupfield)
  * [.setvalueListName(vl)](API-Documentation-v1.0.0.md#lookupfield.setvaluelistname-vl-lookupfield) ⇒ [`LookupField`](API-Documentation-v1.0.0.md#lookupfield)
  * [new LookupField(lookup, dataProvider)](API-Documentation-v1.0.0.md#new-lookupfield-lookup-dataprovider)

***

#### lookupField.getDataProvider() ⇒ `String`

Gets the data provider for this field

***

#### lookupField.getFormat() ⇒ `String`

Gets the display format for this field;

***

#### lookupField.getTitleText() ⇒ `String`

Gets the display text for this field

***

#### lookupField.getValueListName() ⇒ `String`

Gets the value list name for this field

***

#### lookupField.isSearchable() ⇒ `Boolean`

Gets the searchability of this field

***

#### lookupField.isVisible() ⇒ `Boolean`

Indicates if this field should be displayed

***

#### lookupField.setFormat(f) ⇒ [`LookupField`](API-Documentation-v1.0.0.md#lookupfield)

Sets the display format for this field

| Param | Type     |
| ----- | -------- |
| f     | `String` |

***

#### lookupField.setSearchable(b) ⇒ [`LookupField`](API-Documentation-v1.0.0.md#lookupfield)

Indicates if this field is searchable

| Param | Type      | Description                                         |
| ----- | --------- | --------------------------------------------------- |
| b     | `Boolean` | True to make searchable. False to make display-only |

***

#### lookupField.setTitleText(txt) ⇒ [`LookupField`](API-Documentation-v1.0.0.md#lookupfield)

Sets the display text for this field

| Param | Type     |
| ----- | -------- |
| txt   | `String` |

***

#### lookupField.setVisible(b) ⇒ [`LookupField`](API-Documentation-v1.0.0.md#lookupfield)

Sets this field's visibility in the lookup form

| Param | Type      |
| ----- | --------- |
| b     | `Boolean` |

***

#### lookupField.setvalueListName(vl) ⇒ [`LookupField`](API-Documentation-v1.0.0.md#lookupfield)

Sets the valuelist to use to display this field

| Param | Type     |
| ----- | -------- |
| vl    | `String` |

***

#### new LookupField(lookup, dataProvider)

| Param        | Type                                           |
| ------------ | ---------------------------------------------- |
| lookup       | [`Lookup`](API-Documentation-v1.0.0.md#lookup) |
| dataProvider |                                                |

***

### createLookup(dataSource) ⇒ [`Lookup`](API-Documentation-v1.0.0.md#lookup)

Creates a lookup object which can be used to show a pop-up form

| Param      | Type                                   | Description               |
| ---------- | -------------------------------------- | ------------------------- |
| dataSource | `String` \| `JSFoundSet` \| `JSRecord` | The data source to lookup |

***

#### createLookup\~ds : `String`

***
