---
title: SerializedSecurityContext
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SerializedSecurityContext
api_type:
- schema
ms.assetid: a02c4fc1-ed1a-40d9-a18e-6cfdae21a690
description: Das SerializedSecurityContext-Element wird im SOAP-Header (Simple Object Access Protocol) für die Token-Serialisierung in der Server-zu-Server-Authentifizierung verwendet. Die Token-Serialisierung wird nicht unterstützt.
ms.openlocfilehash: 55fe752813fc2d7e3ed5416401ff46b5e00516e3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546042"
---
# <a name="serializedsecuritycontext"></a>SerializedSecurityContext

Das **SerializedSecurityContext-Element** wird im SOAP-Header (Simple Object Access Protocol) für die Token-Serialisierung in der Server-zu-Server-Authentifizierung verwendet. Die Token-Serialisierung wird nicht unterstützt. 
  
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
|[UserSid](usersid.md) <br/> |Stellt die SDDL-Form (Security Descriptor Definition Language) des Benutzersicherheitsbezeichners in einem serialisierten SOAP-Header im Sicherheitskontext dar.  <br/> |
|[GroupSids](groupsids.md) <br/> |Stellt eine Auflistung von Sicherheitsbezeichnern des Active Directory-Verzeichnisdienst-Gruppenobjekts dar.  <br/> |
|[RestrictedGroupSids](restrictedgroupsids.md) <br/> |Stellt die Gruppensicherheits-ID und die Attribute für eine eingeschränkte Gruppe dar.  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Stellt die primäre SMTP-Adresse (Simple Mail Transfer Protocol) eines Kontos dar, das für die Server-zu-Server-Autorisierung verwendet werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffsserverrolle (Client Access Server, CAS) installiert ist.
  
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

