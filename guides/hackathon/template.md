---
description: Guide for using componentName in your applications
---

# componentName

## Overview

(can be changed to match your component:)

This guide will show how to use componentName in your applications. See how easy it is to drag and drop componentName onto your forms and connect them to your business logic. componentName can be modified, styled and even changed at runtime.

## Get Started



## Modifying a componentName at Design-Time

componentName, like all components, have properties which can be modified at design-time to set the appearance and behavior of the component. Select the componentName in the [Form Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/form-editor.md) to see a list of properties in the [Component Properties Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/component-properties-editor.md). Below are some common properties and how to set them at design-time.



### Setting the property1name (text)

Change this to match your component: 
The text displayed on a button can be modified by setting its [`text`]() property. Most often, this will just be plain text, such as "Submit" or "Cancel". In this case, just enter the value into the editor or directly on the component by double-clicking it. For more options open the [Text Property Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/text-property-editor.md).

### Setting the property2name (tooltipText)


Change this to match your component: 
Buttons, like many components, can display tooltip messages when a user hovers their cursor. Most often, this will just be plain text that describes what will happen on-click. In this case, just enter the value into the editor. For more options open the [Text Property Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/text-property-editor.md).

### Setting the property3name (or delete if needed)


### Styling

Like all components, a componentName can be styled using themes, variants and raw CSS. To apply any available style class, simply enter one or more space-delimited values for the `styleClass` property.


#### componentName Variants  - IF AVAILABLE

If you are using Variants, then you can easily drag and drop variations of your componentName onto your form.



## Handling Events

Change this to match your component - if the case: 

Like most components, componentName have events, which allow you to execute some logic when something happens in the UI. Of course, the most common event for a componentName is the `onAction` event, which is triggered when the componentName is clicked or the user hits the `Enter` key while the componentName has focus.

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
```

{% hint style="info" %}
See the [componentName reference]() for comprehensive list of [all events]()
{% endhint %}



## Modifying a componentName at Runtime

componentName, like many components, can be modified at runtime through code. Below are a few examples of controlling a componentName from code.

### Enabling / Disabling a componentName (delete/change if not the case)

You can easily change the `enabled` state of a componentName at runtime.


Change this to match your component: 
```javascript
function disableButton(){
	elements.myButton.enabled = false;
}
```

### Hiding/Showing a componentName (delete/change if not the case)

You can easily change the `visible` state of a componentName at runtime.


Change this to match your component: 
```javascript
function hideButton(){
	elements.myButton.visible = false;
}
```

### other runtime action (delete if not the case)



## Calling componentName API Methods

Like most components, a componentName has API methods which can be called from code. Below is an example of common API calls.

### Give Keyboard Focus (Change this to match your component: )


Change this to match your component: 

You can easily give keyboard focus to a componentName using the [`requestFocus`]() method.

```javascript
function focusButton(){
	elements.myButton.requestFocus();
}
```


### Add CSS Style Class (Change this to match your component: )

You can easily add a style class to a componentName using the [`addStyleClass`]() method.


Change this to match your component: 
```javascript
function AddStyleClassBadge(){
	elements.myBadge.addStyleClass('mycssclass');
}
```


## Related Articles

The following articles are recommended for additional reading:

* [componentName Reference Documentation]()
* [Styling and Themes](../../styling-and-themes/)
* [Scripting the UI](../../../programming-guide/scripting-the-ui/)
