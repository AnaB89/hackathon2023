# API Doc svyProperties

### Classes

[Property](svyProperties-API-Documentation.md#property)

### Functions

[changeExternalDBTransactionSupportFlag(mustSupportExternalTransactions)](svyProperties-API-Documentation.md#changeexternaldbtransactionsupportflag-mustsupportexternaltransactions)

Use this method to change the behavior of the svyProperties module with respect to DB transactions.

If the flag is set to false (default) then when saving or deleting security-related records if an external DB transaction is detected the operation will fail. If the flag is set to true then when saving or deleting security-related records the module will start/commit a DB transaction only if an external DB transaction is not detected. On exceptions any DB transaction will be rolled back regardless if it is started internally or externally (exceptions will be propagated to the external transaction so callers will be able to react on them accordingly)

[deleteProperty(property)](svyProperties-API-Documentation.md#deleteproperty-property-boolean) ⇒ `Boolean`

Immediately and permanently deletes the specified property.

[getGlobalProperty(propertyKey, propertyType)](svyProperties-API-Documentation.md#getglobalproperty-propertykey-propertytype-property) ⇒ [`Property`](svyProperties-API-Documentation.md#property)

Returns the global property with the given key and type\
Global properties are properties where the tenant and user name is not set

[getGlobalPropertyValue(propertyKey, propertyType)](svyProperties-API-Documentation.md#getglobalpropertyvalue-propertykey-propertytype-string) ⇒ `String`

Returns the value of the global property with the given key and type\
Global properties are properties where the tenant and user name is not set

[getProperties(propertyKey, \[propertyType\], \[tenantName\], \[userName\])](svyProperties-API-Documentation.md#getproperties-propertykey-propertytype-tenantname-username-array-.less-than-property-greater-than) ⇒ [`[ 'Array' ].<Property>`](svyProperties-API-Documentation.md#property)

Returns all properties with the given key and type, optional tenant and user name\


If tenantName is not provided, it will not be queried; if a null value is provided, only global properties are returned\
If userName is not provided, it will not be queried; if a null value is provided, only tenant wide properties are returned\


[getPropertiesByType(propertyType, \[tenantName\], \[userName\])](svyProperties-API-Documentation.md#getpropertiesbytype-propertytype-tenantname-username-array-.less-than-property-greater-than) ⇒ [`[ 'Array' ].<Property>`](svyProperties-API-Documentation.md#property)

Returns all properties of the given type, optional tenant and user name\


If tenantName is not provided, it will not be queried; if a null value is provided, only global properties are returned\
If userName is not provided, it will not be queried; if a null value is provided, only tenant wide properties are returned\


[getProperty(propertyKey, propertyType, \[tenantName\], \[userName\])](svyProperties-API-Documentation.md#getproperty-propertykey-propertytype-tenantname-username-property) ⇒ [`Property`](svyProperties-API-Documentation.md#property)

Returns the property with the given key and type or null if not found\
All parameters given need to match exactly

[getTenantProperty(propertyKey, propertyType)](svyProperties-API-Documentation.md#gettenantproperty-propertykey-propertytype-property) ⇒ [`Property`](svyProperties-API-Documentation.md#property)

Returns the tenant wide property with the given key and type for the tenant set via `setUserName()`\
Tenant wide properties are properties where the user name is not set

[getTenantPropertyValue(propertyKey, propertyType)](svyProperties-API-Documentation.md#gettenantpropertyvalue-propertykey-propertytype-string) ⇒ `String`

Returns the value of the tenant wide property with the given key and type for the tenant set via `setUserName()`\
Tenant wide properties are properties where the user name is not set

[getUserProperty(propertyKey, propertyType)](svyProperties-API-Documentation.md#getuserproperty-propertykey-propertytype-property) ⇒ [`Property`](svyProperties-API-Documentation.md#property)

Returns the property with the given key and type for the user set via `setUserName()`

[getUserPropertyValue(propertyKey, propertyType)](svyProperties-API-Documentation.md#getuserpropertyvalue-propertykey-propertytype-string) ⇒ `String`

Returns the value of the property with the given key and type for the user set via `setUserName()`

[getVersion()](svyProperties-API-Documentation.md#getversion-string) ⇒ `String`

Gets the version of this module

[setGlobalProperty(propertyKey, propertyType, value)](svyProperties-API-Documentation.md#setglobalproperty-propertykey-propertytype-value-property) ⇒ [`Property`](svyProperties-API-Documentation.md#property)

Sets the given value to the global property with the given key and type or creates a new property if not found\
Global properties are properties where the tenant and user name is not set

[setProperty(propertyKey, propertyType, value, userName, tenantName)](svyProperties-API-Documentation.md#setproperty-propertykey-propertytype-value-username-tenantname-property) ⇒ [`Property`](svyProperties-API-Documentation.md#property)

Sets the given value to the property with the given key and type or creates a new property if not found

[setTenantProperty(propertyKey, propertyType, value)](svyProperties-API-Documentation.md#settenantproperty-propertykey-propertytype-value-property) ⇒ [`Property`](svyProperties-API-Documentation.md#property)

Sets the given value to the tenant wide property with the given key and type or creates a new property if not found\
Tenant wide properties are properties where the user name is not set

[setUserName(userName, \[tenantName\])](svyProperties-API-Documentation.md#setusername-username-tenantname)

Sets the user and tenant name for the logged in user\
Both are used in all convenience methods to get or set properties for the user or the tenant\
When svySecurity is used, this is called automatically after login

[setUserProperty(propertyKey, propertyType, value)](svyProperties-API-Documentation.md#setuserproperty-propertykey-propertytype-value-property) ⇒ [`Property`](svyProperties-API-Documentation.md#property)

Sets the given value to the user property with the given key and type or creates a new property if not found

### Property

* [Property](svyProperties-API-Documentation.md#property)
  * [.deleteProperty()](svyProperties-API-Documentation.md#property.deleteproperty-boolean) ⇒ `Boolean`
  * [.getDisplayName()](svyProperties-API-Documentation.md#property.getdisplayname-string) ⇒ `String`
  * [.getPropertyUUID()](svyProperties-API-Documentation.md#property.getpropertyuuid-uuid) ⇒ `UUID`
  * [.getPropertyValue()](svyProperties-API-Documentation.md#property.getpropertyvalue-string) ⇒ `String`
  * [.getTenantName()](svyProperties-API-Documentation.md#property.gettenantname-string) ⇒ `String`
  * [.getUserName()](svyProperties-API-Documentation.md#property.getusername-string) ⇒ `String`
  * [.setDisplayName()](svyProperties-API-Documentation.md#property.setdisplayname-property) ⇒ [`Property`](svyProperties-API-Documentation.md#property)
  * [.setPropertyValue(propertyValue)](svyProperties-API-Documentation.md#property.setpropertyvalue-propertyvalue-property) ⇒ [`Property`](svyProperties-API-Documentation.md#property)
  * [new Property(record)](svyProperties-API-Documentation.md#new-property-record)

***

#### property.deleteProperty() ⇒ `Boolean`

Immediately and permanently deletes this property.

**Returns**: `Boolean` - true if property could be deleted

**Note**: USE WITH CAUTION! There is no undo for this operation.

***

#### property.getDisplayName() ⇒ `String`

Gets the display name for this property.

**Returns**: `String` - The property value of this property. Can be null if a display name is not set.

***

#### property.getPropertyUUID() ⇒ `UUID`

Gets the property uuid for this property.

**Returns**: `UUID` - The property uuid of this property.

***

#### property.getPropertyValue() ⇒ `String`

Gets the property value for this property.

**Returns**: `String` - The property value of this property. Can be null if a property value is not set.

***

#### property.getTenantName() ⇒ `String`

Gets the tenant name for this property.

**Returns**: `String` - The property value of this property. Can be null if a display name is not set.

***

#### property.getUserName() ⇒ `String`

Gets the user name for this property.

**Returns**: `String` - The property value of this property. Can be null if a display name is not set.

***

#### property.setDisplayName() ⇒ [`Property`](svyProperties-API-Documentation.md#property)

Sets the property display name for this property.

**Returns**: [`Property`](svyProperties-API-Documentation.md#property) - The property uuid of this property.

***

#### property.setPropertyValue(propertyValue) ⇒ [`Property`](svyProperties-API-Documentation.md#property)

Sets the property value for this property.

**Returns**: [`Property`](svyProperties-API-Documentation.md#property) - This property for call-chaining support.

| Param         | Type     |
| ------------- | -------- |
| propertyValue | `String` |

***

#### new Property(record)

| Param  | Type                              |
| ------ | --------------------------------- |
| record | `[ 'JSRecord' ].<svy_properties>` |

***

### changeExternalDBTransactionSupportFlag(mustSupportExternalTransactions)

Use this method to change the behavior of the svyProperties module with respect to DB transactions.

If the flag is set to false (default) then when saving or deleting security-related records if an external DB transaction is detected the operation will fail. If the flag is set to true then when saving or deleting security-related records the module will start/commit a DB transaction only if an external DB transaction is not detected. On exceptions any DB transaction will be rolled back regardless if it is started internally or externally (exceptions will be propagated to the external transaction so callers will be able to react on them accordingly)

**Note**: If using external DB transactions then callers are responsible for refreshing the state of security-related objects upon transaction rollbacks which occur after successful calls to the svyProperties API.

| Param                           | Type      | Description                                                 |
| ------------------------------- | --------- | ----------------------------------------------------------- |
| mustSupportExternalTransactions | `Boolean` | The value for the supportExternalDBTransaction flag to set. |

***

### deleteProperty(property) ⇒ `Boolean`

Immediately and permanently deletes the specified property.

**Returns**: `Boolean` - False if property could not be deleted.

**Note**: USE WITH CAUTION! There is no undo for this operation.

| Param    | Type                                                                            | Description                                                                         |
| -------- | ------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| property | [`Property`](svyProperties-API-Documentation.md#property) \| `UUID` \| `String` | The property object or the UUID (UUID or UUID as String) of the property to delete. |

***

### getGlobalProperty(propertyKey, propertyType) ⇒ [`Property`](svyProperties-API-Documentation.md#property)

Returns the global property with the given key and type\
Global properties are properties where the tenant and user name is not set

**Returns**: [`Property`](svyProperties-API-Documentation.md#property) - the property found or null if not found

| Param        | Type     | Description                                    |
| ------------ | -------- | ---------------------------------------------- |
| propertyKey  | `String` | the identifier for the property                |
| propertyType | `String` | the type of property (typically an enum value) |

***

### getGlobalPropertyValue(propertyKey, propertyType) ⇒ `String`

Returns the value of the global property with the given key and type\
Global properties are properties where the tenant and user name is not set

**Returns**: `String` - the value of the property found or null if not found

| Param        | Type     | Description                                    |
| ------------ | -------- | ---------------------------------------------- |
| propertyKey  | `String` | the identifier for the property                |
| propertyType | `String` | the type of property (typically an enum value) |

***

### getProperties(propertyKey, \[propertyType], \[tenantName], \[userName]) ⇒ [`[ 'Array' ].<Property>`](svyProperties-API-Documentation.md#property)

Returns all properties with the given key and type, optional tenant and user name\


If tenantName is not provided, it will not be queried; if a null value is provided, only global properties are returned\
If userName is not provided, it will not be queried; if a null value is provided, only tenant wide properties are returned\


| Param           | Type     | Description                                  |
| --------------- | -------- | -------------------------------------------- |
| propertyKey     | `String` | can contain % placeholders for like searches |
| \[propertyType] | `String` | has to match exactly                         |
| \[tenantName]   | `String` | has to match exactly                         |
| \[userName]     | `String` | has to match exactly                         |

***

### getPropertiesByType(propertyType, \[tenantName], \[userName]) ⇒ [`[ 'Array' ].<Property>`](svyProperties-API-Documentation.md#property)

Returns all properties of the given type, optional tenant and user name\


If tenantName is not provided, it will not be queried; if a null value is provided, only global properties are returned\
If userName is not provided, it will not be queried; if a null value is provided, only tenant wide properties are returned\


| Param         | Type     | Description          |
| ------------- | -------- | -------------------- |
| propertyType  | `String` | has to match exactly |
| \[tenantName] | `String` | has to match exactly |
| \[userName]   | `String` | has to match exactly |

***

### getProperty(propertyKey, propertyType, \[tenantName], \[userName]) ⇒ [`Property`](svyProperties-API-Documentation.md#property)

Returns the property with the given key and type or null if not found\
All parameters given need to match exactly

**Returns**: [`Property`](svyProperties-API-Documentation.md#property) - the property found or null if not found

| Param         | Type     | Description                                       |
| ------------- | -------- | ------------------------------------------------- |
| propertyKey   | `String` | the identifier for the property                   |
| propertyType  | `String` | the type of property (typically an enum value)    |
| \[tenantName] | `String` | the tenant name for which this property is stored |
| \[userName]   | `String` | the user name for which this property is stored   |

***

### getTenantProperty(propertyKey, propertyType) ⇒ [`Property`](svyProperties-API-Documentation.md#property)

Returns the tenant wide property with the given key and type for the tenant set via `setUserName()`\
Tenant wide properties are properties where the user name is not set

**Returns**: [`Property`](svyProperties-API-Documentation.md#property) - the property found or null if not found

| Param        | Type     | Description                                    |
| ------------ | -------- | ---------------------------------------------- |
| propertyKey  | `String` | the identifier for the property                |
| propertyType | `String` | the type of property (typically an enum value) |

***

### getTenantPropertyValue(propertyKey, propertyType) ⇒ `String`

Returns the value of the tenant wide property with the given key and type for the tenant set via `setUserName()`\
Tenant wide properties are properties where the user name is not set

**Returns**: `String` - the value of the property found or null if not found

| Param        | Type     | Description                                    |
| ------------ | -------- | ---------------------------------------------- |
| propertyKey  | `String` | the identifier for the property                |
| propertyType | `String` | the type of property (typically an enum value) |

***

### getUserProperty(propertyKey, propertyType) ⇒ [`Property`](svyProperties-API-Documentation.md#property)

Returns the property with the given key and type for the user set via `setUserName()`

**Returns**: [`Property`](svyProperties-API-Documentation.md#property) - the property found or null if not found

| Param        | Type     | Description                                    |
| ------------ | -------- | ---------------------------------------------- |
| propertyKey  | `String` | the identifier for the property                |
| propertyType | `String` | the type of property (typically an enum value) |

**Example**

```js
function onShow(firstShow, event) {
	var propertyKey = application.getSolutionName() + "-" + controller.getName() + "-" + elements.table.getName();
	var columnState = scopes.svyProperties.getUserProperty(propertyKey, 'table-state');
	
	// restore the ng-grid state 
	if (columnState) elements.table.restoreColumnState(columnState.getPropertyValue());
}
```

***

### getUserPropertyValue(propertyKey, propertyType) ⇒ `String`

Returns the value of the property with the given key and type for the user set via `setUserName()`

**Returns**: `String` - the value of the property found or null if not found

| Param        | Type     | Description                                    |
| ------------ | -------- | ---------------------------------------------- |
| propertyKey  | `String` | the identifier for the property                |
| propertyType | `String` | the type of property (typically an enum value) |

**Example**

```js
function onShow(firstShow, event) {
	var propertyKey = application.getSolutionName() + "-" + controller.getName() + "-" + elements.table.getName();
	var columnState = scopes.svyProperties.getUserPropertyValue(propertyKey, 'table-state');
	
	// restore the ng-grid state 
	if (columnState) elements.table.restoreColumnState(columnState);
}
```

***

### getVersion() ⇒ `String`

Gets the version of this module

**Returns**: `String` - the version of the module using the format Major.Minor.Revision

***

### setGlobalProperty(propertyKey, propertyType, value) ⇒ [`Property`](svyProperties-API-Documentation.md#property)

Sets the given value to the global property with the given key and type or creates a new property if not found\
Global properties are properties where the tenant and user name is not set

| Param        | Type     | Description                                    |
| ------------ | -------- | ---------------------------------------------- |
| propertyKey  | `String` | the identifier for the property                |
| propertyType | `String` | the type of property (typically an enum value) |
| value        | `String` | the string value of the property               |

***

### setProperty(propertyKey, propertyType, value, userName, tenantName) ⇒ [`Property`](svyProperties-API-Documentation.md#property)

Sets the given value to the property with the given key and type or creates a new property if not found

| Param        | Type     | Description                                       |
| ------------ | -------- | ------------------------------------------------- |
| propertyKey  | `String` | the identifier for the property                   |
| propertyType | `String` | the type of property (typically an enum value)    |
| value        | `String` | the string value of the property                  |
| userName     | `String` | the user name for which this property is stored   |
| tenantName   | `String` | the tenant name for which this property is stored |

***

### setTenantProperty(propertyKey, propertyType, value) ⇒ [`Property`](svyProperties-API-Documentation.md#property)

Sets the given value to the tenant wide property with the given key and type or creates a new property if not found\
Tenant wide properties are properties where the user name is not set

| Param        | Type     | Description                                    |
| ------------ | -------- | ---------------------------------------------- |
| propertyKey  | `String` | the identifier for the property                |
| propertyType | `String` | the type of property (typically an enum value) |
| value        | `String` | the string value of the property               |

***

### setUserName(userName, \[tenantName])

Sets the user and tenant name for the logged in user\
Both are used in all convenience methods to get or set properties for the user or the tenant\
When svySecurity is used, this is called automatically after login

| Param         | Type     | Description                                                              |
| ------------- | -------- | ------------------------------------------------------------------------ |
| userName      | `String` | the name of the active user for which user related properties are stored |
| \[tenantName] | `String` | the name of the tenant of the active user                                |

**Example**

```js
function onSolutionOpen(arg, queryParams) {
  // don't set the tenant if the solution doesn't support multi-tenancy
  // scopes.svyProperties.setUserName(loggedUserName);

  scopes.svyProperties.setUserName(loggedUniqueUserName, loggedUniqueTenantName);
}
```

***

### setUserProperty(propertyKey, propertyType, value) ⇒ [`Property`](svyProperties-API-Documentation.md#property)

Sets the given value to the user property with the given key and type or creates a new property if not found

| Param        | Type     | Description                                    |
| ------------ | -------- | ---------------------------------------------- |
| propertyKey  | `String` | the identifier for the property                |
| propertyType | `String` | the type of property (typically an enum value) |
| value        | `String` | the string value of the property               |

**Example**

```js
//persist the state of the NG Grid as user property  
function onColumnStateChanged(columnState) {
	 var propertyNameSpace = application.getSolutionName() + "-" + controller.getName() + "." + elements.table.getName();	
	 scopes.svyProperties.setUserProperty(propertyNameSpace, 'table-state', columnState);
}
```

***
