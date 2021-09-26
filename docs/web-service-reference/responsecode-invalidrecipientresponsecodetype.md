---
title: ResponseCode (InvalidRecipientResponseCodeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResponseCode
api_type:
- schema
ms.assetid: 582e9caa-d2bc-4be1-a460-739294f9ef18
description: Das ResponseCode-Element enthält Informationen dazu, warum der Empfänger ungültig ist.
ms.openlocfilehash: 33cd05aca672e250f288aec72d876734132d2e36
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544808"
---
# <a name="responsecode-invalidrecipientresponsecodetype"></a>ResponseCode (InvalidRecipientResponseCodeType)

Das **ResponseCode-Element** enthält Informationen dazu, warum der Empfänger ungültig ist. 
  
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

In der folgenden Tabelle sind die möglichen Werte für das **ResponseCode-Element** aufgeführt. 
  
|**Code**|**Beschreibung**|
|:-----|:-----|
|OtherError  <br/> |Gibt an, dass der Fehler nicht durch einen anderen Fehlerantwortcode angegeben wird.  <br/> |
|RecipientOrganizationNotFederated  <br/> |Gibt an, dass keine Freigabebeziehung mit der in der SMTP-E-Mail-Adresse des Empfängers angegebenen Organisation verfügbar ist.  <br/> |
|CannotObtainTokenFromSTS  <br/> |Gibt an, dass ein Problem beim Abrufen eines Sicherheitstokens vom Tokenserver aufgetreten ist.  <br/> |
|SystemPolicyBlocksSharingWithThisRecipient  <br/> |Gibt an, dass der Systemadministrator eine Systemrichtlinie festgelegt hat, die die Freigabe für den angegebenen Empfänger blockiert.  <br/> |
|RecipientOrganizationFederatedWithUnknownTokenIssuer  <br/> |Gibt an, dass der vom angegebenen Empfänger verwendete sichere Tokendienst unbekannt ist.  <br/> |
   
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



[GetSharingMetadata-Vorgang](getsharingmetadata-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

