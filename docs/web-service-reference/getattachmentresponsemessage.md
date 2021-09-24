---
title: GetAttachmentResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetAttachmentResponseMessage
api_type:
- schema
ms.assetid: f0a841af-422d-4c82-b710-41e2038dbee4
description: Das GetAttachmentResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen GetAttachment-Vorgangsanforderung.
ms.openlocfilehash: 943474827ebc96894fbde973fde0872deadc9ecc
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511593"
---
# <a name="getattachmentresponsemessage"></a>GetAttachmentResponseMessage

Das **GetAttachmentResponseMessage-Element** enthält den Status und das Ergebnis einer einzelnen [GetAttachment-Vorgangsanforderung.](getattachment-operation.md) 
  
- [GetAttachmentResponse](getattachmentresponse.md) 
- [ResponseMessages](responsemessages.md) 
- [GetAttachmentResponseMessage](getattachmentresponsemessage.md)
  
```xml
<GetAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Attachments/>
</GetAttachmentResponseMessage>
```

 **AttachmentInfoResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ResponseClass** <br/> | Beschreibt den Status einer [GetAttachment-Vorgangsantwort.](getattachment-operation.md)<br/><br/> Die folgenden Werte sind für dieses Attribut gültig: <br/> <br/>– Erfolg  <br/>- Warnung  <br/>- Fehler  <br/> |
   
#### <a name="responseclass-attribute"></a>ResponseClass-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Erfolg  <br/> |Beschreibt eine Anforderung, die erfüllt wird.  <br/> |
|Warnung  <br/> | Beschreibt eine Anforderung, die nicht verarbeitet wurde. Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde und nachfolgende Elemente nicht verarbeitet werden konnten. <br/><br/>Es folgen Beispiele für Warnungsquellen: <br/> <br/>– Der Exchange Speicher ist während des Batches offline.  <br/>– Active Directory Domain Services (AD DS) ist offline.  <br/>– Postfächer werden verschoben.  <br/>– Die Nachrichtendatenbank (MDB) ist offline.  <br/>– Ein Kennwort ist abgelaufen.  <br/>– Ein Kontingent wird überschritten.  <br/> |
|Fehler  <br/> | Beschreibt eine Anforderung, die nicht erfüllt werden kann. <br/><br/>Es folgen Beispiele für Fehlerquellen:  <br/><br/>– Ungültige Attribute oder Elemente  <br/>– Attribute oder Elemente außerhalb des Bereichs  <br/>- Unbekanntes Tag  <br/>- Attribut oder Element im Kontext ungültig  <br/>– Versuch eines nicht autorisierten Zugriffs durch einen beliebigen Client  <br/>- Serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf  <br/><br/>  Informationen zu dem Fehler finden Sie in den [ResponseCode-](responsecode.md) und [MessageText-Elementen.](messagetext.md)  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Stellt eine Textbeschreibung des Status der Antwort bereit.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, auf den die Anforderung gestoßen ist.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert. Sie enthält den Wert 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
|[Anhänge](attachments-ex15websvcsotherref.md) <br/> |Enthält die Elemente oder Dateien, die einem Element im Exchange Speicher zugeordnet sind.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Enthält die Antwortnachrichten für eine Exchange Webdienstanforderung.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetAttachment](getattachment.md) 
- [GetAttachment-Vorgang](getattachment-operation.md)

