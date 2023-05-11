
---
description Guide for using the Calendar in your applications
---

# Calendar

## Overview


Calendar-Inline is an input control component. It allows a user us a date-picker to choose Date values for a bound data-provider.
Similar to the Calendar component, the Calendar-Inline provides a date-picker interface to choose a date. The key difference is that the Calendar component is an input field that the shows the date-picker in a popup only when clicked; whereas the Calendar shows the date-picker directly on the form
Common use cases include selecting a value for a filter or search parameter.

## Get Started



## Modifying Calendar at Design-Time

Calendar, like all components, have properties which can be modified at design-time to set the appearance and behavior of the component. Select the componentName in the [Form Editor](..........referencereadme_servoycorepage-3object-editorsform-editor.md) to see a list of properties in the [Component Properties Editor](..........referencereadme_servoycorepage-3object-editorscomponent-properties-editor.md). Below are some common properties and how to set them at design-time.


### Setting the tooltipText


Calendar, like many components, can display tooltip messages when a user hovers their cursor. Most often, this will just be plain text that describes what will happen on-click. In this case, just enter the value into the editor. For more options open the [Text Property Editor](..........referencereadme_servoycorepage-3object-editorstext-property-editor.md).



### Setting the placeholderText 

The text displayed inside the calendar textbox can be modified by setting its [`placeholderText`]() property. This will just be plain text which will be shown as an instruction on what you can do within the calendar's textbox. When you insert a value in the calendar textbox the placeholderText will disappear and your inserted text will take it's place. For more options open the [Text Property Editor](../../../../../reference/readme\_servoycore/page-3/object-editors/text-property-editor.md).



### Setting the property3name (or delete if needed)
				

### Styling

Like all components, Calendar can be styled using themes, variants and raw CSS. To apply any available style class, simply enter one or more space-delimited values for the `styleClass` property.


## Handling Events



Like most components, Calendar has events, which allow you to execute some logic when something happens in the UI. Of course, the most common event for a Calendar is the `onDataChange` event, which is triggered when a date item is clicked.

To Handle the event, double-click the value for the `onDataChange` property in the [Properties Editor](..........referencereadme_servoycorepage-3object-editorscomponent-properties-editor.md). You will see the [Method Selection Wizard](..........referencereadme_servoycorepage-3object-editorsmethod-selection-wizard.md). You'll have the option select an existing Method or create a new Method. The method will be called when the button's `onAction` event is fired and the [Event](..........referencereadme_servoycoredev-apiapplicationjsevent.md) object will be passed to it.



```javascript

  @param {JSEvent} event
 
  @properties={typeid24,uuidA74C281C-00AA-46AA-BB38-500C937F2D1A}
 
function onDataChange(oldValue, newValue, event) {
	 application.output(newValue); //print out the date selected
}
```

{% hint style=info %}
See the [componentName reference]() for comprehensive list of [all events]()
{% endhint %}



## Modifying a Calendar at Runtime

Calendar, like many components, can be modified at runtime through code. Below are a few examples of controlling a Calendar from code.

### Enabling  or Disabling a Calendar

You can easily change the `enabled` state of a Calendar at runtime.


Change this to match your component 
```javascript
function disableCalendar(){
	elements.myCalendar.enabled = false;
}
```

### HidingShowing a Calendar

You can easily change the `visible` state of a Calendar at runtime.


Change this to match your component 
```javascript
function hideCalendar(){
	elements.myCalendar.visible = false;
}
```


## Calling Calendar API Methods

Like most components, a Calendar has API methods which can be called from code. Below is an example of common API calls.

### disableDates


Disable some dates from selection in the calendar [`disableDates`]() method.

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

You can easily add a style class to a Calendar using the [`addStyleClass`]() method.


Change this to match your component 
```javascript
function AddStyleClassBadge(){
	elements.myCalendar.addStyleClass('mycssclass');
}
```


## Related Articles

The following articles are recommended for additional reading

 [componentName Reference Documentation]()
 [Styling and Themes](....styling-and-themes)
 [Scripting the UI](......programming-guidescripting-the-ui)