---
title: AddressBook (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b2d62fd0-741c-4a41-9762-cc7d0ff01c9c
description: Das AddressBook-Element enthält die Spezifikationen zum Verbinden eines Clients mit dem Adressbuchserver mithilfe des MAPI/HTTP-Protokolls.
ms.openlocfilehash: 28de1d41146b082c8b7f82c868fbbed1ce2c483e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546798"
---
# <a name="addressbook-pox"></a>AddressBook (POX)

Das **AddressBook-Element** enthält die Spezifikationen zum Verbinden eines Clients mit dem Adressbuchserver mithilfe des MAPI/HTTP-Protokolls. 
  
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
|[ExternalUrl (POX)](externalurl-pox.md) <br/> |Enthält die URL, die für den Zugriff auf das Adressbuch von außerhalb des Netzwerks der Organisation mithilfe des MAPI/HTTP-Protokolls verwendet werden soll.  <br/> |
|[InternalUrl (POX)](internalurl-pox.md) <br/> |Enthält die URL, die für den Zugriff auf das Adressbuch innerhalb des Netzwerks der Organisation mithilfe des MAPI/HTTP-Protokolls verwendet werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen zum Verbinden eines Clients mit dem Clientzugriffsserver.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **AddressBook-Element** ist in einer Antwort vorhanden, die ein [POX-Element (Protocol)](protocol-pox.md) mit dem **Type-Attributwert** "mapiHttp" aufweist. 
  
Das **AddressBook-Element** ist für Clients verfügbar, die das MAPI/HTTP-Protokoll und die Ziel-Exchange Online, Exchange Online als Teil Office 365 und lokale Versionen von Exchange ab Build 15.00.0847.032 (Exchange Server 2013 SP1) implementieren. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

