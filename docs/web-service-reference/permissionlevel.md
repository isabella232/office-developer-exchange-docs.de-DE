---
title: PermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PermissionLevel
api_type:
- schema
ms.assetid: 87978600-3523-451e-a725-ef092c543e2a
description: Das PermissionLevel-Element stellt die Berechtigungsstufe dar, die ein Benutzer in einem Ordner hat. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 48b8db48afe6ced137acceeade2911a044298d75
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544836"
---
# <a name="permissionlevel"></a>PermissionLevel

Das **PermissionLevel-Element** stellt die Berechtigungsstufe dar, die ein Benutzer in einem Ordner hat. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
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

In der folgenden Tabelle sind die möglichen Werte für das **PermissionLevel-Element** aufgeführt. 
  
**PermissionLevel-Elementtextwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Gibt an, dass der Benutzer keine Berechtigungen für den Ordner hat.  <br/> |
|Besitzer  <br/> |Gibt an, dass der Benutzer alle Elemente im Ordner erstellen, lesen, bearbeiten und löschen und Unterordner erstellen kann. Der Benutzer ist sowohl Ordnerbesitzer als auch Ordnerkontakt.  <br/> |
|PublishingEditor  <br/> |Gibt an, dass der Benutzer alle Elemente im Ordner erstellen, lesen, bearbeiten und löschen und Unterordner erstellen kann.  <br/> |
|Editor  <br/> |Gibt an, dass der Benutzer alle Elemente im Ordner erstellen, lesen, bearbeiten und löschen kann.  <br/> |
|PublishingAuthor  <br/> |Gibt an, dass der Benutzer alle Elemente im Ordner erstellen und lesen, nur vom Benutzer erstellte Elemente bearbeiten und löschen und Unterordner erstellen kann.  <br/> |
|Ursprung  <br/> |Gibt an, dass der Benutzer alle Elemente im Ordner erstellen und lesen und nur elemente bearbeiten und löschen kann, die der Benutzer erstellt.  <br/> |
|NoneditingAuthor  <br/> |Gibt an, dass der Benutzer alle Elemente im Ordner erstellen und lesen und nur elemente löschen kann, die der Benutzer erstellt.  <br/> |
|Reviewer  <br/> |Gibt an, dass der Benutzer alle Elemente im Ordner lesen kann.  <br/> |
|Contributor  <br/> |Gibt an, dass der Benutzer Elemente im Ordner erstellen kann. Der Inhalt des Ordners wird nicht angezeigt.  <br/> |
|Benutzerdefiniert  <br/> |Gibt an, dass der Benutzer über benutzerdefinierte Zugriffsberechtigungen für den Ordner verfügt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

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

