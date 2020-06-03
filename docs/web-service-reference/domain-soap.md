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
description: Das Domain-Element enthält eine Verbunddomäne in einer GetFederationInformation-Antwort oder enthält eine Domäne, deren Konfigurationseinstellungen in einer GetDomainSettings-Anforderung angefordert werden.
ms.openlocfilehash: f90c608ee1fc3356a227bca6411eaeff0c1e8b22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456983"
---
# <a name="domain-soap"></a>Domäne (SOAP)

Das **Domain** -Element enthält eine Verbunddomäne in einer **GetFederationInformation** -Antwort oder enthält eine Domäne, deren Konfigurationseinstellungen in einer **GetDomainSettings** -Anforderung angefordert werden. 
  
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
|[Domänen (SOAP)](domains-soap.md) <br/> |Stellt die Domänen dar, deren Konfigurationseinstellungen in einem **GetDomainSettings** -Vorgang zurückgegeben werden, oder die Domänen, in denen die Organisation einen **GetFederationInformation** -Vorgang Verbund hat.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **Domain** -Elements stellt einen Domänennamen dar. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |Auto Ermittlungs Schema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   

