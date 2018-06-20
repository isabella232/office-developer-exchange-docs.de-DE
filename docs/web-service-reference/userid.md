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
description: UserId-Element identifiziert ein Stellvertreter oder ein Benutzer mit Zugriffsberechtigungen für Ordner.
ms.openlocfilehash: 8e9867f5a8cdd62dd2dae55fbf527595ac14f46d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839445"
---
# <a name="userid"></a>UserId

**UserId** -Element identifiziert ein Stellvertreter oder ein Benutzer mit Zugriffsberechtigungen für Ordner. 
  
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
|[SID](sid.md) <br/> |Stellt die Security Descriptor Definition Language (SDDL) Form die Sicherheits-ID (SID).  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Stellt die primäre Simple Mail Transfer Protocol (SMTP)-Adresse eines Kontos für Stellvertretungszugriff verwendet werden soll.  <br/> |
|[DisplayName (Zeichenfolge)](displayname-string.md) <br/> |Definiert den Anzeigenamen eines Ordners, Kontakt, Verteilerliste oder Stellvertretungsbenutzers.  <br/> |
|[DistinguishedUser](distinguisheduser.md) <br/> |Anonyme und Benutzerkonten für Stellvertretungszugriff identifiziert.  <br/> |
|[ExternalUserIdentity](externaluseridentity.md) <br/> |Identifiziert eine externe Stellvertretungsbenutzers oder ein externer Benutzer, der über Zugriffsberechtigungen für Ordner verfügt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Beauftragte Benutzer](delegateuser.md) <br/> |Identifiziert einen einzelnen Delegaten hinzufügen oder aktualisieren in einem Postfach.  <br/> |
|[Berechtigung](permission.md) <br/> |Definiert den Zugriff, den ein Benutzer verfügt in einen Ordner.  <br/> |
|[CalendarPermission](calendarpermission.md) <br/> |Definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner.  <br/> |
|[Benutzer-IDs](userids.md) <br/> |Enthält ein Array von Benutzer als Stellvertreter zum Abrufen oder aus einem Prinzipal Postfach entfernen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[AddDelegate-Vorgang](adddelegate-operation.md)
  
[UpdateDelegate-Vorgang](updatedelegate-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Hinzufügen von Stellvertretungen](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

