---
title: MailStore (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af338f99-9e62-4124-9bff-8d7cc2008161
description: Das MailStore-Element enthält die Spezifikationen für die Verbindung eines Clients mit dem Postfach des Benutzers mithilfe des MAPI/http-Protokolls.
ms.openlocfilehash: 635228fcfeb3ad791c845050b82666a6e060b229
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459791"
---
# <a name="mailstore-pox"></a>MailStore (POX)

Das **MailStore** -Element enthält die Spezifikationen für die Verbindung eines Clients mit dem Postfach des Benutzers mithilfe des MAPI/http-Protokolls. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[MailStore (POX)](mailstore-pox.md)
  
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
|[ExternalURL (POX)](externalurl-pox.md) <br/> |Enthält die URL, die verwendet werden sollte, um über das MAPI/http-Protokoll von außerhalb des Netzwerks des Unternehmens auf das Postfach des Benutzers zuzugreifen.  <br/> |
|[InternalURL (POX)](internalurl-pox.md) <br/> |Enthält die URL, die für den Zugriff auf das Postfach des Benutzers im Netzwerk des Unternehmens über das MAPI/http-Protokoll verwendet werden sollte.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Clientzugriffsserver.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das **MailStore** -Element ist in einer Antwort vorhanden, die ein [Protocol (POX)-](protocol-pox.md) Element mit dem **Type** -Attributwert "mapiHttp" aufweist. 
  
Das **MailStore** -Element steht für Clients zur Verfügung, die das MAPI/http-Protokoll und die Ziel Exchange Online implementieren, Exchange Online im Rahmen von Office 365 und lokalen Versionen von Exchange, beginnend mit Build 15.00.0847.032 (Exchange Server 2013 SP1). 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

