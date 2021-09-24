---
title: Bedingungen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Conditions
api_type:
- schema
ms.assetid: f049a48c-9585-43f7-8549-0b8cb19a5eea
description: Das Conditions-Element identifiziert die Bedingungen, die bei Erfüllung die Regelaktionen für eine Regel auslösen.
ms.openlocfilehash: 55e569c2aa393c79eb4e712711fb2e7b4107023b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515978"
---
# <a name="conditions"></a>Bedingungen

Das  Conditions-Element identifiziert die Bedingungen, die bei Erfüllung die Regelaktionen für eine Regel auslösen. 
  
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
|[ContainsBodyStrings](containsbodystrings.md) <br/> |Gibt die Zeichenfolgen an, die im Textkörper eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[ContainsHeaderStrings](containsheaderstrings.md) <br/> |Gibt die Zeichenfolgen an, die in den Kopfzeilen eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[ContainsRecipientStrings](containsrecipientstrings.md) <br/> |Gibt die Zeichenfolgen an, die entweder in den **ToRecipients-** oder **CcRecipients-Eigenschaften** eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[ContainsSenderStrings](containssenderstrings.md) <br/> |Gibt die Zeichenfolgen an, die in der **From-Eigenschaft** eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[ContainsSubjectOrBodyStrings](containssubjectorbodystrings.md) <br/> |Gibt die Zeichenfolgen an, die entweder im Textkörper oder im Betreff eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[ContainsSubjectStrings](containssubjectstrings.md) <br/> |Gibt die Zeichenfolgen an, die im Betreff eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[FlaggedForAction](flaggedforaction.md) <br/> |Gibt das Kennzeichen für den Aktionswert an, das in eingehenden Nachrichten angezeigt werden muss, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[FromAddresses](fromaddresses.md) <br/> |Gibt die E-Mail-Adressen an, von denen eingehende Nachrichten gesendet werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[FromConnectedAccounts](fromconnectedaccounts.md) <br/> |Stellt die E-Mail-Kontonamen dar, aus denen eingehende Nachrichten aggregiert werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Gibt an, ob eingehende Nachrichten Anlagen aufweisen müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[Importance](importance.md) <br/> |Gibt die Wichtigkeit für eingehende Nachrichten an, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsApprovalRequest](isapprovalrequest.md) <br/> |Gibt an, ob eingehende Nachrichten Genehmigungsanforderungen sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsAutomaticForward](isautomaticforward.md) <br/> |Gibt an, ob eingehende Nachrichten automatisch weitergeleitet werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsAutomaticReply](isautomaticreply.md) <br/> |Gibt an, ob eingehende Nachrichten automatische Antworten sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsEncrypted](isencrypted.md) <br/> |Gibt an, ob eingehende Nachrichten S/MIME-verschlüsselt sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsMeetingRequest](ismeetingrequest.md) <br/> |Gibt an, ob eingehende Nachrichten Besprechungsanfragen sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsMeetingResponse](ismeetingresponse.md) <br/> |Gibt an, ob eingehende Nachrichten Besprechungsantworten sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsNDR](isndr.md) <br/> |Gibt an, ob eingehende Nachrichten Unzustellbarkeitsberichte (Non-Delivery Reports, NDRs) sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsPermissionControlled](ispermissioncontrolled.md) <br/> |Gibt an, ob eingehende Nachrichten berechtigungsgesteuert (RMS-geschützt) sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsReadReceipt](isreadreceipt.md) <br/> |Gibt an, ob eingehende Nachrichten Lesebestätigungen sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsSigned](issigned.md) <br/> |Gibt an, ob eingehende Nachrichten S/MIME-signiert sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[IsVoicemail](isvoicemail.md) <br/> |Gibt an, ob eingehende Nachrichten Voicemailnachrichten sein müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[ItemClasses](itemclasses.md) <br/> |Stellt die Elementklassen dar, die für eingehende Nachrichten gestempelt werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[MessageClassifications](messageclassifications.md) <br/> |Stellt die Nachrichtenklassifizierungen dar, die für eingehende Nachrichten gestempelt werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[NotSentToMe](notsenttome.md) <br/> |Gibt an, ob sich der Besitzer des Postfachs nicht in der **ToRecipients-Eigenschaft** der eingehenden Nachrichten befinden darf, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[SentCcMe](sentccme.md) <br/> |Gibt an, ob sich der Besitzer des Postfachs in der **CcRecipients-Eigenschaft** eingehender Nachrichten befinden muss, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[SentOnlyToMe](sentonlytome.md) <br/> |Gibt an, ob der Besitzer des Postfachs der einzige in der **ToRecipients-Eigenschaft** eingehender Nachrichten sein muss, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[SentToAddresses](senttoaddresses.md) <br/> |Gibt die E-Mail-Adressen an, an die eingehende Nachrichten gesendet werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[SentToMe](senttome.md) <br/> |Gibt an, ob sich der Besitzer des Postfachs in der **ToRecipients-Eigenschaft** eingehender Nachrichten befinden muss, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[SentToOrCcMe](senttoorccme.md) <br/> |Gibt an, ob sich der Besitzer des Postfachs in einer **ToRecipients-** oder **CcRecipients-Eigenschaft** eingehender Nachrichten befinden muss, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Gibt die Vertraulichkeit an, die für eingehende Nachrichten gestempelt werden muss, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[WithinDateRange](withindaterange.md) <br/> |Gibt den Datumsbereich an, in dem eingehende Nachrichten empfangen werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[WithinSizeRange](withinsizerange.md) <br/> |Gibt die minimale und maximale Größe an, die eingehende Nachrichten haben müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Regel (RuleType)](rule-ruletype.md) <br/> |Enthält eine einzelne Regel und stellt eine Regel im Postfach eines Benutzers dar.  <br/> |
   
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
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Ausnahmen](exceptions.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

