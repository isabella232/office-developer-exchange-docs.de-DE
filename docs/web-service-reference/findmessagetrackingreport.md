---
title: FindMessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindMessageTrackingReport
api_type:
- schema
ms.assetid: 7ca6e2f7-aae1-4920-b839-73513ba8d4d8
description: Das FindMessageTrackingReport-Element gibt die Kriterien für die Typen von Nachrichten suchen.
ms.openlocfilehash: 77545121aa056992248c045af3f3d36566678b94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758468"
---
# <a name="findmessagetrackingreport"></a>FindMessageTrackingReport

Das **FindMessageTrackingReport** -Element gibt die Kriterien für die Typen von Nachrichten suchen. 
  
```xml
<FindMessageTrackingReport>
   <Scope/>
   <Domain/>
   <Sender/>
   <PurportedSender/>
   <Recipient/>
   <Subject/>
   <StartDateTime/>
   <EndDateTime/>
   <MessageId/>
   <FederatedDeliveryMailbox/>
   <DiagnosticsLevel/>
   <ServerHint/>
   <Properties/>
</FindMessageTrackingReport>
```

 **FindMessageTrackingReportRequestType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Bereich (NonEmptyStringType)](scope-nonemptystringtype.md) <br/> |Stellt dar, wie umfangreich die nachrichtenverfolgung Bericht werden soll.  <br/> |
|[Domäne (Nachrichtenverfolgung)](domain-message-tracking.md) <br/> |Enthält den Namen der Domäne, in der mit der Verfolgung ausgeführt wird.  <br/> |
|[Absender (EmailAddressType)](sender-emailaddresstype.md) <br/> |Kontaktinformationen für den Absender der E-mail-Nachricht enthält.  <br/> |
|[PurportedSender](purportedsender.md) <br/> |Kontaktinformationen für den Absender einer e-Mail-Nachricht enthält.  <br/> |
|[Recipient](recipient.md) <br/> |Enthält die E-mail-Adresse für den Empfänger der Nachricht.  <br/> |
|[Betreff](subject.md) <br/> |Enthält den Betreff der E-mail-Nachricht.  <br/> |
|[StartDateTime](startdatetime.md) <br/> |Enthält das Datum und die Uhrzeit für die Suche.  <br/> |
|[EndDateTime](enddatetime.md) <br/> |Enthält das Enddatum und die Uhrzeit für die Suche.  <br/> |
|[MessageId](messageid.md) <br/> |Enthält die ID für die Suche an.  <br/> |
|[FederatedDeliveryMailbox](federateddeliverymailbox.md) <br/> |Enthält den Namen des Postfachs, in dem die standortbasierte Cross-Nachricht gesendet wurde.  <br/> |
|[DiagnosticsLevel](diagnosticslevel.md) <br/> |Stellt die Detailebene für Diagnoseberichte.  <br/> |
|[ServerHint](serverhint.md) <br/> |Den Ausgangspunkt für Nachrichtenstatus wird in einer remote-Standort oder Gesamtstruktur darstellt.  <br/> |
|[Eigenschaften (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Enthält eine Liste der Eigenschaften für eine oder mehrere Tracking an. Dieses Element ist optional.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindMessageTrackingReport-Vorgang](findmessagetrackingreport-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

