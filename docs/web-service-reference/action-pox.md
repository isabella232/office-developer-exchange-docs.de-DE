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
description: Das Action-Element enthält Informationen, die verwendet wird, um festzustellen, ob eine andere autoermittlungsanforderung erforderlich ist, um die Informationen der Benutzerkonfiguration zurückzugeben.
ms.openlocfilehash: 118bb59f2c929e3c74683dbf3f073da34d67a3e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758383"
---
# <a name="action-pox"></a>Aktion (POX)

Das **Action** -Element enthält Informationen, die verwendet wird, um festzustellen, ob eine andere autoermittlungsanforderung erforderlich ist, um die Informationen der Benutzerkonfiguration zurückzugeben. 
  
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
|[Konto (POX)](account-pox.md) <br/> |Gibt die kontoeinstellungen für den Benutzer an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert der angibt, ob einer anderen autoermittlungsanforderung erforderlich sind, um die Konfigurationsinformationen des Benutzers abgerufen wird. In der folgenden Tabelle sind die möglichen Werte aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|redirectUrl  <br/> |Wenn dieser Wert angegeben ist, wird das Element [RedirectUrl (POX)](redirecturl-pox.md) die Clientzugriffs-Server-URL in der nachfolgenden Anforderung der AutoErmittlung verwendet werden angeben. Die Clientanwendung sollte beenden umleiten nach 10 umleitungen zulässig.  <br/> |
|redirectAddr  <br/> |Wenn dieser Wert angegeben ist, wird das Element [RedirectAddr (POX)](redirectaddr-pox.md) die e-Mail-Adresse angeben, die für eine nachfolgende autoermittlungsanforderung verwendet werden soll.  <br/> |
|settings  <br/> |Wenn dieser Wert angegeben wird, enthält die Antwort der AutoErmittlung Einstellungen, mit denen das Konto konfiguriert werden. Die meisten Einstellungen werden im [Protokoll (POX)](protocol-pox.md) -Element gefunden.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

