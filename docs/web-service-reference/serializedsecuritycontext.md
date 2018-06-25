---
title: SerializedSecurityContext
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SerializedSecurityContext
api_type:
- schema
ms.assetid: a02c4fc1-ed1a-40d9-a18e-6cfdae21a690
description: Das SerializedSecurityContext-Element wird in der Kopfzeile (SOAP = Simple Object Access Protocol) für tokenserialisierung für Server-zu-Server-Authentifizierung verwendet. Tokenserialisierung wird nicht unterstützt.
ms.openlocfilehash: c5590551dc0780d918b05902e4f48fb9d1390b59
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831363"
---
# <a name="serializedsecuritycontext"></a>SerializedSecurityContext

Das **SerializedSecurityContext** -Element wird in der Kopfzeile (SOAP = Simple Object Access Protocol) für tokenserialisierung für Server-zu-Server-Authentifizierung verwendet. Tokenserialisierung wird nicht unterstützt. 
  
```xml
<SerializedSecurityContext>
   <UserSid/>
   <GroupSids/>
   <RestrictedGroupSids/>
   <PrimarySmtpAddress/>
</SerializedSecurityContext>
```

 **SerializedSecurityContextType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[UserSid](usersid.md) <br/> |Stellt die Security Descriptor Definition Language (SDDL) Formular der Benutzer Sicherheits-ID in einem serialisierten Sicherheit Kontext SOAP-Header.  <br/> |
|[GroupSids](groupsids.md) <br/> |Stellt eine Auflistung von Sicherheits-IDs von Active Directory Directory Service Group-Objekt.  <br/> |
|[RestrictedGroupSids](restrictedgroupsids.md) <br/> |Stellt die Gruppe Sicherheits-ID und die Attribute für eine eingeschränkte Gruppe.  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Stellt die primäre Simple Mail Transfer Protocol (SMTP)-Adresse eines Kontos für Server-zu-Server-Autorisierung verwendet werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2007 ausgeführt wird, die die Clientzugriffsserver (CAS) Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Server-zu-Server-Autorisierung in Exchange-Webdienste](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

