---
title: ExternalURL (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b647d88-6feb-40d7-9299-b2ca47b707db
description: Das ExternalURL-Element enthält die URL für das Verbinden eines Clients mit dem Adressbuchserver oder einem Benutzerpostfach von außerhalb der Organisation des Benutzers mithilfe des MAPI/http-Protokolls.
ms.openlocfilehash: 94265051be68ed06d1dab8d46dd4ce29d8694c93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457956"
---
# <a name="externalurl-pox"></a>ExternalURL (POX)

Das **ExternalURL** -Element enthält die URL für das Verbinden eines Clients mit dem Adressbuchserver oder einem Benutzerpostfach von außerhalb der Organisation des Benutzers mithilfe des MAPI/http-Protokolls. 
  
```XML
<ExternalUrl/>
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

Der Wert Text stellt eine URL dar, die für den Zugriff auf einen Adressbuchserver oder ein Benutzerpostfach von außerhalb der Organisation des Benutzers verwendet werden kann.
  
## <a name="remarks"></a>Bemerkungen

Das **ExternalURL** -Element kann in einer Antwort vorhanden sein, die ein [Protocol (POX)-](protocol-pox.md) Element mit dem **Type** -Attributwert "mapiHttp" aufweist. 
  
Das **ExternalURL** -Element steht für Clients zur Verfügung, die das MAPI/http-Protokoll und die Ziel Exchange Online implementieren, Exchange Online im Rahmen von Office 365 und lokalen Versionen von Exchange, beginnend mit Build 15.00.0847.032 (Exchange Server 2013 SP1). 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

