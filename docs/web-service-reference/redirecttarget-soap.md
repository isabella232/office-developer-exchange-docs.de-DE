---
title: RedirectTarget (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f8162724-cf9a-4543-a1ad-5846c8b10bfa
description: Das RedirectTarget (SOAP)-Element enthält das Ziel der Umleitungs-URL oder der e-Mail-Adresse.
ms.openlocfilehash: 092d575560379d43b12dd98a3efa155b59c31450
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462199"
---
# <a name="redirecttarget-soap"></a>RedirectTarget (SOAP)

Das [RedirectTarget (SOAP)](redirecttarget-soap.md) -Element enthält das Ziel der Umleitungs-URL oder der e-Mail-Adresse. 
  
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
|[User Response (SOAP)](userresponse-soap.md) <br/> |Stellt eine Antwort auf eine GetUserSettings-Anforderung für einen einzelnen Benutzer dar.  <br/> |
|[DomainResponse (SOAP)](domainresponse-soap.md) <br/> |Enthält die angeforderten Einstellungen für die angegebene Domäne.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert enthält das Ziel der Umleitungs-URL oder e-Mail-Adresse, die für eine nachfolgende GetUserSettings-oder GetDomainSettings-Anforderung verwendet werden soll.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |Auto Ermittlungs Schema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   

