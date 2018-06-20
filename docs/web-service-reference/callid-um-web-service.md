---
title: CallId (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- CallId
api_type:
- schema
ms.assetid: 2e044109-8bf3-488c-a654-459ac62fa1e7
description: Das CallId-Element enthält den Wert, der den Bezeichner des Anrufs in eine GetCallInfo (UM-Webdienst) Anforderung oder eine Anforderung zum Trennen der (UM-Webdienst) darstellt.
ms.openlocfilehash: 49690f41b9a002b05c7c9b1a1240073c7230ab92
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757546"
---
# <a name="callid-um-web-service"></a>CallId (UM-Webdienst)

Das **CallId** -Element enthält den Wert, der den Bezeichner des Anrufs in eine Anforderung von [GetCallInfo (UM-Webdienst)](getcallinfo-um-web-service.md) oder eine Anforderung zum [trennen (UM-Webdienst)](disconnect-um-web-service.md) darstellt. 
  
[GetCallInfo (UM-Webdienst)](getcallinfo-um-web-service.md)
  
[CallId (UM-Webdienst)](callid-um-web-service.md)
  
[Trennen Sie (UM-Webdienst)](disconnect-um-web-service.md)
  
[CallId (UM-Webdienst)](callid-um-web-service.md)
  
```xml
<CallId/>
```

 **string**
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
|[Trennen Sie (UM-Webdienst)](disconnect-um-web-service.md) <br/> |Definiert eine Anforderung an eine Verbindung zu trennen.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Textwert stellt den Bezeichner für einen Anruf.
  
## <a name="remarks"></a>Hinweise

Um einen Anruf anfängliches, verwenden Sie die [PlayOnPhone (UM-Webdienst)](playonphone-operation-um-web-service.md) oder [PlayOnPhoneGreeting-Operation (UM-Webdienst)](playonphonegreeting-operation-um-web-service.md). Verwenden Sie den Textwert, der die Elemente [PlayOnPhoneResponse (UM-Webdienst)](playonphoneresponse-um-web-service.md) oder [PlayOnPhoneGreetingResponse (UM-Webdienst)](playonphonegreetingresponse-um-web-service.md) für den **CallId** Element Textwert zurückgegeben wird. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetCallInfo-Vorgang (UM-Webdienst)](getcallinfo-operation-um-web-service.md)
  
[Trennen Sie (UM-Webdienst)](disconnect-operation-um-web-service.md)
  
[PlayOnPhone-Vorgang (UM-Webdienst)](playonphone-operation-um-web-service.md)
  
[PlayOnPhoneGreeting-Vorgang (UM-Webdienst)](playonphonegreeting-operation-um-web-service.md)

