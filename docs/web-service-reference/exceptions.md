---
title: Ausnahmen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Exceptions
api_type:
- schema
ms.assetid: 7cd63ac2-3441-4ed4-915b-6f90af4b28fc
description: Das Exceptions-Element identifiziert die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen.
ms.openlocfilehash: 1afc2980391ee588f9b9b813b87c2c699de3a6df
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463356"
---
# <a name="exceptions"></a>Ausnahmen

Das **Exceptions** -Element identifiziert die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen. 
  
```XML
<Conditions>
   <Categories/>
   <ContainsBodyStrings/>
   <ContainsHeaderStrings/>
   <ContainsRecipientStrings/>
   <ContainsSenderStrings/>
   <ContainsSubjectOrBodyStrings/>
   <ContainsSubjectStrings/>
   <FlaggedForAction/>
   <FromAddresses/>
   <FromConnectedAccounts/>
   <HasAttachments/>
   <Importance/>
   <IsApprovalRequest/>
   <IsAutomaticForward/>
   <IsAutomaticReply/>
   <IsEncrypted/>
   <IsMeetingRequest/>
   <IsMeetingResponse/>
   <IsNDR/>
   <IsPermissionControlled/>
   <IsReadReceipt/>
   <IsSigned/>
   <IsVoicemail/>
   <ItemClasses/>
   <MessageClassifications/>
   <NotSentToMe/>
   <SentCcMe/>
   <SentOnlyToMe/>
   <SentToAddresses/>
   <SentToMe/>
   <SentToOrCcMe/>
   <Sensitivity/>
   <WithinDateRange/>
   <WithinSizeRange/>
</Conditions>
```

 **RulePredicatesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Categories](categories-ex15websvcsotherref.md) <br/> |Enthält die Kategorien, die auf eine eingehende Nachricht angewendet werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[ContainsBodyStrings](containsbodystrings.md) <br/> |Gibt die Zeichenfolgen an, die im Textkörper von eingehenden Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[ContainsHeaderStrings](containsheaderstrings.md) <br/> |Indicaqtes die Zeichenfolgen, die in den Kopfzeilen eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[ContainsRecipientStrings](containsrecipientstrings.md) <br/> |Gibt die Zeichenfolgen an, die entweder in der **torecipients** -oder der **CcRecipients** -Eigenschaft der eingehenden Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[ContainsSenderStrings](containssenderstrings.md) <br/> |Gibt die Zeichenfolgen an, die in der **from** -Eigenschaft eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[ContainsSubjectOrBodyStrings](containssubjectorbodystrings.md) <br/> |Gibt die Zeichenfolgen an, die entweder im Textkörper oder im Betreff eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[ContainsSubjectStrings](containssubjectstrings.md) <br/> |Gibt die Zeichenfolgen an, die im Betreff eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[FlaggedForAction](flaggedforaction.md) <br/> |Gibt das Flag für Action-Wert an, das in eingehenden Nachrichten angezeigt werden muss, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[FromAddresses](fromaddresses.md) <br/> |Gibt die e-Mail-Adressen an, aus denen eingehende Nachrichten gesendet werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[FromConnectedAccounts](fromconnectedaccounts.md) <br/> |Stellt die e-Mail-Kontonamen dar, aus denen eingehende Nachrichten aggregiert werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Gibt an, ob eingehende Nachrichten Anlagen aufweisen müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[Importance](importance.md) <br/> |Gibt die Wichtigkeit für eingehende Nachrichten an, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsApprovalRequest](isapprovalrequest.md) <br/> |Gibt an, ob eingehende Nachrichten Genehmigungsanforderungen sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsAutomaticForward](isautomaticforward.md) <br/> |Gibt an, ob eingehende Nachrichten automatisch weitergeleitet werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsAutomaticReply](isautomaticreply.md) <br/> |Gibt an, ob eingehende Nachrichten automatische Antworten sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsEncrypted](isencrypted.md) <br/> |Gibt an, ob eingehende Nachrichten S/MIME verschlüsselt sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsMeetingRequest](ismeetingrequest.md) <br/> |Gibt an, ob eingehende Nachrichten Besprechungsanfragen sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsMeetingResponse](ismeetingresponse.md) <br/> |Gibt an, ob eingehende Nachrichten Antworten erfüllen müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsNDR](isndr.md) <br/> |Gibt an, ob eingehende Nachrichten nicht Zustellungsberichte sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsPermissionControlled](ispermissioncontrolled.md) <br/> |Gibt an, ob eingehende Nachrichten berechtigungsgesteuert (RMS protected) sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsReadReceipt](isreadreceipt.md) <br/> |Gibt an, ob eingehende Nachrichten Lesebestätigungen sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsSigned](issigned.md) <br/> |Gibt an, ob eingehende Nachrichten S/MIME signiert sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsVoicemail](isvoicemail.md) <br/> |Gibt an, ob eingehende Nachrichten Voicemail-Nachrichten sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[ItemClasses](itemclasses.md) <br/> |Stellt die Elementklassen dar, die für eingehende Nachrichten gestempelt werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[MessageClassifications](messageclassifications.md) <br/> |Stellt die Nachrichtenklassifikationen dar, die für eingehende Nachrichten gestempelt werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[NotSentToMe](notsenttome.md) <br/> |Gibt an, ob der Besitzer des Postfachs nicht in der **torecipients** -Eigenschaft der eingehenden Nachrichten sein darf, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[SentCcMe](sentccme.md) <br/> |Gibt an, ob der Besitzer des Postfachs in der **CcRecipients** -Eigenschaft der eingehenden Nachrichten sein muss, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[SentOnlyToMe](sentonlytome.md) <br/> |Gibt an, ob der Besitzer des Postfachs der einzige in der **torecipients** -Eigenschaft der eingehenden Nachrichten sein muss, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[SentToAddresses](senttoaddresses.md) <br/> |Gibt die e-Mail-Adressen an, an die eingehende Nachrichten gesendet wurden, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[SentToMe](senttome.md) <br/> |Gibt an, ob der Besitzer des Postfachs in der **torecipients** -Eigenschaft der eingehenden Nachrichten sein muss, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[SentToOrCcMe](senttoorccme.md) <br/> |Gibt an, ob der Besitzer des Postfachs entweder eine **torecipients** -oder eine **CcRecipients** -Eigenschaft eingehender Nachrichten sein muss, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Gibt die Empfindlichkeit an, die für eingehende Nachrichten gestempelt werden muss, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[WithinDateRange](withindaterange.md) <br/> |Gibt den Datumsbereich an, innerhalb dessen eingehende Nachrichten empfangen werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[WithinSizeRange](withinsizerange.md) <br/> |Gibt die Mindest-und Höchstgröße an, die eingehende Nachrichten aufweisen müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Regel (RuleType)](rule-ruletype.md) <br/> |Enthält eine einzelne Regel und stellt eine Regel im Postfach eines Benutzers dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Die Regelprädikate werden als Regelbedingungen oder Ausnahmen verwendet.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Bedingungen:](conditions.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

