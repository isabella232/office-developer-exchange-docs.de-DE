---
title: DistinguishedUser
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DistinguishedUser
api_type:
- schema
ms.assetid: 9362699d-666a-4acf-8fa1-c6669f0a2ae5
description: Das DistinguishedUser-Element identifiziert anonyme und Benutzerkonten für Stellvertretungszugriff. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: b14be22bfe5316b9ab254e63cdfa0757596b8b92
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758073"
---
# <a name="distinguisheduser"></a>DistinguishedUser

Das **DistinguishedUser** -Element identifiziert anonyme und Benutzerkonten für Stellvertretungszugriff. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
```xml
<DistinguishedUser>Default or Anonymous</DistinguishedUser>
```

 **DistinguishedUserType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Benutzer-ID](userid.md) <br/> |Identifiziert ein Stellvertreter oder ein Benutzer mit Zugriffsberechtigungen für Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert von **Default** beschreibt die Standardeinstellung für den Benutzer als Stellvertreter, die den Prinzipal Postfach hinzugefügt werden. Ein Textwert der **Anonym** wird die Stellvertretung Access-Einstellungen, die für den Prinzipal Postfach anonyme Benutzer verfügen über beschrieben. 
  
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

