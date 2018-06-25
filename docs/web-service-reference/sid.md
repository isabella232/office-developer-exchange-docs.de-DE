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
description: SID-Element stellt Security Descriptor Definition Language (SDDL) Form die Sicherheits-ID (SID) für das Konto für den Identitätswechsel verwenden oder Stellvertretungszugriff dar.
ms.openlocfilehash: efcea42c12ec1d26ea31fdb8de337c37a2338a96
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831492"
---
# <a name="sid"></a>SID

**SID** -Element stellt Security Descriptor Definition Language (SDDL) Form die Sicherheits-ID (SID) für das Konto für den Identitätswechsel verwenden oder Stellvertretungszugriff dar. 
  
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
|[ConnectingSID](connectingsid.md) <br/> |Gibt ein Konto Identitätswechsel bei Verwendung des "ExchangeImpersonation" SOAP-Headers.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[Benutzer-ID](userid.md) <br/> |Identifiziert ein Stellvertreter oder von einem Benutzer mit Zugriffsberechtigungen für Ordner.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist eine zeichenfolgendendarstellung einer SID.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, der Exchange-Server, mit die Clientzugriffs-Serverrolle installiert ausgeführt wird.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

