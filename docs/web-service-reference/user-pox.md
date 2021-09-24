---
title: Benutzer (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 7c42b516-77f6-4aee-99d8-b866d82d793a
description: Das User-Element stellt benutzerspezifische Informationen bereit.
ms.openlocfilehash: 832e0a63e75a08406b3aa397ac29ad5aa300cfe0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522406"
---
# <a name="user-pox"></a>Benutzer (POX)

Das **User-Element** stellt benutzerspezifische Informationen bereit. 
  
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
|[LegacyDN (POX)](legacydn-pox.md) <br/> |Identifiziert das Postfach eines Benutzers anhand eines älteren Distinguished Name.  <br/> |
|[DeploymentId (POX)](deploymentid-pox.md) <br/> |Identifiziert die Exchange Gesamtstruktur eindeutig.  <br/> |
|[AutoDiscoverSMTPAddress (POX)](autodiscoversmtpaddress-pox.md) <br/> |Enthält die SMTP-Adresse des Benutzers, die für den AutoErmittlungsprozess verwendet wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Response (POX)](response-pox.md) <br/> |Enthält die Antwort des AutoErmittlungsdiensts.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

AutoErmittlungsanforderungen und -antworten müssen UTF-8-codiert sein.
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

