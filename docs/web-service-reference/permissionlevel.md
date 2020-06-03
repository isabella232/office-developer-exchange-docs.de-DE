---
title: PermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PermissionLevel
api_type:
- schema
ms.assetid: 87978600-3523-451e-a725-ef092c543e2a
description: Das PermissionLevel-Element stellt die Berechtigungsstufe dar, die ein Benutzer für einen Ordner hat. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: e1e441c53b5c40c16051eb852a6b35a8af7476e2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458040"
---
# <a name="permissionlevel"></a>PermissionLevel

Das **PermissionLevel** -Element stellt die Berechtigungsstufe dar, die ein Benutzer für einen Ordner hat. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
```xml
<PermissionLevel>None or Owner or PublishingEditor or Editor or PublishingAuthor or Author or NoneditingAuthor or Reviewer or Contributor or Custom</PermissionLevel>
```

 **PermissionLevelType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Berechtigung](permission.md) <br/> |Definiert den Zugriff, den ein Benutzer verfügt in einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die möglichen Werte für das **PermissionLevel** -Element aufgeführt. 
  
**PermissionLevel-Element Text Werte**

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

