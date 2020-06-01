---
title: UserOofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserOofSettings
api_type:
- schema
ms.assetid: 0a95ca63-660e-4cc0-82e4-3f74fb4ae21c
description: Das UserOofSettings-Element gibt die Abwesenheit (Out of Office, OOF) Einstellungen an.
ms.openlocfilehash: 417c3d5061a6229d41eb57f72e89f03213acf460
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461905"
---
# <a name="useroofsettings"></a>UserOofSettings

Das **UserOofSettings** -Element gibt die Abwesenheit (Out of Office, OOF) Einstellungen an. 
  
[SetUserOofSettingsRequest](setuseroofsettingsrequest.md)
  
[UserOofSettings](useroofsettings.md)
  
```xml
<UserOofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</UserOofSettings>
```

 **UserOofSettings**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[OofState](oofstate.md) <br/> |Legt den Abwesenheitsstatus des Benutzers fest.  <br/> |
|[ExternalAudience](externalaudience.md) <br/> |Legt fest oder enthält einen Wert, der bestimmt, an wen externe Abwesenheitsnachrichten gesendet werden.  <br/> |
|[Dauer (UserOofSettings)](duration-useroofsettings.md) <br/> |Gibt die Dauer an, für die der Abwesenheitsstatus aktiviert ist, wenn das [OofState](oofstate.md) -Element auf **Scheduled**festgelegt ist. Wenn das [OofState](oofstate.md) -Element auf **aktiviert** oder **deaktiviert**festgelegt ist, wird der Wert dieses Elements ignoriert.  <br/> |
|[InternalReply](internalreply.md) <br/> |Enthält die Abwesenheitsantwort, die an andere Benutzer in der Domäne des Benutzers oder an vertrauenswürdigen Domänen gesendet wurde.  <br/> |
|[ExternalReply](externalreply.md) <br/> |Enthält die Abwesenheitsantwort, die an Adressen außerhalb der Domäne des Empfängers oder vertrauenswürdiger Domänen gesendet wurde.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SetUserOofSettingsRequest](setuseroofsettingsrequest.md) <br/> |Enthält die Argumente, die zum Festlegen der Abwesenheitseinstellungen und Nachrichten eines Postfachbenutzers verwendet werden.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel einer SetUserOofSettings-Anforderung wird die OoFState auf **Enabled**festgelegt, die Dauer von OOF für 10 Tage festgelegt und die internen und externen Abwesenheitsnachrichten festgelegt.
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Enabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2005-10-05T00:00:00</StartTime>
          <EndTime>2005-10-25T00:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office.  This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [SetUserOofSettings-Vorgang](setuseroofsettings-operation.md)

