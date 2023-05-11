# Switch

The switch component can be used as an alternative for checkboxes and radios.

Switch example:

![switch](https://cloud.githubusercontent.com/assets/7150474/26816814/421ea9f0-4a59-11e7-9269-384d340c1ce5.PNG)

## Table of contents

* [Switch properties](switch.md#properties-summary)
* [Switch events](switch.md#events-summary)
* [Switch API](switch.md#methods-summary)

## Properties Summary

The component has the following properties:

| Property      | Type         | Default | Description                                                                                                   |
| ------------- | ------------ | ------- | ------------------------------------------------------------------------------------------------------------- |
| animate       | Boolean      | true    | determines if the switch animates when toggled.                                                               |
| componentSize | String       | Normal  | determines size of switch, choose from (Mini,Small,Normal, and Large).                                        |
| dataProvider  | dataprovider | null    | The dataprovider for the switch.                                                                              |
| enabled       | Boolean      | true    | The enable state of the component, default true.                                                              |
| handleWidth   | Number       | 150     | sets the width of both handles.                                                                               |
| label         | String       | Switch  | sets the toggle label.                                                                                        |
| labelWidth    | Number       | 150     | sets the width of the middle label.                                                                           |
| offColor      | String       | Primary | sets the negative (unchecked) class, can be default (as default), primary, info, success, warning, or danger. |
| offText       | String       | Off     | sets the negative (unchecked) text                                                                            |
| onColor       | String       | Primary | sets the positive (checked) class, can be default (as default), primary, info, success, warning, or danger.   |
| onText        | String       | On      | sets the positive (checked) text                                                                              |
| styleClass    | String       | null    | Additional style class(es) of the component                                                                   |
| tabSeq        | Number       | null    | The element's tab sequence                                                                                    |
| visible       | Boolean      | true    | The visible property of the component, default true.                                                          |

## Events Summary

| Event        | Params        | Return | Description                        |
| ------------ | ------------- | ------ | ---------------------------------- |
| [onAction](switch.md#onaction)      | event:JSEvent |        | Fired when a switch is clicked     |
| [onDataChange](switch.md#ondatachange)  | event:JSEvent |        | Fired when dataprovider is updated |

## Methods Summary

The component offers the following API methods:

| Method       | Parameters                             | Return | Description                       |
| ------------ | -------------------------------------- | ------ | --------------------------------- |
| [requestFocus](switch.md#requestfocus) | mustExecuteOnFocusGainedMethod:Boolean |        | Sets the focus to this component. |
| [addStyleClass](switch.md#addstyleclass) |            |        | Add a style class to styleclass named property or other property marked as mainStyleClass in the spec |


## Properties Details

### animate

### componentSize

### dataProvider

### enabled

### handleWidth

### label

### labelWidth

### offColor

### onColor

### onText

### styleClass

### tabSeq

### visible

## Events Details

### onAction

### onDataChange


## Methods Details

### requestFocus

### addStyleClass