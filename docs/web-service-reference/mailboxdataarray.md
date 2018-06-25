---
title: MailboxDataArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxDataArray
api_type:
- schema
ms.assetid: a14af788-beee-452c-b5d0-37bcb4ef02ff
description: Das MailboxDataArray-Element enthält eine Liste der Postfächer, um Informationen zur Verfügbarkeit abzufragen.
ms.openlocfilehash: b76e71ee9127dc2221e0065a27d3c781f8b5786a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830283"
---
# <a name="mailboxdataarray"></a>MailboxDataArray

Das **MailboxDataArray** -Element enthält eine Liste der Postfächer, um Informationen zur Verfügbarkeit abzufragen. 
  
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
- [MailboxDataArray](mailboxdataarray.md)
  
- [MailboxData](mailboxdata.md)
  
```xml
<MailboxDataArray>
   <MailboxData>...</MailboxData>
</MailboxDataArray>
```

**ArrayOfMailboxData**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MailboxData](mailboxdata.md) <br/> |Stellt eine einzelne Postfachbenutzer und Optionen für den Typ der Daten zu den Postfachbenutzer zurückgegeben werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserAvailabilityRequest](getuseravailabilityrequest.md) <br/> |Enthält die Argumente, die zum Abrufen von Informationen zur Verfügbarkeit der Benutzer verwendet. Dies ist eine Stammelements.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft® Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserAvailability-Vorgang](getuseravailability-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [Erste Benutzer Verfügbarkeit](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

