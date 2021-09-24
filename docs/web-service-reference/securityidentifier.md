---
title: SecurityIdentifier
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SecurityIdentifier
api_type:
- schema
ms.assetid: f7656729-f2c9-41cc-b1ec-60f480fc4dab
description: Das SecurityIdentifier-Element stellt die SDDL-Form (Security Descriptor Definition Language) einer Sicherheits-ID (SID) dar.
ms.openlocfilehash: 803c8c0efae1ccd6356d9ce3b5aa85e1d86aa565
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521601"
---
# <a name="securityidentifier"></a>SecurityIdentifier

Das **SecurityIdentifier-Element** stellt die SDDL-Form (Security Descriptor Definition Language) eines Sicherheitsbezeichners [(SID)](sid.md)dar.
  
```xml
<SecurityIdentifier/>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GroupIdentifier](groupidentifier.md) <br/> |Stellt einen einzelnen Sicherheitsbezeichner und ein Attribut für eine Active Directory-Objektgruppe dar, in der das Konto Mitglied ist.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/SerializedSecurityContext/GroupSids/GroupIdentifier[i]` <br/> |
|[RestrictedGroupIdentifier](restrictedgroupidentifier.md) <br/> |Stellt die Gruppensicherheits-ID und die Attribute für eine eingeschränkte Gruppe innerhalb eines Benutzertokens dar.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wird im SOAP-Header (Simple Object Access Protocol) verwendet.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

