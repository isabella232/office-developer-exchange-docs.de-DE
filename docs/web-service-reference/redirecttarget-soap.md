---
title: RedirectTarget (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: f8162724-cf9a-4543-a1ad-5846c8b10bfa
description: Das SOAP-Element (RedirectTarget) enthält das Ziel der Umleitungs-URL oder E-Mail-Adresse.
ms.openlocfilehash: 0e09529f62dfde66f1ef05875bb0b0a0886db452
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513542"
---
# <a name="redirecttarget-soap"></a>RedirectTarget (SOAP)

Das [SOAP-Element (RedirectTarget)](redirecttarget-soap.md) enthält das Ziel der Umleitungs-URL oder E-Mail-Adresse. 
  
```XML
<RedirectTarget/>
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
|[UserResponse (SOAP)](userresponse-soap.md) <br/> |Stellt eine Antwort auf eine GetUserSettings-Anforderung für einen einzelnen Benutzer dar.  <br/> |
|[DomainResponse (SOAP)](domainresponse-soap.md) <br/> |Enthält die angeforderten Einstellungen für die angegebene Domäne.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert enthält das Ziel der Umleitungs-URL oder E-Mail-Adresse, die für eine nachfolgende GetUserSettings- oder GetDomainSettings-Anforderung verwendet werden soll.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   

