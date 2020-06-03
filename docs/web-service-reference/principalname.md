---
title: PrincipalName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PrincipalName
api_type:
- schema
ms.assetid: 88c142d4-0bc7-43ea-a997-d7200664d900
description: Das PrincipalName-Element stellt den Benutzerprinzipalnamen (User Principal Name, UPN) des Kontos dar, das für den Exchange-Identitätswechsel verwendet werden soll.
ms.openlocfilehash: 31412c1461264e28bf8d52c957a457e8d1e847ef
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44440190"
---
# <a name="principalname"></a>PrincipalName

Das **PrincipalName** -Element stellt den Benutzerprinzipalnamen (User Principal Name, UPN) des Kontos dar, das für den Exchange-Identitätswechsel verwendet werden soll. 
  
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
|[ConnectingSID](connectingsid.md) <br/> |Stellt ein Konto für den Identitätswechsel dar, wenn Sie den SOAP-ExchangeImpersonation-Header verwenden.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert Text stellt den UPN eines Benutzers dar. Dieser Wert ist für das Benutzerobjekt im Active Directory Verzeichnisdienst vorhanden. Dieser enthält den Benutzeranmeldenamen und einen Domänennamen, der die Domäne identifiziert, in der sich das Benutzerkonto befindet, im folgenden Format: `someone@example.com` .
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.
  
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

