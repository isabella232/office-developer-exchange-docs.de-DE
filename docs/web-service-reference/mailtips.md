---
title: E-Mail-Infos
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
description: Das e-Mail-Infos Element stellt Werte für verschiedene Arten von e-Mail-Infos.
ms.openlocfilehash: 3a2e95225b09fd2d81db32f821ea3069ab7e7852
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830311"
---
# <a name="mailtips"></a>E-Mail-Infos

Das **e-Mail-Infos** Element stellt Werte für verschiedene Arten von e-Mail-Infos. 
  
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

 **E-Mail-Infos**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RecipientAddress](recipientaddress.md) <br/> |Das Postfach des Empfängers darstellt.  <br/> |
|[PendingMailTips](pendingmailtips.md) <br/> |Gibt an, dass die e-Mail-Infos in diesem Element nicht ausgewertet werden konnte, bevor die Verarbeitung der Servertimeout abgelaufen.  <br/> |
|[OutOfOffice](outofoffice.md) <br/> |Stellt die Antwortnachricht und einer Zeitdauer für die Response-Nachricht senden.  <br/> |
|[MailboxFull](mailboxfull.md) <br/> |Gibt an, ob das Postfach des Empfängers voll ist.  <br/> |
|[CustomMailTip](custommailtip.md) <br/> |Stellt eine benutzerdefinierte e-Mail-Info.  <br/> |
|[TotalMemberCount](totalmembercount.md) <br/> |Stellt die Anzahl aller Elemente in einer Gruppe.  <br/> |
|[ExternalMemberCount](externalmembercount.md) <br/> |Stellt die Anzahl der externen Elemente in einer Gruppe.  <br/> |
|[MaxMessageSize](maxmessagesize.md) <br/> |Stellt die maximale Größe von Nachrichten, die der Empfänger akzeptieren kann.  <br/> |
|[DeliveryRestricted](deliveryrestricted.md) <br/> |Gibt an, ob Einschränkungen Übermittlung des Absenders der Nachricht verhindern Erreichen des Empfängers.  <br/> |
|[IsModerated](ismoderated.md) <br/> |Gibt an, ob das Postfach des Empfängers ist moderiert wird.  <br/> |
|[InvalidRecipient (e-Mail-Infos)](invalidrecipient-mailtips.md) <br/> |Gibt an, ob der Empfänger ungültig ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MailTipsResponseMessageType](mailtipsresponsemessagetype.md) <br/> |Stellt e-Mail-Tipps Einstellungen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

