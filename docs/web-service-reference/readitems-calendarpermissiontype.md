---
title: ReadItems (CalendarPermissionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReadItems
api_type:
- schema
ms.assetid: bec01982-26a1-4373-b1e6-2e0c838d83c4
description: Das ReadItems-Element gibt an, ob ein Benutzer über Berechtigungen zum Lesen von Elementen in einem Kalenderordner verfügt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 532b90c47cca7117a89d59e7012436268be9ebb0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830964"
---
# <a name="readitems-calendarpermissiontype"></a>ReadItems (CalendarPermissionType)

Das **ReadItems** -Element gibt an, ob ein Benutzer über Berechtigungen zum Lesen von Elementen in einem Kalenderordner verfügt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
```xml
<ReadItems>None or TimeOnly or TimeAndSubjectAndLocation or FullDetails</ReadItems>
```

 **CalendarPermissionReadAccessType**
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

Die folgende Tabelle enthält die möglichen Werte für das **ReadItems** -Element. 
  
**ReadItems Elementwerte text**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Gibt an, dass der Benutzer die Berechtigung zum Anzeigen von Elementen im Kalender nicht vorhanden ist.  <br/> |
|TimeOnly  <br/> |Gibt an, dass der Benutzer die Berechtigung zum Anzeigen der nur Frei/Gebucht-Zeit im Kalender hat.  <br/> |
|TimeAndSubjectAndLocation  <br/> |Gibt an, dass der Benutzer über die Berechtigung zum Anzeigen von Frei/Gebucht-Zeit in den Kalender und den Betreff und Ort von Terminen verfügt.  <br/> |
|FullDetails  <br/> |Gibt an, dass der Benutzer die Berechtigung zum Anzeigen aller Elemente im Kalender, einschließlich der Frei/Gebucht-Zeit und Betreff, Ort und Details von Terminen verfügt.  <br/> |
   
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

