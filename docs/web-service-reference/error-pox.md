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
description: Das Error-Element enthält eine AutoErmittlung-Fehlerantwort.
ms.openlocfilehash: 1a1a3e83898674e605921cb75371036a8a561a95
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530649"
---
# <a name="error-pox"></a>Fehler (POX)

Das **Error** -Element enthält eine AutoErmittlung-Fehlerantwort. 
  
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
|Time  <br/> |Stellt die Uhrzeit dar, zu der die Fehlerantwort zurückgegeben wurde.  <br/> |
|Id  <br/> |Stellt einen Hash des Namens des Computers dar, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ErrorCode (POX)](errorcode-pox.md) <br/> |Enthält den Fehlercode für eine fehlerhafte Auto Ermittlungs Antwort.  <br/> |
|[Nachricht (POX)](message-pox.md) <br/> |Enthält die Fehlermeldung für eine fehlerhafte Auto Ermittlungs Antwort.  <br/> |
|[DebugData (POX)](debugdata-pox.md) <br/> |Enthält die Debugdaten für eine fehlerhafte Auto Ermittlungs Antwort.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Konto (POX)](account-pox.md) <br/> |Enthält eine AutoErmittlung-Fehlerantwort.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

