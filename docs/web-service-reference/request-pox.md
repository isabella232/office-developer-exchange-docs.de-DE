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
description: Das Request-Element enthält die Anforderung an den AutoErmittlungsdienst.
ms.openlocfilehash: bc215d614441ed8f12c0f1490f4abdbb7b574ad0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459546"
---
# <a name="request-pox"></a>Anforderung (POX)

Das **Request** -Element enthält die Anforderung an den AutoErmittlungsdienst. 
  
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
|[AcceptableResponseSchema (POX)](acceptableresponseschema-pox.md) <br/> |Gibt das Schema für eine Auto Ermittlungs Antwort an.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Gibt die e-Mail-Adresse des Benutzers an.  <br/> |
|[LegacyDN (POX)](legacydn-pox.md) <br/> |Identifiziert das Postfach eines Benutzers anhand des Distinguished Name-Legacy namens.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AutoErmittlung (POX)](autodiscover-pox.md) <br/> |Das Stammelement in einer Auto Ermittlungsanforderung.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

