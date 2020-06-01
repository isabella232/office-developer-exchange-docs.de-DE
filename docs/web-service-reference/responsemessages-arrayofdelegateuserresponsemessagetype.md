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
description: Das ResponseMessages-Element enthält die Antwortnachrichten für eine Exchange Webdienste Delegate-Verwaltungsanforderung.
ms.openlocfilehash: 6b035f4ee46af1750a275e2c61b2cddea06b37a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465457"
---
# <a name="responsemessages-arrayofdelegateuserresponsemessagetype"></a>ResponseMessages (ArrayOfDelegateUserResponseMessageType)

Das **ResponseMessages** -Element enthält die Antwortnachrichten für eine Exchange Webdienste Delegate-Verwaltungsanforderung. 
  
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
|[DelegateUserResponseMessageType](delegateuserresponsemessagetype.md) <br/> |Enthält Antwortnachrichten für Delegate-Verwaltungsvorgänge.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AddDelegateResponse](adddelegateresponse.md) <br/> |Enthält den Status und das Ergebnis einer [AddDelegate-Vorgangs](adddelegate-operation.md) Anforderung.  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |Enthält den Status und das Ergebnis einer [getdelegate-Vorgangs](getdelegate-operation.md) Anforderung.  <br/> |
|[UpdateDelegateResponse](updatedelegateresponse.md) <br/> |Enthält den Status und das Ergebnis einer [UpdateDelegate-Vorgangs](updatedelegate-operation.md) Anforderung.  <br/> |
|[RemoveDelegateResponse](removedelegateresponse.md) <br/> |Enthält den Status und das Ergebnis einer [RemoveDelegate-Vorgangs](removedelegate-operation.md) Anforderung.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element wird im [AddDelegate-Vorgang](adddelegate-operation.md), im [getdelegate](getdelegate-operation.md)-Vorgang, im [UpdateDelegate-Vorgang](updatedelegate-operation.md)und im RemoveDelegate- [Vorgang](removedelegate-operation.md)verwendet. Die Antwort auf den Delegate-Verwaltungsvorgang ist anders strukturiert als andere Antworten. Die Antwortnachrichten der Delegate-Verwaltung sind stark typisiert.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server mit installierter Client Zugriffs-Server Rolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[AddDelegate-Vorgang](adddelegate-operation.md)
  
[GetDelegate-Vorgang](getdelegate-operation.md)
  
[UpdateDelegate-Vorgang](updatedelegate-operation.md)
  
[RemoveDelegate-Vorgang](removedelegate-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

