---
title: MailTips
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MailTips
api_type:
- schema
ms.assetid: c1cba493-bccc-4b8e-be8e-bfa8a8b10882
description: Das MailTips-Element stellt Werte für verschiedene Typen von E-Mail-Tipps dar.
ms.openlocfilehash: bf7ed542d51f2a8cb3172275be12cb72104bc5b2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511138"
---
# <a name="mailtips"></a>MailTips

Das **MailTips-Element** stellt Werte für verschiedene Typen von E-Mail-Tipps dar. 
  
```XML
<MailTips>
   <RecipientAddress/>
   <PendingMailTips/>
   <OutOfOffice/>
   <MailboxFull/>
   <CustomMailTip/>
   <TotalMemberCount/>
   <ExternalMemberCount/>
   <MaxMessageSize/>
   <DeliveryRestricted/>
   <IsModerated/>
   <InvalidRecipient/>
</MailTips>
```

 **E-Mail-Info**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RecipientAddress](recipientaddress.md) <br/> |Stellt das Postfach des Empfängers dar.  <br/> |
|[PendingMailTips](pendingmailtips.md) <br/> |Gibt an, dass die E-Mail-Tipps in diesem Element nicht ausgewertet werden konnten, bevor das Verarbeitungstimeout des Servers abgelaufen ist.  <br/> |
|[OutOfOffice](outofoffice.md) <br/> |Stellt die Antwortnachricht und eine Dauer für das Senden der Antwortnachricht dar.  <br/> |
|[MailboxFull](mailboxfull.md) <br/> |Gibt an, ob das Postfach für den Empfänger voll ist.  <br/> |
|[CustomMailTip](custommailtip.md) <br/> |Stellt eine angepasste E-Mail-Infonachricht dar.  <br/> |
|[TotalMemberCount](totalmembercount.md) <br/> |Stellt die Anzahl aller Mitglieder in einer Gruppe dar.  <br/> |
|[ExternalMemberCount](externalmembercount.md) <br/> |Stellt die Anzahl der externen Mitglieder in einer Gruppe dar.  <br/> |
|[MaxMessageSize](maxmessagesize.md) <br/> |Stellt die maximale Nachrichtengröße dar, die der Empfänger annehmen kann.  <br/> |
|[DeliveryRestricted](deliveryrestricted.md) <br/> |Gibt an, ob Übermittlungseinschränkungen verhindern, dass die Nachricht des Absenders den Empfänger erreicht.  <br/> |
|[IsModerated](ismoderated.md) <br/> |Gibt an, ob das Postfach des Empfängers moderiert wird.  <br/> |
|[InvalidRecipient (MailTips)](invalidrecipient-mailtips.md) <br/> |Gibt an, ob der Empfänger ungültig ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MailTipsResponseMessageType](mailtipsresponsemessagetype.md) <br/> |Stellt Einstellungen für E-Mail-Tipps dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

