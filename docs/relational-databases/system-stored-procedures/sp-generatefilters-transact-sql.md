---
description: "sp_generatefilters (Transact-SQL)"
title: "sp_generatefilters (Transact-SQL) | Microsoft Docs"
ms.custom: ""
ms.date: "03/03/2017"
ms.service: sql
ms.reviewer: ""
ms.subservice: replication
ms.topic: "reference"
dev_langs: 
  - "TSQL"
f1_keywords: 
  - "sp_generatefilters"
  - "sp_generatefilters_TSQL"
helpviewer_keywords: 
  - "sp_generatefilters"
ms.assetid: 0aeb5b7a-89d1-4bd5-a371-c27fa924360a
author: markingmyname
ms.author: maghan
---
# sp_generatefilters (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Creates filters on foreign key tables when a specified table is replicated. This stored procedure is executed at the Publisher on the publication database.  
  
 :::image type="icon" source="../../includes/media/topic-link-icon.svg" border="false"::: [Transact-SQL syntax conventions](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## Syntax  
  
```  
  
sp_generatefilters [ @publication =] 'publication'  
```  
  
## Arguments  
`[ @publication = ] 'publication'`
 Is the name of the publication to be filtered. *publication* is **sysname**, with no default.  
  
## Return Code Values  
 **0** (success) or **1** (failure)  
  
## Remarks  
 **sp_generatefilters** is used in merge replication.  
  
## Permissions  
 Only members of the **sysadmin** fixed server role or the **db_owner** fixed database role can execute **sp_generatefilters**.  
  
## See Also  
 [sp_bindsession &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sp-bindsession-transact-sql.md)   
 [System Stored Procedures &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/system-stored-procedures-transact-sql.md)  
  
  
