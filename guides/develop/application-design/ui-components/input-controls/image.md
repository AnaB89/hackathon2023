---
description: Guide for using Image component in your applications
---

# Image

## Overview

This guide will show how to use the image component  in your applications. The image component can be used for a variety of purposes, such as displaying logos, icons, product images, and other graphics. It can also be used to display dynamically generated images, such as charts or graphs.
Overall, the image component is a simple but essential component in Servoy for displaying visual content on forms.

## Get Started

## Modifying the image container at Design-Time

Image, like all components, have properties which can be modified at design-time to set the appearance and behavior of the component. Select the image in the [Form Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/form-editor.md) to see a list of properties in the [Component Properties Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/component-properties-editor.md). Below are some common properties and how to set them at design-time.

### Setting the Tooltip message

Image, like many components, can display tooltip messages when a user hovers their cursor. Most often, this will just be plain text that describes what will happen on-click. In this case, just enter the value into the editor. For more options open the [Text Property Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/text-property-editor.md).

### Setting the image

The image can be selected from the ones pre-loaded in the media folder of the application or related to a media field of a database
Just select the desired field or image in the media field of the property editor of the image component.

Note: Make sure that the image file or the URL you specify is accessible and correctly formatted. Additionally, consider using relative paths or dynamically retrieving the image source from a database or other data source for more flexibility.

### Styling

Like all components, a Image can be styled using themes, variants and raw CSS. To apply any available style class, simply enter one or more space-delimited values for the `styleClass` property.

## Handling Events

Like most components, Image have events, which allow you to execute some logic when something happens in the UI. Of course, the most common event for a Image is the `onAction` event, which is triggered when the Image is clicked or the user hits the `Enter` key while the Image has focus.

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
See the [Image reference]() for comprehensive list of [all events]()
{% endhint %}

## Modifying Image at Runtime

Image, like many components, can be modified at runtime through code. Below are a few examples of controlling a image from code.

### Enabling / Disabling an image

You can easily change the `enabled` state of a image at runtime.
Enabling the image component will allow to import or export an image during runtime. If the image component is enabled buttons for import and export images will be shown

```javascript
function disableButton(){
	elements.myImage.enabled = false;
}
```

### Hiding/Showing an image

You can easily change the `visible` state of the image component at runtime.

```javascript
function hideButton(){
	elements.myImage.visible = false;
}
```

## Calling Image API Methods

Like most components, a Image has API methods which can be called from code. Below is an example of common API calls.

### Give Keyboard Focus

You can easily give keyboard focus to a image using the [`requestFocus`]() method.

```javascript
function focusButton(){
	elements.myImage.requestFocus();
}
```

### Add CSS Style Class

You can easily add a style class to a image using the [`addStyleClass`]() method.
```javascript
function AddStyleClassBadge(){
	elements.myImage.addStyleClass('mycssclass');
}
```

## Related Articles

The following articles are recommended for additional reading:

* [Image Reference Documentation]()
* [Styling and Themes](../../styling-and-themes/)
* [Scripting the UI](../../../programming-guide/scripting-the-ui/)