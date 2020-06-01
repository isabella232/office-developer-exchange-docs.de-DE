---
title: MailTips
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTips
api_type:
- schema
ms.assetid: c1cba493-bccc-4b8e-be8e-bfa8a8b10882
description: Das MailTips-Element stellt Werte für verschiedene Arten von e-Mail-Tipps dar.
ms.openlocfilehash: 9bacdea7b4f3108f700ed102025445e01a73e69d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44447596"
---
# <a name="mailtips"></a>MailTips

Das **MailTips** -Element stellt Werte für verschiedene Arten von e-Mail-Tipps dar. 
  
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
|[PendingMailTips](pendingmailtips.md) <br/> |Gibt an, dass die e-Mail-Tipps in diesem Element nicht ausgewertet werden konnten, bevor das Verarbeitungstimeout des Servers abgelaufen war.  <br/> |
|[OutOfOffice](outofoffice.md) <br/> |Stellt die Antwortnachricht und einen Zeitraum für das Senden der Antwortnachricht dar.  <br/> |
|[MailboxFull](mailboxfull.md) <br/> |Gibt an, ob das Postfach für den Empfänger voll ist.  <br/> |
|[CustomMailTip](custommailtip.md) <br/> |Stellt eine angepasste e-Mail-Tipp Nachricht dar.  <br/> |
|[TotalMemberCount](totalmembercount.md) <br/> |Stellt die Anzahl aller Elemente in einer Gruppe dar.  <br/> |
|[ExternalMemberCount](externalmembercount.md) <br/> |Stellt die Anzahl externer Mitglieder in einer Gruppe dar.  <br/> |
|[MaxMessageSize](maxmessagesize.md) <br/> |Stellt die maximale Nachrichtengröße dar, die der Empfänger annehmen kann.  <br/> |
|[DeliveryRestricted](deliveryrestricted.md) <br/> |Gibt an, ob durch Übermittlungseinschränkungen verhindert wird, dass die Nachricht des Absenders den Empfänger erreicht.  <br/> |
|[Ismoderiert](ismoderated.md) <br/> |Gibt an, ob das Postfach des Empfängers moderiert wird.  <br/> |
|[InvalidRecipient (e-Mail-Infos)](invalidrecipient-mailtips.md) <br/> |Gibt an, ob der Empfänger ungültig ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MailTipsResponseMessageType](mailtipsresponsemessagetype.md) <br/> |Stellt Einstellungen für e-Mail-Tipps dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

