---
title: 'Mindkey Integrations API'
sidebar_position: 2
---

# Integrations API

⛏Builds the connection between MindKey and the customer’s existing applications.

# API Access Prerequisites

Before you can start using the MindKey Integrations API, you need to ensure that you have the following prerequisites in place:

1. **Local Certificate and API Key:** Contact your primary consultant at MindKey to obtain a local certificate and API key required for authentication.
2. **List of IP Numbers: **Provide MindKey with a list of IP numbers that will be accessing the API.
3. **GitHub Account:** If you wish to access API demo samples, share your GitHub account(s) with the MindKey team.

# Recommended Tools

To work effectively with the MindKey Integrations API, it is recommended to use the following tools:

1. **Postman: **Postman is a popular API development and testing tool that provides a user-friendly interface for making API requests.
2. **PowerShell:** PowerShell is a powerful scripting language that can be used to automate API interactions and perform various tasks.
3. **Git:** Git is a version control system that can be useful for managing your code and collaborating with others.

# Authentication

The authentication process for the MindKey API requires a certificate and an API key. MindKey provides a local certificate that you can use on your local development machine. Additionally, an API key is provided to add an extra layer of security. The API key, along with the certificate, serves as the authenticator for accessing the API.

> 📘 Note:
>
> - You need to provide MindKey with the list of IP numbers that will be accessing the API to ensure secure access.
> - Please note that the MindKey API does not support customizable authentication.

# Integration Samples and PowerShell Module

To help you get started, MindKey provides integration samples in both PowerShell and C#. These samples illustrate how to use the API effectively. In the case of PowerShell, MindKey has developed a shared module that simplifies making requests to the MindKey API. You can request these samples and the PowerShell module from the MindKey team.

# Quick Start Guide for Your First Request

To help you get started quickly, here's an example in PowerShell that demonstrates how to obtain a list of employees in your MindKey:

# Modules

Download the PowerShell modules from the integrations-shared repository to successfully complete the following steps.

In PowerShell, import the MindKeyRest module with the following command:

```
Import-Module (PATH-TO-MindKey-Rest.psm1) -Force
```

Connect to the API using the Connect-MindKeyRest method provided by the module:

```
Connect-MindKeyRest "integration.mindkey.com" -CertificateThumbprint THUMBPRINT -CustomerId CUSTOMERID
```

> 📘 Note:
>
> Replace THUMBPRINT and CUSTOMERID with the appropriate values provided by MindKey.

Next, set up the request body by specifying the columns from the employee table that you want to include:

```
$body = @{
    columns = "EmployeeId, Name_FullName, ExternalReference, Address_Street, Address_ZipPostalCode, Address_City, Address_CountryRegion, SeniorityDate, PrivateMobilePhoneNumber_FullPhoneNumber, HomePhoneNumber_FullPhoneNumber, Email"}
```

Now you are ready to make your first request. Use the Invoke-MindKeyRestPost method from the shared module:

```
$Employees = Invoke-MindKeyRestPost "employees/find" -InputObject $body
```

The variable $Employees now contains employee objects for each employee in your MindKey.

You can display the names of all employees using the following code:

```
foreach ($Employee in $Employees) {
    $Employee.Name_FullName}
```

For more examples in PowerShell or C#, you can explore the integration-samples repository.

# CRUD Operations

The MindKey Integrations API supports CRUD (Create, Read, Update, Delete) operations for various controllers. Here are examples of how to perform each operation:

## Insert

To insert a new record in a specific controller, you can use the following syntax:

```
$Controller = New-Object NameSpaceTarget.ControllerInsertTarget
$Controller.ControllerId = "ControllerId"
$Controller.ControllerField1 = "Controller Field1 value"

try {
    $insertedController = Invoke-MindKeyRestPost "controllers/insert" -InputObject $Controller
} catch {
    Add-Error "A critical error occurred while inserting controller: $($_.Exception)"
}
```

The $insertedController variable will contain the newly inserted controller record with all its fields.

## Update

To update an existing record in a specific controller, use the following syntax:

```
$Controller = New-Object NameSpaceTarget.ControllerUpdateTarget
$Controller.ControllerField1 = "Controller Field1 value update"

try {
    Invoke-MindKeyRestPost "controllers/update?ControllerId="+$controllerIdValue -InputObject $Controller
} catch {
    Add-Error "A critical error occurred while updating controller: $($_.Exception)"}

```

## Delete

To delete a record from a specific controller, use the following syntax:

```
try {
    Invoke-MindKeyRestPost "controllers/delete?ControllerId="+$controllerIdValue
} catch {
    Add-Error "A critical error occurred while deleting controller: $($_.Exception)
}
```

## Write

The write operation either inserts or updates a record in the specified controller, depending on whether the key value already exists. Here's an example:

```
$Controller = New-Object NameSpaceTarget.ControllerWriteTarget
$Controller.ControllerId = "ControllerId"
$Controller.ControllerField1 = "Controller Field1 value"

try {
    Invoke-MindKeyRestPost "controllers/write?ControllerId="+$Controller.ControllerId -InputObject $Controller
} catch {
    Add-Error "A critical error occurred while writing controller: $($_.Exception)"
}

```

## Find

To search for records in a controller based on specific conditions, use the find operation. Here's an example:

```
try {
    $ControllerId = 'controllerId'
    Add-Info ("Find Controller: " + $ControllerId)

    # Setup search condition
    $body = @{
        searchCondition = @(
            @{ column = "ControllerId"; value = $ControllerId }
        )
    }

    $Result = Invoke-MindKeyRestPost "controllers/find" -InputObject $body

    if (!$Result) {
        Add-Info ("No match for criteria: ControllerId = " + $ControllerId)
    }
} catch {
    Add-Error "A critical error occurred while getting controller: $($_.Exception)"
}
```

