---
title: TokenIssuers (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 26c55228-184e-4340-bd80-f86be56f3e7a
description: Die TokenIssuers-Elemente stellen die TokenIssuer (SOAP)-Auflistung dar.
ms.openlocfilehash: 68ff3ed515b346a84734596fae6fe127768b4476
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520402"
---
# <a name="tokenissuers-soap"></a>TokenIssuers (SOAP)

Die **TokenIssuers-Elemente** stellen die [TokenIssuer (SOAP)-Auflistung](tokenissuer-soap.md) dar. 
  
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
|[TokenIssuer (SOAP)](tokenissuer-soap.md) <br/> |Gibt den [Uri (SOAP)](uri-soap.md) und [den Endpunkt (SOAP)](endpoint-soap.md) für den Sicherheitstokendienst an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md) <br/> |Enthält die [SOAP-Antwort (GetFederationInformation-Vorgang).](getfederationinformation-operation-soap.md)  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

**TokenIssuers** stellt eine Sammlung von [TokenIssuer (SOAP)-Elementen](tokenissuer-soap.md) dar, die in der AutoDiscovery verwendet werden sollen. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
  
[SOAP AutoDiscover XML-Elemente für Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

