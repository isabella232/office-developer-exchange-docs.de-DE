---
title: ResponseMessages (ArrayOfDelegateUserResponseMessageType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseMessages
api_type:
- schema
ms.assetid: 14819975-ce54-4f0e-9f90-d4b275895ea0
description: Das ResponseMessages-Element enthält die Antwortnachrichten für eine Exchange-Webdienste-Delegaten Management-Anforderung.
ms.openlocfilehash: e4b5567f3ded003e9648eb8ebebfadf8f1748d6c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831193"
---
# <a name="responsemessages-arrayofdelegateuserresponsemessagetype"></a>ResponseMessages (ArrayOfDelegateUserResponseMessageType)

Das **ResponseMessages** -Element enthält die Antwortnachrichten für eine Exchange-Webdienste-Delegaten Management-Anforderung. 
  
```
<ResponseMessages>
   <DelegateUserResponseMessageType/>
</ResponseMessages>
```

 **ArrayOfDelegateUserResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DelegateUserResponseMessageType](delegateuserresponsemessagetype.md) <br/> |Antwortnachrichten für Verwaltungsvorgänge Stellvertreter enthält.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AddDelegateResponse](adddelegateresponse.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung [AddDelegate-Vorgang](adddelegate-operation.md) .  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung [GetDelegate Vorgang](getdelegate-operation.md) .  <br/> |
|[UpdateDelegateResponse](updatedelegateresponse.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung [UpdateDelegate Vorgang](updatedelegate-operation.md) .  <br/> |
|[RemoveDelegateResponse](removedelegateresponse.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung [RemoveDelegate Vorgang](removedelegate-operation.md) .  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wird in den [AddDelegate-Vorgang](adddelegate-operation.md), der [GetDelegate-Vorgang](getdelegate-operation.md), der [UpdateDelegate Vorgang](updatedelegate-operation.md)und den [RemoveDelegate Vorgang](removedelegate-operation.md)verwendet. Die Stellvertretung Management Vorgangsantworten werden anders als andere Antworten strukturiert. Verwaltungsnachrichten Antwort der Stellvertretung sind eine starke Typisierung.
  
Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, der Exchange-Server, mit die Clientzugriffs-Serverrolle installiert ausgeführt wird.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[AddDelegate-Vorgang](adddelegate-operation.md)
  
[GetDelegate-Vorgang](getdelegate-operation.md)
  
[UpdateDelegate-Vorgang](updatedelegate-operation.md)
  
[RemoveDelegate-Vorgang](removedelegate-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

