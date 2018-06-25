---
title: ExternalUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b647d88-6feb-40d7-9299-b2ca47b707db
description: Das ExternalUrl-Element enthält die URL für die Verbindung eines Clients mit der Adressbuchserver oder dem Postfach eines Benutzers von außerhalb der Organisation des Benutzers mithilfe des MAPI/HTTP-Protokolls.
ms.openlocfilehash: 603e2109e7b3c98acdd4cbc13df81ed9717630ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758396"
---
# <a name="externalurl-pox"></a>ExternalUrl (POX)

Das **ExternalUrl** -Element enthält die URL für die Verbindung eines Clients mit der Adressbuchserver oder dem Postfach eines Benutzers von außerhalb der Organisation des Benutzers mithilfe des MAPI/HTTP-Protokolls. 
  
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
|[AddressBook (POX)](addressbook-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit der Adressbuchserver mithilfe des MAPI/HTTP-Protokolls.  <br/> |
|[Postspeicher weitergeleitet (POX)](mailstore-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients an das Postfach des Benutzers mithilfe des MAPI/HTTP-Protokolls.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt eine URL, die Zugriff auf eine Adressbuchserver oder Postfach des Benutzers von außerhalb der Organisation des Benutzers verwendet werden kann.
  
## <a name="remarks"></a>Hinweise

Das Element **ExternalUrl** kann in einer Antwort vorhanden sein, die ein [Protokoll (POX)](protocol-pox.md) -Element mit dem Wert **Type** -Attribut "MapiHttp" hat. 
  
Das Element **ExternalUrl** ist von Clients, mit die die MAPI/HTTP-Protokoll und das Ziel Exchange Online, Exchange Online als Teil von Office 365, implementiert und lokale Versionen von Exchange, beginnend mit erstellen 15.00.0847.032 (Exchange Server 2013 SP1) . 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

