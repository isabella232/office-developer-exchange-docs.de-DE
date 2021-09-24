---
title: GetDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetDelegate
api_type:
- schema
ms.assetid: 6d5efe59-596f-46f8-bdc6-ca9cded9bb8e
description: Das GetDelegate-Element definiert eine Anforderung zum Abrufen von Informationen über Stellvertretungen an ein Postfach. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 922a1d92856ba92abdc0fba717879b9a9e2687ef
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512968"
---
# <a name="getdelegate"></a>GetDelegate

Das **GetDelegate-Element** definiert eine Anforderung zum Abrufen von Informationen über Stellvertretungen an ein Postfach. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
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
|**IncludePermissions** <br/> |Gibt an, ob die Antwort Berechtigungseinstellungen für jeden Stellvertreterbenutzer enthält.  <br/> |
   
#### <a name="includepermissions-attribute-values"></a>IncludePermissions-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**True** <br/> |Stellvertretungsbenutzerberechtigungen werden zusätzlich zu den Stellvertretungsbenutzerinformationen zurückgegeben, die im [UserId-Element](userid.md) zurückgegeben werden.  <br/> |
|**False** <br/> |[UserId-Informationen](userid.md) werden zurückgegeben.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Postfach](mailbox.md) <br/> |Identifiziert das Postfach des Prinzipals.  <br/> |
|[UserIds](userids.md) <br/> |Enthält ein Array von Delegiertenbenutzern, die aus dem Postfach eines Prinzipals abgerufen werden sollen. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetDelegate-Vorgang](getdelegate-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

