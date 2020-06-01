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
description: Das SerializedSecurityContext-Element wird in der Simple Object Access Protocol (SOAP) Kopfzeile für die Token-Serialisierung in der Server-zu-Server-Authentifizierung verwendet. Die Serialisierung von Token wird nicht unterstützt.
ms.openlocfilehash: 58fea1c7f613315d59e81935561f92f318afc769
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462052"
---
# <a name="serializedsecuritycontext"></a>SerializedSecurityContext

Das **SerializedSecurityContext** -Element wird in der Simple Object Access Protocol (SOAP) Kopfzeile für die Token-Serialisierung in der Server-zu-Server-Authentifizierung verwendet. Die Serialisierung von Token wird nicht unterstützt. 
  
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
|[UserSID](usersid.md) <br/> |Stellt das SDDL-Formular (Security Descriptor Definition Language) der Benutzer Sicherheits-ID in einem serialisierten Sicherheitskontext-SOAP-Header dar.  <br/> |
|[GroupSids](groupsids.md) <br/> |Stellt eine Auflistung von Sicherheits-IDs für das Verzeichnisdienst-Gruppenobjekt Active Directory dar.  <br/> |
|[RestrictedGroupSids](restrictedgroupsids.md) <br/> |Stellt die Gruppen Sicherheits-ID und die Attribute für eine eingeschränkte Gruppe dar.  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Stellt die primäre Simple Mail Transfer Protocol (SMTP) Adresse eines Kontos dar, das für die Server-zu-Server-Autorisierung verwendet werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs Server-Rolle (CAS) installiert ist.
  
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

