---
title: CreateFolderPathResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f7b3507-713d-4ccf-8518-75fa6f967d6d
description: Das CreateFolderPathResponseMessage-Element gibt die Antwortnachricht für eine CreateFolderPath-Anforderung an.
ms.openlocfilehash: 3c0c4e98b568a6398dcd0e71a6e6931a3f47e3da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458887"
---
# <a name="createfolderpathresponsemessage"></a>CreateFolderPathResponseMessage

Das **CreateFolderPathResponseMessage** -Element gibt die Antwortnachricht für eine **CreateFolderPath** -Anforderung an. 
  
```XML
<CreateFolderPathResponseMessage ResponseClass="">
    <Folders></Folders>
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</CreateFolderPathResponseMessage>
```

 **FolderInfoResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|ResponseClass  <br/> |Gibt die Klasse der Antwort an.  <br/> |
   
#### <a name="responseclass"></a>ResponseClass

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Erfolgreich  <br/> |Gibt den Erfolg an.  <br/> |
|Warnung  <br/> |Gibt eine Warnung an.  <br/> |
|Fehler (ungefährer Wortlaut)  <br/> |Gibt einen Fehler an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Ordner](folders-ex15websvcsotherref.md) <br/> |Enthält ein Array von Ordnern, die in Ordnervorgängen verwendet werden.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.  <br/> |
|[MessageText](messagetext.md) <br/> |Enthält eine Textbeschreibung des Status der Antwort.  <br/> |
|[Messagexml verwendet](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Stellt Statusinformationen zur Anforderung bereit.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

