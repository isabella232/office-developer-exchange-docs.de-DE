---
title: CalendarFolderPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarFolderPermissionLevel
api_type:
- schema
ms.assetid: 2a5c9381-dc2c-4fc6-b9b5-893477d0970e
description: Das CalendarFolderPermissionLevel-Element enthält die Berechtigungen für den Standardordner Kalender. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: dcbd57da42b5e701d898c3756ce9bcc100c20af7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461464"
---
# <a name="calendarfolderpermissionlevel"></a>CalendarFolderPermissionLevel

Das **CalendarFolderPermissionLevel** -Element enthält die Berechtigungen für den Standardordner Kalender. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
```xml
<CalendarFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</CalendarFolderPermissionLevel>
```

 **DelegateFolderPermissionLevelType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DelegatePermissions](delegatepermissions.md) <br/> |Enthält die Einstellungen für die Stell Vertretungs Berechtigungsstufe für einen Benutzer. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die Textwerte aufgeführt, die die Berechtigungsstufen darstellen.
  
**Text Werte für Berechtigungsstufen**

|**Berechtigungsstufe**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Der Stellvertreter Benutzer verfügt über keine Zugriffsberechtigungen für den Ordner Kalender.  <br/> |
|Reviewer  <br/> |Der Stellvertreter-Benutzer kann Elemente im Kalenderordner lesen.  <br/> |
|Ursprung  <br/> |Der Stellvertreter Benutzer kann Elemente im Kalenderordner lesen und erstellen.  <br/> |
|Editor  <br/> |Der Stellvertreter Benutzer kann Elemente im Kalenderordner lesen, erstellen und ändern.  <br/> |
|Benutzerdefiniert  <br/> |Der Stellvertreter Benutzer verfügt über benutzerdefinierte Zugriffsberechtigungen für den Ordner Kalender.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[AddDelegate-Vorgang](adddelegate-operation.md)
  
[UpdateDelegate-Vorgang](updatedelegate-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Hinzufügen von Stellvertretungen](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

