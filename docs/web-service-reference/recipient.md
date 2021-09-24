---
title: Empfänger
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Recipient
api_type:
- schema
ms.assetid: 52adbb30-3bfd-48aa-9ea8-9f7d3b4bee44
description: Das Recipient-Element stellt den Empfänger dar, für den das Ereignis aufgetreten ist.
ms.openlocfilehash: 5978ca36a6caa33be086e6a051df944cfd07b457
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59532224"
---
# <a name="recipient"></a>Empfänger

Das **Recipient-Element** stellt den Empfänger dar, für den das Ereignis aufgetreten ist. 
  
```XML
<Recipient>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Recipient>
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
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Definiert die primäre SMTP-Adresse (Simple Mail Transfer Protocol) eines Postfachbenutzers. Dieses Element ist optional.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Definiert die Weiterleitung, die für das Postfach verwendet wird. Der Standardwert ist SMTP. Dieses Element ist optional.  <br/> |
|[MailboxType](mailboxtype.md) <br/> |Stellt den Typ des Postfachs dar, das durch die E-Mail-Adresse dargestellt wird. Dieses Element ist optional.  <br/> |
|[ItemId](itemid.md) <br/> |Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |Enthält Informationen zu einem einzelnen Ereignis für einen Empfänger.  <br/> |
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |Gibt Kriterien für die Typen von Nachrichten an, die gesucht werden sollen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

