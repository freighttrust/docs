# Getting started

## How to Build

The generated code uses the Newtonsoft Json.NET NuGet Package. If the automatic NuGet package restore
is enabled, these dependencies will be installed automatically. Therefore,
you will need internet access for build.

"This library requires Visual Studio 2017 for compilation."
1. Open the solution (LoopBackApplication.sln) file.
2. Invoke the build process using `Ctrl+Shift+B` shortcut key or using the `Build` menu as shown below.

![Building SDK using Visual Studio](https://apidocs.io/illustration/cs?step=buildSDK&workspaceFolder=LoopBack%20Application-CSharp&workspaceName=LoopBackApplication&projectName=LoopBackApplication.Standard)

## How to Use

The build process generates a portable class library, which can be used like a normal class library. The generated library is compatible with Windows Forms, Windows RT, Windows Phone 8,
Silverlight 5, Xamarin iOS, Xamarin Android and Mono. More information on how to use can be found at the [MSDN Portable Class Libraries documentation](http://msdn.microsoft.com/en-us/library/vstudio/gg597391%28v=vs.100%29.aspx).

The following section explains how to use the LoopBackApplication library in a new console project.

### 1. Starting a new project

For starting a new project, right click on the current solution from the *solution explorer* and choose  ``` Add -> New Project ```.

![Add a new project in the existing solution using Visual Studio](https://apidocs.io/illustration/cs?step=addProject&workspaceFolder=LoopBack%20Application-CSharp&workspaceName=LoopBackApplication&projectName=LoopBackApplication.Standard)

Next, choose "Console Application", provide a ``` TestConsoleProject ``` as the project name and click ``` OK ```.

![Create a new console project using Visual Studio](https://apidocs.io/illustration/cs?step=createProject&workspaceFolder=LoopBack%20Application-CSharp&workspaceName=LoopBackApplication&projectName=LoopBackApplication.Standard)

### 2. Set as startup project

The new console project is the entry point for the eventual execution. This requires us to set the ``` TestConsoleProject ``` as the start-up project. To do this, right-click on the  ``` TestConsoleProject ``` and choose  ``` Set as StartUp Project ``` form the context menu.

![Set the new cosole project as the start up project](https://apidocs.io/illustration/cs?step=setStartup&workspaceFolder=LoopBack%20Application-CSharp&workspaceName=LoopBackApplication&projectName=LoopBackApplication.Standard)

### 3. Add reference of the library project

In order to use the LoopBackApplication library in the new project, first we must add a projet reference to the ``` TestConsoleProject ```. First, right click on the ``` References ``` node in the *solution explorer* and click ``` Add Reference... ```.

![Open references of the TestConsoleProject](https://apidocs.io/illustration/cs?step=addReference&workspaceFolder=LoopBack%20Application-CSharp&workspaceName=LoopBackApplication&projectName=LoopBackApplication.Standard)

Next, a window will be displayed where we must set the ``` checkbox ``` on ``` LoopBackApplication.Standard ``` and click ``` OK ```. By doing this, we have added a reference of the ```LoopBackApplication.Standard``` project into the new ``` TestConsoleProject ```.

![Add a reference to the TestConsoleProject](https://apidocs.io/illustration/cs?step=createReference&workspaceFolder=LoopBack%20Application-CSharp&workspaceName=LoopBackApplication&projectName=LoopBackApplication.Standard)

### 4. Write sample code

Once the ``` TestConsoleProject ``` is created, a file named ``` Program.cs ``` will be visible in the *solution explorer* with an empty ``` Main ``` method. This is the entry point for the execution of the entire solution.
Here, you can add code to initialize the client library and acquire the instance of a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

![Add a reference to the TestConsoleProject](https://apidocs.io/illustration/cs?step=addCode&workspaceFolder=LoopBack%20Application-CSharp&workspaceName=LoopBackApplication&projectName=LoopBackApplication.Standard)

## How to Test

The generated SDK also contain one or more Tests, which are contained in the Tests project.
In order to invoke these test cases, you will need *NUnit 3.0 Test Adapter Extension for Visual Studio*.
Once the SDK is complied, the test cases should appear in the Test Explorer window.
Here, you can click *Run All* to execute these test cases.

## Initialization

### 

API client can be initialized as following.

```csharp

LoopBackApplicationClient client = new LoopBackApplicationClient();
```



# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [SystemController](#system_controller)
* [DriverController](#driver_controller)
* [ShipperController](#shipper_controller)
* [CarrierController](#carrier_controller)
* [ReceiverController](#receiver_controller)
* [DriverPassportController](#driver_passport_controller)
* [AddDriverController](#add_driver_controller)
* [CreateDriverPassportController](#create_driver_passport_controller)
* [UpdateDriverPassportController](#update_driver_passport_controller)
* [ChangeDriverCarrierController](#change_driver_carrier_controller)
* [RemoveDriverCarrierController](#remove_driver_carrier_controller)
* [DailyLogDefectsReportController](#daily_log_defects_report_controller)
* [DailyLogController](#daily_log_controller)
* [DriverDailyLogTickController](#driver_daily_log_tick_controller)
* [BillOfLadingController](#bill_of_lading_controller)
* [DetentionController](#detention_controller)
* [QuoteController](#quote_controller)
* [LoadController](#load_controller)
* [AssignDriverToLoadController](#assign_driver_to_load_controller)
* [OriginArrivalController](#origin_arrival_controller)
* [LoadPickupController](#load_pickup_controller)
* [DestinationArrivalController](#destination_arrival_controller)
* [LoadDropOffController](#load_drop_off_controller)
* [ListLoadController](#list_load_controller)
* [SubmitQuoteController](#submit_quote_controller)
* [AcceptQuoteController](#accept_quote_controller)

## <a name="system_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.SystemController") SystemController

### Get singleton instance

The singleton instance of the ``` SystemController ``` class can be accessed from the API Client.

```csharp
SystemController system = client.System;
```

### <a name="get_system_ping"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.SystemController.GetSystemPing") GetSystemPing

> *Tags:*  ``` Skips Authentication ``` 

> Test the connection to the business network


```csharp
Task<Models.PingResponse> GetSystemPing()
```

#### Example Usage

```csharp

Models.PingResponse result = await system.GetSystemPing();

```


### <a name="get_system_get_all_identities"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.SystemController.GetSystemGetAllIdentities") GetSystemGetAllIdentities

> *Tags:*  ``` Skips Authentication ``` 

> Get all identities from the identity registry


```csharp
Task<dynamic> GetSystemGetAllIdentities()
```

#### Example Usage

```csharp

dynamic result = await system.GetSystemGetAllIdentities();

```


### <a name="get_system_get_identity_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.SystemController.GetSystemGetIdentityByID") GetSystemGetIdentityByID

> *Tags:*  ``` Skips Authentication ``` 

> Get the specified identity from the identity registry


```csharp
Task<dynamic> GetSystemGetIdentityByID(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string id = "id";

dynamic result = await system.GetSystemGetIdentityByID(id);

```


### <a name="create_system_issue_identity"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.SystemController.CreateSystemIssueIdentity") CreateSystemIssueIdentity

> *Tags:*  ``` Skips Authentication ``` 

> Issue an identity to the specified participant


```csharp
Task<Stream> CreateSystemIssueIdentity(Models.IssueIdentityRequest data)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var data = new Models.IssueIdentityRequest();

Stream result = await system.CreateSystemIssueIdentity(data);

```


### <a name="create_system_bind_identity"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.SystemController.CreateSystemBindIdentity") CreateSystemBindIdentity

> *Tags:*  ``` Skips Authentication ``` 

> Bind an identity to the specified participant


```csharp
Task CreateSystemBindIdentity(Models.BindIdentityRequest data)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var data = new Models.BindIdentityRequest();

await system.CreateSystemBindIdentity(data);

```


### <a name="create_system_revoke_identity"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.SystemController.CreateSystemRevokeIdentity") CreateSystemRevokeIdentity

> *Tags:*  ``` Skips Authentication ``` 

> Revoke the specified identity


```csharp
Task CreateSystemRevokeIdentity(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string id = "id";

await system.CreateSystemRevokeIdentity(id);

```


### <a name="get_system_get_all_historian_records"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.SystemController.GetSystemGetAllHistorianRecords") GetSystemGetAllHistorianRecords

> *Tags:*  ``` Skips Authentication ``` 

> Get all Historian Records from the Historian


```csharp
Task<dynamic> GetSystemGetAllHistorianRecords()
```

#### Example Usage

```csharp

dynamic result = await system.GetSystemGetAllHistorianRecords();

```


### <a name="get_system_get_historian_record_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.SystemController.GetSystemGetHistorianRecordByID") GetSystemGetHistorianRecordByID

> *Tags:*  ``` Skips Authentication ``` 

> Get the specified Historian Record from the Historian


```csharp
Task<dynamic> GetSystemGetHistorianRecordByID(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string id = "id";

dynamic result = await system.GetSystemGetHistorianRecordByID(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="driver_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.DriverController") DriverController

### Get singleton instance

The singleton instance of the ``` DriverController ``` class can be accessed from the API Client.

```csharp
DriverController driver = client.Driver;
```

### <a name="get_driver_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DriverController.GetDriverFind") GetDriverFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.Driver>> GetDriverFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.Driver> result = await driver.GetDriverFind(filter);

```


### <a name="create_driver_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DriverController.CreateDriverCreate") CreateDriverCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.Driver> CreateDriverCreate(Models.Driver data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.Driver();

Models.Driver result = await driver.CreateDriverCreate(data);

```


### <a name="get_driver_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DriverController.GetDriverFindById") GetDriverFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.Driver> GetDriverFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.Driver result = await driver.GetDriverFindById(id, filter);

```


### <a name="update_driver_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DriverController.UpdateDriverReplaceById") UpdateDriverReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.Driver> UpdateDriverReplaceById(string id, Models.Driver data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.Driver();

Models.Driver result = await driver.UpdateDriverReplaceById(id, data);

```


### <a name="delete_driver_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DriverController.DeleteDriverDeleteById") DeleteDriverDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteDriverDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await driver.DeleteDriverDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="shipper_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.ShipperController") ShipperController

### Get singleton instance

The singleton instance of the ``` ShipperController ``` class can be accessed from the API Client.

```csharp
ShipperController shipper = client.Shipper;
```

### <a name="get_shipper_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.ShipperController.GetShipperFind") GetShipperFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.Shipper>> GetShipperFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.Shipper> result = await shipper.GetShipperFind(filter);

```


### <a name="create_shipper_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.ShipperController.CreateShipperCreate") CreateShipperCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.Shipper> CreateShipperCreate(Models.Shipper data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.Shipper();

Models.Shipper result = await shipper.CreateShipperCreate(data);

```


### <a name="get_shipper_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.ShipperController.GetShipperFindById") GetShipperFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.Shipper> GetShipperFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.Shipper result = await shipper.GetShipperFindById(id, filter);

```


### <a name="update_shipper_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.ShipperController.UpdateShipperReplaceById") UpdateShipperReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.Shipper> UpdateShipperReplaceById(string id, Models.Shipper data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.Shipper();

Models.Shipper result = await shipper.UpdateShipperReplaceById(id, data);

```


### <a name="delete_shipper_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.ShipperController.DeleteShipperDeleteById") DeleteShipperDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteShipperDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await shipper.DeleteShipperDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="carrier_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.CarrierController") CarrierController

### Get singleton instance

The singleton instance of the ``` CarrierController ``` class can be accessed from the API Client.

```csharp
CarrierController carrier = client.Carrier;
```

### <a name="get_carrier_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.CarrierController.GetCarrierFind") GetCarrierFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.Carrier>> GetCarrierFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.Carrier> result = await carrier.GetCarrierFind(filter);

```


### <a name="create_carrier_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.CarrierController.CreateCarrierCreate") CreateCarrierCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.Carrier> CreateCarrierCreate(Models.Carrier data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.Carrier();

Models.Carrier result = await carrier.CreateCarrierCreate(data);

```


### <a name="get_carrier_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.CarrierController.GetCarrierFindById") GetCarrierFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.Carrier> GetCarrierFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.Carrier result = await carrier.GetCarrierFindById(id, filter);

```


### <a name="update_carrier_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.CarrierController.UpdateCarrierReplaceById") UpdateCarrierReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.Carrier> UpdateCarrierReplaceById(string id, Models.Carrier data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.Carrier();

Models.Carrier result = await carrier.UpdateCarrierReplaceById(id, data);

```


### <a name="delete_carrier_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.CarrierController.DeleteCarrierDeleteById") DeleteCarrierDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteCarrierDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await carrier.DeleteCarrierDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="receiver_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.ReceiverController") ReceiverController

### Get singleton instance

The singleton instance of the ``` ReceiverController ``` class can be accessed from the API Client.

```csharp
ReceiverController receiver = client.Receiver;
```

### <a name="get_receiver_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.ReceiverController.GetReceiverFind") GetReceiverFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.Receiver>> GetReceiverFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.Receiver> result = await receiver.GetReceiverFind(filter);

```


### <a name="create_receiver_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.ReceiverController.CreateReceiverCreate") CreateReceiverCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.Receiver> CreateReceiverCreate(Models.Receiver data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.Receiver();

Models.Receiver result = await receiver.CreateReceiverCreate(data);

```


### <a name="get_receiver_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.ReceiverController.GetReceiverFindById") GetReceiverFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.Receiver> GetReceiverFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.Receiver result = await receiver.GetReceiverFindById(id, filter);

```


### <a name="update_receiver_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.ReceiverController.UpdateReceiverReplaceById") UpdateReceiverReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.Receiver> UpdateReceiverReplaceById(string id, Models.Receiver data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.Receiver();

Models.Receiver result = await receiver.UpdateReceiverReplaceById(id, data);

```


### <a name="delete_receiver_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.ReceiverController.DeleteReceiverDeleteById") DeleteReceiverDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteReceiverDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await receiver.DeleteReceiverDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="driver_passport_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.DriverPassportController") DriverPassportController

### Get singleton instance

The singleton instance of the ``` DriverPassportController ``` class can be accessed from the API Client.

```csharp
DriverPassportController driverPassport = client.DriverPassport;
```

### <a name="get_driver_passport_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DriverPassportController.GetDriverPassportFind") GetDriverPassportFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.DriverPassport>> GetDriverPassportFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.DriverPassport> result = await driverPassport.GetDriverPassportFind(filter);

```


### <a name="create_driver_passport_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DriverPassportController.CreateDriverPassportCreate") CreateDriverPassportCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.DriverPassport> CreateDriverPassportCreate(Models.DriverPassport data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.DriverPassport();

Models.DriverPassport result = await driverPassport.CreateDriverPassportCreate(data);

```


### <a name="get_driver_passport_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DriverPassportController.GetDriverPassportFindById") GetDriverPassportFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.DriverPassport> GetDriverPassportFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.DriverPassport result = await driverPassport.GetDriverPassportFindById(id, filter);

```


### <a name="update_driver_passport_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DriverPassportController.UpdateDriverPassportReplaceById") UpdateDriverPassportReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.DriverPassport> UpdateDriverPassportReplaceById(string id, Models.DriverPassport data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.DriverPassport();

Models.DriverPassport result = await driverPassport.UpdateDriverPassportReplaceById(id, data);

```


### <a name="delete_driver_passport_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DriverPassportController.DeleteDriverPassportDeleteById") DeleteDriverPassportDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteDriverPassportDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await driverPassport.DeleteDriverPassportDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="add_driver_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.AddDriverController") AddDriverController

### Get singleton instance

The singleton instance of the ``` AddDriverController ``` class can be accessed from the API Client.

```csharp
AddDriverController addDriver = client.AddDriver;
```

### <a name="get_add_driver_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.AddDriverController.GetAddDriverFind") GetAddDriverFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.AddDriver>> GetAddDriverFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.AddDriver> result = await addDriver.GetAddDriverFind(filter);

```


### <a name="add_driver_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.AddDriverController.AddDriverCreate") AddDriverCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.AddDriver> AddDriverCreate(Models.AddDriver data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.AddDriver();

Models.AddDriver result = await addDriver.AddDriverCreate(data);

```


### <a name="get_add_driver_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.AddDriverController.GetAddDriverFindById") GetAddDriverFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.AddDriver> GetAddDriverFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.AddDriver result = await addDriver.GetAddDriverFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="create_driver_passport_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.CreateDriverPassportController") CreateDriverPassportController

### Get singleton instance

The singleton instance of the ``` CreateDriverPassportController ``` class can be accessed from the API Client.

```csharp
CreateDriverPassportController createDriverPassport = client.CreateDriverPassport;
```

### <a name="get_create_driver_passport_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.CreateDriverPassportController.GetCreateDriverPassportFind") GetCreateDriverPassportFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.CreateDriverPassport>> GetCreateDriverPassportFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.CreateDriverPassport> result = await createDriverPassport.GetCreateDriverPassportFind(filter);

```


### <a name="create_driver_passport_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.CreateDriverPassportController.CreateDriverPassportCreate") CreateDriverPassportCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.CreateDriverPassport> CreateDriverPassportCreate(Models.CreateDriverPassport data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.CreateDriverPassport();

Models.CreateDriverPassport result = await createDriverPassport.CreateDriverPassportCreate(data);

```


### <a name="get_create_driver_passport_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.CreateDriverPassportController.GetCreateDriverPassportFindById") GetCreateDriverPassportFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.CreateDriverPassport> GetCreateDriverPassportFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.CreateDriverPassport result = await createDriverPassport.GetCreateDriverPassportFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="update_driver_passport_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.UpdateDriverPassportController") UpdateDriverPassportController

### Get singleton instance

The singleton instance of the ``` UpdateDriverPassportController ``` class can be accessed from the API Client.

```csharp
UpdateDriverPassportController updateDriverPassport = client.UpdateDriverPassport;
```

### <a name="get_update_driver_passport_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.UpdateDriverPassportController.GetUpdateDriverPassportFind") GetUpdateDriverPassportFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.UpdateDriverPassport>> GetUpdateDriverPassportFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.UpdateDriverPassport> result = await updateDriverPassport.GetUpdateDriverPassportFind(filter);

```


### <a name="update_driver_passport_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.UpdateDriverPassportController.UpdateDriverPassportCreate") UpdateDriverPassportCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.UpdateDriverPassport> UpdateDriverPassportCreate(Models.UpdateDriverPassport data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.UpdateDriverPassport();

Models.UpdateDriverPassport result = await updateDriverPassport.UpdateDriverPassportCreate(data);

```


### <a name="get_update_driver_passport_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.UpdateDriverPassportController.GetUpdateDriverPassportFindById") GetUpdateDriverPassportFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.UpdateDriverPassport> GetUpdateDriverPassportFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.UpdateDriverPassport result = await updateDriverPassport.GetUpdateDriverPassportFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="change_driver_carrier_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.ChangeDriverCarrierController") ChangeDriverCarrierController

### Get singleton instance

The singleton instance of the ``` ChangeDriverCarrierController ``` class can be accessed from the API Client.

```csharp
ChangeDriverCarrierController changeDriverCarrier = client.ChangeDriverCarrier;
```

### <a name="get_change_driver_carrier_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.ChangeDriverCarrierController.GetChangeDriverCarrierFind") GetChangeDriverCarrierFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ChangeDriverCarrier>> GetChangeDriverCarrierFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ChangeDriverCarrier> result = await changeDriverCarrier.GetChangeDriverCarrierFind(filter);

```


### <a name="change_driver_carrier_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.ChangeDriverCarrierController.ChangeDriverCarrierCreate") ChangeDriverCarrierCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ChangeDriverCarrier> ChangeDriverCarrierCreate(Models.ChangeDriverCarrier data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ChangeDriverCarrier();

Models.ChangeDriverCarrier result = await changeDriverCarrier.ChangeDriverCarrierCreate(data);

```


### <a name="get_change_driver_carrier_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.ChangeDriverCarrierController.GetChangeDriverCarrierFindById") GetChangeDriverCarrierFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ChangeDriverCarrier> GetChangeDriverCarrierFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ChangeDriverCarrier result = await changeDriverCarrier.GetChangeDriverCarrierFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="remove_driver_carrier_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.RemoveDriverCarrierController") RemoveDriverCarrierController

### Get singleton instance

The singleton instance of the ``` RemoveDriverCarrierController ``` class can be accessed from the API Client.

```csharp
RemoveDriverCarrierController removeDriverCarrier = client.RemoveDriverCarrier;
```

### <a name="get_remove_driver_carrier_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.RemoveDriverCarrierController.GetRemoveDriverCarrierFind") GetRemoveDriverCarrierFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.RemoveDriverCarrier>> GetRemoveDriverCarrierFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.RemoveDriverCarrier> result = await removeDriverCarrier.GetRemoveDriverCarrierFind(filter);

```


### <a name="create_remove_driver_carrier_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.RemoveDriverCarrierController.CreateRemoveDriverCarrierCreate") CreateRemoveDriverCarrierCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.RemoveDriverCarrier> CreateRemoveDriverCarrierCreate(Models.RemoveDriverCarrier data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.RemoveDriverCarrier();

Models.RemoveDriverCarrier result = await removeDriverCarrier.CreateRemoveDriverCarrierCreate(data);

```


### <a name="get_remove_driver_carrier_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.RemoveDriverCarrierController.GetRemoveDriverCarrierFindById") GetRemoveDriverCarrierFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.RemoveDriverCarrier> GetRemoveDriverCarrierFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.RemoveDriverCarrier result = await removeDriverCarrier.GetRemoveDriverCarrierFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="daily_log_defects_report_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.DailyLogDefectsReportController") DailyLogDefectsReportController

### Get singleton instance

The singleton instance of the ``` DailyLogDefectsReportController ``` class can be accessed from the API Client.

```csharp
DailyLogDefectsReportController dailyLogDefectsReport = client.DailyLogDefectsReport;
```

### <a name="get_daily_log_defects_report_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DailyLogDefectsReportController.GetDailyLogDefectsReportFind") GetDailyLogDefectsReportFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.DailyLogDefectsReport>> GetDailyLogDefectsReportFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.DailyLogDefectsReport> result = await dailyLogDefectsReport.GetDailyLogDefectsReportFind(filter);

```


### <a name="create_daily_log_defects_report_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DailyLogDefectsReportController.CreateDailyLogDefectsReportCreate") CreateDailyLogDefectsReportCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.DailyLogDefectsReport> CreateDailyLogDefectsReportCreate(Models.DailyLogDefectsReport data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.DailyLogDefectsReport();

Models.DailyLogDefectsReport result = await dailyLogDefectsReport.CreateDailyLogDefectsReportCreate(data);

```


### <a name="get_daily_log_defects_report_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DailyLogDefectsReportController.GetDailyLogDefectsReportFindById") GetDailyLogDefectsReportFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.DailyLogDefectsReport> GetDailyLogDefectsReportFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.DailyLogDefectsReport result = await dailyLogDefectsReport.GetDailyLogDefectsReportFindById(id, filter);

```


### <a name="update_daily_log_defects_report_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DailyLogDefectsReportController.UpdateDailyLogDefectsReportReplaceById") UpdateDailyLogDefectsReportReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.DailyLogDefectsReport> UpdateDailyLogDefectsReportReplaceById(string id, Models.DailyLogDefectsReport data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.DailyLogDefectsReport();

Models.DailyLogDefectsReport result = await dailyLogDefectsReport.UpdateDailyLogDefectsReportReplaceById(id, data);

```


### <a name="delete_daily_log_defects_report_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DailyLogDefectsReportController.DeleteDailyLogDefectsReportDeleteById") DeleteDailyLogDefectsReportDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteDailyLogDefectsReportDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await dailyLogDefectsReport.DeleteDailyLogDefectsReportDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="daily_log_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.DailyLogController") DailyLogController

### Get singleton instance

The singleton instance of the ``` DailyLogController ``` class can be accessed from the API Client.

```csharp
DailyLogController dailyLog = client.DailyLog;
```

### <a name="get_daily_log_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DailyLogController.GetDailyLogFind") GetDailyLogFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.DailyLog>> GetDailyLogFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.DailyLog> result = await dailyLog.GetDailyLogFind(filter);

```


### <a name="create_daily_log_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DailyLogController.CreateDailyLogCreate") CreateDailyLogCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.DailyLog> CreateDailyLogCreate(Models.DailyLog data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.DailyLog();

Models.DailyLog result = await dailyLog.CreateDailyLogCreate(data);

```


### <a name="get_daily_log_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DailyLogController.GetDailyLogFindById") GetDailyLogFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.DailyLog> GetDailyLogFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.DailyLog result = await dailyLog.GetDailyLogFindById(id, filter);

```


### <a name="update_daily_log_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DailyLogController.UpdateDailyLogReplaceById") UpdateDailyLogReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.DailyLog> UpdateDailyLogReplaceById(string id, Models.DailyLog data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.DailyLog();

Models.DailyLog result = await dailyLog.UpdateDailyLogReplaceById(id, data);

```


### <a name="delete_daily_log_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DailyLogController.DeleteDailyLogDeleteById") DeleteDailyLogDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteDailyLogDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await dailyLog.DeleteDailyLogDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="driver_daily_log_tick_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.DriverDailyLogTickController") DriverDailyLogTickController

### Get singleton instance

The singleton instance of the ``` DriverDailyLogTickController ``` class can be accessed from the API Client.

```csharp
DriverDailyLogTickController driverDailyLogTick = client.DriverDailyLogTick;
```

### <a name="get_driver_daily_log_tick_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DriverDailyLogTickController.GetDriverDailyLogTickFind") GetDriverDailyLogTickFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.DriverDailyLogTick>> GetDriverDailyLogTickFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.DriverDailyLogTick> result = await driverDailyLogTick.GetDriverDailyLogTickFind(filter);

```


### <a name="create_driver_daily_log_tick_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DriverDailyLogTickController.CreateDriverDailyLogTickCreate") CreateDriverDailyLogTickCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.DriverDailyLogTick> CreateDriverDailyLogTickCreate(Models.DriverDailyLogTick data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.DriverDailyLogTick();

Models.DriverDailyLogTick result = await driverDailyLogTick.CreateDriverDailyLogTickCreate(data);

```


### <a name="get_driver_daily_log_tick_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DriverDailyLogTickController.GetDriverDailyLogTickFindById") GetDriverDailyLogTickFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.DriverDailyLogTick> GetDriverDailyLogTickFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.DriverDailyLogTick result = await driverDailyLogTick.GetDriverDailyLogTickFindById(id, filter);

```


### <a name="update_driver_daily_log_tick_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DriverDailyLogTickController.UpdateDriverDailyLogTickReplaceById") UpdateDriverDailyLogTickReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.DriverDailyLogTick> UpdateDriverDailyLogTickReplaceById(string id, Models.DriverDailyLogTick data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.DriverDailyLogTick();

Models.DriverDailyLogTick result = await driverDailyLogTick.UpdateDriverDailyLogTickReplaceById(id, data);

```


### <a name="delete_driver_daily_log_tick_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DriverDailyLogTickController.DeleteDriverDailyLogTickDeleteById") DeleteDriverDailyLogTickDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteDriverDailyLogTickDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await driverDailyLogTick.DeleteDriverDailyLogTickDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="bill_of_lading_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.BillOfLadingController") BillOfLadingController

### Get singleton instance

The singleton instance of the ``` BillOfLadingController ``` class can be accessed from the API Client.

```csharp
BillOfLadingController billOfLading = client.BillOfLading;
```

### <a name="get_bill_of_lading_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.BillOfLadingController.GetBillOfLadingFind") GetBillOfLadingFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.BillOfLading>> GetBillOfLadingFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.BillOfLading> result = await billOfLading.GetBillOfLadingFind(filter);

```


### <a name="create_bill_of_lading_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.BillOfLadingController.CreateBillOfLadingCreate") CreateBillOfLadingCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.BillOfLading> CreateBillOfLadingCreate(Models.BillOfLading data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.BillOfLading();

Models.BillOfLading result = await billOfLading.CreateBillOfLadingCreate(data);

```


### <a name="get_bill_of_lading_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.BillOfLadingController.GetBillOfLadingFindById") GetBillOfLadingFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.BillOfLading> GetBillOfLadingFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.BillOfLading result = await billOfLading.GetBillOfLadingFindById(id, filter);

```


### <a name="update_bill_of_lading_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.BillOfLadingController.UpdateBillOfLadingReplaceById") UpdateBillOfLadingReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.BillOfLading> UpdateBillOfLadingReplaceById(string id, Models.BillOfLading data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.BillOfLading();

Models.BillOfLading result = await billOfLading.UpdateBillOfLadingReplaceById(id, data);

```


### <a name="delete_bill_of_lading_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.BillOfLadingController.DeleteBillOfLadingDeleteById") DeleteBillOfLadingDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteBillOfLadingDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await billOfLading.DeleteBillOfLadingDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="detention_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.DetentionController") DetentionController

### Get singleton instance

The singleton instance of the ``` DetentionController ``` class can be accessed from the API Client.

```csharp
DetentionController detention = client.Detention;
```

### <a name="get_detention_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DetentionController.GetDetentionFind") GetDetentionFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.Detention>> GetDetentionFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.Detention> result = await detention.GetDetentionFind(filter);

```


### <a name="create_detention_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DetentionController.CreateDetentionCreate") CreateDetentionCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.Detention> CreateDetentionCreate(Models.Detention data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.Detention();

Models.Detention result = await detention.CreateDetentionCreate(data);

```


### <a name="get_detention_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DetentionController.GetDetentionFindById") GetDetentionFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.Detention> GetDetentionFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.Detention result = await detention.GetDetentionFindById(id, filter);

```


### <a name="update_detention_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DetentionController.UpdateDetentionReplaceById") UpdateDetentionReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.Detention> UpdateDetentionReplaceById(string id, Models.Detention data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.Detention();

Models.Detention result = await detention.UpdateDetentionReplaceById(id, data);

```


### <a name="delete_detention_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DetentionController.DeleteDetentionDeleteById") DeleteDetentionDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteDetentionDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await detention.DeleteDetentionDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="quote_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.QuoteController") QuoteController

### Get singleton instance

The singleton instance of the ``` QuoteController ``` class can be accessed from the API Client.

```csharp
QuoteController quote = client.Quote;
```

### <a name="get_quote_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.QuoteController.GetQuoteFind") GetQuoteFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.Quote>> GetQuoteFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.Quote> result = await quote.GetQuoteFind(filter);

```


### <a name="create_quote_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.QuoteController.CreateQuoteCreate") CreateQuoteCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.Quote> CreateQuoteCreate(Models.Quote data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.Quote();

Models.Quote result = await quote.CreateQuoteCreate(data);

```


### <a name="get_quote_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.QuoteController.GetQuoteFindById") GetQuoteFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.Quote> GetQuoteFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.Quote result = await quote.GetQuoteFindById(id, filter);

```


### <a name="update_quote_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.QuoteController.UpdateQuoteReplaceById") UpdateQuoteReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.Quote> UpdateQuoteReplaceById(string id, Models.Quote data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.Quote();

Models.Quote result = await quote.UpdateQuoteReplaceById(id, data);

```


### <a name="delete_quote_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.QuoteController.DeleteQuoteDeleteById") DeleteQuoteDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteQuoteDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await quote.DeleteQuoteDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="load_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.LoadController") LoadController

### Get singleton instance

The singleton instance of the ``` LoadController ``` class can be accessed from the API Client.

```csharp
LoadController load = client.Load;
```

### <a name="load_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.LoadController.LoadFind") LoadFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.Load>> LoadFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.Load> result = await load.LoadFind(filter);

```


### <a name="create_load_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.LoadController.CreateLoadCreate") CreateLoadCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.Load> CreateLoadCreate(Models.Load data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.Load();

Models.Load result = await load.CreateLoadCreate(data);

```


### <a name="load_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.LoadController.LoadFindById") LoadFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.Load> LoadFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.Load result = await load.LoadFindById(id, filter);

```


### <a name="update_load_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.LoadController.UpdateLoadReplaceById") UpdateLoadReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.Load> UpdateLoadReplaceById(string id, Models.Load data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.Load();

Models.Load result = await load.UpdateLoadReplaceById(id, data);

```


### <a name="delete_load_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.LoadController.DeleteLoadDeleteById") DeleteLoadDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteLoadDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await load.DeleteLoadDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="assign_driver_to_load_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.AssignDriverToLoadController") AssignDriverToLoadController

### Get singleton instance

The singleton instance of the ``` AssignDriverToLoadController ``` class can be accessed from the API Client.

```csharp
AssignDriverToLoadController assignDriverToLoad = client.AssignDriverToLoad;
```

### <a name="get_assign_driver_to_load_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.AssignDriverToLoadController.GetAssignDriverToLoadFind") GetAssignDriverToLoadFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.AssignDriverToLoad>> GetAssignDriverToLoadFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.AssignDriverToLoad> result = await assignDriverToLoad.GetAssignDriverToLoadFind(filter);

```


### <a name="create_assign_driver_to_load_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.AssignDriverToLoadController.CreateAssignDriverToLoadCreate") CreateAssignDriverToLoadCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.AssignDriverToLoad> CreateAssignDriverToLoadCreate(Models.AssignDriverToLoad data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.AssignDriverToLoad();

Models.AssignDriverToLoad result = await assignDriverToLoad.CreateAssignDriverToLoadCreate(data);

```


### <a name="get_assign_driver_to_load_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.AssignDriverToLoadController.GetAssignDriverToLoadFindById") GetAssignDriverToLoadFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.AssignDriverToLoad> GetAssignDriverToLoadFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.AssignDriverToLoad result = await assignDriverToLoad.GetAssignDriverToLoadFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="origin_arrival_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.OriginArrivalController") OriginArrivalController

### Get singleton instance

The singleton instance of the ``` OriginArrivalController ``` class can be accessed from the API Client.

```csharp
OriginArrivalController originArrival = client.OriginArrival;
```

### <a name="get_origin_arrival_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.OriginArrivalController.GetOriginArrivalFind") GetOriginArrivalFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.OriginArrival>> GetOriginArrivalFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.OriginArrival> result = await originArrival.GetOriginArrivalFind(filter);

```


### <a name="create_origin_arrival_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.OriginArrivalController.CreateOriginArrivalCreate") CreateOriginArrivalCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.OriginArrival> CreateOriginArrivalCreate(Models.OriginArrival data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.OriginArrival();

Models.OriginArrival result = await originArrival.CreateOriginArrivalCreate(data);

```


### <a name="get_origin_arrival_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.OriginArrivalController.GetOriginArrivalFindById") GetOriginArrivalFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.OriginArrival> GetOriginArrivalFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.OriginArrival result = await originArrival.GetOriginArrivalFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="load_pickup_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.LoadPickupController") LoadPickupController

### Get singleton instance

The singleton instance of the ``` LoadPickupController ``` class can be accessed from the API Client.

```csharp
LoadPickupController loadPickup = client.LoadPickup;
```

### <a name="load_pickup_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.LoadPickupController.LoadPickupFind") LoadPickupFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.LoadPickup>> LoadPickupFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.LoadPickup> result = await loadPickup.LoadPickupFind(filter);

```


### <a name="create_load_pickup_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.LoadPickupController.CreateLoadPickupCreate") CreateLoadPickupCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.LoadPickup> CreateLoadPickupCreate(Models.LoadPickup data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.LoadPickup();

Models.LoadPickup result = await loadPickup.CreateLoadPickupCreate(data);

```


### <a name="load_pickup_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.LoadPickupController.LoadPickupFindById") LoadPickupFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.LoadPickup> LoadPickupFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.LoadPickup result = await loadPickup.LoadPickupFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="destination_arrival_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.DestinationArrivalController") DestinationArrivalController

### Get singleton instance

The singleton instance of the ``` DestinationArrivalController ``` class can be accessed from the API Client.

```csharp
DestinationArrivalController destinationArrival = client.DestinationArrival;
```

### <a name="get_destination_arrival_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DestinationArrivalController.GetDestinationArrivalFind") GetDestinationArrivalFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.DestinationArrival>> GetDestinationArrivalFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.DestinationArrival> result = await destinationArrival.GetDestinationArrivalFind(filter);

```


### <a name="create_destination_arrival_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DestinationArrivalController.CreateDestinationArrivalCreate") CreateDestinationArrivalCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.DestinationArrival> CreateDestinationArrivalCreate(Models.DestinationArrival data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.DestinationArrival();

Models.DestinationArrival result = await destinationArrival.CreateDestinationArrivalCreate(data);

```


### <a name="get_destination_arrival_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.DestinationArrivalController.GetDestinationArrivalFindById") GetDestinationArrivalFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.DestinationArrival> GetDestinationArrivalFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.DestinationArrival result = await destinationArrival.GetDestinationArrivalFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="load_drop_off_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.LoadDropOffController") LoadDropOffController

### Get singleton instance

The singleton instance of the ``` LoadDropOffController ``` class can be accessed from the API Client.

```csharp
LoadDropOffController loadDropOff = client.LoadDropOff;
```

### <a name="load_drop_off_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.LoadDropOffController.LoadDropOffFind") LoadDropOffFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.LoadDropOff>> LoadDropOffFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.LoadDropOff> result = await loadDropOff.LoadDropOffFind(filter);

```


### <a name="create_load_drop_off_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.LoadDropOffController.CreateLoadDropOffCreate") CreateLoadDropOffCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.LoadDropOff> CreateLoadDropOffCreate(Models.LoadDropOff data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.LoadDropOff();

Models.LoadDropOff result = await loadDropOff.CreateLoadDropOffCreate(data);

```


### <a name="load_drop_off_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.LoadDropOffController.LoadDropOffFindById") LoadDropOffFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.LoadDropOff> LoadDropOffFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.LoadDropOff result = await loadDropOff.LoadDropOffFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="list_load_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.ListLoadController") ListLoadController

### Get singleton instance

The singleton instance of the ``` ListLoadController ``` class can be accessed from the API Client.

```csharp
ListLoadController listLoad = client.ListLoad;
```

### <a name="list_load_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.ListLoadController.ListLoadFind") ListLoadFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ListLoad>> ListLoadFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ListLoad> result = await listLoad.ListLoadFind(filter);

```


### <a name="create_list_load_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.ListLoadController.CreateListLoadCreate") CreateListLoadCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ListLoad> CreateListLoadCreate(Models.ListLoad data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ListLoad();

Models.ListLoad result = await listLoad.CreateListLoadCreate(data);

```


### <a name="list_load_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.ListLoadController.ListLoadFindById") ListLoadFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ListLoad> ListLoadFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ListLoad result = await listLoad.ListLoadFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="submit_quote_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.SubmitQuoteController") SubmitQuoteController

### Get singleton instance

The singleton instance of the ``` SubmitQuoteController ``` class can be accessed from the API Client.

```csharp
SubmitQuoteController submitQuote = client.SubmitQuote;
```

### <a name="get_submit_quote_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.SubmitQuoteController.GetSubmitQuoteFind") GetSubmitQuoteFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.SubmitQuote>> GetSubmitQuoteFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.SubmitQuote> result = await submitQuote.GetSubmitQuoteFind(filter);

```


### <a name="create_submit_quote_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.SubmitQuoteController.CreateSubmitQuoteCreate") CreateSubmitQuoteCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.SubmitQuote> CreateSubmitQuoteCreate(Models.SubmitQuote data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.SubmitQuote();

Models.SubmitQuote result = await submitQuote.CreateSubmitQuoteCreate(data);

```


### <a name="get_submit_quote_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.SubmitQuoteController.GetSubmitQuoteFindById") GetSubmitQuoteFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.SubmitQuote> GetSubmitQuoteFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.SubmitQuote result = await submitQuote.GetSubmitQuoteFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="accept_quote_controller"></a>![Class: ](https://apidocs.io/img/class.png "LoopBackApplication.Standard.Controllers.AcceptQuoteController") AcceptQuoteController

### Get singleton instance

The singleton instance of the ``` AcceptQuoteController ``` class can be accessed from the API Client.

```csharp
AcceptQuoteController acceptQuote = client.AcceptQuote;
```

### <a name="get_accept_quote_find"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.AcceptQuoteController.GetAcceptQuoteFind") GetAcceptQuoteFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.AcceptQuote>> GetAcceptQuoteFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.AcceptQuote> result = await acceptQuote.GetAcceptQuoteFind(filter);

```


### <a name="create_accept_quote_create"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.AcceptQuoteController.CreateAcceptQuoteCreate") CreateAcceptQuoteCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.AcceptQuote> CreateAcceptQuoteCreate(Models.AcceptQuote data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.AcceptQuote();

Models.AcceptQuote result = await acceptQuote.CreateAcceptQuoteCreate(data);

```


### <a name="get_accept_quote_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "LoopBackApplication.Standard.Controllers.AcceptQuoteController.GetAcceptQuoteFindById") GetAcceptQuoteFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.AcceptQuote> GetAcceptQuoteFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.AcceptQuote result = await acceptQuote.GetAcceptQuoteFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)



