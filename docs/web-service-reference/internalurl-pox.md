---
title: InternalUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4649baa9-eec9-426d-952b-361818c25fe0
description: Das InternalUrl-Element enthält die URL für die Verbindung eines Clients mit der Adressbuchserver oder dem Postfach eines Benutzers von innerhalb der Organisation des Benutzers mithilfe des MAPI/HTTP-Protokolls.
ms.openlocfilehash: 3823236081961128b31bb2c0f563062897c55814
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829950"
---
# <a name="internalurl-pox"></a>InternalUrl (POX)

Das **InternalUrl** -Element enthält die URL für die Verbindung eines Clients mit der Adressbuchserver oder dem Postfach eines Benutzers von innerhalb der Organisation des Benutzers mithilfe des MAPI/HTTP-Protokolls. 
  
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
|[AddressBook (POX)](addressbook-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit der Adressbuchserver mithilfe des MAPI/HTTP-Protokolls.  <br/> |
|[Postspeicher weitergeleitet (POX)](mailstore-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients an das Postfach des Benutzers mithilfe des MAPI/HTTP-Protokolls.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt eine URL, die Zugriff auf eine Adressbuchserver oder Postfach des Benutzers aus innerhalb der Organisation des Benutzers verwendet werden kann.
  
## <a name="remarks"></a>Hinweise

Das Element **InternalUrl** kann in einer Antwort vorhanden sein, die ein [Protokoll (POX)](protocol-pox.md) -Element mit dem Wert **Type** -Attribut "MapiHttp" hat. 
  
Das **InternalUrl** -Element wird von Clients, mit die die MAPI/HTTP-Protokoll und das Ziel Exchange Online, Exchange Online als Teil von Office 365, implementiert und lokale Versionen von Exchange, beginnend mit erstellen 15.00.0847.032 (Exchange Server 2013 SP1) . 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

