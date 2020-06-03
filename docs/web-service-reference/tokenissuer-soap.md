---
title: TokenIssuer (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d7be675-626c-4173-89e9-e32beef81ad5
description: Das TokenIssuer-Element gibt den URI (SOAP) und den Endpunkt (SOAP) für den Sicherheitstokendienst an.
ms.openlocfilehash: e9c0b4140de26c7ff05daf4e863b3e8a17fedc62
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526326"
---
# <a name="tokenissuer-soap"></a>TokenIssuer (SOAP)

Das **TokenIssuer** -Element gibt den [URI (SOAP)](uri-soap.md) und den [Endpunkt (SOAP)](endpoint-soap.md) für den Sicherheitstokendienst an. 
  
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
|[URI (SOAP)](uri-soap.md) <br/> |Der URI des Sicherheitstokendienst, der den Sicherheitstoken ausgestellt hat.  <br/> |
|[Endpunkt (SOAP)](endpoint-soap.md) <br/> |Der Endpunkt-URI des Webdiensts.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[TokenIssuers (SOAP)](tokenissuers-soap.md) <br/> |Stellt eine Auflistung von Security Token Service [URI (SOAP)](uri-soap.md) und [EndPoint (SOAP)](endpoint-soap.md)dar.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie das **TokenIssuer** -Element, um den Sicherheitstokendienst Bei Verwendung von Sicherheitstoken anzugeben. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |Auto Ermittlungs Schema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
  
[XML-Elemente der SOAP-AutoErmittlung für Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

