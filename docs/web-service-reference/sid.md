---
title: SID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SID
api_type:
- schema
ms.assetid: 2f33b29b-163b-4106-a74d-6fb76ec38951
description: Das SID-Element stellt die Sicherheitsdeskriptordefinitionssprache (Security Descriptor Definition Language, SDDL) der Sicherheits-ID (SID) für das Konto dar, das für den Identitätswechsel oder Stellvertretungszugriff verwendet werden soll.
ms.openlocfilehash: 436f284b59d5146b481a25b7b0986db4aeee67ce
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59547057"
---
# <a name="sid"></a>SID

Das **SID-Element** stellt die Sicherheitsdeskriptordefinitionssprache (Security Descriptor Definition Language, SDDL) der Sicherheits-ID (SID) für das Konto dar, das für den Identitätswechsel oder Stellvertretungszugriff verwendet werden soll. 
  
```xml
<SID/>
```

 **SIDType**
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
|[UserId](userid.md) <br/> |Identifiziert einen Stellvertreterbenutzer oder einen Benutzer mit Ordnerzugriffsberechtigungen.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist eine Zeichenfolgendarstellung einer SID.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

