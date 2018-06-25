---
title: InvalidRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InvalidRecipients
api_type:
- schema
ms.assetid: e4e7b50e-2fa9-4649-94a6-6002f341ecc4
description: Das InvalidRecipients -Element darstellt, die Empfänger eines Ordners Freigabeanfrage, die ungültig sind.
ms.openlocfilehash: 02ad8935bde347c563875bf5bfb31968b70d81b6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829966"
---
# <a name="invalidrecipients"></a>InvalidRecipients

Das **InvalidRecipients** -Element darstellt, die Empfänger eines Ordners Freigabeanfrage, die ungültig sind. 
  
```XML
<InvalidRecipients>
   <InvalidRecipient/>
</InvalidRecipients>
```

 **ArrayOfInvalidRecipientsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[InvalidRecipient](invalidrecipient.md) <br/> |Enthält die SMTP-Adresse des ungültige Empfänger und Informationen dazu, warum der Empfänger ungültig.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetSharingMetadataResponse](getsharingmetadataresponse.md) <br/> |Definiert eine Antwort auf eine [GetSharingMetadata-Vorgang](getsharingmetadata-operation.md) an.  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen [GetSharingMetadata-Vorgang](getsharingmetadata-operation.md) -Anforderung.  <br/> |
   
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



[GetSharingMetadata-Vorgang](getsharingmetadata-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

