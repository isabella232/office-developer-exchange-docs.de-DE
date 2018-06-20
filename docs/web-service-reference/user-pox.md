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
description: Das Element enthält benutzerspezifische Informationen.
ms.openlocfilehash: 3f90ff0cc00170170c7304f2a19fe1d7abd9d1bc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839432"
---
# <a name="user-pox"></a>Benutzer (POX)

**Das Element** enthält benutzerspezifische Informationen. 
  
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
|[DisplayName (Zeichenfolge)](displayname-string.md) <br/> |Anzeigenamen des Benutzers darstellt.  <br/> |
|[LegacyDN (POX)](legacydn-pox.md) <br/> |Postfach eines Benutzers identifiziert anhand der legacy-DN.  <br/> |
|[DeploymentId (POX)](deploymentid-pox.md) <br/> |Die Exchange-Gesamtstruktur identifiziert eindeutig.  <br/> |
|[AutoDiscoverSMTPAddress (POX)](autodiscoversmtpaddress-pox.md) <br/> |Enthält die SMTP-Adresse des Benutzers, die für die AutoErmittlung-Prozesses verwendet wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Response (POX)](response-pox.md) <br/> |Enthält die Antwort vom AutoErmittlungsdienst.  <br/> |
   
## <a name="remarks"></a>Hinweise

AutoErmittlung-Anforderungen und-Antworten müssen UTF-8 codiert sein.
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

