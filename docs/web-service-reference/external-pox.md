---
title: Extern (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8eed1f79-6eb3-4a88-80fb-d4edf9f34fda
description: Das externe Element enthält eine Sammlung von URLs, die ein Client für die Verbindung mit Exchange von außerhalb des Netzwerks der Organisation verwenden kann.
ms.openlocfilehash: 45d7e72c5a43c5c468c1edd303a5e5ea8c2cb62e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457970"
---
# <a name="external-pox"></a>Extern (POX)

Das **externe** Element enthält eine Sammlung von URLs, die ein Client für die Verbindung mit Exchange von außerhalb des Netzwerks der Organisation verwenden kann. 
  
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
|[OWAUrl (POX)](owaurl-pox.md) <br/> |Beschreibt die URL und das Authentifizierungsschema, das für den Zugriff auf einen bestimmten Computer verwendet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist, die Outlook Web Access hostet.  <br/> |
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist. Dieses **Protokoll** Element hat nur zwei untergeordnete Elemente: ein [Type (POX)](type-pox.md) -Element, das das Verbindungsprotokoll angibt, und ein [vom asurl (POX)](asurl-pox.md) -Element, das den EWS-Endpunkt für den Verfügbarkeits-Webdienst angibt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das **externe** Element ist ein optionales untergeordnetes Element des **Protocol** -Elements. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

