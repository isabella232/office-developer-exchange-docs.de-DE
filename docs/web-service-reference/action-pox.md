---
title: Aktion (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a3462c6b-453c-462a-830d-f29ee4a2babb
description: Das Action-Element enthält Informationen, die verwendet werden, um zu bestimmen, ob eine andere Auto Ermittlungsanforderung erforderlich ist, um die Benutzerkonfigurationsinformationen zurückzugeben.
ms.openlocfilehash: f6d542b908948d09020b850b60ca1bdb025dd342
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529693"
---
# <a name="action-pox"></a>Aktion (POX)

Das **Action** -Element enthält Informationen, die verwendet werden, um zu bestimmen, ob eine andere Auto Ermittlungsanforderung erforderlich ist, um die Benutzerkonfigurationsinformationen zurückzugeben. 
  
- [AutoErmittlung (POX)](autodiscover-pox.md)
  
- [Response (POX)](response-pox.md)
  
- [Konto (POX)](account-pox.md)
  
- [Aktion (POX)](action-pox.md)
  
```xml
<Action>redirectUrl or redirectAddr or settings</Action>
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

Der Text-Wert gibt an, ob eine andere Auto Ermittlungsanforderung zum Abrufen der Konfigurationsinformationen des Benutzers erforderlich ist. In der folgenden Tabelle sind die möglichen Werte aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|redirectUrl  <br/> |Wenn dieser Wert angegeben ist, gibt das [RedirectUrl (POX)-](redirecturl-pox.md) Element die Client Zugriffsserver-URL an, die in der nachfolgenden Auto Ermittlungsanforderung verwendet werden soll. Die Clientanwendung sollte die Umleitung nach 10 Umleitungen beenden.  <br/> |
|redirectAddr  <br/> |Wenn dieser Wert angegeben ist, gibt das [RedirectAddr (POX)](redirectaddr-pox.md) -Element die e-Mail-Adresse an, die für eine nachfolgende Auto Ermittlungsanforderung verwendet werden soll.  <br/> |
|settings  <br/> |Wenn dieser Wert angegeben ist, enthält die Auto Ermittlungs Antworteinstellungen, die zum Konfigurieren des Kontos verwendet werden. Die meisten Einstellungen finden Sie im [Protokoll (POX)](protocol-pox.md) -Element.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

