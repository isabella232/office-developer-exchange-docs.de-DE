---
title: CalendarPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarPermissionLevel
api_type:
- schema
ms.assetid: 6ac2b792-4326-4a3f-b6cb-977bf523b5b2
description: Das CalendarPermissionLevel-Element stellt die Berechtigungsstufe dar, die ein Benutzer in einem Kalenderordner hat. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 670f78e0b3cef7a40339c83d84916871f8969536
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527180"
---
# <a name="calendarpermissionlevel"></a>CalendarPermissionLevel

Das **CalendarPermissionLevel** -Element stellt die Berechtigungsstufe dar, die ein Benutzer in einem Kalenderordner hat. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
```xml
<CalendarPermissionLevel>None or Owner or PublishingEditor or Editor or PublishingAuthor or Author or NoneditingAuthor or Reviewer or Contributor or FreeBusyTimeOnly or FreeBusyTimeAndSubjectAndLocation or Custom</CalendarPermissionLevel>
```

 **CalendarPermissionLevelType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarPermission](calendarpermission.md) <br/> |Definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die möglichen Werte für das **CalendarPermissionLevel** -Element aufgeführt. 
  
**CalendarPermissionLevel-Element Text Werte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Gibt an, dass der Benutzer über keine Berechtigungen für den Ordner verfügt.  <br/> |
|Besitzer  <br/> |Gibt an, dass der Benutzer alle Elemente im Ordner erstellen, lesen, bearbeiten und löschen und Unterordner erstellen kann. Der Benutzer ist sowohl Ordnerbesitzer als auch Ordner Kontakt.  <br/> |
|Publishing Editor  <br/> |Gibt an, dass der Benutzer alle Elemente im Ordner erstellen, lesen, bearbeiten und löschen und Unterordner erstellen kann.  <br/> |
|Editor  <br/> |Gibt an, dass der Benutzer alle Elemente im Ordner erstellen, lesen, bearbeiten und löschen kann.  <br/> |
|PublishingAuthor  <br/> |Gibt an, dass der Benutzer alle Elemente im Ordner erstellen und lesen, nur vom Benutzer erstellte Elemente bearbeiten und löschen sowie Unterordner erstellen kann.  <br/> |
|Ursprung  <br/> |Gibt an, dass der Benutzer alle Elemente im Ordner erstellen und lesen kann, und nur vom Benutzer erstellte Elemente bearbeiten und löschen können.  <br/> |
|Noneditingauthorcreateitems  <br/> |Gibt an, dass der Benutzer alle Elemente im Ordner erstellen und lesen und nur vom Benutzer erstellte Elemente löschen kann.  <br/> |
|Reviewer  <br/> |Gibt an, dass der Benutzer alle Elemente im Ordner lesen kann.  <br/> |
|Contributor  <br/> |Gibt an, dass der Benutzer Elemente im Ordner erstellen kann. Der Inhalt des Ordners wird nicht angezeigt.  <br/> |
|FreeBusyTimeOnly  <br/> |Gibt an, dass der Benutzer nur die Frei/Gebucht-Zeit im Kalender anzeigen kann.  <br/> |
|FreeBusyTimeAndSubjectAndLocation  <br/> |Gibt an, dass der Benutzer die Frei/Gebucht-Zeit innerhalb des Kalenders sowie den Betreff und den Ort von Terminen anzeigen kann.  <br/> |
|Benutzerdefiniert  <br/> |Gibt an, dass der Benutzer benutzerdefinierte Zugriffsberechtigungen für den Ordner besitzt.  <br/> |
   
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



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Setting Folder-Level Permissions](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

