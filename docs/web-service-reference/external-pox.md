---
title: Externe (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8eed1f79-6eb3-4a88-80fb-d4edf9f34fda
description: Externe Element enthält eine Auflistung von URLs, die ein Client zum Verbinden mit Exchange von außerhalb des Netzwerks der Organisation verwenden können.
ms.openlocfilehash: 7f01fc29b5ce63b02de0a4a6e42887dcffbb4b82
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758358"
---
# <a name="external-pox"></a>Externe (POX)

**Externes** Element enthält eine Auflistung von URLs, die ein Client zum Verbinden mit Exchange von außerhalb des Netzwerks der Organisation verwenden können. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[Externe (POX)](external-pox.md)
  
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
|[OWAUrl (POX)](owaurl-pox.md) <br/> |Beschreibt die URL und Authentifizierung Schema, das verwendet wird, auf einen bestimmten Computer zugreifen, der Microsoft Exchange Server ausgeführt wird, hat die Clientzugriffs-Serverrolle installiert, die Outlook Web Access gehostet wird.  <br/> |
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist. Dieses **Protokoll** -Element hat nur zwei untergeordnete Elemente: ein Element einer [Typ (POX)](type-pox.md) , das Verbindungsprotokoll und ein [ASUrl (POX)](asurl-pox.md) -Element, EWS-Endpunkts für den Webdienst Verfügbarkeit angeben.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.  <br/> |
   
## <a name="remarks"></a>Hinweise

**Externes** Element ist ein optionales untergeordnetes Element des **Protokoll** -Elements. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

