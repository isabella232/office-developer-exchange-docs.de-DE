---
title: RedirectAddr (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4
description: Das RedirectAddr-Element gibt die e-Mail-Adresse an, die für eine nachfolgende Auto Ermittlungsanforderung verwendet werden soll.
ms.openlocfilehash: 6bff28001851f421b4c7429770185401f2f0a743
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529875"
---
# <a name="redirectaddr-pox"></a>RedirectAddr (POX)

Das **RedirectAddr** -Element gibt die e-Mail-Adresse an, die für eine nachfolgende Auto Ermittlungsanforderung verwendet werden soll. 
  
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
|[Konto (POX)](account-pox.md) <br/> |Gibt Kontoeinstellungen für den Benutzer an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert Text stellt die e-Mail-Adresse dar, die für eine nachfolgende Auto Ermittlungsanforderung verwendet werden sollte.
  
## <a name="remarks"></a>Bemerkungen

Wenn dieses Element in der Auto Ermittlungs Antwort vorhanden ist, stellen Sie eine weitere Anforderung mithilfe des Textwerts des **RedirectAddr** -Elements. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

