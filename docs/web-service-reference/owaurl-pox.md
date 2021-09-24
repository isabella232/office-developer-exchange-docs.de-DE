---
title: OWAUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 450b86a1-1722-49f5-b541-16c1edc3db7a
description: Das OWAUrl-Element beschreibt die URL und das Authentifizierungsschema, die für den Zugriff auf einen bestimmten Computer verwendet werden, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist, die Outlook Web Access hostet.
ms.openlocfilehash: fbd61eb75018c57dada40f5ed7472379d365e752
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59534891"
---
# <a name="owaurl-pox"></a>OWAUrl (POX)

Das **OWAUrl-Element** beschreibt die URL und das Authentifizierungsschema, das für den Zugriff auf einen bestimmten Computer verwendet wird, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist, die Outlook Web Access hostet. 
  
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
|Digest  <br/> |Digestauthentifizierung.  <br/> |
|Standard  <br/> |Standardauthentifizierung.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Interne (POX)](internal-pox.md) <br/> |Enthält die Auflistung von Outlook Web Access-URLs, mit denen ein Client eine Verbindung herstellen kann, wenn er sich innerhalb der Firewall befindet.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt die URL für den Outlook Web Access-Dienst auf einem Clientzugriffsserver dar.
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

