---
title: Fehler (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 91c63b62-ab68-4c32-a2f7-5a87c188335b
description: Das Error-Element enthält eine AutoErmittlungsfehlerantwort.
ms.openlocfilehash: 2f96f8b9d6d154aac6f10924095b5a5864e76750
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530889"
---
# <a name="error-pox"></a>Fehler (POX)

Das **Error-Element** enthält eine AutoErmittlungsfehlerantwort. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Fehler (POX)](error-pox.md)
  
```xml
<Error Time="" Id="">
   <ErrorCode/>
   <Message/>
   <DebugData/>
</Error>
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Zeit  <br/> |Stellt den Zeitpunkt dar, zu dem die Fehlerantwort zurückgegeben wurde.  <br/> |
|Id  <br/> |Stellt einen Hash des Namens des Computers dar, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ErrorCode (POX)](errorcode-pox.md) <br/> |Enthält den Fehlercode für eine Fehler-AutoErmittlungsantwort.  <br/> |
|[Nachricht (POX)](message-pox.md) <br/> |Enthält die Fehlermeldung für eine Fehler-AutoErmittlungsantwort.  <br/> |
|[DebugData (POX)](debugdata-pox.md) <br/> |Enthält die Debugdaten für eine Fehlerantwort der AutoErmittlung.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Konto (POX)](account-pox.md) <br/> |Enthält eine AutoErmittlungsfehlerantwort.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

