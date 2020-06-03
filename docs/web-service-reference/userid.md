---
title: UserId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserId
api_type:
- schema
ms.assetid: 244af9e0-bf3c-46b4-8bfa-9719a1ed3107
description: Das UserID-Element identifiziert einen Stellvertreter Benutzer oder einen Benutzer, der über Ordnerzugriffsberechtigungen verfügt.
ms.openlocfilehash: 68075e335383835ddce9575d85ba5fa945ed305c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455541"
---
# <a name="userid"></a>UserId

Das **UserID** -Element identifiziert einen Stellvertreter Benutzer oder einen Benutzer, der über Ordnerzugriffsberechtigungen verfügt. 
  
```xml
<UserId>
   <SID/>
   <PrimarySmtpAddress/>
   <DisplayName/>
   <DistinguishedUser/>
   <ExternalUserIdentity/>
</UserId>
```

 **Useridtype**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SID](sid.md) <br/> |Stellt das SDDL-Formular (Security Descriptor Definition Language) der Sicherheits-ID (Security Identifier, SID) dar.  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Stellt die primäre Simple Mail Transfer Protocol (SMTP) Adresse eines Kontos dar, das für den Stellvertretungszugriff verwendet werden soll.  <br/> |
|[DisplayName (Zeichenfolge)](displayname-string.md) <br/> |Definiert den Anzeigenamen eines Ordners, Kontakts, einer Verteilerliste oder eines Stellvertreter Benutzers.  <br/> |
|[DistinguishedUser](distinguisheduser.md) <br/> |Identifiziert anonyme und Standardbenutzerkonten für den Stellvertretungszugriff.  <br/> |
|[ExternalUserIdentity](externaluseridentity.md) <br/> |Identifiziert einen externen stellvertretungsbenutzer oder einen externen Benutzer mit Ordnerzugriffsberechtigungen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DelegateUser](delegateuser.md) <br/> |Bezeichnet einen einzelnen Delegaten, der in einem Postfach hinzugefügt oder aktualisiert werden soll.  <br/> |
|[Berechtigung](permission.md) <br/> |Definiert den Zugriff, den ein Benutzer verfügt in einen Ordner.  <br/> |
|[CalendarPermission](calendarpermission.md) <br/> |Definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner.  <br/> |
|[UserIds](userids.md) <br/> |Enthält ein Array von Delegate-Benutzern, die aus dem Postfach eines Prinzipals abgerufen oder daraus entfernt werden sollen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

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


[Hinzufügen von Stellvertretungen](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

