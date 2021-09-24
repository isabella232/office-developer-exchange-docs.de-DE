---
title: ApplyConversationActionResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ApplyConversationActionResponseMessage
api_type:
- schema
ms.assetid: a09edc89-7f2f-4846-a3a5-06694c97b9f6
description: Das ApplyConversationActionResponseMessage-Element enthält den Status und die Ergebnisse einer ApplyConversationAction-Vorgangsanforderung.
ms.openlocfilehash: 81378c822a473d969035f46f34ffca8939d7059d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522047"
---
# <a name="applyconversationactionresponsemessage"></a>ApplyConversationActionResponseMessage

Das **ApplyConversationActionResponseMessage-Element** enthält den Status und die Ergebnisse einer [ApplyConversationAction-Vorgangsanforderung.](applyconversationaction-operation.md)  
  
- [ApplyConversationActionResponse](applyconversationactionresponse.md)
- [ResponseMessages](responsemessages.md)
- [ApplyConversationActionResponseMessage](applyconversationactionresponsemessage.md)
  
```XML
<ApplyConversationActionResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</ApplyConversationActionResponseMessage>
```

 **ApplyConversationActionResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ResponseClass** <br/> | Beschreibt den Status der Antwort.<br/><br/>Die folgenden Werte sind für dieses Attribut gültig:<ul><li>Erfolg</li><li>Warnung</li><li>Fehler</li></ul> |
   
#### <a name="responseclass-attribute-values"></a>ResponseClass-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**Success** <br/> |Beschreibt eine Anforderung, die erfüllt wird.  <br/> |
|**Warning** <br/> | Beschreibt eine Anforderung, die nicht verarbeitet wurde. Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde und nachfolgende Elemente nicht verarbeitet werden konnten.<br/><br/>Es folgen Beispiele für Warnungsquellen:<ul><li>Der Exchange Speicher ist während des Batches offline.</li><li>Active Directory Domain Services (AD DS) ist offline.</li><li>Postfächer wurden verschoben.</li><li>Die Nachrichtendatenbank (MDB) ist offline.</li><li>Ein Kennwort ist abgelaufen.</li><li>Ein Kontingent wurde überschritten.</li></ul> |
|**Error** <br/> | Beschreibt eine Anforderung, die nicht erfüllt werden kann.<br/><br/>Es folgen Beispiele für Fehlerquellen:  <ul><li>Ungültige Attribute oder Elemente</li><li>Attribute oder Elemente außerhalb des Gültigen Bereichs</li><li>Ein unbekanntes Tag  </li><li>Ein Attribut oder Element, das im Kontext ungültig ist</li><li>Ein nicht autorisierter Zugriffsversuch durch einen beliebigen Client</li><li>Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</li></ul>Informationen zu dem Fehler finden Sie in den [ResponseCode-](responsecode.md) und [MessageText-Elementen.](messagetext.md)  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Stellt eine Textbeschreibung des Status der Antwort bereit.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, auf den die Anforderung gestoßen ist.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Derzeit nicht verwendet und für die zukünftige Verwendung reserviert. Dieses Element enthält den Wert 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Enthält die Antwortnachrichten für eine Exchange Webdienstanforderung.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
### <a name="version-differences"></a>Versionsunterschiede

In Versionen von Exchange ab Build 15.00.0986.00 ist das **ApplyConversationActionResponseMessage-Element** vom Typ **ApplyConversationActionResponseMessageType**. In früheren Versionen ist das Element vom Typ **ResponseMessageType**.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ApplyConversationAction-Vorgang](applyconversationaction-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

