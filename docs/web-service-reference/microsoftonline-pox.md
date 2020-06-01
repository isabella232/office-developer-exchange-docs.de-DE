---
title: Microsoft Online (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0b88f02a-9c50-44b3-841b-560b24e37af5
description: Das Microsoft Online-Element enthält einen Wert, der angibt, ob das Postfach des Benutzers in Exchange Online oder Exchange Online als Teil Office 365 gehostet wird.
ms.openlocfilehash: f3144a673a4c98aad821e21c562141b0ae00f426
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467984"
---
# <a name="microsoftonline-pox"></a>Microsoft Online (POX)

Das **Microsoft Online** -Element enthält einen Wert, der angibt, ob das Postfach des Benutzers in Exchange Online oder Exchange Online als Teil Office 365 gehostet wird. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Microsoft Online (POX)](microsoftonline-pox.md)
  
```XML
<MicrosoftOnline/>
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
|[Konto (POX)](account-pox.md) <br/> |Gibt Kontoeinstellungen für den Benutzer an oder enthält Fehlerantworten.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert Text gibt an, ob das Postfach des Benutzers in Exchange Online gehostet wird. Der Wert ist **true** , wenn das Postfach des Benutzers in Exchange Online gehostet wird; andernfalls **false**.
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

