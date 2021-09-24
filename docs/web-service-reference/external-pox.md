---
title: Extern (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 8eed1f79-6eb3-4a88-80fb-d4edf9f34fda
description: Das External-Element enthält eine Auflistung von URLs, die ein Client verwenden kann, um eine Verbindung mit Exchange von außerhalb des Netzwerks der Organisation herzustellen.
ms.openlocfilehash: 0e7e92029a01a25d5017d3b5199a7899403c975f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510099"
---
# <a name="external-pox"></a>Extern (POX)

Das **External-Element** enthält eine Auflistung von URLs, die ein Client zum Herstellen einer Verbindung mit Exchange von außerhalb des Unternehmensnetzwerks verwenden kann. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[Extern (POX)](external-pox.md)
  
```XML
<External>
   <OWAUrl/>
   <Protocol>
      <Type/>
      <ASUrl/>
   </Protocol>
</External>

```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[OWAUrl (POX)](owaurl-pox.md) <br/> |Beschreibt die URL und das Authentifizierungsschema, die für den Zugriff auf einen bestimmten Computer verwendet werden, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist, die Outlook Web Access hostet.  <br/> |
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen zum Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist. Dieses **Protokollelement** verfügt nur über zwei untergeordnete Elemente: ein [Type (POX)-Element,](type-pox.md) das das Verbindungsprotokoll angibt, und ein [ASUrl (POX)-Element,](asurl-pox.md) das den EWS-Endpunkt für den Verfügbarkeitswebdienst angibt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen zum Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **External-Element** ist ein optionales untergeordnetes Element des **Protocol-Elements.** 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

