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
description: Das FindMessageTrackingReport-Element gibt Kriterien für die Typen von Nachrichten an, die gesucht werden sollen.
ms.openlocfilehash: d30e5391bb4305cae0004a9788df971a57297cae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462936"
---
# <a name="findmessagetrackingreport"></a>FindMessageTrackingReport

Das **FindMessageTrackingReport** -Element gibt Kriterien für die Typen von Nachrichten an, die gesucht werden sollen. 
  
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
|[Bereich (NonEmptyStringType)](scope-nonemptystringtype.md) <br/> |Stellt dar, wie umfangreich der Nachrichtenverfolgungsbericht sein soll.  <br/> |
|[Domäne (Nachrichtenverfolgung)](domain-message-tracking.md) <br/> |Enthält den Namen der Domäne, in der die Nachrichtenverfolgung ausgeführt wird.  <br/> |
|[Absender (e-mailemailtype)](sender-emailaddresstype.md) <br/> |Enthält Kontaktinformationen für den Absender der e-Mail-Nachricht.  <br/> |
|[PurportedSender](purportedsender.md) <br/> |Enthält Kontaktinformationen für den mutmaßlichen Absender einer e-Mail-Nachricht.  <br/> |
|[Empfänger](recipient.md) <br/> |Enthält die e-Mail-Adresse des Empfängers der Nachricht.  <br/> |
|[Betreff](subject.md) <br/> |Enthält den Betreff der e-Mail-Nachricht.  <br/> |
|[StartDateTime](startdatetime.md) <br/> |Enthält das Startdatum und die Startzeit für die Suche.  <br/> |
|[EndDateTime](enddatetime.md) <br/> |Enthält das Enddatum und die Endzeit für die Suche.  <br/> |
|[MessageId](messageid.md) <br/> |Enthält den Nachrichtenbezeichner für die Suche.  <br/> |
|[FederatedDeliveryMailbox](federateddeliverymailbox.md) <br/> |Enthält den Namen des Postfachs, in dem die standortübergreifende Nachricht gesendet wurde.  <br/> |
|[DiagnosticsLevel](diagnosticslevel.md) <br/> |Stellt die Detailebene für Diagnoseberichte dar.  <br/> |
|[ServerHint](serverhint.md) <br/> |Stellt den Ausgangspunkt zum Nachverfolgen einer Nachricht an einem Remotestandort oder einer Remotegesamtstruktur dar.  <br/> |
|[Eigenschaften (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Enthält eine Liste mit einer oder mehreren Überwachungseigenschaften. Dieses Element ist optional.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindMessageTrackingReport-Vorgang](findmessagetrackingreport-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

