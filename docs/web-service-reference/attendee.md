---
title: Teilnehmer
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Attendee
api_type:
- schema
ms.assetid: 393c3d7e-7416-458a-b976-270b88eaaa03
description: Das Attendee-Element darstellt, Teilnehmer und Ressourcen für eine Besprechung.
ms.openlocfilehash: 60cb0839c2f6de69b833c11f4594d40c14cd8887
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757399"
---
# <a name="attendee"></a>Teilnehmer

Das **Attendee** -Element darstellt, Teilnehmer und Ressourcen für eine Besprechung. 
  
```xml
<Attendee>
   <Mailbox/>
   <ResponseType/>
   <LastResponseTime/>
</Attendee>
```

 **AttendeeType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Postfach](mailbox.md) <br/> |Identifiziert eine vollständig aufgelöster E-mail-Adresse.  <br/> |
|[ResponseType](responsetype.md) <br/> |Stellt den Typ der Empfänger Antwort, die für eine Besprechung empfangen wird. Diese Eigenschaft ist nur relevant, Kalenderelement Organisator einer Besprechung.  <br/> |
|[LastResponseTime](lastresponsetime.md) <br/> |Stellt das Datum und Uhrzeit der neuesten Antwort, die empfangen wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RequiredAttendees](requiredattendees.md) <br/> |Stellt die Teilnehmer, die erforderlich sind, an einer Besprechung teilnehmen.  <br/> |
|[OptionalAttendees](optionalattendees.md) <br/> |Stellt die Teilnehmer, die nicht erforderlich sind, an einer Besprechung teilnehmen.  <br/> |
|[Ressourcen ](resources.md) <br/> |Stellt eine geplante Ressource für eine Besprechung.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

