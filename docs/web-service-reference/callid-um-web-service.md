---
title: Anrufdienst (um-Webdienst)
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
description: Das Call-ID-Element enthält den Wert, der den Bezeichner des Aufrufs in einer GetCallInfo (um-Webdienst)-Anforderungs-oder-Trennanforderung (um-Webdienst) darstellt.
ms.openlocfilehash: 5d5f596d4a98cbfb4b53be04278dae2305fc10c3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529455"
---
# <a name="callid-um-web-service"></a>Anrufdienst (um-Webdienst)

Das **Call** -ID-Element enthält den Wert, der den Bezeichner des Aufrufs in einer [GetCallInfo (](getcallinfo-um-web-service.md) um-Webdienst)-Anforderungs-oder- [Trennanforderung (um-Webdienst)](disconnect-um-web-service.md) darstellt. 
  
[GetCallInfo (um-Webdienst)](getcallinfo-um-web-service.md)
  
[Anrufdienst (um-Webdienst)](callid-um-web-service.md)
  
[Trennen (um-Webdienst)](disconnect-um-web-service.md)
  
[Anrufdienst (um-Webdienst)](callid-um-web-service.md)
  
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
|[GetCallInfo (um-Webdienst)](getcallinfo-um-web-service.md) <br/> |Definiert eine Anforderung zum Abrufen von Informationen zu einem Anruf.  <br/> |
|[Trennen (um-Webdienst)](disconnect-um-web-service.md) <br/> |Definiert eine Anforderung zum Trennen eines Anrufs.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Wert Text stellt den Bezeichner für einen Anruf dar.
  
## <a name="remarks"></a>Bemerkungen

Verwenden Sie zum ersten Aufrufen eines Anrufs den [PlayOnPhone-Vorgang (um-Webdienst)](playonphone-operation-um-web-service.md) oder den [PlayOnPhoneGreeting-Vorgang (um-Webdienst)](playonphonegreeting-operation-um-web-service.md). Verwenden Sie den Textwert, der in den [PlayOnPhoneResponse-Elementen (um-Webdienst)](playonphoneresponse-um-web-service.md) oder [PlayOnPhoneGreetingResponse (um-Webdienst)](playonphonegreetingresponse-um-web-service.md) für den Textwert des **Calling** -Elements zurückgegeben wird. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetCallInfo-Vorgang (um-Webdienst)](getcallinfo-operation-um-web-service.md)
  
[Trennungsvorgang (um-Webdienst)](disconnect-operation-um-web-service.md)
  
[PlayOnPhone-Vorgang (um-Webdienst)](playonphone-operation-um-web-service.md)
  
[PlayOnPhoneGreeting-Vorgang (um-Webdienst)](playonphonegreeting-operation-um-web-service.md)

