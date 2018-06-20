---
title: GetInboxRulesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetInboxRulesResponse
api_type:
- schema
ms.assetid: 6d6c1950-c328-489a-94bf-a250fdbd5cd9
description: Das GetInboxRulesResponse-Element definiert eine Antwort auf eine GetInboxRules Vorgang an.
ms.openlocfilehash: d84064ab777fe13ded7727381842ddd1ee9d047d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758715"
---
# <a name="getinboxrulesresponse"></a>GetInboxRulesResponse

Das **GetInboxRulesResponse** -Element definiert eine Antwort auf eine [GetInboxRules Vorgang](getinboxrules-operation.md) an. 
  
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
|**ResponseClass** <br/> | Beschreibt den Status einer Antwort [GetInboxRules Vorgang](getinboxrules-operation.md) . <br/><br/>Die folgenden Werte sind für dieses Attribut gültig: <br/> <br/>-Success  <br/>-Warnung  <br/>-Fehler  <br/> |
   
#### <a name="responseclass-attribute"></a>ResponseClass-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**Success** <br/> |Beschreibt eine Anforderung, die erfüllt ist.  <br/> |
|**Warning** <br/> | Beschreibt eine Anforderung, die nicht verarbeitet wurde. Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte. <br/><br/>Es folgen Beispiele für die Quellen der Warnungen:  <br/><br/>-Der Exchange-Speicher ist während der Batchaktualisierung offline.  <br/>-Active Directory-Domänendienste (AD DS) ist offline.  <br/>-Postfächer werden verschoben.  <br/>-Die Nachrichtendatenbank (MDB) ist offline.  <br/>-Ein Kennwort ist abgelaufen.  <br/>-Ein Kontingent überschritten wird.  <br/> |
|**Fehler** <br/> | Beschreibt eine Anforderung, die nicht gewährleistet werden kann. <br/><br/>Es folgen Beispiele für Datenquellen von Fehlern:  <br/><br/>-Ungültige Attribute oder Elemente  <br/>-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.  <br/>-Eine unbekannte Marke  <br/>-Eines Attributs oder Elements, das nicht im Kontext gültig ist.  <br/>-Einen nicht autorisierten Zugriffsversuch von jedem client  <br/>-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf  <br/><br/>  Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Beschreibung des Status der Antwort enthält.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Enthält Statusinformationen über die Anforderung.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert. Es enthält einen Wert von 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
|[OutlookRuleBlobExists](outlookruleblobexists.md) <br/> |Gibt an, ob ein Microsoft Outlook-Regel Blob im Postfach des Benutzers vorhanden ist.  <br/> |
|[InboxRules](inboxrules.md) <br/> |Stellt ein Array von Regeln in das Postfach des Benutzers an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
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
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetInboxRules](getinboxrules.md)
- [GetInboxRules-Vorgang](getinboxrules-operation.md)

