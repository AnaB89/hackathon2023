# Checkbox

![Checkbox](https://github.com/Servoy/bootstrapcomponents/wiki/images/checkbox.png)

## Table of contents

* [Checkbox properties](checkbox.md#properties-summary)
* [Checkbox events](checkbox.md#events-summary)
* [Checkbox methods](checkbox.md#methods-summary)

## Properties Summary

The component has the following properties:

| Property      | Type         | Default | Description                                                                    |
| ------------- | ------------ | ------- | ------------------------------------------------------------------------------ |
| dataProvider  | dataprovider |         | The dataprovider (typically an integer column or variable)                     |
| enabled       | Boolean      | true    | Whether the component is enabled or not; blocks onAction, onDataChange events. |
| selectedValue | String       |         | The value returned when the checkbox is checked (defaults to 1)                |
| styleClass    | String       |         | Style class of this component                                                  |
| tabSeq        | Number       |         | Tab sequence index of the form                                                 |
| text          | String       |         | The text shown as label next to the check                                      |
| toolTipText   | String       |         | Tooltip text shown when hovering over the calendar (i18n is supported)         |
| visible       | Boolean      | true    | Whether the component is visible or not                                        |

## Events Summary

The component allows to attach handlers for the following events:

| Event         | Parameters                                  | Return  | Description                         |
| ------------- | ------------------------------------------- | ------- | ----------------------------------- |
| [onAction](checkbox.md#onaction)      | event:JSEvent                               |         | Fired when the enter key is hit     |
| [onDataChange](checkbox.md#ondatachange)  | oldValue:Date, newValue:Date, event:JSEvent | Boolean | Fired when the value is changed     |
| [onFocusGained](checkbox.md#onfocusgained) | event:JSEvent                               |         | Fired when the calendar gets focus  |
| [onFocusLost](checkbox.md#onfocuslost)   | event:JSEvent                               |         | Fired when the calendar loses focus |

## Methods Summary

The component offers the following API methods:

| Method        | Parameters | Return | Description                                                                                           |
| ------------- | ---------- | ------ | ----------------------------------------------------------------------------------------------------- |
| [addStyleClass](checkbox.md#addstyleclass) |            |        | Add a style class to styleclass named property or other property marked as mainStyleClass in the spec |
| [requestFocus](checkbox.md#requestfocus) |        |        | Sets the focus to this button. |


## Properties Details

### text

### toolTipText

### imageStyleClass

## Events Details

### onAction

### onDataChange

### onFocusGained

### onFocusLost

## Methods Details

### requestFocus

### addStyleClass