---
title: GetFederationInformationResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2033c14f-dcc8-43c2-9fd9-a51946ec7055
description: Das GetFederationInformationResponse-Element enthält die Antwort des GetFederationInformation-Vorgang (SOAP).
ms.openlocfilehash: 28b002b45968278ad4c7160b4eed29721422646d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758672"
---
# <a name="getfederationinformationresponse-soap"></a>GetFederationInformationResponse (SOAP)

Das **GetFederationInformationResponse** -Element enthält die Antwort [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) . 
  
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
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Stellt einen Fehlercode, der von den AutoErmittlungsdienst zurückgegeben wird.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Stellt eine Nachricht, die ein Fehlercode zugeordnet ist, die von den AutoErmittlungsdienst zurückgegeben wird.  <br/> |
|[ApplicationUri (SOAP)](applicationuri-soap.md) <br/> |Definiert den Ort einer Anwendung.  <br/> |
|[TokenIssuers (SOAP)](tokenissuers-soap.md) <br/> |Stellt eine Auflistung von Sicherheitstoken, die Sicherheits-Tokens-Dienst-IDs und Endpunkte enthalten.  <br/> |
|[Domänen (SOAP)](domains-soap.md) <br/> |Stellt die Domänen, die die Konfigurationen für die in einem Vorgang [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md) **GetDomainSettings** zurückgegeben werden oder die Domänen, die die Organisation in einem [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) federated hat **GetFederationInformation** Vorgang.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)

