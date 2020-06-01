---
title: GetStreamingEventsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetStreamingEventsResponseMessage
api_type:
- schema
ms.assetid: 655e4e78-af74-48b0-a988-7d86ab368feb
description: Das GetStreamingEventsResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen GetStreamingEvents-Vorgangsanforderung.
ms.openlocfilehash: 055fb7eeb12e241739eb860cecbe398b8a322bd2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459146"
---
# <a name="getstreamingeventsresponsemessage"></a>GetStreamingEventsResponseMessage

Das **GetStreamingEventsResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [GetStreamingEvents-Vorgangs](getstreamingevents-operation.md) Anforderung. 
  
```xml
<GetStreamingEventsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Notifications/>
   <ErrorSubscriptionIds/>
   <ConnectionStatus/>
</GetStreamingEventsResponseMessage>
```

 **GetStreamingEventsResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ResponseClass** <br/> | Beschreibt den Status einer [GetStreamingEvents-Vorgangs](getstreamingevents-operation.md) Antwort. <br/><br/>Die folgenden Werte sind für dieses Attribut gültig:  <br/><br/>-Success  <br/>-Warnung  <br/>-Error  <br/> |
   
#### <a name="responseclass-attribute"></a>ResponseClass-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Erfolg  <br/> |Beschreibt eine Anforderung, die erfüllt ist.  <br/> |
|Warnung  <br/> | Beschreibt eine Anforderung, die nicht verarbeitet wurde. Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden. <br/><br/>Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:  <br/><br/>-Der Exchange-Informationsspeicher ist während des Batches offline.  <br/>-Active Directory-Domänendienste (AD DS) ist offline.  <br/>-Postfächer wurden verschoben.  <br/>-Die Postfachdatenbank (MDB) ist offline.  <br/>-Ein Kennwort ist abgelaufen.  <br/>-Ein Kontingent wurde überschritten.  <br/> |
|Fehler (ungefährer Wortlaut)  <br/> | Beschreibt eine Anforderung, die nicht erfüllt werden kann. <br/><br/>Im folgenden finden Sie Beispiele für Fehlerquellen:  <br/><br/>-Ungültige Attribute oder Elemente  <br/>-Attribute oder Elemente außerhalb des gültigen Bereichs  <br/>-Ein unbekanntes Tag  <br/>-Ein Attribut oder Element, das im Kontext ungültig ist  <br/>-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client  <br/>-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf  <br/><br/>  Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Enthält eine Textbeschreibung des Status der Antwort.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert. Sie enthält den Wert 0.  <br/> |
|[Messagexml verwendet](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
|[Benachrichtigungen](notifications.md) <br/> |Enthält eine Liste mit Informationen zum Abonnement und zu den Ereignissen, die seit der letzten Benachrichtigung aufgetreten sind.  <br/> |
|[ErrorSubscriptionIds](errorsubscriptionids.md) <br/> |Enthält eine Liste von Abonnement-IDs, die ungültig sind.  <br/> |
|[Den ConnectionStatus](connectionstatus.md) <br/> |Enthält eine Textbeschreibung des Status eines Streaming-Abonnements.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetStreamingEvents](getstreamingevents.md) 
- [GetStreamingEventsResponse](getstreamingeventsresponse.md)
- [GetStreamingEvents-Vorgang](getstreamingevents-operation.md)

