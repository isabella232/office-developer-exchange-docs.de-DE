---
title: Antwort (POX)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 002b72f2-f94d-467c-8e6c-b3818f7e51dc
description: 'Gilt für:'
ms.openlocfilehash: d613bbb1d8573c1eb60c053ddc064f564676a7c4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523482"
---
# <a name="response-pox"></a>Antwort (POX)


  
Das **Response-Element** enthält die Antwort des AutoErmittlungsdiensts. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
```xml
<Response>
   <User/>
   <Account/>
</Response>
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Benutzer (POX)](user-pox.md) <br/> |Stellt benutzerspezifische Informationen bereit. Dieses Element ist optional.  <br/> |
|[Konto (POX)](account-pox.md) <br/> |Gibt die Kontoeinstellungen für den Benutzer an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AutoErmittlung (POX)](autodiscover-pox.md) <br/> |Das Stammelement in einer AutoErmittlungsantwort.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

