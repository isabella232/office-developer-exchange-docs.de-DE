---
title: CreateManagedFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateManagedFolderResponseMessage
api_type:
- schema
ms.assetid: a72eefc3-ef0b-4b44-a74b-e6907b5b5f68
description: Das CreateManagedFolderResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung CreateManagedFolder Vorgang.
ms.openlocfilehash: e561cac949ebebc647b16578c6acbcd6132eeef7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757798"
---
# <a name="createmanagedfolderresponsemessage"></a>CreateManagedFolderResponseMessage

Das **CreateManagedFolderResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [CreateManagedFolder Vorgang](createmanagedfolder-operation.md) . 
  
- [CreateManagedFolderResponse](createmanagedfolderresponse.md)  
- [ResponseMessages](responsemessages.md) 
- [CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)
  
```xml
<CreateManagedFolderResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</CreateManagedFolderResponseMessage>
```

**FolderInfoResponseMessageType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ResponseClass** <br/> | Beschreibt den Status einer Antwort [CreateManagedFolder Vorgang](createmanagedfolder-operation.md) .<br/><br/>Die folgenden Werte sind für dieses Attribut gültig:<br/><br/>-Success  <br/>-Warnung  <br/>-Fehler  <br/> |
   
#### <a name="responseclass-attribute-values"></a>Attributwerte ResponseClass

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**Success** <br/> |Beschreibt eine Anforderung, die erfüllt ist.  <br/> |
|**Warning** <br/> | Beschreibt eine Anforderung, die nicht verarbeitet wurde. Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.<br/><br/>Es folgen Beispiele für die Quellen der Warnungen:<br/><br/>-Der Exchange-Speicher ist während der Batchaktualisierung offline.  <br/>-Active Directory-Domänendienste (AD DS) ist offline.  <br/>-Postfächer werden verschoben.  <br/>-Die Nachrichtendatenbank (MDB) ist offline.  <br/>-Ein Kennwort ist abgelaufen.  <br/>-Ein Kontingent überschritten wird.  <br/> |
|**Fehler** <br/> | Beschreibt eine Anforderung, die nicht gewährleistet werden kann.<br/><br/>Es folgen Beispiele für Datenquellen von Fehlern:  <br/><br/>-Ungültige Attribute oder Elemente  <br/>-Attribute oder Elemente außerhalb des gültigen Bereichs  <br/>-Unbekanntes tag  <br/>-Attribut oder ein Element im Kontext ist ungültig.  <br/>-Versuch von jedem Client Zugriff  <br/>-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf<br/><br/>  Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Enthält einen beschreibenden Text für den Status der Antwort.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert. Es enthält einen Wert von 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
|[Ordner](folders-ex15websvcsotherref.md) <br/> |Enthält ein Array von erstellte verwaltete Ordner.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [CreateManagedFolder-Vorgang](createmanagedfolder-operation.md)
- [EWS-Referenz für Exchange](ews-reference-for-exchange.md) 
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

