---
title: Bedingungen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Conditions
api_type:
- schema
ms.assetid: f049a48c-9585-43f7-8549-0b8cb19a5eea
description: Conditions-Element identifiziert die Bedingungen, die beim erfüllt, Regelaktionen für eine Regel ausgelöst wird.
ms.openlocfilehash: f66777e82892122c4c7dac45bdef3c42f5c4a577
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757592"
---
# <a name="conditions"></a>Bedingungen

**Conditions** -Element identifiziert die Bedingungen, die beim erfüllt, Regelaktionen für eine Regel ausgelöst wird. 
  
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
|[Categories](categories-ex15websvcsotherref.md) <br/> |Enthält die Kategorien, die auf eine eingehende Nachricht in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende angewendet werden müssen.  <br/> |
|[ContainsBodyStrings](containsbodystrings.md) <br/> |Gibt die Zeichenfolgen, die im Textkörper der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende angezeigt werden müssen.  <br/> |
|[ContainsHeaderStrings](containsheaderstrings.md) <br/> |Gibt die Zeichenfolgen, die in den Kopfzeilen der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende angezeigt werden müssen.  <br/> |
|[ContainsRecipientStrings](containsrecipientstrings.md) <br/> |Gibt die Zeichenfolgen, die die **ToRecipients** oder **CcRecipients** Eigenschaften der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende vorhanden sein müssen.  <br/> |
|[ContainsSenderStrings](containssenderstrings.md) <br/> |Gibt die Zeichenfolgen, die in der Eigenschaft **aus** der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende angezeigt werden müssen.  <br/> |
|[ContainsSubjectOrBodyStrings](containssubjectorbodystrings.md) <br/> |Gibt die Zeichenfolgen, die im Text oder den Betreff der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende angezeigt werden müssen.  <br/> |
|[ContainsSubjectStrings](containssubjectstrings.md) <br/> |Gibt die Zeichenfolgen, die den Betreff der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende vorhanden sein müssen.  <br/> |
|[FlaggedForAction](flaggedforaction.md) <br/> |Gibt die Kennzeichen für den Aktionswert, die angezeigt werden, muss auf eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anwenden.  <br/> |
|[FromAddresses](fromaddresses.md) <br/> |Gibt die E-mail-Adressen aus denen eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende gesendet werden müssen.  <br/> |
|[FromConnectedAccounts](fromconnectedaccounts.md) <br/> |Stellt die Namen der e-Mail-Konten aus denen eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende zusammengefasst wurden verfügen müssen.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Gibt an, ob eingehende Nachrichten mit Anlagen in der Reihenfolge für die Bedingung oder Ausnahme angewendet haben.  <br/> |
|[Importance](importance.md) <br/> |Gibt die Bedeutung, die versehen ist in eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anwenden.  <br/> |
|[IsApprovalRequest](isapprovalrequest.md) <br/> |Gibt an, ob eingehende Nachrichten Genehmigung Anforderungen in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.  <br/> |
|[IsAutomaticForward](isautomaticforward.md) <br/> |Gibt an, ob eingehende Nachrichten automatische Weiterleitungen in Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.  <br/> |
|[IsAutomaticReply](isautomaticreply.md) <br/> |Gibt an, ob eingehende Nachrichten automatische Antworten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.  <br/> |
|[IsEncrypted](isencrypted.md) <br/> |Gibt an, ob eingehende Nachrichten S/MIME verschlüsselt in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.  <br/> |
|[IsMeetingRequest](ismeetingrequest.md) <br/> |Gibt an, ob eingehende Nachrichten Anforderungen in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende meeting werden müssen.  <br/> |
|[IsMeetingResponse](ismeetingresponse.md) <br/> |Gibt an, ob eingehende Nachrichten Antworten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende meeting werden müssen.  <br/> |
|[IsNDR](isndr.md) <br/> |Gibt an, ob eingehende Nachrichten Unzustellbarkeitsberichte (NDR) müssen in der Reihenfolge für die Bedingung oder Ausnahme anwenden.  <br/> |
|[IsPermissionControlled](ispermissioncontrolled.md) <br/> |Gibt an, ob eingehende Nachrichten Berechtigung gesteuert (RMS geschützte) in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.  <br/> |
|[IsReadReceipt](isreadreceipt.md) <br/> |Gibt an, ob eingehende Nachrichten Empfangsbestätigungen in Reihenfolge für die Bedingung oder Ausnahme anzuwendende gelesen werden müssen.  <br/> |
|[IsSigned](issigned.md) <br/> |Gibt an, ob eingehende Nachrichten, dass in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende S/MIME signiert sein müssen.  <br/> |
|[IsVoicemail](isvoicemail.md) <br/> |Gibt an, ob eingehende Nachrichten Voicemailnachrichten in Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.  <br/> |
|[ItemClasses](itemclasses.md) <br/> |Stellt die Element-Klassen, die auf eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende gekennzeichnet sein müssen.  <br/> |
|[MessageClassifications](messageclassifications.md) <br/> |Stellt die Nachrichtenklassifikationen, die auf eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende gekennzeichnet sein müssen.  <br/> |
|[NotSentToMe](notsenttome.md) <br/> |Gibt an, ob der Besitzer des Postfachs nicht in der **ToRecipients** -Eigenschaft der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss.  <br/> |
|[SentCcMe](sentccme.md) <br/> |Gibt an, ob der Besitzer des Postfachs in die **CcRecipients** -Eigenschaft des eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden.  <br/> |
|[SentOnlyToMe](sentonlytome.md) <br/> |Gibt an, ob der Besitzer des Postfachs das einzige Objekt in der **ToRecipients** -Eigenschaft des eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden.  <br/> |
|[SentToAddresses](senttoaddresses.md) <br/> |Gibt die E-mail-Adressen, die eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende an gesendet wurden.  <br/> |
|[SentToMe](senttome.md) <br/> |Gibt an, ob der Besitzer des Postfachs in die **ToRecipients** -Eigenschaft des eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden.  <br/> |
|[SentToOrCcMe](senttoorccme.md) <br/> |Gibt an, ob der Besitzer des Postfachs in einem **ToRecipients** oder **CcRecipients** -Eigenschaft des eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden.  <br/> |
|[Vertraulichkeit](sensitivity.md) <br/> |Gibt an, die Vertraulichkeit, die auf eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende gekennzeichnet sein muss.  <br/> |
|[WithinDateRange](withindaterange.md) <br/> |Gibt den Datumsbereich, in dem eingehende Nachrichten müssen in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende empfangen wurden.  <br/> |
|[WithinSizeRange](withinsizerange.md) <br/> |Gibt die minimale und maximale Größe, die eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Regel (RuleType)](rule-ruletype.md) <br/> |Enthält eine einzelne Regel und stellt eine Regel in dem Postfach eines Benutzers.  <br/> |
   
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
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Ausnahmen](exceptions.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

