---
title: AddressBook (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b2d62fd0-741c-4a41-9762-cc7d0ff01c9c
description: Das AddressBook-Element enthält die Spezifikationen für die Verbindung eines Clients mit der Adressbuchserver mithilfe des MAPI/HTTP-Protokolls.
ms.openlocfilehash: c30f0ee7c36de7e63157d07d003a11187d661fd7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757237"
---
# <a name="addressbook-pox"></a>AddressBook (POX)

Das **AddressBook** -Element enthält die Spezifikationen für die Verbindung eines Clients mit der Adressbuchserver mithilfe des MAPI/HTTP-Protokolls. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[AddressBook (POX)](addressbook-pox.md)
  
```XML
<AddressBook>
   <ExternalUrl/>
   <InternalUrl/>
</AddressBook>
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ExternalUrl (POX)](externalurl-pox.md) <br/> |Enthält die URL, die zum Adressbuch von außerhalb des Netzwerks der Organisation zugreifen, indem Sie mit dem MAPI/HTTP-Protokoll verwendet werden soll.  <br/> |
|[InternalUrl (POX)](internalurl-pox.md) <br/> |Enthält die URL, die zum Adressbuch von innerhalb des Netzwerks der Organisation zugreifen, indem Sie mit dem MAPI/HTTP-Protokoll verwendet werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Clientzugriffsserver an.  <br/> |
   
## <a name="remarks"></a>Hinweise

**AddressBook** -Element ist in einer Antwort, die ein [Protokoll (POX)](protocol-pox.md) -Element mit dem **Type** -Attributwert "MapiHttp" ist vorhanden. 
  
**AddressBook** -Element wird von Clients, mit die die MAPI/HTTP-Protokoll und das Ziel Exchange Online, Exchange Online als Teil von Office 365, implementiert und lokale Versionen von Exchange, beginnend mit erstellen 15.00.0847.032 (Exchange Server 2013 SP1) . 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

