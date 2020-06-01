---
title: DelegateUser
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
description: Das DelegateUser-Element identifiziert einen einzelnen Delegaten, der in einem Postfach oder einer Stellvertretung, die in einer Delegate-Verwaltungs Antwort zurückgegeben wird, hinzugefügt oder aktualisiert werden soll. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 40d9dacbd544436a3edf3213cf078cd33f961a74
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458803"
---
# <a name="delegateuser"></a>DelegateUser

Das **DelegateUser** -Element identifiziert einen einzelnen Delegaten, der in einem Postfach oder einer Stellvertretung, die in einer Delegate-Verwaltungs Antwort zurückgegeben wird, hinzugefügt oder aktualisiert werden soll. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
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
|[DelegatePermissions](delegatepermissions.md) <br/> |Enthält die Einstellungen für Stellvertreter-Berechtigungsstufen. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[ReceiveCopiesOfMeetingMessages](receivecopiesofmeetingmessages.md) <br/> |Gibt an, ob eine Stellvertretung Kopien von Besprechungs bezogenen Nachrichten empfängt, die an den Prinzipal adressiert sind. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[ViewPrivateItems](viewprivateitems.md) <br/> |Gibt an, ob eine Stellvertretung über die Berechtigung zum Anzeigen privater Kalenderelemente im Postfach des Prinzipals verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DelegateUsers](delegateusers.md) <br/> |Enthält die Identitäten von Stellvertretungen, die in einem Postfach hinzugefügt oder aktualisiert werden sollen.  <br/> |
|[DelegateUserResponseMessageType](delegateuserresponsemessagetype.md) <br/> |Enthält Antwortnachrichten für Delegate-Verwaltungsvorgänge. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

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
- [Hinzufügen von Stellvertretungen](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

