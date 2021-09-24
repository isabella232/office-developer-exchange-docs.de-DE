---
title: ResponseMessages (ArrayOfDelegateUserResponseMessageType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResponseMessages
api_type:
- schema
ms.assetid: 14819975-ce54-4f0e-9f90-d4b275895ea0
description: Das ResponseMessages-Element enthält die Antwortnachrichten für eine Exchange Webdienste-Stellvertretungs-Verwaltungsanforderung.
ms.openlocfilehash: aa90d2572679ecf3e5d99cc55731d388e083ff01
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525567"
---
# <a name="responsemessages-arrayofdelegateuserresponsemessagetype"></a>ResponseMessages (ArrayOfDelegateUserResponseMessageType)

Das **ResponseMessages-Element** enthält die Antwortnachrichten für eine Exchange Webdienste-Stellvertretungs-Verwaltungsanforderung. 
  
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
|[DelegateUserResponseMessageType](delegateuserresponsemessagetype.md) <br/> |Enthält Antwortnachrichten für Stellvertretungsverwaltungsvorgänge.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AddDelegateResponse](adddelegateresponse.md) <br/> |Enthält den Status und das Ergebnis einer [AddDelegate-Vorgangsanforderung.](adddelegate-operation.md)  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |Enthält den Status und das Ergebnis einer [GetDelegate-Vorgangsanforderung.](getdelegate-operation.md)  <br/> |
|[UpdateDelegateResponse](updatedelegateresponse.md) <br/> |Enthält den Status und das Ergebnis einer [UpdateDelegate-Vorgangsanforderung.](updatedelegate-operation.md)  <br/> |
|[RemoveDelegateResponse](removedelegateresponse.md) <br/> |Enthält den Status und das Ergebnis einer [RemoveDelegate-Vorgangsanforderung.](removedelegate-operation.md)  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wird im [AddDelegate-Vorgang,](adddelegate-operation.md)im [GetDelegate-Vorgang,](getdelegate-operation.md)im [UpdateDelegate-Vorgang](updatedelegate-operation.md)und im [RemoveDelegate-Vorgang](removedelegate-operation.md)verwendet. Die Antworten auf den Delegatverwaltungsvorgang sind anders strukturiert als andere Antworten. Die Antwortnachrichten der Stellvertretungsverwaltung sind stark typisiert.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server mit installierter Clientzugriffsserverrolle ausgeführt wird.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[AddDelegate-Vorgang](adddelegate-operation.md)
  
[GetDelegate-Vorgang](getdelegate-operation.md)
  
[UpdateDelegate-Vorgang](updatedelegate-operation.md)
  
[RemoveDelegate-Vorgang](removedelegate-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

