---
title: SyncFolderHierarchyResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchyResponseMessage
api_type:
- schema
ms.assetid: ab96c649-1005-401c-9d1c-9917f0b19a60
description: Das SyncFolderHierarchyResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen SyncFolderHierarchy-Vorgangsanforderung.
ms.openlocfilehash: fda0a37178f89ba0fd5ef860f8b009f335a11391
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465345"
---
# <a name="syncfolderhierarchyresponsemessage"></a>SyncFolderHierarchyResponseMessage

Das **SyncFolderHierarchyResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [SyncFolderHierarchy-Vorgangs](syncfolderhierarchy-operation.md) Anforderung. 
  
- [SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md) 
- [ResponseMessages](responsemessages.md)
- [SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)
  
```xml
<SyncFolderHierarchyResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <SyncState/>
   <IncludesLastFolderInRange/>
   <Changes/>
</SyncFolderHierarchyResponseMessage>
```

 **SyncFolderHierarchyResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ResponseClass** <br/> | Beschreibt den Status einer [SyncFolderHierarchy-Vorgangs](syncfolderhierarchy-operation.md) Antwort. <br/><br/>Die folgenden Werte sind für dieses Attribut gültig:<br/>  <br/>-Success  <br/>-Warnung  <br/>-Error  <br/> |
   
#### <a name="responseclass-attribute-values"></a>ResponseClass-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**Success** <br/> |Beschreibt eine Anforderung, die erfüllt ist.  <br/> |
|**Warning** <br/> | Beschreibt eine Anforderung, die nicht verarbeitet wurde. Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden. <br/><br/>Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:  <br/><br/>-Der Exchange-Informationsspeicher ist während des Batches offline.  <br/>-Active Directory-Domänendienste (AD DS) ist offline.  <br/>-Postfächer wurden verschoben.  <br/>-Die Nachrichtendatenbank (MDB) ist offline.  <br/>-Ein Kennwort ist abgelaufen.  <br/>-Ein Kontingent wurde überschritten.  <br/> |
|**Error** <br/> | Beschreibt eine Anforderung, die nicht erfüllt werden kann. <br/><br/>Im folgenden finden Sie Beispiele für Fehlerquellen:  <br/><br/>-Ungültige Attribute oder Elemente  <br/>-Attribute oder Elemente außerhalb des gültigen Bereichs  <br/>-Ein unbekanntes Tag  <br/>-Ein Attribut oder Element, das im Kontext ungültig ist  <br/>-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client  <br/>-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf  <br/><br/>  Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Enthält eine Textbeschreibung des Status der Antwort.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert. Sie enthält den Wert 0.  <br/> |
|[Messagexml verwendet](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
|[Von "SyncState](syncstate-ex15websvcsotherref.md) <br/> |Enthält eine Base64-codierte Form der Synchronisierungsdaten, die nach jeder erfolgreichen Anforderung aktualisiert wird. Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren.  <br/> |
|[IncludesLastFolderInRange](includeslastfolderinrange.md) <br/> |Gibt an, ob das letzte zu synchronisierende Element in die Antwort eingeschlossen wurde.  <br/> |
|[Änderungen (Hierarchie)](changes-hierarchy.md) <br/> |Enthält ein Sequenz Array von Änderungstypen, die die Arten von Unterschieden zwischen den Elementen auf dem Client und den Elementen auf dem Exchange-Server darstellen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [SyncFolderHierarchy-Vorgang](syncfolderhierarchy-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

