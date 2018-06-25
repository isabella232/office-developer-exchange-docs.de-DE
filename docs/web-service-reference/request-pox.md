---
title: Anforderung (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: da54eb32-7ce5-4384-9893-255a2243a959
description: Das angeforderte Element enthält die Anforderung an den AutoErmittlungsdienst.
ms.openlocfilehash: ed6b0a80e83e160287f382a881dc5405bfb47a37
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831124"
---
# <a name="request-pox"></a>Anforderung (POX)

Das **angeforderte** Element enthält die Anforderung an den AutoErmittlungsdienst. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Anforderung (POX)](request-pox.md)
  
```xml
<Request>
   <AcceptableResponseSchema/>
   <EMailAddress/>
</Request>
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AcceptableResponseSchema (POX)](acceptableresponseschema-pox.md) <br/> |Das Schema für eine Antwort der AutoErmittlung identifiziert.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Identifiziert die e-Mail-Adresse des Benutzers an.  <br/> |
|[LegacyDN (POX)](legacydn-pox.md) <br/> |Postfach eines Benutzers identifiziert anhand der legacy-DN.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AutoErmittlung (POX)](autodiscover-pox.md) <br/> |Das Stammelement in einer autoermittlungsanforderung für die.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

