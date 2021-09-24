---
title: RedirectAddr (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4
description: Das RedirectAddr-Element gibt die E-Mail-Adresse an, die für eine nachfolgende AutoErmittlungsanforderung verwendet werden soll.
ms.openlocfilehash: 75db62a84ccce743e73c812082ab9dbbc4fdb1cd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540594"
---
# <a name="redirectaddr-pox"></a>RedirectAddr (POX)

Das **RedirectAddr-Element** gibt die E-Mail-Adresse an, die für eine nachfolgende AutoErmittlungsanforderung verwendet werden soll. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[RedirectAddr (POX)](redirectaddr-pox.md)
  
```xml
<RedirectAddr/>
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
|[Konto (POX)](account-pox.md) <br/> |Gibt die Kontoeinstellungen für den Benutzer an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt die E-Mail-Adresse dar, die für eine nachfolgende AutoErmittlungsanforderung verwendet werden soll.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn dieses Element in der AutoErmittlungsantwort vorhanden ist, stellen Sie eine weitere Anforderung mithilfe des Textwerts des **RedirectAddr-Elements.** 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

