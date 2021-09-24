---
title: MessageTrackingSearchResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MessageTrackingSearchResult
api_type:
- schema
ms.assetid: 8ea77aa8-b93f-4287-be36-0a9da06e0946
description: Das MessageTrackingSearchResult-Element enthält ein einzelnes Nachrichtenergebnis für ein FindMessageTrackingReportResponse-Element.
ms.openlocfilehash: 2bd70461b2896d0204b163365d525f76d42bb213
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523880"
---
# <a name="messagetrackingsearchresult"></a>MessageTrackingSearchResult

Das **MessageTrackingSearchResult-Element** enthält ein einzelnes Nachrichtenergebnis für ein [FindMessageTrackingReportResponse-Element.](findmessagetrackingreportresponse.md) 
  
```xml
<MessageTrackingSearchResult>
   <Subject/>
   <Sender/>
   <PurportedSender/>
   <Recipients/>
   <SubmittedTime/>
   <MessageTrackingReportId/>
   <PreviousHopServer/>
   <FirstHopServer/>
   <Properties/>
</MessageTrackingSearchResult>
```

 **FindMessageTrackingSearchResultType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Betreff](subject.md) <br/> |Enthält den Betreff der E-Mail-Nachricht.  <br/> |
|[Absender (EmailAddressType)](sender-emailaddresstype.md) <br/> |Enthält die Adresse des Absenders der E-Mail-Nachricht.  <br/> |
|[PurportedSender](purportedsender.md) <br/> |Enthält Kontaktinformationen für den Absender einer E-Mail-Nachricht.  <br/> |
|[Empfänger (ArrayOfRecipientsType)](recipients-arrayofrecipientstype.md) <br/> |Enthält eine Liste der E-Mail-Adressen, die diese Nachricht empfangen haben.  <br/> |
|[SubmittedTime](submittedtime.md) <br/> |Enthält die Uhrzeit, zu der die Nachricht gesendet wurde.  <br/> |
|[MessageTrackingReportId](messagetrackingreportid.md) <br/> |Enthält eine interne ID, die die Nachricht in der Transportdatenbank identifiziert.  <br/> |
|[PreviousHopServer](previoushopserver.md) <br/> |Enthält den Namen des Servers in der Gesamtstruktur, der die Nachricht zuvor akzeptiert hat.  <br/> |
|[FirstHopServer](firsthopserver.md) <br/> |Enthält den Namen des Servers in der Gesamtstruktur, der die Nachricht zuerst akzeptiert hat.  <br/> |
|[Eigenschaften (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Enthält eine Liste einer oder mehrerer Nachverfolgungseigenschaften.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageTrackingSearchResults](messagetrackingsearchresults.md) <br/> |Enthält eine Liste von Nachrichten, die den Suchkriterien entsprechen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindMessageTrackingReport-Vorgang](findmessagetrackingreport-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

