---
description: "Error Messages (Visual FoxPro ODBC Driver)"
title: "Error Messages (Visual FoxPro ODBC Driver) | Microsoft Docs"
ms.custom: ""
ms.date: "01/19/2017"
ms.service: sql
ms.reviewer: ""
ms.subservice: connectivity
ms.topic: conceptual
helpviewer_keywords: 
  - "error messages [ODBC], Visual FoxPro ODBC driver"
  - "Visual FoxPro ODBC driver [ODBC], error messages"
  - "SQLSTATE [ODBC]"
  - "FoxPro ODBC driver [ODBC], error messages"
ms.assetid: 58ea9734-4edf-44da-ba80-938aa7b340e4
author: David-Engel
ms.author: v-davidengel
---
# Error Messages (Visual FoxPro ODBC Driver)
When an error occurs, the Visual FoxPro driver returns the following information:  
  
-   The native error number and error message text  
  
-   The SQLSTATE (an ODBC error code) and error message text  
  
 You access this error information by calling [SQLError](../../odbc/microsoft/sqlerror-visual-foxpro-odbc-driver.md).  
  
## Native Errors  
 For errors that occur in the data source, the Visual FoxPro driver returns the native error number and error message text. For a list of native error numbers, see [Visual FoxPro ODBC Driver Native Error Messages](../../odbc/microsoft/visual-foxpro-odbc-driver-native-error-messages.md).  
  
## SQLSTATE (ODBC Error Codes)  
 For errors that are detected and returned by the Visual FoxPro driver, the driver maps the returned native error number to the appropriate SQLSTATE. If a native error number does not have an ODBC error code to map to, the Visual FoxPro driver returns SQLSTATE S1000 (General error).  
  
 For a list of SQLSTATE values generated by the Visual FoxPro ODBC Driver for corresponding Visual FoxPro errors, see [ODBC Error Codes](../../odbc/microsoft/odbc-error-codes-visual-foxpro-odbc-driver.md).  
  
## Syntax  
 Error messages have the following format:  
  
 **[** *vendor* **][** *ODBC_component* **]** *error_message*  
  
 The prefixes in brackets ([ ]) identify the source of the error as defined in the following table.  
  
|Data source|Prefix|Value|  
|-----------------|------------|-----------|  
|Driver Manager|[vendor]<br />[ODBC_component]<br />[data_source]|[Microsoft]<br />[ODBC Driver Manager]<br />N/A|  
|Visual FoxPro driver|vendor]<br />[ODBC_component]<br />[data_source]|[Microsoft]<br />[ODBC Visual FoxPro driver]<br />N/A|  
  
 For example, if the Visual FoxPro ODBC Driver could not find the file employee.dbf, it might return the following error message:  
  
 "[*Microsoft*][*ODBC Visual FoxPro Driver*]File 'employee.dbf' does not exist"
