---
title: ResponseCode (InvalidRecipientResponseCodeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseCode
api_type:
- schema
ms.assetid: 582e9caa-d2bc-4be1-a460-739294f9ef18
description: Das ResponseCode-Element enthält Informationen dazu, warum der Empfänger ungültig.
ms.openlocfilehash: 3bff99dd1ac6603ce31d5ceb074e73ef48190bb2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831186"
---
# <a name="responsecode-invalidrecipientresponsecodetype"></a>ResponseCode (InvalidRecipientResponseCodeType)

Das **ResponseCode** -Element enthält Informationen dazu, warum der Empfänger ungültig. 
  
```XML
<ResponseCode>OtherError or RecipientOrganizationNotFederated or CannotObtainTokenFromSTS or SystemPolicyBlocksSharingWithThisRecipient or RecipientOrganizationFederatedWithUnknownTokenIssuer</ResponseCode>
```

 **InvalidRecipientResponseCodeType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[InvalidRecipient](invalidrecipient.md) <br/> |Enthält die SMTP-Adresse des ungültige Empfänger und Informationen dazu, warum der Empfänger ungültig.  <br/> |
   
## <a name="text-value"></a>Textwert

Die folgende Tabelle enthält die möglichen Werte für das **ResponseCode** -Element. 
  
|**Code**|**Beschreibung**|
|:-----|:-----|
|OtherError  <br/> |Gibt an, dass der Fehler nicht von einem anderen Fehlercode Antwort angegeben ist.  <br/> |
|RecipientOrganizationNotFederated  <br/> |Gibt an, dass eine Beziehung mit der Organisation im SMTP-e-Mail-Adresse des Empfängers angegebene nicht verfügbar ist.  <br/> |
|CannotObtainTokenFromSTS  <br/> |Gibt an, dass beim Abrufen von ein Sicherheitstoken vom Sicherheitstokendienst-Server ein Problem aufgetreten.  <br/> |
|SystemPolicyBlocksSharingWithThisRecipient  <br/> |Gibt an, dass der Systemadministrator eine Systemrichtlinie festgelegt hat, die Freigabe für den angegebenen Empfänger blockiert.  <br/> |
|RecipientOrganizationFederatedWithUnknownTokenIssuer  <br/> |Gibt an, dass des Sicherheitstokendiensts, die von den angegebenen Empfänger verwendet ist unbekannt ist.  <br/> |
   
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



[GetSharingMetadata-Vorgang](getsharingmetadata-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

