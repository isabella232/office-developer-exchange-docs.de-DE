---
title: DelegateUser
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DelegateUser
api_type:
- schema
ms.assetid: aac4e74e-f69b-4c41-a0c9-489610330fbf
description: Das DelegateUser-Element identifiziert einen einzelnen Delegaten, der in einem Postfach hinzugefügt oder aktualisiert werden soll, oder ein Delegat, der in einer Stellvertretungsverwaltungsantwort zurückgegeben wird. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 1963bef64e32ff536f0544a03f019e7785bae4d0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510256"
---
# <a name="delegateuser"></a>DelegateUser

Das **DelegateUser-Element** identifiziert einen einzelnen Delegaten, der in einem Postfach hinzugefügt oder aktualisiert werden soll, oder einen Delegaten, der in einer Stellvertretungsverwaltungsantwort zurückgegeben wird. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
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
|[UserId](userid.md) <br/> |Identifiziert den Delegaten. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[DelegatePermissions](delegatepermissions.md) <br/> |Enthält die Einstellungen für die Stellvertretungsberechtigungsstufe. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[ReceiveCopiesOfMeetingMessages](receivecopiesofmeetingmessages.md) <br/> |Gibt an, ob eine Stellvertretung Kopien von Besprechungsnachrichten empfängt, die an den Prinzipal adressiert sind. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[ViewPrivateItems](viewprivateitems.md) <br/> |Gibt an, ob ein Stellvertreter über die Berechtigung zum Anzeigen privater Kalenderelemente im Postfach des Prinzipals verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DelegateUsers](delegateusers.md) <br/> |Enthält die Identitäten von Stellvertretern, die in einem Postfach hinzugefügt oder aktualisiert werden sollen.  <br/> |
|[DelegateUserResponseMessageType](delegateuserresponsemessagetype.md) <br/> |Enthält Antwortnachrichten für Stellvertretungsverwaltungsvorgänge. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [AddDelegate-Vorgang](adddelegate-operation.md) 
- [UpdateDelegate-Vorgang](updatedelegate-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Hinzufügen von Delegaten](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

