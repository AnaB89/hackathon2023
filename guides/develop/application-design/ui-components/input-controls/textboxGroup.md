---
description: Guide for using textboxGroup in your applications
---

# textboxGroup

## Overview

(can be changed to match your component:)

This guide will show how to use textboxGroup in your applications. See how easy it is to drag and drop textboxGroup onto your forms and connect them to your business logic. textboxGroup can be modified, styled and even changed at runtime.

## Get Started



## Modifying a textboxGroup at Design-Time

textboxGroup, like all components, have properties which can be modified at design-time to set the appearance and behavior of the component. Select the textboxGroup in the [Form Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/form-editor.md) to see a list of properties in the [Component Properties Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/component-properties-editor.md). Below are some common properties and how to set them at design-time.



### Setting the placeholderText 

The text displayed inside the textboxGroup can be modified by setting its [`placeholderText`]() property. This will just be plain text which will be shown as an instruction on what you can do within the textbox. When you insert a value in the textboxGroup the placeholderText will disappear and your inserted text will take it's place. For more options open the [Text Property Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/text-property-editor.md).


### Setting the faclass 

The icon attached on the textbox can be changed from [`faclass`]() property. You can use different icons from fontawosome. For more options open the [Text Property Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/text-property-editor.md).


### Setting the inputType 

The inputType of the textbox and be changed from [`inputType`]() property. Here we have two types, text and password. For more options open the [Text Property Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/text-property-editor.md).


### Setting the tooltipText

TextBoxGroup, like many components, can display tooltip messages when a user hovers their cursor. Most often, this will just be plain text that describes what will happen on-click. In this case, just enter the value into the editor. For more options open the [Text Property Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/text-property-editor.md).




### Styling

Like all components, a textboxGroup can be styled using themes, variants and raw CSS. To apply any available style class, simply enter one or more space-delimited values for the `styleClass` property.


#### textboxGroup Variants  - IF AVAILABLE

If you are using Variants, then you can easily drag and drop variations of your textboxGroup onto your form.



## Handling Events

Change this to match your component - if the case: 

Like most components, textboxGroup have events, which allow you to execute some logic when something happens in the UI. Of course, the most common event for a textboxGroup is the `onDataChange` event, which is triggered when the textboxGroup is clicked or the user hits the `Enter` key while the textboxGroup has focus.

To Handle the event, double-click the value for the `onDataChange` property in the [Properties Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/component-properties-editor.md). You will see the [Method Selection Wizard](../../../../../reference/readme\_servoycore/page-3/object-editors/method-selection-wizard.md). You'll have the option select an existing Method or create a new Method. The method will be called when the TextBoxGroup's `onDataChange` event is fired and the [Event](../../../../../reference/readme\_servoycore/dev-api/application/jsevent.md) object will be passed to it.



```javascript
/**
 * @param {JSEvent} event
 *
 * @properties={typeid:24,uuid:"A74C281C-00AA-46AA-BB38-500C937F2D1A"}
 */
function onDataChange(event) {
	// Enter custom code
}


```

{% hint style="info" %}
See the [textboxGroup reference]() for comprehensive list of [all events]()
{% endhint %}



## Modifying a textboxGroup at Runtime

textboxGroup, like many components, can be modified at runtime through code. Below are a few examples of controlling a textboxGroup from code.

### Enabling / Disabling a textboxGroup (delete/change if not the case)

You can easily change the `enabled` state of a textboxGroup at runtime.



```javascript
function disableTextBoxGroup(){
	elements.myTextBoxGroup.enabled = false;
}
```

### Hiding/Showing a textboxGroup (delete/change if not the case)

You can easily change the `visible` state of a textboxGroup at runtime.



```javascript
function hideTextBoxGroup(){
	elements.myTextBoxGroup.visible = false;
}
```

### other runtime action (delete if not the case)



## Calling textboxGroup API Methods

Like most components, a textboxGroup has API methods which can be called from code. Below is an example of common API calls.

### Give Keyboard Focus ()




You can easily give keyboard focus to a textboxGroup using the [`requestFocus`]() method.

```javascript
function focusTextBoxGroup(){
	elements.myTextBoxGroup.requestFocus();
}
```


### Add CSS Style Class ()

You can easily add a style class to a textboxGroup using the [`addStyleClass`]() method.



```javascript
function AddStyleClassBadge(){
	elements.myBadge.addStyleClass('mycssclass');
}


```


## Related Articles

The following articles are recommended for additional reading:

* [textboxGroup Reference Documentation]()
* [Styling and Themes](../../styling-and-themes/)
* [Scripting the UI](../../../programming-guide/scripting-the-ui/)
