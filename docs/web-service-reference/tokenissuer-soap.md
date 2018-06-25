---
title: TokenIssuer (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d7be675-626c-4173-89e9-e32beef81ad5
description: Das TokenIssuer-Element gibt den Uri (SOAP) und Endpunkt (SOAP) für den Sicherheitstokendienst.
ms.openlocfilehash: 1c267fc6cbfdadd471c568473cc9aeeafb43ae2d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839220"
---
# <a name="tokenissuer-soap"></a>TokenIssuer (SOAP)

Das **TokenIssuer** -Element gibt den [Uri (SOAP)](uri-soap.md) und [Endpunkt (SOAP)](endpoint-soap.md) für den Sicherheitstokendienst. 
  
```XML
<TokenIssuer>
   <Uri/>
   <Endpoint/>
</TokenIssuer>
```

 **TokenIssuer**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Der URI (SOAP)](uri-soap.md) <br/> |Der URI des Sicherheitstokendiensts, der das Sicherheitstoken ausgestellt hat.  <br/> |
|[Endpunkt (SOAP)](endpoint-soap.md) <br/> |Der Webdienst-Endpunkt-URI.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[TokenIssuers (SOAP)](tokenissuers-soap.md) <br/> |Stellt eine Auflistung von Sicherheitstokendienst [Uri (SOAP)](uri-soap.md) und [Endpunkt (SOAP)](endpoint-soap.md).  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie das **TokenIssuer** -Element des Sicherheitstokendiensts an, wann Sicherheitstoken verwenden. 
  
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

