---
title: OWAUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 450b86a1-1722-49f5-b541-16c1edc3db7a
description: Das OWAUrl-Element beschreibt die URL und das Authentifizierungsschema, das verwendet wird, um auf einen bestimmten Computer zuzugreifen, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist, die Outlook Web Access hostet.
ms.openlocfilehash: c0728af063cfbf1353eb7d3b81f5fcfe8b398f7d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457263"
---
# <a name="owaurl-pox"></a>OWAUrl (POX)

Das **OWAUrl** -Element beschreibt die URL und das Authentifizierungsschema, das verwendet wird, um auf einen bestimmten Computer zuzugreifen, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist, die Outlook Web Access hostet. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[Interne (POX)](internal-pox.md)
  
[OWAUrl (POX)](owaurl-pox.md)
  
```xml
<OWAUrl AuthenticationMethod=""/>
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**AuthenticationMethod** <br/> |Beschreibt die Authentifizierungsmethoden für den Zugriff auf Outlook Web Access.  <br/> |
   
#### <a name="authenticationmethod-attribute"></a>AuthenticationMethod-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|WindowsIntegrated  <br/> |Integrierte Windows-Authentifizierung.  <br/> |
|FBA  <br/> |Formularbasierte Authentifizierung.  <br/> |
|NTLM  <br/> |NTLM-Authentifizierung.  <br/> |
|Digest  <br/> |Digest-Authentifizierung.  <br/> |
|Basic  <br/> |Standardauthentifizierung.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Interne (POX)](internal-pox.md) <br/> |Enthält die Sammlung von Outlook Web Access-URLs, mit denen ein Client eine Verbindung herstellen kann, wenn er sich innerhalb der Firewall befindet.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert Text stellt die URL für den Outlook Web Access Dienst auf einem Client Zugriffsserver dar.
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

