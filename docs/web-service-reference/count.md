---
title: Anzahl
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Count
api_type:
- schema
ms.assetid: 68314b4a-1e17-4e21-9c2e-224d70ef7a32
description: Das Count-Element enthält die Anzahl der Konflikte in einer Antwort ein UpdateItem Vorgang.
ms.openlocfilehash: 15cea49eb250336cdc6b7d551d53951aff1372c2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757730"
---
# <a name="count"></a>Anzahl

Das [Count](count.md) -Element enthält die Anzahl der Konflikte in einer Antwort [UpdateItem Vorgang](updateitem-operation.md) . 
  
[UpdateItemResponse](updateitemresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[UpdateItemResponseMessage](updateitemresponsemessage.md)
  
[ConflictResults](conflictresults.md)
  
[Count](count.md)
  
```xml
<Count/>
```

 **int**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConflictResults](conflictresults.md) <br/> |Enthält die Anzahl der Konflikte in einer Antwort [UpdateItem Vorgang](updateitem-operation.md) .  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist eine ganze Zahl, die die Anzahl der Konflikte in einer Antwort [UpdateItem Vorgang](updateitem-operation.md) darstellt. 
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[UpdateItem Operation](updateitem-operation.md)
  
 **ConflictResultsType**

