---
title: Postspeicher weitergeleitet (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af338f99-9e62-4124-9bff-8d7cc2008161
description: Das Postspeicher bezeichnet-Element enthält die Spezifikationen für die Verbindung eines Clients an das Postfach des Benutzers mithilfe des MAPI/HTTP-Protokolls.
ms.openlocfilehash: 4c82c7b61752cf7d91287a3968f6c642f4943855
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830301"
---
# <a name="mailstore-pox"></a>Postspeicher weitergeleitet (POX)

Das **Postspeicher bezeichnet** -Element enthält die Spezifikationen für die Verbindung eines Clients an das Postfach des Benutzers mithilfe des MAPI/HTTP-Protokolls. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[Postspeicher weitergeleitet (POX)](mailstore-pox.md)
  
```XML
<MailStore>
   <ExternalUrl/>
   <InternalUrl/>
</MailStore>
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ExternalUrl (POX)](externalurl-pox.md) <br/> |Enthält die URL, die zum Zugriff auf das Postfach des Benutzers von außerhalb des Netzwerks der Organisation über das MAPI/HTTP-Protokoll verwendet werden soll.  <br/> |
|[InternalUrl (POX)](internalurl-pox.md) <br/> |Enthält die URL, die zum Zugriff auf das Postfach des Benutzers aus im Netzwerk der Organisation über das MAPI/HTTP-Protokoll verwendet werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Clientzugriffsserver an.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Element **Postspeicher bezeichnet** ist in eine Antwort, die ein [Protokoll (POX)](protocol-pox.md) -Element mit dem **Type** -Attributwert "MapiHttp" ist vorhanden. 
  
**Postspeicher bezeichnet** -Element wird von Clients, mit die die MAPI/HTTP-Protokoll und das Ziel Exchange Online, Exchange Online als Teil von Office 365, implementiert und lokale Versionen von Exchange, beginnend mit 15.00.0847.032 (Exchange Server 2013 SP1) erstellen. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

