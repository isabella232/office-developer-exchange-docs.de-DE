---
title: CallId (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- CallId
api_type:
- schema
ms.assetid: 2e044109-8bf3-488c-a654-459ac62fa1e7
description: Das CallId-Element enthält den Wert, der den Bezeichner des Aufrufs in einer Anforderung getCallInfo (UM-Webdienst) oder einer Verbindung (UM-Webdienst)-Anforderung darstellt.
ms.openlocfilehash: c19f1061d81bf7683fd2c84fb1c6968826046be6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522032"
---
# <a name="callid-um-web-service"></a>CallId (UM-Webdienst)

Das **CallId-Element** enthält den Wert, der den Bezeichner des Aufrufs in einer [Anforderung getCallInfo (UM-Webdienst)](getcallinfo-um-web-service.md) oder [einer Verbindung (UM-Webdienst)-Anforderung](disconnect-um-web-service.md) darstellt. 
  
[GetCallInfo (UM-Webdienst)](getcallinfo-um-web-service.md)
  
[CallId (UM-Webdienst)](callid-um-web-service.md)
  
[Disconnect (UM-Webdienst)](disconnect-um-web-service.md)
  
[CallId (UM-Webdienst)](callid-um-web-service.md)
  
```xml
<CallId/>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetCallInfo (UM-Webdienst)](getcallinfo-um-web-service.md) <br/> |Definiert eine Anforderung zum Abrufen von Informationen zu einem Anruf.  <br/> |
|[Disconnect (UM-Webdienst)](disconnect-um-web-service.md) <br/> |Definiert eine Anforderung zum Trennen eines Anrufs.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Textwert stellt den Bezeichner für einen Aufruf dar.
  
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie zum Starten eines Anrufs den [PlayOnPhone-Vorgang (UM-Webdienst)](playonphone-operation-um-web-service.md) oder [den PlayOnPhoneGreeting-Vorgang (UM-Webdienst).](playonphonegreeting-operation-um-web-service.md) Verwenden Sie den Textwert, der in den [PlayOnPhoneResponse-Elementen (UM-Webdienst)](playonphoneresponse-um-web-service.md) oder [PlayOnPhoneGreetingResponse-Elementen (UM-Webdienst)](playonphonegreetingresponse-um-web-service.md) zurückgegeben wird, für den Textwert des **CallId-Elements.** 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetCallInfo-Vorgang (UM-Webdienst)](getcallinfo-operation-um-web-service.md)
  
[Disconnect-Vorgange (UM-Webdienst)](disconnect-operation-um-web-service.md)
  
[PlayOnPhone-Vorgang (UM-Webdienst)](playonphone-operation-um-web-service.md)
  
[PlayOnPhoneGreeting-Vorgang (UM-Webdienst)](playonphonegreeting-operation-um-web-service.md)

