---
title: SID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SID
api_type:
- schema
ms.assetid: 2f33b29b-163b-4106-a74d-6fb76ec38951
description: Das sid-Element stellt das SDDL-Formular (Security Descriptor Definition Language) der Sicherheits-ID (Security Identifier, SID) für das Konto dar, das für den Identitätswechsel oder den Stellvertretungszugriff verwendet werden soll.
ms.openlocfilehash: 0e3f740e9a056f7c0042049d97757b5f2d3c441d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468047"
---
# <a name="sid"></a>SID

Das **sid** -Element stellt das SDDL-Formular (Security Descriptor Definition Language) der Sicherheits-ID (Security Identifier, SID) für das Konto dar, das für den Identitätswechsel oder den Stellvertretungszugriff verwendet werden soll. 
  
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
|[ConnectingSID](connectingsid.md) <br/> |Stellt ein Konto für den Identitätswechsel dar, wenn der ExchangeImpersonation-SOAP-Header verwendet wird.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[UserId](userid.md) <br/> |Identifiziert einen Stellvertreter Benutzer oder einen Benutzer mit Ordnerzugriffsberechtigungen.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert Text ist eine Zeichenfolgendarstellung einer SID.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server mit installierter Client Zugriffs-Server Rolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

