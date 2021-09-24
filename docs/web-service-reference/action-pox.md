---
title: Aktion (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: a3462c6b-453c-462a-830d-f29ee4a2babb
description: Das Action-Element stellt Informationen bereit, die verwendet werden, um zu bestimmen, ob eine andere AutoErmittlungsanforderung erforderlich ist, um die Benutzerkonfigurationsinformationen zurückzugeben.
ms.openlocfilehash: b1c07fefc6b8033b9b93bd044c04fb07ba289177
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513857"
---
# <a name="action-pox"></a>Aktion (POX)

Das **Action-Element** stellt Informationen bereit, die verwendet werden, um zu bestimmen, ob eine andere AutoErmittlungsanforderung erforderlich ist, um die Benutzerkonfigurationsinformationen zurückzugeben. 
  
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
|[Konto (POX)](account-pox.md) <br/> |Gibt die Kontoeinstellungen für den Benutzer an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert gibt an, ob eine weitere AutoErmittlungsanforderung erforderlich ist, um die Konfigurationsinformationen des Benutzers abzurufen. In der folgenden Tabelle sind die möglichen Werte aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|redirectUrl  <br/> |Wenn dieser Wert angegeben ist, gibt das [RedirectUrl (POX)-Element](redirecturl-pox.md) die Clientzugriffsserver-URL an, die in der nachfolgenden AutoErmittlungsanforderung verwendet werden soll. Die Clientanwendung sollte die Umleitung nach 10 Umleitungen beenden.  <br/> |
|redirectAddr  <br/> |Wenn dieser Wert angegeben ist, gibt das [RedirectAddr (POX)-Element](redirectaddr-pox.md) die E-Mail-Adresse an, die für eine nachfolgende AutoErmittlungsanforderung verwendet werden soll.  <br/> |
|Einstellungen  <br/> |Wenn dieser Wert angegeben ist, enthält die AutoErmittlungsantwort Einstellungen, die zum Konfigurieren des Kontos verwendet werden. Die meisten Einstellungen finden Sie im [POX-Element (Protocol).](protocol-pox.md)  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

