---
title: UserId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UserId
api_type:
- schema
ms.assetid: 244af9e0-bf3c-46b4-8bfa-9719a1ed3107
description: Das UserId-Element identifiziert einen delegierten Benutzer oder einen Benutzer, der über Ordnerzugriffsberechtigungen verfügt.
ms.openlocfilehash: f03914745f8f7f47c64685b3e7c52eefece5ff6d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510757"
---
# <a name="userid"></a>UserId

Das **UserId-Element** identifiziert einen delegierten Benutzer oder einen Benutzer, der über Ordnerzugriffsberechtigungen verfügt. 
  
```xml
<UserId>
   <SID/>
   <PrimarySmtpAddress/>
   <DisplayName/>
   <DistinguishedUser/>
   <ExternalUserIdentity/>
</UserId>
```

 **UserIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SID](sid.md) <br/> |Stellt die SDDL-Form (Security Descriptor Definition Language) der Sicherheits-ID (SID) dar.  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Stellt die primäre SMTP-Adresse (Simple Mail Transfer Protocol) eines Kontos dar, das für den Delegatenzugriff verwendet werden soll.  <br/> |
|[DisplayName (Zeichenfolge)](displayname-string.md) <br/> |Definiert den Anzeigenamen eines Ordners, Kontakts, einer Verteilerliste oder eines Stellvertreterbenutzers.  <br/> |
|[DistinguishedUser](distinguisheduser.md) <br/> |Identifiziert anonyme und Standardbenutzerkonten für den Delegatenzugriff.  <br/> |
|[ExternalUserIdentity](externaluseridentity.md) <br/> |Identifiziert einen externen Stellvertretungsbenutzer oder einen externen Benutzer, der über Ordnerzugriffsberechtigungen verfügt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DelegateUser](delegateuser.md) <br/> |Identifiziert einen einzelnen Delegaten, der in einem Postfach hinzugefügt oder aktualisiert werden soll.  <br/> |
|[Berechtigung](permission.md) <br/> |Definiert den Zugriff, den ein Benutzer verfügt in einen Ordner.  <br/> |
|[CalendarPermission](calendarpermission.md) <br/> |Definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner.  <br/> |
|[UserIds](userids.md) <br/> |Enthält ein Array von Delegiertenbenutzern, die aus dem Postfach eines Prinzipals abgerufen oder entfernt werden sollen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[AddDelegate-Vorgang](adddelegate-operation.md)
  
[UpdateDelegate-Vorgang](updatedelegate-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Hinzufügen von Delegaten](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

