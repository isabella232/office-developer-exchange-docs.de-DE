---
title: GetStreamingEventsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetStreamingEventsResponseMessage
api_type:
- schema
ms.assetid: 655e4e78-af74-48b0-a988-7d86ab368feb
description: Das GetStreamingEventsResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen GetStreamingEvents-Vorgangsanforderung.
ms.openlocfilehash: a1af394fa55ab04f42096ebc1c29c879c9cffb9c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533427"
---
# <a name="getstreamingeventsresponsemessage"></a>GetStreamingEventsResponseMessage

Das **GetStreamingEventsResponseMessage-Element** enthält den Status und das Ergebnis einer einzelnen [GetStreamingEvents-Vorgangsanforderung.](getstreamingevents-operation.md) 
  
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
|**ResponseClass** <br/> | Beschreibt den Status einer [GetStreamingEvents-Vorgangsantwort.](getstreamingevents-operation.md) <br/><br/>Die folgenden Werte sind für dieses Attribut gültig:  <br/><br/>– Erfolg  <br/>- Warnung  <br/>- Fehler  <br/> |
   
#### <a name="responseclass-attribute"></a>ResponseClass-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Erfolg  <br/> |Beschreibt eine Anforderung, die erfüllt wird.  <br/> |
|Warnung  <br/> | Beschreibt eine Anforderung, die nicht verarbeitet wurde. Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde und nachfolgende Elemente nicht verarbeitet werden konnten. <br/><br/>Es folgen Beispiele für Warnungsquellen:  <br/><br/>– Der Exchange Speicher ist während des Batches offline.  <br/>– Active Directory Domain Services (AD DS) ist offline.  <br/>– Postfächer wurden verschoben.  <br/>– Die Postfachdatenbank (MDB) ist offline.  <br/>– Ein Kennwort ist abgelaufen.  <br/>– Ein Kontingent wurde überschritten.  <br/> |
|Fehler  <br/> | Beschreibt eine Anforderung, die nicht erfüllt werden kann. <br/><br/>Es folgen Beispiele für Fehlerquellen:  <br/><br/>– Ungültige Attribute oder Elemente  <br/>– Attribute oder Elemente, die außerhalb des Gültigen liegen  <br/>– Ein unbekanntes Tag  <br/>– Ein Attribut oder Element, das im Kontext ungültig ist  <br/>– Ein nicht autorisierter Zugriffsversuch durch einen beliebigen Client  <br/>– Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf  <br/><br/>  Informationen zu dem Fehler finden Sie in den [ResponseCode-](responsecode.md) und [MessageText-Elementen.](messagetext.md)  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Stellt eine Textbeschreibung des Status der Antwort bereit.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, auf den die Anforderung gestoßen ist.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert. Sie enthält den Wert 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
|[Benachrichtigungen](notifications.md) <br/> |Enthält eine Liste der Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.  <br/> |
|[ErrorSubscriptionIds](errorsubscriptionids.md) <br/> |Enthält eine Liste ungültiger Abonnement-IDs.  <br/> |
|[ConnectionStatus](connectionstatus.md) <br/> |Stellt eine Textbeschreibung des Status eines Streamingabonnements bereit.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Enthält die Antwortnachrichten für eine Exchange Webdienstanforderung.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetStreamingEvents](getstreamingevents.md) 
- [GetStreamingEventsResponse](getstreamingeventsresponse.md)
- [GetStreamingEvents-Vorgang](getstreamingevents-operation.md)

