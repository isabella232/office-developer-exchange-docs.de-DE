---
title: MailStore (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: af338f99-9e62-4124-9bff-8d7cc2008161
description: Das MailStore-Element enthält die Spezifikationen zum Verbinden eines Clients mit dem Postfach des Benutzers mithilfe des MAPI/HTTP-Protokolls.
ms.openlocfilehash: 543bcb8df84904f2b70d6feeabf16d1cc021f3e5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511122"
---
# <a name="mailstore-pox"></a>MailStore (POX)

Das **MailStore-Element** enthält die Spezifikationen zum Verbinden eines Clients mit dem Postfach des Benutzers mithilfe des MAPI/HTTP-Protokolls. 
  
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
|[ExternalUrl (POX)](externalurl-pox.md) <br/> |Enthält die URL, die verwendet werden soll, um über das MAPI/HTTP-Protokoll von außerhalb des Unternehmensnetzwerks auf das Postfach des Benutzers zuzugreifen.  <br/> |
|[InternalUrl (POX)](internalurl-pox.md) <br/> |Enthält die URL, die verwendet werden soll, um über das MAPI/HTTP-Protokoll innerhalb des Unternehmensnetzwerks auf das Postfach des Benutzers zuzugreifen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen zum Verbinden eines Clients mit dem Clientzugriffsserver.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **MailStore-Element** ist in einer Antwort vorhanden, die ein [POX-Element (Protocol)](protocol-pox.md) mit dem **Type-Attributwert** "mapiHttp" aufweist. 
  
Das **MailStore-Element** ist für Clients verfügbar, die das MAPI/HTTP-Protokoll und die Ziel-Exchange Online implementieren, Exchange Online als Teil von Office 365 und lokale Versionen von Exchange ab Build 15.00.0847.032 (Exchange Server 2013 SP1). 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

