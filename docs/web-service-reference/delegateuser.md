---
title: Beauftragte Benutzer
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegateUser
api_type:
- schema
ms.assetid: aac4e74e-f69b-4c41-a0c9-489610330fbf
description: Das Element Beauftragte Benutzer identifiziert einen einzelnen Delegaten hinzufügen oder aktualisieren in einem Postfach oder eine Stellvertretung, die in einer Antwort der Stellvertretung Management zurückgegeben. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 72ddc313a5a76cd0345918cad63b7775ff85026b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757896"
---
# <a name="delegateuser"></a>Beauftragte Benutzer

Das Element **Beauftragte Benutzer** identifiziert einen einzelnen Delegaten hinzufügen oder aktualisieren in einem Postfach oder eine Stellvertretung, die in einer Antwort der Stellvertretung Management zurückgegeben. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
```xml
<DelegateUser>
   <UserId/>
   <DelegatePermissions/>
   <ReceiveCopiesOfMeetingMessages/>
   <ViewPrivateItems/>
</DelegateUser>
```

**DelegateUserType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Benutzer-ID](userid.md) <br/> |Identifiziert den Delegaten. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[DelegatePermissions](delegatepermissions.md) <br/> |Die Ebene Delegaten berechtigungseinstellungen enthält. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[ReceiveCopiesOfMeetingMessages](receivecopiesofmeetingmessages.md) <br/> |Gibt an, ob eine Stellvertretung Kopien der Nachrichten empfängt, die dem Prinzipal adressiert sind. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[ViewPrivateItems](viewprivateitems.md) <br/> |Gibt an, ob eine Stellvertretung über die Berechtigung zum Anzeigen von privaten Kalenderelementen in den Prinzipal Postfach verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DelegateUsers](delegateusers.md) <br/> |Die Identität der Stellvertretungen hinzufügen oder aktualisieren in einem Postfach enthält.  <br/> |
|[DelegateUserResponseMessageType](delegateuserresponsemessagetype.md) <br/> |Antwortnachrichten für Verwaltungsvorgänge Stellvertreter enthält. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [AddDelegate-Vorgang](adddelegate-operation.md) 
- [UpdateDelegate-Vorgang](updatedelegate-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Hinzufügen von Stellvertretungen](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

