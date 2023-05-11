---
description: Guide for using Switch in your applications
---

# Switch

## Overview

This guide will show how to use Switch in your applications. See how easy it is to drag and drop switches onto your forms and connect them to your business logic. Switch can be modified, styled and even changed at runtime.

To see a live sample of the component you can go [here](https://samples-dev.samples.servoy-cloud.eu/solution/components?a=switchButton).

## Get Started

In the [Form Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/form-editor.md), drag the Switch component from the Pallet onto the form.

{% hint style="info" %}
If the component does not appear in the pallet, it means you do not have the Bootstrap Extra Components package installed. Click "Get more components" at the top of the pallet to open the [Servoy Package Manager](../../../../../reference/readme\_servoycore/page-3/package-manager.md) and install it.
{% endhint %}

## Modifying a Switch at Design-Time

Switch, like all components, have properties which can be modified at design-time to set the appearance and behavior of the component. Select the Switch in the [Form Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/form-editor.md) to see a list of properties in the [Component Properties Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/component-properties-editor.md). Below are some common properties and how to set them at design-time.


{% hint style="info" %}
See the reference docs for [Switch](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/switch.md) for a complete list of its [properties](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/switch.md#properties-summary).
{% endhint %}

### Setting the animate

The animate property can be set on true or false. To apply this property on the webpage you need to check or uncheck the box depends on your preferences.

### Setting the componentSize

In case you want to change the size of the switch button you have 4 types of size that you can change in js file dinamically or hardcode in the property.

### Setting the dataProvider

The column or variable to provide the data for this label.

### Setting the onText/OffText

The text displayed on the sides of the button can be modified by setting its [`onText`](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/switch.md#ontext) property and [`offText`](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/switch.md#offtext) property. Most often, this will just be plain text for example on the left side "On" and on the right side "Off". In this case, just enter the value into the editor or directly on the component by double-clicking it.

### Setting the label 

The text displayed on the middle of the button can be modified by setting its [`label`](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/switch.md#label) property.

### Setting the labelWidth 

You can adjust the width of the middle container of the switch button.

### Styling

Like all components, a Switch can be styled using themes, variants and raw CSS. To apply any available style class, simply enter one or more space-delimited values for the `styleClass` property.

### Setting the offColor/onColor

You can change the color of the off button or on button by selecting from properties from the dropdown a class that is predifined by servoy. Also, you can change the color from JS file hardcoded or dinamically but keep in mind that you need to assign those classes using **lowercase** not uppercase!

### Setting the onColor

You can adjust the width of the middle container of the switch button

## Handling Events

Like most components, switches have events, which allow you to execute some logic when something happens in the UI. Of course, the most common event for a Switch is the `onDataChange` event, which is triggered when dataprovider is updated.

To handle the event, double-click the value for the `onDataChange` property in the [Properties Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/component-properties-editor.md). You will see the [Method Selection Wizard](../../../../../reference/readme\_servoycore/page-3/object-editors/method-selection-wizard.md). You'll have the option select an existing Method or create a new Method. The method will be called when the button's `onDataChange` event is fired and the [Event](../../../../../reference/readme\_servoycore/dev-api/application/jsevent.md) object will be passed to it.

```javascript
/**
 * Handle changed data, return false if the value should not be accepted.
 * JSEvent.data will contain extra information about dataproviderid, its scope and the scope id (record datasource or form/global variable scope)
 *
 * @param oldValue
 * @param newValue
 * @param {JSEvent} event
 *
 * @return {Boolean}
 *
 * @private
 *
 * @properties={typeid:24,uuid:"4A599FE8-D13D-4E4E-88AE-9B40DF8434F5"}
 */
function onDataChange(oldValue, newValue, event) {
	// Enter custom code
}
```

{% hint style="info" %}
See the [Switch reference](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/switch.md) for comprehensive list of [all events](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/switch.md#events-summary)
{% endhint %}

## Modifying a Switch at Runtime

Switch, like many components, can be modified at runtime through code. Below are a few examples of controlling a Switch from code.

### Enabling / Disabling a Switch

You can easily change the `enabled` state of a Switch at runtime.

```javascript
function disableSwitch(){
	elements.mySwitch.enabled = false;
}
```

### Hiding/Showing a Switch

You can easily change the `visible` state of a Switch at runtime.

```javascript
function hideSwitch(){
	elements.mySwitch.visible = false;
}
```

## Calling Switch API Methods

Like most components, a Switch has API methods which can be called from code. Below is an example of common API calls.

### Give Keyboard Focus

Change this to match your component: 

You can easily give keyboard focus to a Switch using the [`requestFocus`](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/switch.md#requestfocus) method.

```javascript
function focusSwitch(){
	elements.mySwitch.requestFocus();
}
```

### Add CSS Style Class

You can easily add a style class to a Switch using the [`addStyleClass`](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/switch.md#addstyleclass) method.

```javascript
function AddStyleClassSwitch(){
	elements.mySwitch.addStyleClass('mycssclass');
}
```

## Related Articles

The following articles are recommended for additional reading:

* [Switch Reference Documentation](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/switch.md)
* [Styling and Themes](../../styling-and-themes/)
* [Scripting the UI](../../../programming-guide/scripting-the-ui/)
