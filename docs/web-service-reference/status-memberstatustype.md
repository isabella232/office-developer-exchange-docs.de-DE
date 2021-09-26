---
title: Status (MemberStatusType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Status
api_type:
- schema
ms.assetid: 4f8a860b-0a48-4a0d-9a7a-69a0304aa747
description: Das Status-Element enthält Informationen über den Status eines Verteilerlistenmitglieds auf dem Server.
ms.openlocfilehash: 0142ac1fa88c4cc4e513f23bbfad2869e7df32e7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544598"
---
# <a name="status-memberstatustype"></a>Status (MemberStatusType)

Das **Status-Element** enthält Informationen über den Status eines Verteilerlistenmitglieds auf dem Server. 
  
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

In der folgenden Tabelle sind die möglichen Werte für das **Status-Element** aufgeführt. 
  
**Status-Elementwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Unbekannte  <br/> |Memberinformationen sind ungültig oder nicht erkannt.  <br/> |
|Standard  <br/> |Memberinformationen in einer Verteilerliste werden mit dem referenzierten Objekt synchronisiert.  <br/> |
|Degradiert  <br/> |Referenziertes Objekt ist nicht verfügbar.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

