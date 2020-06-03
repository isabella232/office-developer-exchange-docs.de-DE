---
title: Benutzer (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 7c42b516-77f6-4aee-99d8-b866d82d793a
description: Das User-Element enthält benutzerspezifische Informationen.
ms.openlocfilehash: 8f53319bcf34595305748adafc9aa1e25283611e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530218"
---
# <a name="user-pox"></a>Benutzer (POX)

Das **User** -Element enthält benutzerspezifische Informationen. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Benutzer (POX)](user-pox.md)
  
```xml
<User>
   <DisplayName/>
   <LegacyDN/>
   <DeploymentId/>
   <AutoDiscoverSMTPAddress/>
</User>
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DisplayName (Zeichenfolge)](displayname-string.md) <br/> |Stellt den Anzeigenamen des Benutzers dar.  <br/> |
|[LegacyDN (POX)](legacydn-pox.md) <br/> |Identifiziert das Postfach eines Benutzers anhand des Distinguished Name-Legacy namens.  <br/> |
|[DeploymentId (POX)](deploymentid-pox.md) <br/> |Identifiziert die Exchange-Gesamtstruktur eindeutig.  <br/> |
|[AutoDiscoverSMTPAddress (POX)](autodiscoversmtpaddress-pox.md) <br/> |Enthält die SMTP-Adresse des Benutzers, die für den Auto Ermittlungsprozess verwendet wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Response (POX)](response-pox.md) <br/> |Enthält die Antwort des AutoErmittlungsdiensts.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

AutoErmittlung-Anforderungen und-Antworten müssen UTF-8-codiert sein.
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

