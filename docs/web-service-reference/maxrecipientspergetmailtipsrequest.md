---
title: MaxRecipientsPerGetMailTipsRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaxRecipientsPerGetMailTipsRequest
api_type:
- schema
ms.assetid: 8ff5df18-1989-4217-b4c0-599232911d0c
description: Das MaxRecipientsPerGetMailTipsRequest-Element gibt die maximale Anzahl von Empfängern an, die an den GetMailTips-Vorgang übergeben werden können.
ms.openlocfilehash: cec343182b364fce040d5e32928cbeb569a22124
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468404"
---
# <a name="maxrecipientspergetmailtipsrequest"></a>MaxRecipientsPerGetMailTipsRequest

Das **MaxRecipientsPerGetMailTipsRequest** -Element gibt die maximale Anzahl von Empfängern an, die an den [GetMailTips-Vorgang](getmailtips-operation.md)übergeben werden können.
  
```XML
<MaxRecipientsPerGetMailTipsRequest/>
```

 **int**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MailTipsConfiguration (MailTipsServiceConfiguration)](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |Enthält Dienstkonfigurationsinformationen für den e-Mail-Spitzen Dienst.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist ein Integer-Wert, der die maximale Anzahl von Empfängern darstellt, die an den [GetMailTips-Vorgang](getmailtips-operation.md)übergeben werden können.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetMailTips-Vorgang](getmailtips-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

