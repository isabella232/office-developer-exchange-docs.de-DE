---
title: GetDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetDelegate
api_type:
- schema
ms.assetid: 6d5efe59-596f-46f8-bdc6-ca9cded9bb8e
description: Das GetDelegate-Element definiert eine Anforderung zum Abrufen von Informationen über Delegaten an ein Postfach. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: e31d6bd4f4387094beb467fcc4dff31ca7ec5d62
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758629"
---
# <a name="getdelegate"></a>GetDelegate

Das **GetDelegate** -Element definiert eine Anforderung zum Abrufen von Informationen über Delegaten an ein Postfach. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
```xml
<GetDelegate IncludePermissions="">
      <Mailbox/>
   <UserIds/>
</GetDelegate>
```

 **GetDelegateType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**IncludePermissions** <br/> |Gibt an, ob die Antwort berechtigungseinstellungen für jeden Benutzer Stellvertreter enthält.  <br/> |
   
#### <a name="includepermissions-attribute-values"></a>Attributwerte IncludePermissions

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**True** <br/> |Delegieren der Benutzer, den Berechtigungen zusätzlich zu den Delegaten Benutzerinformationen zurückgegeben werden, die im [UserId](userid.md) -Element zurückgegeben wird.  <br/> |
|**False** <br/> |[Benutzer-ID](userid.md) -Informationen werden zurückgegeben.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Postfach](mailbox.md) <br/> |Identifiziert den Prinzipal Postfach an.  <br/> |
|[Benutzer-IDs](userids.md) <br/> |Enthält ein Array von Delegaten Benutzern von einem Prinzipal Postfach abgerufen. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
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


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

