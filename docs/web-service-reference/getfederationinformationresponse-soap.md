---
title: GetFederationInformationResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 2033c14f-dcc8-43c2-9fd9-a51946ec7055
description: Das GetFederationInformationResponse-Element enthält die SOAP-Antwort (GetFederationInformation- Operation).
ms.openlocfilehash: 20d00f047acae6c9eba1347ae7e8110656fefb4b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529879"
---
# <a name="getfederationinformationresponse-soap"></a>GetFederationInformationResponse (SOAP)

Das **GetFederationInformationResponse-Element** enthält die [SOAP-Antwort (GetFederationInformation- Operation).](getfederationinformation-operation-soap.md) 
  
```XML
<GetFederationInformationResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <TokenIssuers/>
   <ApplicationUri/>
   <Domains/>
</GetFederationInformationResponse>
```

 **GetFederationInformationResponse**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Stellt einen Fehlercode dar, der vom AutoErmittlungsdienst zurückgegeben wird.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Stellt eine Meldung dar, die einem Fehlercode zugeordnet ist, der vom AutoErmittlungsdienst zurückgegeben wird.  <br/> |
|[ApplicationUri (SOAP)](applicationuri-soap.md) <br/> |Definiert den Speicherort einer Anwendung.  <br/> |
|[TokenIssuers (SOAP)](tokenissuers-soap.md) <br/> |Stellt eine Auflistung von Sicherheitstoken dar, die Sicherheitstokendienst-IDs und Endpunkte enthalten.  <br/> |
|[Domänen (SOAP)](domains-soap.md) <br/> |Stellt die Domänen dar, für die die Konfigurationen in einem [GETDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md) **GetDomainSettings-Vorgang** zurückgegeben werden, oder die Domänen, für die die Organisation in einem [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) **GetFederationInformation-Vorgang** verbunden ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)

