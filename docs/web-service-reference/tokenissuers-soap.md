---
title: TokenIssuers (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 26c55228-184e-4340-bd80-f86be56f3e7a
description: Die Elemente TokenIssuers stellt die Auflistung TokenIssuer (SOAP) dar.
ms.openlocfilehash: b070d85b32d5bce8461ac4e930329f237885bad7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839232"
---
# <a name="tokenissuers-soap"></a>TokenIssuers (SOAP)

Die Elemente **TokenIssuers** stellt die Auflistung [TokenIssuer (SOAP)](tokenissuer-soap.md) dar. 
  
```XML
<TokenIssuers>
    <TokenIssuer/>
</TokenIssuers>
```

 **TokenIssuers**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[TokenIssuer (SOAP)](tokenissuer-soap.md) <br/> |Gibt den [Uri (SOAP)](uri-soap.md) und [Endpunkt (SOAP)](endpoint-soap.md) für den Sicherheitstokendienst an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md) <br/> |Enthält die Antwort [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) .  <br/> |
   
## <a name="remarks"></a>Hinweise

Die **TokenIssuers** stellt eine Sammlung von [TokenIssuer (SOAP)](tokenissuer-soap.md) -Elementen in der AutoErmittlung verwendet werden. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
  
[SOAP-Autodiscover XML-Elemente für Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

