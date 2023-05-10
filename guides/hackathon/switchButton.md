---
description: Guide for using Switch in your applications
---

# Switch

## Overview

This guide will show how to use Switch in your applications. See how easy it is to drag and drop Switch onto your forms and connect them to your business logic. Switch can be modified, styled and even changed at runtime.

## Get Started



## Modifying a Switch at Design-Time

Switch, like all components, have properties which can be modified at design-time to set the appearance and behavior of the component. Select the Switch in the [Form Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/form-editor.md) to see a list of properties in the [Component Properties Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/component-properties-editor.md). Below are some common properties and how to set them at design-time.

### Setting the animate

The animate property can be set on true or false. To apply this property on the webpage you need to check or uncheck the box depends of your preferences.

### Setting the componentSize

In case you want to change the size of the switch button you have 4 types of size that you can change in js file dinamically or hardcode in the property.

### Setting the dataProvider

The column or variable to provide the data for this label.

### Setting the onText/OffText

The text displayed on the sides of the button can be modified by setting its [`onText`]() property and [`offText`]() property. Most often, this will just be plain text for example on the left side "On" and on the right side "Off". In this case, just enter the value into the editor or directly on the component by double-clicking it.

### Setting the label 

The text displayed on the middle of the button can be modified by setting its [`label`]() property.

### Setting the labelWidth 

You can adjust the width of the middle container of the switch button

### Styling

Like all components, a Switch can be styled using themes, variants and raw CSS. To apply any available style class, simply enter one or more space-delimited values for the `styleClass` property.

### Setting the offColor/onColor

You can change the color of the off button or on button by selecting from properties from the dropdown a class that is predifined by servoy. Also, you can change the color from JS file hardcoded or dinamically but keep in mind that you need to assign those classes using **lowercase** not uppercase!

### Setting the onColor

You can adjust the width of the middle container of the switch button

#### Switch Variants  - IF AVAILABLE

If you are using Variants, then you can easily drag and drop variations of your Switch onto your form.



## Handling Events

Change this to match your component - if the case: 

Like most components, Switch have events, which allow you to execute some logic when something happens in the UI. Of course, the most common event for a Switch is the `onAction` event, which is triggered when the Switch is clicked or the user hits the `Enter` key while the Switch has focus.

To Handle the event, double-click the value for the `onAction` property in the [Properties Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/component-properties-editor.md). You will see the [Method Selection Wizard](../../../../../reference/readme\_servoycore/page-3/object-editors/method-selection-wizard.md). You'll have the option select an existing Method or create a new Method. The method will be called when the button's `onAction` event is fired and the [Event](../../../../../reference/readme\_servoycore/dev-api/application/jsevent.md) object will be passed to it.



```javascript
/**
 * @param {JSEvent} event
 *
 * @properties={typeid:24,uuid:"A74C281C-00AA-46AA-BB38-500C937F2D1A"}
 */
function onAction(event) {
	// Enter custom code
}

function onDataChange(oldValue, newValue, event) {
	// Enter custom code
}
```

{% hint style="info" %}
See the [Switch reference]() for comprehensive list of [all events]()
{% endhint %}



## Modifying a Switch at Runtime

Switch, like many components, can be modified at runtime through code. Below are a few examples of controlling a Switch from code.

### Enabling / Disabling a Switch (delete/change if not the case)

You can easily change the `enabled` state of a Switch at runtime.


Change this to match your component: 
```javascript
function disableButton(){
	elements.myButton.enabled = false;
}
```

### Hiding/Showing a Switch (delete/change if not the case)

You can easily change the `visible` state of a Switch at runtime.


Change this to match your component: 
```javascript
function hideButton(){
	elements.myButton.visible = false;
}
```

### other runtime action (delete if not the case)



## Calling Switch API Methods

Like most components, a Switch has API methods which can be called from code. Below is an example of common API calls.

### Give Keyboard Focus (Change this to match your component: )


Change this to match your component: 

You can easily give keyboard focus to a Switch using the [`requestFocus`]() method.

```javascript
function focusButton(){
	elements.myButton.requestFocus();
}
```


### Add CSS Style Class (Change this to match your component: )

You can easily add a style class to a Switch using the [`addStyleClass`]() method.


Change this to match your component: 
```javascript
function AddStyleClassBadge(){
	elements.myBadge.addStyleClass('mycssclass');
}
```


## Related Articles

The following articles are recommended for additional reading:

* [Switch Reference Documentation]()
* [Styling and Themes](../../styling-and-themes/)
* [Scripting the UI](../../../programming-guide/scripting-the-ui/)
