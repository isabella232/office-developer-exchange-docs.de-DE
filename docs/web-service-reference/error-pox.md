---
title: Fehler (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 91c63b62-ab68-4c32-a2f7-5a87c188335b
description: Das Error-Element enthält eine Fehlerantwort AutoErmittlung.
ms.openlocfilehash: 3135a352365fe3000ce2d202ad78452d5c8ccc7f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758260"
---
# <a name="error-pox"></a>Fehler (POX)

Das **Error** -Element enthält eine Fehlerantwort AutoErmittlung. 
  
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
|Zeit  <br/> |Gibt die Zeit an, wann die Fehlerantwort zurückgegeben wurde.  <br/> |
|Id  <br/> |Stellt einen Hash des Namens des Computers, auf dem Microsoft Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ErrorCode (POX)](errorcode-pox.md) <br/> |Enthält den Fehlercode für ein Fehler Antwort der AutoErmittlung an.  <br/> |
|[Nachricht (POX)](message-pox.md) <br/> |Enthält die Fehlermeldung Fehler Antwort der AutoErmittlung an.  <br/> |
|[DebugData (POX)](debugdata-pox.md) <br/> |Enthält die Debugdaten für eine Antwort der AutoErmittlung-Fehler.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Konto (POX)](account-pox.md) <br/> |Enthält eine Fehlerantwort AutoErmittlung an.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

