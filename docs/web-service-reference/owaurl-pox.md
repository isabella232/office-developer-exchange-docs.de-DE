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
description: Das OWAUrl-Element beschreibt die URL und Authentifizierung Schema, das verwendet wird, auf einen bestimmten Computer zugreifen, der Microsoft Exchange Server 2007 ausgeführt wird, hat die Clientzugriffs-Serverrolle installiert, die Outlook Web Access gehostet wird.
ms.openlocfilehash: 93d03506e2a74aa1b4ef6d2a49ccbda01cfc1f9a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830673"
---
# <a name="owaurl-pox"></a>OWAUrl (POX)

Das **OWAUrl** -Element beschreibt die URL und Authentifizierung Schema, das verwendet wird, auf einen bestimmten Computer zugreifen, der Microsoft Exchange Server 2007 ausgeführt wird, hat die Clientzugriffs-Serverrolle installiert, die Outlook Web Access gehostet wird. 
  
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
   
#### <a name="authenticationmethod-attribute"></a>AuthenticationMethod--Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|WindowsIntegrated  <br/> |Integrierte Windows-Authentifizierung.  <br/> |
|FBA  <br/> |Formularbasierte Authentifizierung.  <br/> |
|NTLM  <br/> |NTLM-Authentifizierung.  <br/> |
|Digest  <br/> |Digest-Authentifizierung.  <br/> |
|Standard  <br/> |Standardauthentifizierung.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Interne (POX)](internal-pox.md) <br/> |Enthält die Auflistung von Outlook Web Access-URLs, die ein Client herstellen kann, wenn es innerhalb der Firewall ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt die URL für die Outlook Web Access-Dienst auf einem Clientzugriffsserver.
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

