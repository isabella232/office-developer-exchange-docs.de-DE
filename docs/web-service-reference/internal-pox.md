---
title: Interne (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 69c22546-ebd6-4a03-b0b4-bbac72ec5551
description: Das internal-Element enthält die Auflistung von URLs, die ein Client für die Verbindung mit Exchange aus dem Netzwerk der Organisation verwenden kann.
ms.openlocfilehash: 8164a018a11f9bae9c3abcbfebf6cf0694ca4183
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465597"
---
# <a name="internal-pox"></a>Interne (POX)

Das **internal** -Element enthält die Auflistung von URLs, die ein Client für die Verbindung mit Exchange aus dem Netzwerk der Organisation verwenden kann. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[Interne (POX)](internal-pox.md)
  
```xml
<Internal>
   <OWAUrl/>
   <Protocol>
      <Type/>
      <ASUrl/>
   </Protocol>
</Internal>
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

Das **internal** -Element ist ein optionales untergeordnetes Element des **Protocol** -Elements. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

