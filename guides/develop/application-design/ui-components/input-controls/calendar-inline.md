---
description Guide for using the Calendar Inline in your applications
---

# Calendar Inline

## Overview

Calendar-Inline is an input control component. It allows a user us a date-picker to choose Date values for a bound data-provider.
Similar to the Calendar component, the Calendar-Inline provides a date-picker interface to choose a date. The key difference is that the Calendar component is an input field that the shows the date-picker in a popup only when clicked; whereas the Calendar Inline shows the date-picker directly on the form.
Common use cases include selecting a value for a filter or search parameter.

## Get Started

In the [Form Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/form-editor.md), drag the Calendar-Inline component from the Pallet onto the form.


{% hint style="info" %}
If the component does not appear in the pallet, it means you do not have the Bootstrap Components package installed. Click "Get more components" at the top of the pallet to open the [Servoy Package Manager](../../../../../reference/readme\_servoycore/page-3/package-manager.md) and install it.
{% endhint %}

## Modifying Calendar Inline at Design-Time

Calendar Inline, like all components, have properties which can be modified at design-time to set the appearance and behavior of the component. Select the Calendar Inline in the [Form Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/form-editor.md) to see a list of properties in the [Component Properties Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/component-properties-editor.md). Below are some common properties and how to set them at design-time.

{% hint style="info" %}
See the reference docs for [Calendar Inline](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/inline-calendar.md) for a complete list of its [properties](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/inline-calendar.md#properties-summary).
{% endhint %}

### Setting the toolTipText

Calendar Inline, like many components, can display tooltip messages when a user hovers their cursor. Most often, this will just be plain text that describes what will happen on-click. In this case, just enter the value into the editor. For more options open the [Text Property Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/text-property-editor.md).
		

### Styling

Like all components, Calendar Inline can be styled using themes, variants and raw CSS. To apply any available style class, simply enter one or more space-delimited values for the `styleClass` property.

## Handling Events

Like most components, Calendar Inline has events, which allow you to execute some logic when something happens in the UI. Of course, the most common event for a Calendar Inline is the `onDataChange` event, which is triggered when a date item is clicked.

To handle the event, double-click the value for the `onDataChange` property in the [Properties Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/component-properties-editor.md). You will see the [Method Selection Wizard](../../../../../reference/readme\_servoycore/page-3/object-editors/method-selection-wizard.md). You'll have the option select an existing Method or create a new Method. The method will be called when the component's `onDataChange` event is fired and the [Event](../../../../../reference/readme\_servoycore/dev-api/application/jsevent.md) object will be passed to it.

```javascript
/**
 * @param {JSEvent} event
 *
 * @properties={typeid24,uuidA74C281C-00AA-46AA-BB38-500C937F2D1A}
*/ 
function onDataChange(oldValue, newValue, event) {
	 application.output(newValue); //print out the date selected
}
```

{% hint style=info %}
See the [Calendar Inline reference](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/inline-calendar.md) for comprehensive list of [all events](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/inline-calendar.md#events-summary)
{% endhint %}


## Modifying a Calendar Inline at Runtime

Calendar Inline, like many components, can be modified at runtime through code. Below are a few examples of controlling a Calendar Inline from code.

### Enabling  or Disabling a Calendar Inline

You can easily change the `enabled` state of a Calendar Inline at runtime.

```javascript
function disableCalendar(){
	elements.myCalendar.enabled = false;
}
```

### HidingShowing a Calendar Inline

You can easily change the `visible` state of a Calendar Inline at runtime.

```javascript
function hideCalendar(){
	elements.myCalendar.visible = false;
}
```

## Calling Calendar Inline API Methods

Like most components, a Calendar Inline has API methods which can be called from code. Below is an example of common API calls.

### disableDates

Disable some dates from selection in the calendar [`disableDates`](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/inline-calendar.md#disabledates) method.

```javascript
function disableDates(){
	var dates = [];
	var d = new Date(); //create a new date object for today's date
	d.setDate(d.getDate() + 1); //set the date to the next day
	dates.push(d); // add that date object to an array
	elements.myCalendar.disableDates(dates); // send the array to the api which will then disable the day after today.
}
```

### Add CSS Style Class 

You can easily add a style class to a Calendar Inline using the [`addStyleClass`](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/inline-calendar.md#addstyleclass) method.

```javascript
function AddStyleClassCalendar(){
	elements.myCalendar.addStyleClass('mycssclass');
}
```

## Related Articles

The following articles are recommended for additional reading

* [Calendar Inline Reference Documentation](../../../../../reference/readme\_servoyextensions/ui-components/input-controls/inline-calendar.md)
* [Styling and Themes](../../styling-and-themes/)
* [Scripting the UI](../../../programming-guide/scripting-the-ui/)