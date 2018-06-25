---
title: Domäne (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 849629a0-0467-422f-88f6-3b8a95c17bba
description: Das Domäne-Element enthält eine verbunddomäne in einer Antwort GetFederationInformation oder eine Domäne, die Konfigurationseinstellungen für die in einer Anforderung GetDomainSettings angefordert werden.
ms.openlocfilehash: 411ca866800322ef06eeecc2ab92adc6f711917c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758087"
---
# <a name="domain-soap"></a>Domäne (SOAP)

Das **Domäne** -Element enthält eine verbunddomäne in einer Antwort **GetFederationInformation** oder eine Domäne, die Konfigurationseinstellungen für die in einer Anforderung **GetDomainSettings** angefordert werden. 
  
```XML
<Domain/> 
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Domänen (SOAP)](domains-soap.md) <br/> |Stellt die Domänen, die Konfigurationseinstellungen für die in einem Vorgang **GetDomainSettings** zurückgegeben werden, oder die Domänen, die die Organisation in einem Vorgang **GetFederationInformation** federated hat.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert der **Domäne** -Element stellt einen Domänennamen ein. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   

