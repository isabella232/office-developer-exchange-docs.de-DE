---
title: ExternalUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3b647d88-6feb-40d7-9299-b2ca47b707db
description: Das ExternalUrl-Element enthält die URL zum Verbinden eines Clients mit dem Adressbuchserver oder dem Postfach eines Benutzers von außerhalb der Organisation des Benutzers mithilfe des MAPI/HTTP-Protokolls.
ms.openlocfilehash: 90aaf9cabedba4ea89e0ed47da010245006407ba
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510072"
---
# <a name="externalurl-pox"></a>ExternalUrl (POX)

Das **ExternalUrl-Element** enthält die URL zum Verbinden eines Clients mit dem Adressbuchserver oder dem Postfach eines Benutzers von außerhalb der Organisation des Benutzers mithilfe des MAPI/HTTP-Protokolls. 
  
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
|[AddressBook (POX)](addressbook-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Adressbuchserver mithilfe des MAPI/HTTP-Protokolls.  <br/> |
|[MailStore (POX)](mailstore-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Postfach des Benutzers mithilfe des MAPI/HTTP-Protokolls.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt eine URL dar, die für den Zugriff auf einen Adressbuchserver oder das Postfach eines Benutzers von außerhalb der Organisation des Benutzers verwendet werden kann.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das **ExternalUrl-Element** kann in einer Antwort vorhanden sein, die ein [POX-Element (Protocol)](protocol-pox.md) mit dem **Type-Attributwert** "mapiHttp" aufweist. 
  
Das **ExternalUrl-Element** ist für Clients verfügbar, die das MAPI/HTTP-Protokoll und die Ziel-Exchange Online, Exchange Online als Teil von Office 365 und lokale Versionen von Exchange ab Build 15.00.0847.032 (Exchange Server 2013 SP1) implementieren. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

