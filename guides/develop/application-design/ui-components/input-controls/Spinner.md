---
description: Guide for using Spinner in your applications
---

# Spinner

## Overview

This guide will show how to use a Spinner in your applications. A spinner can be used to select a value from a predefined set of values, which are usually presented in a valuelist.
See how easy it is to drag and drop spinners onto your forms and connect them to your business logic. Spinner can be modified, styled and even changed at runtime.

## Get Started

In the [Form Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/form-editor.md), drag the Spinner component from the Pallet onto the form.

{% hint style="info" %}
If the component does not appear in the pallet, it means you do not have the Servot Extra Components package installed. Click "Get more components" at the top of the pallet to open the [Servoy Package Manager](../../../../../reference/readme\_servoycore/page-3/package-manager.md) and install it.
{% endhint %} 

## Modifying a Spinner at Design-Time

Spinners, like all components, have properties which can be modified at design-time to set the appearance and behavior of the component. Select the spinner in the [Form Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/form-editor.md) to see a list of properties in the [Component Properties Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/component-properties-editor.md). Below are some common properties and how to set them at design-time.

{% hint style="info" %}
See the reference docs for [Spinner](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/Spinner.md) for a complete list of its [properties](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/Spinner.md#properties-summary).
{% endhint %}

### Selecting the Valuelist associated with the Spinner

The possible values of the spinner are the ones in the valuelist that is related to the component
To select the valuelist just enter the name of the desired valuelist on the valuelist property of the spinner.
More information about valuelists can be found [here](../../../../../guides/develop/application-design/data-modeling/value-lists.md).


### Setting the Tooltip message

Spinner, like many components, can display tooltip messages when a user hovers their cursor. Most often, this will just be plain text that describes what will happen on-click. In this case, just enter the value into the editor. For more options open the [Text Property Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/text-property-editor.md).


{% hint style="info" %}
Remember that text can also be dynamic, data-driven or localized. For more options, you can open edit the text property in the [Text Property Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/text-property-editor.md).
{% endhint %}

### Styling

Like all components, a spinner can be styled using themes, variants and raw CSS. To apply any available style class, simply enter one or more space-delimited values for the `styleClass` property.

## Handling Events

Like most components, spinners have events, which allow you to execute some logic when something happens in the UI. Of course, the most common event for a spinners is the `onDataChange` event, which is triggered when the value is changed.

To Handle the event, double-click the value for the `onDataChange` property in the [Properties Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/component-properties-editor.md). You will see the [Method Selection Wizard](../../../../../reference/readme\_servoycore/page-3/object-editors/method-selection-wizard.md). You'll have the option select an existing Method or create a new Method. The method will be called when the button's `onDataChange` event is fired and the [Event](../../../../../reference/readme\_servoycore/dev-api/application/jsevent.md) object will be passed to it.

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
	return true
}
```

{% hint style="info" %}
See the [Spinner reference](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/Spinner.md) for comprehensive list of [all events](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/Spinner.md#events-summary)
{% endhint %}

## Modifying a Spinner at Runtime

Spinner, like many components, can be modified at runtime through code. Below are a few examples of controlling a spinner from code.

### Enabling / Disabling a Spinner

You can easily change the `enabled` state of a spinner at runtime.

```javascript
function disableSpinner(){
	elements.mySpinner.enabled = false;
}
```

### Hiding/Showing a Spinner

You can easily change the `visible` state of a spinner at runtime.

```javascript
function hideSpinner(){
	elements.mySpinner.visible = false;
}
```

## Calling Spinner API Methods

Like most components, a spinner has API methods which can be called from code. Below is an example of common API calls.

### Give Keyboard Focus

You can easily give keyboard focus to a spinner using the [`requestFocus`](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/Spinner.md#requestfocus) method.

```javascript
function focusSpinner(){
	elements.mySpinner.requestFocus();
}
```

### Add CSS Style Class

You can easily add a style class to a spinner using the [`addStyleClass`](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/Spinner.md#addstyleclass) method.

```javascript
function AddStyleClassSpinner(){
	elements.mySpinner.addStyleClass('mycssclass');
}
```

## Related Articles

The following articles are recommended for additional reading:

* [Spinner Reference Documentation](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/Spinner.md)
* [Styling and Themes](../../styling-and-themes/)
* [Scripting the UI](../../../programming-guide/scripting-the-ui/)