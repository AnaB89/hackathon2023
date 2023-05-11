---
description:  Guide for using checkboxes in your applications
---

# Checkbox

## Overview

This guide will show how to use a checkbox in your applications. See how easy it is to drag and drop the checkboxes onto your forms and connect them to your business logic. Checkbox can be modified, styled and even changed at runtime.


## Get Started

 In the [Form Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/form-editor.md), drag the Checkbox component from the Pallet onto the form.

{% hint style="info" %}
If the component does not appear in the pallet, it means you do not have the Bootstrap Components package installed. Click "Get more components" at the top of the pallet to open the [Servoy Package Manager](../../../../../reference/readme\_servoycore/page-3/package-manager.md) and install it.
{% endhint %} 
  
## Modifying a Checkbox at Design-Time

The checkbox, like all components, have properties which can be modified at design-time to set the appearance and behavior of the component. Select the checkbox in the [Form Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/form-editor.md) to see a list of properties in the [Component Properties Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/component-properties-editor.md). Below are some common properties and how to set them at design-time.

{% hint style="info" %}
See the reference docs for [Checkbox](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/checkbox.md) for a complete list of its [properties](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/checkbox.md#properties-summary).
{% endhint %}

### Setting the text

The text displayed on a checkbox can be modified by setting its [`text`](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/checkbox.md#text) property. Most often, this will just be plain text. In this case, just enter the value into the editor or directly on the component by double-clicking it. For more options open the [Text Property Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/text-property-editor.md).


### Setting the tooltipText

Checkboxes, like many components, can display tooltip messages when a user hovers their cursor. Most often, this will just be plain text that describes what value will be checked or unchecked. In this case, just enter the value into the editor. For more options open the [Text Property Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/text-property-editor.md).

 
{% hint style="info" %}
Remember that text can also be dynamic, data-driven or localized. For more options, you can open edit the text property in the [Text Property Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/text-property-editor.md).
{% endhint %}

### Styling

Like all components, a checkbox can be styled using themes, variants and raw CSS. To apply any available style class, simply enter one or more space-delimited values for the `styleClass` property.

<img src="" alt="" data-size="original">For example, `styleClass="checkbox"`

If you are using Variants, then you can easily drag and drop variations of your checkbox onto your form. 

## Handling Events

Like most components, checkbox have events, which allow you to execute some logic when something happens in the UI. Of course, the most common event for a checkbox is the `onDataChange` event, which is triggered when the checkbox is clicked.

To Handle the event, double-click the value for the `onDataChange` property in the [Properties Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/component-properties-editor.md). You will see the [Method Selection Wizard](../../../../../reference/readme\_servoycore/page-3/object-editors/method-selection-wizard.md). You'll have the option select an existing Method or create a new Method. The method will be called when the component's `onDataChange` event is fired and the [Event](../../../../../reference/readme\_servoycore/dev-api/application/jsevent.md) object will be passed to it.


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
See the [Checkbox reference](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/checkbox.md) for comprehensive list of [all events](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/checkbox.md#events-summary)
{% endhint %}

## Modifying a Checkbox at Runtime

Checkbox, like many components, can be modified at runtime through code. Below are a few examples of controlling a checkbox from code.

### Enabling / Disabling a Checkbox

You can easily change the `enabled` state of a checkbox at runtime.

```javascript
function  disableCheckbox(){
elements.myCheckbox.enabled = false;
}
```


## Calling Checkbox API Methods

Like most components, a checkbox has API methods which can be called from code. Below is an example of common API calls.

### Add CSS Style Class

You can easily add a style class to a checkbox using the [`addStyleClass`](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/checkbox.md#addstyleclass) method.

```javascript
function  AddStyleClassCheckbox(){
elements.myCheckbox.addStyleClass('mycssclass');
}
```

 {% hint style="info" %}
See the [Checkbox Reference Docs](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/checkbox.md) for a complete list of programmable [properties](../../../../../reference/readme\_servoyextensions/input-controls/checkbox.md#properties-summary) and [methods](../../../../../reference/readme\_servoyextensions/input-controls/checkbox.md#methods-summary).
{% endhint %} 
  
## Related Articles

The following articles are recommended for additional reading:

* [Checkbox Reference Documentation](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/checkbox.md)
* [Styling and Themes](../../styling-and-themes/)
* [Scripting the UI](../../../programming-guide/scripting-the-ui/)