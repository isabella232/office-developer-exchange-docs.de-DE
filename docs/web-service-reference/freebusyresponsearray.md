---
title: FreeBusyResponseArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyResponseArray
api_type:
- schema
ms.assetid: 5592a37e-cf4b-4643-8a2a-fa58c40345b9
description: Das FreeBusyResponseArray-Element enthält Informationen zur Verfügbarkeit der angeforderten Benutzer und den Antwortstatus.
ms.openlocfilehash: cc6022c28213667c40dc00b5627ed88c4f78e2f2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758542"
---
# <a name="freebusyresponsearray"></a>FreeBusyResponseArray

Das **FreeBusyResponseArray** -Element enthält Informationen zur Verfügbarkeit der angeforderten Benutzer und den Antwortstatus. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
```xml
<FreeBusyResponseArray>
   <FreeBusyResponse>...</FreeBusyResponse>
</FreeBusyResponseArray>
```

 **ArrayOfFreeBusyResponse**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FreeBusyResponse](freebusyresponse.md) <br/> |Enthält die Frei/Gebucht-Informationen für ein einzelnes Postfach-Benutzer und den Antwortstatus.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserAvailabilityResponse](getuseravailabilityresponse.md) <br/> |Enthält die Eigenschaften, die Verfügbarkeitsinformationen für Benutzer definieren oder Besprechungsinformationen Zeit vorgeschlagen.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetUserAvailabilityResponse` <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element ist nicht in einer Antwort GetUserAvailability enthalten, wenn Frei/Gebucht-Informationen nicht angefordert wird.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserAvailability-Vorgang](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Erste Benutzer Verfügbarkeit](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

