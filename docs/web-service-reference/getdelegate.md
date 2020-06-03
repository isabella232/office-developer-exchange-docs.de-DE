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
description: Das getdelegate-Element definiert eine Anforderung zum Abrufen von Informationen zu Delegaten an ein Postfach. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: bd7fb55800b51eb2d69184bc4e04cdef3e6b9a89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461030"
---
# <a name="getdelegate"></a>GetDelegate

Das **getdelegate** -Element definiert eine Anforderung zum Abrufen von Informationen zu Delegaten an ein Postfach. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
```xml
<GetDelegate IncludePermissions="">
      <Mailbox/>
   <UserIds/>
</GetDelegate>
```

 **Getdelegattype**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**IncludePermissions** <br/> |Gibt an, ob die Antwort Berechtigungseinstellungen für jeden Delegate-Benutzer enthält.  <br/> |
   
#### <a name="includepermissions-attribute-values"></a>IncludePermissions-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**True** <br/> |Stellvertreter Benutzerberechtigungen werden zusätzlich zu den Delegate-Benutzerinformationen zurückgegeben, die im [UserID](userid.md) -Element zurückgegeben werden.  <br/> |
|**False** <br/> |[UserID](userid.md) -Informationen werden zurückgegeben.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Postfach](mailbox.md) <br/> |Identifiziert das Postfach des Prinzipals.  <br/> |
|[UserIds](userids.md) <br/> |Enthält ein Array von Delegate-Benutzern, die aus dem Postfach eines Prinzipals abgerufen werden sollen. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetDelegate-Vorgang](getdelegate-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

