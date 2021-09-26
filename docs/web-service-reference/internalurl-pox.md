---
title: InternalUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4649baa9-eec9-426d-952b-361818c25fe0
description: Das InternalUrl-Element enthält die URL zum Verbinden eines Clients mit dem Adressbuchserver oder dem Postfach eines Benutzers innerhalb der Organisation des Benutzers mithilfe des MAPI/HTTP-Protokolls.
ms.openlocfilehash: 4ce04743c7d0f260439849a02f8f6d389f6c83fa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542196"
---
# <a name="internalurl-pox"></a>InternalUrl (POX)

Das **InternalUrl-Element** enthält die URL zum Verbinden eines Clients mit dem Adressbuchserver oder dem Postfach eines Benutzers innerhalb der Organisation des Benutzers mithilfe des MAPI/HTTP-Protokolls. 
  
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
|[AddressBook (POX)](addressbook-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Adressbuchserver mithilfe des MAPI/HTTP-Protokolls.  <br/> |
|[MailStore (POX)](mailstore-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Postfach des Benutzers mithilfe des MAPI/HTTP-Protokolls.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt eine URL dar, die für den Zugriff auf einen Adressbuchserver oder das Postfach eines Benutzers innerhalb der Organisation des Benutzers verwendet werden kann.
  
## <a name="remarks"></a>HinwBemerkungeneise

The **InternalUrl** element can be present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp". 
  
Das **InternalUrl-Element** ist für Clients verfügbar, die das MAPI/HTTP-Protokoll und die Ziel-Exchange Online implementieren, Exchange Online als Teil von Office 365 und lokale Versionen von Exchange ab Build 15.00.0847.032 (Exchange Server 2013 SP1). 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

