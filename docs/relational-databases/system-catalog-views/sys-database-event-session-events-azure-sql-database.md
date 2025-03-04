---
title: "sys.database_event_session_events"
titleSuffix: Azure SQL Database and Azure SQL Managed Instance
description: sys.database_event_session_events (Azure SQL Database and Azure SQL Managed Instance)
author: rwestMSFT
ms.author: randolphwest
ms.date: "04/18/2022"
ms.service: sql
ms.subservice: system-objects
ms.topic: "reference"
dev_langs:
  - "TSQL"
ms.assetid: f4c9eb0a-173c-4c66-8dd8-6f7176b2657f
monikerRange: "=azuresqldb-current||>=sql-server-2016||>=sql-server-linux-2017||=azuresqldb-mi-current"
---
# sys.database_event_session_events (Azure SQL Database and Azure SQL Managed Instance)
[!INCLUDE [sqlserver2016-asdb-asdbmi](../../includes/applies-to-version/sqlserver2016-asdb-asdbmi.md)]

Returns a row for each event in a database-scoped event session. For information on events in *active* database-scoped sessions, see [sys.dm_xe_database_session_events](../system-dynamic-management-views/sys-dm-xe-database-session-events-azure-sql-database.md).

Azure SQL Database supports only [database-scoped sessions](/azure/azure-sql/database/xevent-db-diff-from-svr). Azure SQL Managed Instance supports both database-scoped sessions and [server-scoped sessions](../extended-events/extended-events.md). Server-scoped sessions are recommended for managed instances: learn more in [CREATE EVENT SESSION](../../t-sql/statements/create-event-session-transact-sql.md#code-examples-can-differ-for-azure-sql-database-and-sql-managed-instance).
  
|Column name|Data type|Description|  
|-----------------|---------------|-----------------|  
|event_session_id|**int**|The ID of the event session. Is not nullable.|  
|event_id|**int**|The ID of the event. This ID is unique within an event session object. Is not nullable.|  
|name|**sysname**|The name of the event. Is not nullable.|  
|package|**sysname**|The name of the event package that contains the event. Is not nullable.|  
|module|**sysname**|The name of the module that contains the event. Is not nullable.|  
|predicate|**nvarchar(3000)**|The predicate expression that is applied to the event. Is nullable.|  
|predicate_xml|**nvarchar(3000)**|The XML predicate expression that is applied to the event. Is nullable.|  
  
## Permissions  

Requires the VIEW DATABASE STATE permission.
  
## Remarks  

This view has the following relationship cardinalities.  
  
| From | To | Relationship |
| ---- | -- | ------------ |
|sys.database_event_session_events.event_session_id|sys.database_event_sessions.event_session_id|Many to one|  
  
## Next steps

Learn more about related concepts in the following articles:

- [Extended events in Azure SQL Database](/azure/azure-sql/database/xevent-db-diff-from-svr)
- [Event File target code for extended events in Azure SQL Database and SQL Managed Instance](/azure/azure-sql/database/xevent-code-event-file)
- [sys.database_event_sessions (Azure SQL Database and Azure SQL Managed Instance)](sys-database-event-sessions-azure-sql-database.md)
- [sys.database_event_session_actions (Azure SQL Database and Azure SQL Managed Instance)](sys-database-event-session-actions-azure-sql-database.md)
- [Monitoring Microsoft Azure SQL Database and Azure SQL Managed Instance performance using dynamic management views](/azure/azure-sql/database/monitoring-with-dmvs)
