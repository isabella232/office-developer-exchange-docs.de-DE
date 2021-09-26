---
title: PrincipalName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PrincipalName
api_type:
- schema
ms.assetid: 88c142d4-0bc7-43ea-a997-d7200664d900
description: Das PrincipalName-Element stellt den Benutzerprinzipalnamen (USER Principal Name, UPN) des Kontos dar, das für Exchange Identitätswechsel verwendet werden soll.
ms.openlocfilehash: f3cc23b1cab69e166b59d7c358f663772e71ea09
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543016"
---
# <a name="principalname"></a>PrincipalName

Das **PrincipalName-Element** stellt den Benutzerprinzipalnamen (USER Principal Name, UPN) des Kontos dar, das für Exchange Identitätswechsel verwendet werden soll. 
  
```xml
<PrincipalName/>
```

 **PrincipalNameType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConnectingSID](connectingsid.md) <br/> |Stellt ein Konto dar, das bei Verwendung des ExchangeImpersonation-SOAP-Headers als Identitätswechsel verwendet werden soll.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt den UPN eines Benutzers dar. Dieser Wert ist für das Benutzerobjekt im Active Directory-Verzeichnisdienst vorhanden. Diese enthält den Benutzeranmeldenamen und einen Domänennamen, der die Domäne identifiziert, in der sich das Benutzerkonto befindet, im folgenden Format:  `someone@example.com` .
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Server-zu-Server-Autorisierung in EWS](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

