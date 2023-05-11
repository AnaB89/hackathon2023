---
description: Guide for using dropdown in your applications
---

# Dropdown

## Overview



This guide will show how to use Dropdown in your applications. See how easy it is to drag and drop Dropdown onto your forms and connect them to your business logic. Dropdown can be modified, styled and even changed at runtime.

## Get Started



## Modifying a Dropdown at Design-Time

Dropdown, like all components, have properties which can be modified at design-time to set the appearance and behavior of the component. Select the Dropdown in the [Form Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/form-editor.md) to see a list of properties in the [Component Properties Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/component-properties-editor.md). Below are some common properties and how to set them at design-time.



### Setting the text


The text displayed on a dropdown can be modified by setting its [`text`]() property. Most often, this will just be plain text, such as "Options" or "Choices". In this case, just enter the value into the editor. For more options open the [Text Property Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/text-property-editor.md).

### Setting the tooltipText

 
Dropdown, like many components, can display tooltip messages when a user hovers their cursor. Most often, this will just be plain text that describes what will happen on-click. In this case, just enter the value into the editor. For more options open the [Text Property Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/text-property-editor.md).

### Setting the enabled 

Dropdown, like many components, can be enabled or not enabled in order to allow users to interact with it or not. It can also be changed on runtime.


### Setting the visible

Dropdown, like many components, can be set as visible or not visible when launching an application. It can also be changed on runtime. 



 
### Styling

Like all components, a dropdown can be styled using themes, variants and raw CSS. To apply any available style class, simply enter one or more space-delimited values for the `styleClass` property.




## Handling Events



Like most components, dropdown has events, which allow you to execute some logic when something happens in the UI. Of course, the most common event for a dropdown is the `onMenuItemSelected` event, which is triggered when a menu item from the dropdown component is clicked.

To Handle the event, double-click the value for the `onMenuItemSelected` property in the [Properties Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/component-properties-editor.md). You will see the [Method Selection Wizard](../../../../../reference/readme\_servoycore/page-3/object-editors/method-selection-wizard.md). You'll have the option select an existing Method or create a new Method. The method will be called when the button's `onMenuItemSelected` event is fired and the [Event](../../../../../reference/readme\_servoycore/dev-api/application/jsevent.md) object will be passed to it.



```javascript
/**
 * @param {JSEvent} event
 *
 * @properties={typeid:24,uuid:"A74C281C-00AA-46AA-BB38-500C937F2D1A"}
 */
function onMenuItemSelected(event, menuItem) {
	// Enter custom code
}
```

{% hint style="info" %}
See the [dropdown reference]() for comprehensive list of [all events]()
{% endhint %}



## Modifying a dropdown at Runtime

dropdown, like many components, can be modified at runtime through code. Below are a few examples of controlling a dropdown from code.

### Enabling / Disabling a dropdown 

You can easily change the `enabled` state of a dropdown at runtime.



```javascript
function disableDropdown(){
	elements.myDropdown.enabled = false;
}
```

### Hiding/Showing a dropdown 

You can easily change the `visible` state of a dropdown at runtime.



```javascript
function hideDropdown(){
	elements.myDropdown.visible = false;
}
```



## Calling dropdown API Methods

Like most components, a dropdown has API methods which can be called from code. Below is an example of common API calls.

### Add item in the dropdown menu 

You can easily give keyboard focus to a dropdown using the [`addMenuItem`]() method.

```javascript
function focusButton(){
	elements.myButton.addMenuItem();
}
```


### Add CSS Style Class (Change this to match your component: )

You can easily add a style class to a dropdown using the [`addStyleClass`]() method.



```javascript
function AddStyleClassBadge(){
	elements.myDropdown.addStyleClass('mycssclass');
}
```


## Related Articles

The following articles are recommended for additional reading:

* [dropdown Reference Documentation]()
* [Styling and Themes](../../styling-and-themes/)
* [Scripting the UI](../../../programming-guide/scripting-the-ui/)
