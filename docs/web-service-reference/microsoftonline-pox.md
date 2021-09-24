---
title: MicrosoftOnline (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0b88f02a-9c50-44b3-841b-560b24e37af5
description: Das MicrosoftOnline-Element enthält einen Wert, der angibt, ob das Postfach des Benutzers in Exchange Online oder Exchange Online als Teil Office 365 gehostet wird.
ms.openlocfilehash: fbf230df18ca488babb1523cc7f689923eaeb55b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510945"
---
# <a name="microsoftonline-pox"></a>MicrosoftOnline (POX)

Das **MicrosoftOnline-Element** enthält einen Wert, der angibt, ob das Postfach des Benutzers in Exchange Online oder Exchange Online als Teil Office 365 gehostet wird. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[MicrosoftOnline (POX)](microsoftonline-pox.md)
  
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
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Textwert gibt an, ob das Postfach des Benutzers in Exchange Online gehostet wird. Der Wert ist **"true",** wenn das Postfach des Benutzers in Exchange Online gehostet wird. andernfalls **false**.
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

