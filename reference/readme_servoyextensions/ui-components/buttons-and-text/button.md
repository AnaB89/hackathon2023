# Button

Just that!

![Button](https://github.com/Servoy/bootstrapcomponents/wiki/images/button.png)

## Table of contents

* [Button properties](button.md#properties-summary)
* [Button events](button.md#events-summary)
* [Button methods](button.md#methods-summary)

## Properties Summary

The component has the following properties:

| Property                                     | Type    | Default           | Description                                                                                   |
| -------------------------------------------- | ------- | ----------------- | --------------------------------------------------------------------------------------------- |
| enabled                                      | Boolean | true              | Whether the component is enabled or not; blocks onAction, onDoubleClick, onRightClick events. |
| [imageStyleClass](button.md#imagestyleclass) | String  |                   | Image style class for an optional image of the button (e.g. a FontAwesome or glyphicon class) |
| tabSeq                                       | Number  |                   | Tab sequence index of the form                                                                |
| styleClass                                   | String  | "btn btn-default" | Button style class, typically one of the bootstrap button classes (e.g. "btn btn-primary")    |
| [text](button.md#text)                       | String  |                   | The text shown for the button (i18n is supported)                                             |
| [toolTipText](button.md#tooltiptext)         | String  |                   | Tooltip text shown when hovering over the button (i18n is supported)                          |
| visible                                      | Boolean | true              | Whether the button is visible or not                                                          |

## Events Summary

The component allows to attach handlers for the following events:

| Event                                    | Params        | Return | Description                             |
| ---------------------------------------- | ------------- | ------ | --------------------------------------- |
| [onAction](button.md#onaction)           | event:JSEvent |        | Fired when the button is clicked        |
| [onDoubleClick](button.md#ondoubleclick) | event:JSEvent |        | Fired when the button is double clicked |
| [onRightClick](button.md#onrightclick)   | event:JSEvent |        | Fired when the button is right clicked  |

## Methods Summary

The component offers the following API methods:

| Method                                 | Params | Return | Description                    |
| -------------------------------------- | ------ | ------ | ------------------------------ |
| [requestFocus](button.md#requestfocus) |        |        | Sets the focus to this button. |
| [addStyleClass](button.md#addstyleclass) |        |        | Add a style class to styleclass named property or other property marked as mainStyleClass in the spec |

## Properties Details

### text

### toolTipText

### imageStyleClass

## Events Details

### onAction

### onDoubleClick

### onRightClick

## Methods Details

### requestFocus
### addStyleClass
