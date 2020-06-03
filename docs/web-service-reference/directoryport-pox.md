---
title: DirectoryPort (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ab436b54-ceba-4cd9-aeb4-134f9b93986d
description: Das DirectoryPort-Element gibt den Port an, der zum Herstellen einer Verbindung mit dem Verzeichnis verwendet wird, wenn das NSPI-Protokoll (Name Service Provider Interface) verwendet wird.
ms.openlocfilehash: 2ba0a15cea0b4eb9b6069fab384edb3d9747a360
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462087"
---
# <a name="directoryport-pox"></a>DirectoryPort (POX)

Das **DirectoryPort** -Element gibt den Port an, der zum Herstellen einer Verbindung mit dem Verzeichnis verwendet wird, wenn das NSPI-Protokoll (Name Service Provider Interface) verwendet wird. 
  
- [AutoErmittlung (POX)](autodiscover-pox.md) 
- [Response (POX)](response-pox.md)  
- [Konto (POX)](account-pox.md)  
- [Protokoll (POX)](protocol-pox.md)  
- [DirectoryPort (POX)](directoryport-pox.md)
  
```xml
<DirectoryPort/>
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert Text stellt den Port dar, der für den Zugriff auf den Exchange-Server verwendet wird.
  
## <a name="remarks"></a>Bemerkungen

Das **DirectoryPort** -Element wird nur verwendet, wenn der [Typ (POX)-](type-pox.md) Element mit dem Wert "$" oder "expr" identisch ist. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

