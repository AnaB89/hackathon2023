# Badge

The badges component can be used to easily highlight new or unread items in labels or buttons.

Label example:

![Label](../../../../.gitbook/assets/image\_01.png)

Button example:

![Button](../../../../.gitbook/assets/image\_02.png)

## Table of contents

* [Badge properties](badges.md#properties-summary)
* [Badge events](badges.md#events-summary)
* [Badge methods](badges.md#methods-summary)

## Properties Summary

The component has the following properties:

| Property                                     | Type    | Default | Description                                                                                                                                        |
| -------------------------------------------- | ------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| enabled                                      | Boolean | true    | Whether the component is enabled or not                                                                                                            |
| displayType                                  | String  | BUTTON  | Controls the display type of the component: either "BUTTON" or "LABEL"                                                                             |
| [imageStyleClass](badges.md#imagestyleclass) | String  |         | Image style class for an optional image of the button (e.g. a FontAwesome or glyphicon class)                                                      |
| [styleClass](badges.md#styleclass)           | String  | null    | Additional style class(es) of the component. When the displayType is BUTTON, any of the bootstrap button classes (e.g. 'btn-primary') can be used. |
| [text](badges.md#text)                       | String  | Badge   | The text shown on the label or button                                                                                                              |
| [badgeText](badges.md#badgetext)             | String  | 0       | The badge text shown on the label or button                                                                                                        |
| visible                                      | Boolean | true    | The visible property of the component, default true.                                                                                               |

## Events Summary

| Event                                    | Params        | Return | Description                          |
| ---------------------------------------- | ------------- | ------ | ------------------------------------ |
| [onAction](badges.md#onaction)           | event:JSEvent |        | Fired when a badge is clicked        |
| [onDoubleClick](badges.md#ondoubleclick) | event:JSEvent |        | Fired when a badge is double clicked |
| [onRightClick](badges.md#onrightclick)   | event:JSEvent |        | Fired when a badge is right clicked  |

## Methods Summary

The component offers the following API methods:

| Method                                   | Params            | Return | Description                                                                                           |
| ---------------------------------------- | ----------------- | ------ | ----------------------------------------------------------------------------------------------------- |
| [addStyleClass](badges.md#addstyleclass) | styleclass:String |        | Add a style class to styleclass named property or other property marked as mainStyleClass in the spec |

## Properties Details

### text

### badgeText

### imageStyleClass

### styleClass

## Events Details

### onAction

### onDoubleClick

### onRightClick

## Methods Details

### addStyleClass
