---
title: InternalURL (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4649baa9-eec9-426d-952b-361818c25fe0
description: Das InternalURL-Element enthält die URL für das Verbinden eines Clients mit dem Adressbuchserver oder dem Postfach eines Benutzers in der Organisation des Benutzers mithilfe des MAPI/http-Protokolls.
ms.openlocfilehash: 9c6ba621a681ec54d88089de6b7ae1eefdebc679
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465576"
---
# <a name="internalurl-pox"></a>InternalURL (POX)

Das **InternalURL** -Element enthält die URL für das Verbinden eines Clients mit dem Adressbuchserver oder dem Postfach eines Benutzers in der Organisation des Benutzers mithilfe des MAPI/http-Protokolls. 
  
```XML
<InternalUrl/>
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Adressbuch (POX)](addressbook-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Adressbuchserver mithilfe des MAPI/http-Protokolls.  <br/> |
|[MailStore (POX)](mailstore-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Postfach des Benutzers mithilfe des MAPI/http-Protokolls.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt eine URL dar, die für den Zugriff auf einen Adressbuchserver oder ein Benutzerpostfach in der Organisation des Benutzers verwendet werden kann.
  
## <a name="remarks"></a>Bemerkungen

Das **InternalURL** -Element kann in einer Antwort vorhanden sein, die ein [Protocol (POX)-](protocol-pox.md) Element mit dem **Type** -Attributwert "mapiHttp" aufweist. 
  
Das **InternalURL** -Element steht für Clients zur Verfügung, die das MAPI/http-Protokoll und die Ziel Exchange Online implementieren, Exchange Online im Rahmen von Office 365 und lokalen Versionen von Exchange, beginnend mit Build 15.00.0847.032 (Exchange Server 2013 SP1). 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

