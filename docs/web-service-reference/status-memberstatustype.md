---
title: Status (MemberStatusType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Status
api_type:
- schema
ms.assetid: 4f8a860b-0a48-4a0d-9a7a-69a0304aa747
description: Status-Element enthält Informationen über den Status der Verteilung Listenmitglieder auf dem Server.
ms.openlocfilehash: ef062433c80f0cca413c33012e1164b17e226faf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831580"
---
# <a name="status-memberstatustype"></a>Status (MemberStatusType)

**Status** -Element enthält Informationen über den Status der Verteilung Listenmitglieder auf dem Server. 
  
```
<Status>Unrecognized or Normal or Demoted</Status>
```

 **MemberStatusType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Member](member-ex15websvcsotherref.md) <br/> |Stellt ein Element einer Verteilerliste dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Die folgende Tabelle enthält die möglichen Werte für die **Status** -Element. 
  
**Status-Elementwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Unbekannte  <br/> |Informationen zu Mitgliedern ist ungültig oder nicht erkannte.  <br/> |
|Standard  <br/> |Memberinformationen in einer Verteilerliste ist Synchronisierung mit dem Objekt verwiesen wird.  <br/> |
|Tiefer gestuft  <br/> |Das Objekt verwiesen wird, ist nicht verfügbar.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

