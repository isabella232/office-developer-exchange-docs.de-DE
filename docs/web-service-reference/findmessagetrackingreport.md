---
title: FindMessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FindMessageTrackingReport
api_type:
- schema
ms.assetid: 7ca6e2f7-aae1-4920-b839-73513ba8d4d8
description: Das FindMessageTrackingReport-Element gibt Kriterien für die Typen von Nachrichten an, die gesucht werden sollen.
ms.openlocfilehash: ec2ab16c6649d85edd86b9438e00ea7cfb9841ef
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513689"
---
# <a name="findmessagetrackingreport"></a>FindMessageTrackingReport

Das **FindMessageTrackingReport-Element** gibt Kriterien für die Typen von Nachrichten an, die gesucht werden sollen. 
  
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
|[Bereich (NonEmptyStringType)](scope-nonemptystringtype.md) <br/> |Gibt an, wie umfangreich der Bericht zur Nachrichtenverfolgung sein sollte.  <br/> |
|[Domäne (Nachrichtenverfolgung)](domain-message-tracking.md) <br/> |Enthält den Namen der Domäne, in der die Nachrichtenverfolgung ausgeführt wird.  <br/> |
|[Absender (EmailAddressType)](sender-emailaddresstype.md) <br/> |Enthält Kontaktinformationen für den Absender der E-Mail-Nachricht.  <br/> |
|[PurportedSender](purportedsender.md) <br/> |Enthält Kontaktinformationen für den Absender einer E-Mail-Nachricht.  <br/> |
|[Empfänger](recipient.md) <br/> |Enthält die E-Mail-Adresse für den Empfänger der Nachricht.  <br/> |
|[Betreff](subject.md) <br/> |Enthält den Betreff der E-Mail-Nachricht.  <br/> |
|[StartDateTime](startdatetime.md) <br/> |Enthält das Startdatum und die Startzeit für die Suche.  <br/> |
|[EndDateTime](enddatetime.md) <br/> |Enthält das Enddatum und die Endzeit für die Suche.  <br/> |
|[MessageId](messageid.md) <br/> |Enthält den Nachrichtenbezeichner für die Suche.  <br/> |
|[FederatedDeliveryMailbox](federateddeliverymailbox.md) <br/> |Enthält den Namen des Postfachs, in das die standortübergreifende Nachricht gesendet wurde.  <br/> |
|[DiagnosticsLevel](diagnosticslevel.md) <br/> |Stellt die Detailebene für Diagnoseberichte dar.  <br/> |
|[ServerHint](serverhint.md) <br/> |Stellt den Ausgangspunkt zum Nachverfolgen einer Nachricht an einem Remotestandort oder einer Remotegesamtstruktur dar.  <br/> |
|[Eigenschaften (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Enthält eine Liste einer oder mehrerer Nachverfolgungseigenschaften. Dieses Element ist optional.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindMessageTrackingReport-Vorgang](findmessagetrackingreport-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

