---
title: ShowExternalRecipientCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ShowExternalRecipientCount
api_type:
- schema
ms.assetid: db28dbcb-d051-4e5c-a9c2-4b8d5149b4e1
description: Das ShowExternalRecipientCount-Element gibt an, ob Consumer des Vorgangs GetMailTips müssen e-Mail-Infos anzeigen, die die Anzahl der externe Empfänger angeben, zu denen eine Nachricht adressiert ist.
ms.openlocfilehash: 1fd3ceb629689c560dc60afe01f0413602f79a0d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831491"
---
# <a name="showexternalrecipientcount"></a>ShowExternalRecipientCount

Das **ShowExternalRecipientCount** -Element gibt an, ob Consumer der [GetMailTips Vorgang](getmailtips-operation.md) müssen e-Mail-Infos anzeigen, die die Anzahl der externe Empfänger angeben, zu denen eine Nachricht adressiert ist. 
  
```XML
<ShowExternalRecipientCount>true | false</ShowExternalRecipientCount>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MailTipsConfiguration (MailTipsServiceConfiguration)](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |Enthält Konfigurationsinformationen für den e-Mail-Dienst Tipps Service.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert der dieses Element ist **true** , wenn die Consumer der [GetMailTips Vorgang](getmailtips-operation.md) müssen e-Mail-Infos anzeigen, die die Anzahl der externe Empfänger angeben, zu denen eine Nachricht adressiert ist. Der Wert ist **false** , wenn Consumer der [GetMailTips Vorgang](getmailtips-operation.md) keinen e-Mail-Infos anzeigen, die die Anzahl der externe Empfänger angeben, zu denen eine Nachricht adressiert ist. 
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetMailTips-Vorgang](getmailtips-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