# Logical Operators (AND/OR) and Condition Operators

The MindKey Integrations API allows you to use logical operators (AND/OR) and condition operators to modify search conditions. Here are examples:

## Logical Operators

```
$body = @{
    columns = "ControllerId, Controller_Name"
    searchCondition =  @(
        @{ column = "ControllerId"; value = $ControllerId1 },
        @{ column = "ControllerId"; value = $ControllerId2; logicalOperator = "OR" }
    )
}

$Controllers = Invoke-MindKeyRestPost "controllers/find" -InputObject $body

```

## Condition Operators

```
$body = @{
    columns = "ControllerId, Controller_Name"
    searchCondition =  @(
        @{ column = "ControllerId"; value = "100"; conditionOperator = "NOTEQUAL" }
    )
}

$Controllers = Invoke-MindKeyRestPost "controllers/find" -InputObject $body

```

# Employee Position Mode

You can add a position mode to retrieve connected position Versions records of different types. The position Mode can be one of the following:

1. **CurrentOuterJoin:** Returns all employees and includes positionVersion fields if available.
2. **CurrentInnerJoin:** Returns employees with positionVersion records.
3. T**erminatedInnerJoin:** Returns terminated employees since a specified date (mandatory customSearchCondition: FromDate).
4. **FutureInnerJoin:** Returns employees with future employment from a specified date (mandatory customSearchCondition: FromDate).

> 📘 Note:
>
> To specify the position mode, use the positionMode parameter along with the desired positionVersion fields.

# User-Defined Fields

To retrieve attached columns for user-defined fields on the employee record, add **userDefinedColumns = "UserDefinedColumnName"** to the employee search. The returned user-defined fields will have names like **$Employee.** UserDefinedColumn_UserDefinedColumnName.

> 📘 Note:
>
> Please note that renaming fields used in the API can cause scripts to fail as the field names and selections will be incorrect.

# Integration with Leave, Time Tracking, and Mileage

If you want to integrate leave, time tracking, or mileage functionalities, MindKey provides specific records for these integrations: LeaveIntegration, TimeTrackingIntegration, and MileageIntegration. These records are created when leave, time tracking or mileage transactions are approved in MindKey.

The integration records have status fields specific to API integration. The status values can be:

1: Ready (ready to export transaction)  
2: Found (export job has read the transaction)  
3: Updated (export has finished updating the transaction)

> 📘 Note:
>
> You can read these integration records to determine the status of your integration.

# Logging Results to MindKey

To log integration results in MindKey, you can use the syslogs/insert endpoint. Here's an example of an object that can be posted to the syslog:

```
$SysLog.MessageText = {{Log_As_String}}
$SysLog.TransDateTime = {{Current_DateTime}}
$SysLog.HostName = {{Machine_Name / Ip_Address}}
$SysLog.UserName = {{User_Running_Integration}}
$SysLog.JobName = {{Integration_Name}}
$SysLog.Application = 'MindKey Integration Service'

if (Get-ErrorCount -ge 1) {
    $SysLog.Status = 3
} else {
    if (Get-WarningCount -ge 1) {
        $SysLog.Status = 2
    } else {
        $SysLog.Status = 1
    }
}

# Invoke-MindKeyRestPost to post the SysLog object to the syslog
```

The above example illustrates three possible statuses:

1: Success  
2: Warning  
3: Error

It is recommended to set up notifications based on these statuses in MindKey to stay informed about integration results.

# HTTP Headers for MindKey REST Requests

When making REST requests to the MindKey API, you may need to include specific HTTP headers. Here are the headers you may encounter:

1. **Accept:** This header indicates the formats the client accepts for the response. The MindKey API currently supports JSON format, so the Accept header should be set to application/json.
2. **Content-Type: **This header specifies the format of the request body provided by the client. For all POST and PUT operations, the Content-Type should be set to application/json.
3. **TimeZone:** This custom header should be specified when a POST operation contains date time values passed as UTC. The TimeZone header specifies the time zone, such as "Romance Standard Time".
4. **SystemUser:** This custom header can be used to specify a username for tracking modifications made in MindKey. If not set, it defaults to "MindKey Service".
5. **ApplicationName: **This custom header allows you to provide the name of the application making the API request.
6. **Culture: **This custom header can be used to specify the culture for the response. If not set, it defaults to "en-US".
7. **Language:** This custom header allows you to specify the language in which you want to receive the response. If not set or set to an unsupported language, it defaults to "en-US".

# Controllers:

The MindKey API provides various controllers that allow you to access different data sets. To obtain a list of all controllers, you can make a GET request to the following endpoint:

```
{{api_root}}/{{customer_id}}/system/controllers
```

Replace {{api_root}} with integration.mindkey.com/api and {{customer_id}} with the appropriate customer ID.

For more information about an individual controller, you can retrieve its metadata by calling:

```
{{api_root}}/{{customer_id}}/{{controller_name}}/metadata
```

This will provide you with the data model for the selected controller, including available request methods, filters, and possible fields in a JSON post body.

It is recommended to refer to the metadata for controllers to understand their structure and available options.

# HTTP Status Codes and Errors

The MindKey Integrations API uses standard HTTP status codes to indicate the success or failure of requests. Here are some common status codes you may encounter:

**200:** The request was successful.  
**404:** The requested resource could not be found.  
**405:** The HTTP method used is not allowed for the endpoint.  
**500:** An error occurred on the MindKey API server.

When handling errors, it's essential to consider the appropriate HTTP status code and any error messages provided in the response.

For obtaining logging-in information click [here:](https://dash.readme.com/project/pena-team-sandbox/v2.0/docs/system-api)
