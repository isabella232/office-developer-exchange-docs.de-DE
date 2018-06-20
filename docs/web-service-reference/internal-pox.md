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
description: Das interne Element enthält die Auflistung von URLs, die ein Client zum Verbinden mit Exchange von innerhalb des Netzwerks der Organisation verwenden können.
ms.openlocfilehash: 0dc5b679af98b52f15ef3b40181c2d97f102f373
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829946"
---
# <a name="internal-pox"></a>Interne (POX)

Das **Internal** -Element enthält die Auflistung von URLs, die ein Client zum Verbinden mit Exchange von innerhalb des Netzwerks der Organisation verwenden können. 
  
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
|[OWAUrl (POX)](owaurl-pox.md) <br/> |Beschreibt die URL und Authentifizierung Schema, das verwendet wird, auf einen bestimmten Computer zugreifen, der Microsoft Exchange Server ausgeführt wird, hat die Clientzugriffs-Serverrolle installiert, die Outlook Web Access gehostet wird.  <br/> |
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist. Dieses **Protokoll** -Element hat nur zwei untergeordnete Elemente: ein Element einer [Typ (POX)](type-pox.md) , das Verbindungsprotokoll und ein [ASUrl (POX)](asurl-pox.md) -Element, EWS-Endpunkts für den Webdienst Verfügbarkeit angeben.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **Internal** -Element ist ein optionales untergeordnetes Element des **Protokoll** -Elements. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

