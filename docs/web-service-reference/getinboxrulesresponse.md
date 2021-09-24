---
title: GetInboxRulesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetInboxRulesResponse
api_type:
- schema
ms.assetid: 6d6c1950-c328-489a-94bf-a250fdbd5cd9
description: Das GetInboxRulesResponse-Element definiert eine Antwort auf eine GetInboxRules-Vorgangsanforderung.
ms.openlocfilehash: e2d3b186922c2a61feb0a2c13fbaa3d02dbdd953
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520549"
---
# <a name="getinboxrulesresponse"></a>GetInboxRulesResponse

Das **GetInboxRulesResponse-Element** definiert eine Antwort auf eine [GetInboxRules-Vorgangsanforderung.](getinboxrules-operation.md) 
  
```XML
<GetInboxRulesResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <OutlookRuleBlobExists/>
   <InboxRules/>
</GetInboxRulesResponse>
```

 **GetInboxRulesResponseType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ResponseClass** <br/> | Beschreibt den Status einer [GetInboxRules-Vorgangsantwort.](getinboxrules-operation.md) <br/><br/>Die folgenden Werte sind für dieses Attribut gültig: <br/> <br/>– Erfolg  <br/>- Warnung  <br/>- Fehler  <br/> |
   
#### <a name="responseclass-attribute"></a>ResponseClass-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**Success** <br/> |Beschreibt eine Anforderung, die erfüllt wird.  <br/> |
|**Warning** <br/> | Beschreibt eine Anforderung, die nicht verarbeitet wurde. Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde und nachfolgende Elemente nicht verarbeitet werden konnten. <br/><br/>Es folgen Beispiele für Warnungsquellen:  <br/><br/>– Der Exchange Speicher ist während des Batches offline.  <br/>– Active Directory Domain Services (AD DS) ist offline.  <br/>– Postfächer werden verschoben.  <br/>– Die Nachrichtendatenbank (MDB) ist offline.  <br/>– Ein Kennwort ist abgelaufen.  <br/>– Ein Kontingent wird überschritten.  <br/> |
|**Error** <br/> | Beschreibt eine Anforderung, die nicht erfüllt werden kann. <br/><br/>Es folgen Beispiele für Fehlerquellen:  <br/><br/>– Ungültige Attribute oder Elemente  <br/>– Attribute oder Elemente, die außerhalb des Gültigen liegen  <br/>– Ein unbekanntes Tag  <br/>– Ein Attribut oder Element, das im Kontext ungültig ist  <br/>– Ein nicht autorisierter Zugriffsversuch durch einen beliebigen Client  <br/>– Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf  <br/><br/>  Informationen zu dem Fehler finden Sie in den [ResponseCode-](responsecode.md) und [MessageText-Elementen.](messagetext.md)  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Stellt eine Textbeschreibung des Status der Antwort bereit.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Stellt Statusinformationen zu der Anforderung bereit.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert. Sie enthält den Wert 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
|[OutlookRuleBlobExists](outlookruleblobexists.md) <br/> |Gibt an, ob ein Microsoft Outlook Regel-Blob im Postfach des Benutzers vorhanden ist.  <br/> |
|[InboxRules](inboxrules.md) <br/> |Stellt ein Array der Regeln im Postfach des Benutzers dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine
  
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
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetInboxRules](getinboxrules.md)
- [GetInboxRules-Vorgang](getinboxrules-operation.md)

