---
title: Teilnehmer
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Attendee
api_type:
- schema
ms.assetid: 393c3d7e-7416-458a-b976-270b88eaaa03
description: Das Attendee-Element stellt Teilnehmer und Ressourcen für eine Besprechung dar.
ms.openlocfilehash: d48dcee42292b045ffc7cdcc5fd02f70109b1853
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531194"
---
# <a name="attendee"></a>Teilnehmer

Das **Attendee-Element** stellt Teilnehmer und Ressourcen für eine Besprechung dar. 
  
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
|[Postfach](mailbox.md) <br/> |Identifiziert eine vollständig aufgelöste E-Mail-Adresse.  <br/> |
|[ResponseType](responsetype.md) <br/> |Stellt den Typ der Empfängerantwort dar, die für eine Besprechung empfangen wird. Diese Eigenschaft ist nur für das Kalenderelement eines Besprechungsorganisators relevant.  <br/> |
|[LastResponseTime](lastresponsetime.md) <br/> |Stellt das Datum und die Uhrzeit der letzten empfangenen Antwort dar.  <br/> |
|[ProposedStart](proposedstart-attendeetype.md) <br/> |Stellt die vorgeschlagene Startzeit eines Teilnehmers für eine Besprechung dar. <br/> |
|[ProposedEnd](proposedend-attendeetype.md) <br/> |Stellt die vorgeschlagene Endzeit eines Teilnehmers für eine Besprechung dar. <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RequiredAttendees](requiredattendees.md) <br/> |Stellt Teilnehmer dar, die an einer Besprechung teilnehmen müssen.  <br/> |
|[OptionalAttendees](optionalattendees.md) <br/> |Stellt Teilnehmer dar, die nicht an einer Besprechung teilnehmen müssen.  <br/> |
|[Ressourcen](resources.md) <br/> |Stellt eine geplante Ressource für eine Besprechung dar.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

