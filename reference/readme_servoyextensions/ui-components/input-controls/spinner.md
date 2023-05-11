# Spinner

## Table of contents

* [Spinner properties](spinner.md#properties-summary)
* [Spinner events](spinner.md#events-summary)
* [Spinner methods](spinner.md#methods-summary)

## Properties Summary

The component has the following properties:

| Property         | Type         | Default | Description                                                                    |
| ---------------- | ------------ | ------- | ------------------------------------------------------------------------------ |
| dataProvider     | dataprovider |         | The dataprovider of the component                                              |
| displayTags      | Boolean      | true    | Whether texts should evaluate tags                                             |
| editable         | Boolean      | true    | Whether the component is editable                                              |
| enabled          | Boolean      | true    | Whether the component is enabled or not; blocks onAction, onDataChange events. |
| format           | format       |         | A format to format the data shown.                                             |
| placeholderText  | String       |         | Text shown when no value is yet selected (i18n is supported)                   |
| responsiveHeight | Number       |         | Component height                                                               |
| styleClass       | String       |         | Style class of this component                                                  |
| tabSeq           | Number       |         | Tab sequence index of the form                                                 |
| toolTipText      | String       |         | Tooltip text shown when hovering over the component (i18n is supported)        |
| valuelist        | valuelist    |         | The value list which offers the values presented                               |
| visible          | Boolean      | true    | Whether the component is visible or not                                        |

## Events Summary

The component allows to attach handlers for the following events:

| Event         | Parameters                                  | Return  | Description                          |
| ------------- | ------------------------------------------- | ------- | ------------------------------------ |
| [onAction](spinner.md#onaction)       | event:JSEvent                               |         | Fired when the enter key is hit      |
| [onDataChange](spinner.md#ondatachange)  | oldValue:Date, newValue:Date, event:JSEvent | Boolean | Fired when the value is changed      |
| [onFocusGained](spinner.md#onfocusgained) | event:JSEvent                               |         | Fired when the component gets focus  |
| [onFocusLost](spinner.md#onfocuslost)   | event:JSEvent                               |         | Fired when the component loses focus |
| [onRightClick](spinner.md#onrightclick)  | event:JSEvent                               |         | Fired for mouse right click          |

## Methods Summary

The component offers the following API methods:

| Method       | Parameters                             | Return | Description                       |
| ------------ | -------------------------------------- | ------ | --------------------------------- |
| [requestFocus](spinner.md#requestfocus) | mustExecuteOnFocusGainedMethod:Boolean |        | Sets the focus to this component. |
| [addStyleClass](spinner.md#addstyleclass) |            |        | Add a style class to styleclass named property or other property marked as mainStyleClass in the spec |


## Properties Details

### text

### toolTipText

### imageStyleClass

## Events Details

### onAction

### onDataChange

### onFocusGained

### onFocusLost

### onRightClick

## Methods Details

### requestFocus

### addStyleClass