---
title: PurportedSender
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PurportedSender
api_type:
- schema
ms.assetid: eb7a54ec-2e48-4030-bbcf-50a31609691b
description: Das PurportedSender-Element enthält Kontaktinformationen für den Absender einer E-Mail-Nachricht.
ms.openlocfilehash: 115aecad08211f838cabb7dae39f8eb5989ddc81
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523720"
---
# <a name="purportedsender"></a>PurportedSender

Das **PurportedSender-Element** enthält Kontaktinformationen für den Absender einer E-Mail-Nachricht. 
  
```XML
<PurportedSender>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</PurportedSender>
```

 **EmailAddressType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Name (EmailAddressType)](name-emailaddresstype.md) <br/> |Stellt den Namen des Postfachbenutzers dar. Dieses Element ist optional.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Definiert die Simple Mail Transfer Protocol (SMTP)-Adresse eines Postfachbenutzers. Dieses Element ist optional.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Stellt das Routingprotokoll für den Empfänger dar. Der Standardwert ist SMTP. Dieses Element ist optional.  <br/> |
|[MailboxType](mailboxtype.md) <br/> |Stellt den Postfachtyp dar, der durch die E-Mail-Adresse dargestellt wird. Dieses Element ist optional.  <br/> |
|[ItemId](itemid.md) <br/> |Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |Gibt Kriterien für die Typen von Nachrichten an, die gesucht werden sollen.  <br/> |
|[MessageTrackingReport](messagetrackingreport.md) <br/> |Enthält eine Nachricht, die in einem [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)zurückgegeben wird.  <br/> |
|[MessageTrackingSearchResult](messagetrackingsearchresult.md) <br/> |Enthält ein einzelnes Nachrichtenergebnis für ein [FindMessageTrackingReportResponse-Element.](findmessagetrackingreportresponse.md)  <br/> |
   
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



[GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

