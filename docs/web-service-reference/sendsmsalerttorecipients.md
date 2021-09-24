---
title: SendSMSAlertToRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SendSMSAlertToRecipients
api_type:
- schema
ms.assetid: c4dd000b-11b6-4b7b-91e0-dbfeae11d770
description: Das SendSMSAlertToRecipients -Element gibt an, die Mobiltelefonnummer, die ist eine Warnung Short Message Service (SMS) gesendet werden.
ms.openlocfilehash: ed53ef0cdd420eea53103c1579e8c53f334d0f3c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521529"
---
# <a name="sendsmsalerttorecipients"></a>SendSMSAlertToRecipients

Das **SendSMSAlertToRecipients** -Element gibt an, die Mobiltelefonnummer, die ist eine Warnung Short Message Service (SMS) gesendet werden. 
  
```XML
<SendSMSAlertToRecipients>
   <Address/>
</SendSMSAlertToRecipients>
```

 **ArrayOfEmailAddressesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Adresse (EmailAddressType)](address-emailaddresstype.md) <br/> |Stellt eine vollständig aufgelöster E-mail-Adresse dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Aktionen](actions.md) <br/> |Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.  <br/> |
   
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
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

