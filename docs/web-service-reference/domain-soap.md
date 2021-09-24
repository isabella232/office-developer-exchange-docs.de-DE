---
title: Domäne (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 849629a0-0467-422f-88f6-3b8a95c17bba
description: Das Domain-Element enthält eine Verbunddomäne in einer GetFederationInformation-Antwort oder eine Domäne, deren Konfigurationseinstellungen in einer GetDomainSettings-Anforderung angefordert werden.
ms.openlocfilehash: a2e69dc845f9841931263fe90e39550bceb81ab8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520822"
---
# <a name="domain-soap"></a>Domäne (SOAP)

Das **Domain-Element** enthält eine Verbunddomäne in einer **GetFederationInformation-Antwort** oder eine Domäne, deren Konfigurationseinstellungen in einer **GetDomainSettings-Anforderung** angefordert werden. 
  
```XML
<Domain/> 
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Domänen (SOAP)](domains-soap.md) <br/> |Stellt die Domänen dar, für die die Konfigurationseinstellungen in einem **GetDomainSettings-Vorgang** zurückgegeben werden, oder die Domänen, die die Organisation in einem **GetFederationInformation-Vorgang** verbunden hat.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **Domain-Elements** stellt einen Domänennamen dar. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   

