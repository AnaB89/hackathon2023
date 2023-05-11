{\rtf1\ansi\ansicpg1252\cocoartf2709
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0\fs24 \cf0 \
---\
description: Guide for using Spinner in your applications\
---\
\
# Spinner\
\
## Overview\
\
This guide will show how to use a Spinner in your applications. A spinner can be used to select a value from a predefined set of values, which are usually presented in a valuelist.\
See how easy it is to drag and drop Spinner onto your forms and connect them to your business logic. Spinner can be modified, styled and even changed at runtime.\
\
## Get Started\
\
\
\
## Modifying a spinner at Design-Time\
\
Spinner, like all components, have properties which can be modified at design-time to set the appearance and behavior of the component. Select the spinner in the [Form Editor](../../../../../reference/readme\\_servoycore/page-3/object-editors/form-editor.md) to see a list of properties in the [Component Properties Editor](../../../../../reference/readme\\_servoycore/page-3/object-editors/component-properties-editor.md). Below are some common properties and how to set them at design-time.\
\
### Selecting the Valuelist associated with the spinner\
\
The possible values of the spinner are the ones in the valuelist that is related to the component\
To select the valuelist just enter the name of the desired valuelist on the valuelist property of the spinner.\
More information about valuelists can be found here...\
\
### Setting the Tooltip message\
\
Spinner, like many components, can display tooltip messages when a user hovers their cursor. Most often, this will just be plain text that describes what will happen on-click. In this case, just enter the value into the editor. For more options open the [Text Property Editor](../../../../../reference/readme\\_servoycore/page-3/object-editors/text-property-editor.md).\
\
### Styling\
\
Like all components, a spinner can be styled using themes, variants and raw CSS. To apply any available style class, simply enter one or more space-delimited values for the `styleClass` property.\
\
## Handling Events\
\
Like most components, componentName have events, which allow you to execute some logic when something happens in the UI. Of course, the most common event for a componentName is the `onAction` event, which is triggered when the componentName is clicked or the user hits the `Enter` key while the componentName has focus.\
\
To Handle the event, double-click the value for the `onAction` property in the [Properties Editor](../../../../../reference/readme\\_servoycore/page-3/object-editors/component-properties-editor.md). You will see the [Method Selection Wizard](../../../../../reference/readme\\_servoycore/page-3/object-editors/method-selection-wizard.md). You'll have the option select an existing Method or create a new Method. The method will be called when the button's `onAction` event is fired and the [Event](../../../../../reference/readme\\_servoycore/dev-api/application/jsevent.md) object will be passed to it.\
\
\
\
```javascript\
/**\
 * @param \{JSEvent\} event\
 *\
 * @properties=\{typeid:24,uuid:"A74C281C-00AA-46AA-BB38-500C937F2D1A"\}\
 */\
function onAction(event) \{\
	// Enter custom code\
\}\
```\
\
\{% hint style="info" %\}\
See the [componentName reference]() for comprehensive list of [all events]()\
\{% endhint %\}\
\
\
\
## Modifying a spinner at Runtime\
\
Spinner, like many components, can be modified at runtime through code. Below are a few examples of controlling a componentName from code.\
\
### Enabling / Disabling a spinner\
\
You can easily change the `enabled` state of a componentName at runtime.\
\
\
Change this to match your component: \
```javascript\
function disableButton()\{\
	elements.mySpinner.enabled = false;\
\}\
```\
\
### Hiding/Showing a spinner\
\
You can easily change the `visible` state of a componentName at runtime.\
\
\
Change this to match your component: \
```javascript\
function hideButton()\{\
	elements.mySpinner.visible = false;\
\}\
```\
\
## Calling componentName API Methods\
\
Like most components, a spinner has API methods which can be called from code. Below is an example of common API calls.\
\
### Give Keyboard Focus\
\
You can easily give keyboard focus to a spinner using the [`requestFocus`]() method.\
\
```javascript\
function focusButton()\{\
	elements.mySpinner.requestFocus();\
\}\
```\
\
\
### Add CSS Style Class\
\
You can easily add a style class to a spinner using the [`addStyleClass`]() method.\
\
\
Change this to match your component: \
```javascript\
function AddStyleClassBadge()\{\
	elements.mySpinner.addStyleClass('mycssclass');\
\}\
```\
\
\
## Related Articles\
\
The following articles are recommended for additional reading:\
\
* [componentName Reference Documentation]()\
* [Styling and Themes](../../styling-and-themes/)\
* [Scripting the UI](../../../programming-guide/scripting-the-ui/)}