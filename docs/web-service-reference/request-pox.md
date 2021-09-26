---
title: Anforderung (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: da54eb32-7ce5-4384-9893-255a2243a959
description: Das Request-Element enthält die Anforderung an den AutoErmittlungsdienst.
ms.openlocfilehash: 91bc9cad6df976e8a8500eecc997f573a7df7289
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542833"
---
# <a name="request-pox"></a>Anforderung (POX)

Das **Request-Element** enthält die Anforderung an den AutoErmittlungsdienst. 
  
- [AutoErmittlung (POX)](autodiscover-pox.md) 
- [Anforderung (POX)](request-pox.md)
  
```xml
<Request>
   <AcceptableResponseSchema/>
   <EMailAddress/>
</Request>
```

```xml
<Request>
   <AcceptableResponseSchema/> 
   <LegacyDN/>
</Request>
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AcceptableResponseSchema (POX)](acceptableresponseschema-pox.md) <br/> |Identifiziert das Schema für eine AutoErmittlungsantwort.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Identifiziert die E-Mail-Adresse des Benutzers.  <br/> |
|[LegacyDN (POX)](legacydn-pox.md) <br/> |Identifiziert das Postfach eines Benutzers anhand eines älteren Distinguished Name.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AutoErmittlung (POX)](autodiscover-pox.md) <br/> |Das Stammelement in einer AutoErmittlungsanforderung.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

