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
description: Das PermissionLevel-Element darstellt, die Berechtigungsstufe, die ein Benutzer für einen Ordner verfügt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 7cc734f5807fe039467065315c220341f47d3fb4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830730"
---
# <a name="permissionlevel"></a>PermissionLevel

Das **PermissionLevel** -Element darstellt, die Berechtigungsstufe, die ein Benutzer für einen Ordner verfügt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
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

Die folgende Tabelle enthält die möglichen Werte für das **PermissionLevel** -Element. 
  
**Text-Elementwerte PermissionLevel**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Gibt an, dass der Benutzer keine Berechtigungen für den Ordner verfügt.  <br/> |
|Besitzer  <br/> |Gibt an, dass der Benutzer kann erstellen, lesen, bearbeiten und löschen alle Elemente im Ordner und Unterordner erstellen. Der Benutzer ist Besitzer des Ordners und Ordner Kontakt.  <br/> |
|Vom Typ PublishingEditor  <br/> |Gibt an, dass der Benutzer kann erstellen, lesen, bearbeiten und löschen alle Elemente im Ordner und Unterordner erstellen.  <br/> |
|Herausgeber  <br/> |Gibt an, dass der Benutzer erstellen, lesen, bearbeiten und löschen alle Elemente im Ordner.  <br/> |
|PublishingAuthor  <br/> |Gibt an, dass der Benutzer kann erstellen und Lesen aller Elemente im Ordner, bearbeiten und Löschen nur Elemente, die der Benutzer erstellt und Unterordner erstellen.  <br/> |
|Autor  <br/> |Gibt an, dass der Benutzer erstellen und aller Elemente in den Ordner lesen und bearbeiten und löschen kann nur Elemente, die der Benutzer erstellt.  <br/> |
|NoneditingAuthor  <br/> |Gibt an, dass der Benutzer kann erstellen und alle Elemente im Ordner lesen und nur Elemente löschen, die der Benutzer erstellt.  <br/> |
|Prüfer  <br/> |Gibt an, dass der Benutzer alle Elemente im Ordner lesen kann.  <br/> |
|Mitwirkender  <br/> |Gibt an, dass der Benutzer Elemente im Ordner erstellt werden kann. Der Inhalt des Ordners wird nicht angezeigt.  <br/> |
|Benutzerdefiniert  <br/> |Gibt an, dass der Benutzer benutzerdefinierte Zugriffsberechtigungen für den Ordner verfügt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Setting Folder-Level Permissions](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

