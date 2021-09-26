---
title: DirectoryPort (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: ab436b54-ceba-4cd9-aeb4-134f9b93986d
description: Das DirectoryPort-Element gibt den Port an, der zum Herstellen einer Verbindung mit dem Verzeichnis verwendet wird, wenn das NSPI-Protokoll (Name Service Provider Interface) verwendet wird.
ms.openlocfilehash: 223e82840628e19896bde196d7467622a2ad5002
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543331"
---
# <a name="directoryport-pox"></a>DirectoryPort (POX)

Das **DirectoryPort-Element** gibt den Port an, der zum Herstellen einer Verbindung mit dem Verzeichnis verwendet wird, wenn das NSPI-Protokoll (Name Service Provider Interface) verwendet wird. 
  
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen zum Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt den Port dar, der für den Zugriff auf den Exchange Server verwendet wird.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das **DirectoryPort-Element** wird nur verwendet, wenn das [Type (POX)-Element](type-pox.md) EXCH oder EXPR entspricht. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

