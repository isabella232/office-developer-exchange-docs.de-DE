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
description: Das MaxRecipientsPerGetMailTipsRequest-Element gibt die maximale Anzahl von Empfängern, die für den Betrieb GetMailTips übergeben werden kann.
ms.openlocfilehash: 4c873fe534582e582bf5b1c1d5fd2789616e056a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830386"
---
# <a name="maxrecipientspergetmailtipsrequest"></a>MaxRecipientsPerGetMailTipsRequest

Das **MaxRecipientsPerGetMailTipsRequest** -Element gibt die maximale Anzahl von Empfängern, die an den [GetMailTips Vorgang](getmailtips-operation.md)übergeben werden kann.
  
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
|[MailTipsConfiguration (MailTipsServiceConfiguration)](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |Enthält Konfigurationsinformationen für den e-Mail-Dienst Tipps Service.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist eine ganze Zahl, die die maximale Anzahl von Empfängern darstellt, um den [Vorgang GetMailTips](getmailtips-operation.md)übergeben werden können.
  
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

