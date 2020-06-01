---
title: UserSID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserSid
api_type:
- schema
ms.assetid: f8a0dcd9-8564-4e35-b307-c5d2761b48d8
description: Das users-Element stellt das SDDL-Formular (Security Descriptor Definition Language) der Benutzer Sicherheits-ID in einem serialisierten Sicherheitskontext-SOAP-Header dar. Die Serialisierung von Token wird nicht unterstützt.
ms.openlocfilehash: b8ee51b1998546fc4ab14bd3666192ae63c8dba8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462017"
---
# <a name="usersid"></a>UserSID

Das **Users** -Element stellt das SDDL-Formular (Security Descriptor Definition Language) der Benutzer Sicherheits-ID in einem serialisierten Sicherheitskontext-SOAP-Header dar. Die Serialisierung von Token wird nicht unterstützt. 
  
```xml
<UserSid/>
```

 **String**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SerializedSecurityContext](serializedsecuritycontext.md) <br/> |Wird im SOAP-Header für die Token-Serialisierung in der Server-zu-Server-Authentifizierung verwendet.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert Text stellt die Sicherheits-ID eines Benutzers dar.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

