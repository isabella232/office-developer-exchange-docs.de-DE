---
title: MessageTrackingSearchResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageTrackingSearchResult
api_type:
- schema
ms.assetid: 8ea77aa8-b93f-4287-be36-0a9da06e0946
description: Das MessageTrackingSearchResult-Element enthält eine einzelne Nachricht Ergebnis für ein FindMessageTrackingReportResponse-Element.
ms.openlocfilehash: ad4fb9d9e2266222303bd2015a7afba0bb46721b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830460"
---
# <a name="messagetrackingsearchresult"></a>MessageTrackingSearchResult

Das **MessageTrackingSearchResult** -Element enthält eine einzelne Nachricht Ergebnis für ein [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) -Element. 
  
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
|[Betreff](subject.md) <br/> |Der Betreff der e-Mail-Nachricht enthält.  <br/> |
|[Absender (EmailAddressType)](sender-emailaddresstype.md) <br/> |Enthält die e-Mail-Nachricht Adresse des Absenders.  <br/> |
|[PurportedSender](purportedsender.md) <br/> |Kontaktinformationen für den Absender einer e-Mail-Nachricht enthält.  <br/> |
|[Empfänger (ArrayOfRecipientsType)](recipients-arrayofrecipientstype.md) <br/> |Enthält eine Liste von E-mail-Adressen, die diese Meldung erhalten.  <br/> |
|[SubmittedTime](submittedtime.md) <br/> |Enthält die Zeit, die die Nachricht gesendet wurde.  <br/> |
|[MessageTrackingReportId](messagetrackingreportid.md) <br/> |Enthält eine interne ID, die Nachricht in der Datenbank Transport identifiziert.  <br/> |
|[PreviousHopServer](previoushopserver.md) <br/> |Enthält den Namen des Servers in der Gesamtstruktur, die zuvor die Nachricht akzeptiert.  <br/> |
|[FirstHopServer](firsthopserver.md) <br/> |Enthält den Namen des Servers in der Gesamtstruktur, die zuerst die Nachricht akzeptiert.  <br/> |
|[Eigenschaften (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Enthält eine Liste der Eigenschaften für eine oder mehrere Tracking an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageTrackingSearchResults](messagetrackingsearchresults.md) <br/> |Enthält eine Liste von Nachrichten, die den Suchkriterien entsprechen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindMessageTrackingReport-Vorgang](findmessagetrackingreport-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

