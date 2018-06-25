---
title: Benutzer-IDs
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserIds
api_type:
- schema
ms.assetid: 78a09c3a-1646-4c55-95a2-1109fb11e1c6
description: Die Benutzer-IDs enthaltenen Element ein Array von delegieren Benutzer erhalten oder aus einem Prinzipal Postfach entfernen. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 277ae96fdbc30f1b39ef20553e10ff1de3ff7a8b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839448"
---
# <a name="userids"></a>Benutzer-IDs

Das **Benutzer-IDs** -Element enthält ein Array von Benutzer als Stellvertreter zum Abrufen oder aus einem Prinzipal Postfach entfernen. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
```xml
<UserIds>
   <UserId/>
</UserIds>
```

 **ArrayOfUserIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Benutzer-ID](userid.md) <br/> |Identifiziert eine Stellvertretung zum Abrufen oder aus einem Prinzipal Postfach entfernen. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetDelegate](getdelegate.md) <br/> |Definiert eine Anforderung zum Abrufen von Informationen zu Stellvertretern für ein Postfach. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[RemoveDelegate](removedelegate.md) <br/> |Definiert eine Anforderung zum Entfernen von Stellvertretern aus einem Postfach. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetDelegate-Vorgang](getdelegate-operation.md)
  
[RemoveDelegate-Vorgang](removedelegate-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

