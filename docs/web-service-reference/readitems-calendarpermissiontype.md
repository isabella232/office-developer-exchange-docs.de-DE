---
title: ReadItems (CalendarPermissionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ReadItems
api_type:
- schema
ms.assetid: bec01982-26a1-4373-b1e6-2e0c838d83c4
description: Das ReadItems-Element gibt an, ob ein Benutzer über die Berechtigung zum Lesen von Elementen in einem Kalenderordner verfügt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: a12b5316eaebfdf6d0d70468f172f227db7ab3ef
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519086"
---
# <a name="readitems-calendarpermissiontype"></a>ReadItems (CalendarPermissionType)

Das **ReadItems-Element** gibt an, ob ein Benutzer über die Berechtigung zum Lesen von Elementen in einem Kalenderordner verfügt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
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

In der folgenden Tabelle sind die möglichen Werte für das **ReadItems-Element** aufgeführt. 
  
**ReadItems-Elementtextwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Gibt an, dass der Benutzer nicht über die Berechtigung zum Anzeigen von Elementen im Kalender verfügt.  <br/> |
|TimeOnly  <br/> |Gibt an, dass der Benutzer über die Berechtigung verfügt, nur Frei/Gebucht-Zeit im Kalender anzuzeigen.  <br/> |
|TimeAndSubjectAndLocation  <br/> |Gibt an, dass der Benutzer über die Berechtigung zum Anzeigen von Frei/Gebucht-Zeit im Kalender sowie zum Betreff und Ort von Terminen verfügt.  <br/> |
|FullDetails  <br/> |Gibt an, dass der Benutzer über die Berechtigung zum Anzeigen aller Elemente im Kalender verfügt, einschließlich Frei/Gebucht-Zeit und Betreff, Standort und Details zu Terminen.  <br/> |
   
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

