---
title: FolderShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderShape
api_type:
- schema
ms.assetid: 244f4f46-a33d-4764-92e3-1bddb4dc6a49
description: Das FolderShape-Element identifiziert die Ordnereigenschaften in einer Antwort GetFolder, FindFolder oder SyncFolderHierarchy aufzunehmen.
ms.openlocfilehash: 8ebdd70ef13ee9f0cce9020b9212576cba782be4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758524"
---
# <a name="foldershape"></a>FolderShape

Das **FolderShape** -Element identifiziert die Ordnereigenschaften in einer Antwort [GetFolder](getfolder.md), [FindFolder](findfolder.md)oder [SyncFolderHierarchy](syncfolderhierarchy.md) aufzunehmen. 
  
```xml
<FolderShape>
   <BaseShape/>
   <AdditionalProperties/>
</FolderShape>
```

 **FolderResponseShapeType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[BaseShape](baseshape.md) <br/> |Identifiziert die grundlegende Konfiguration von Eigenschaften in einer Antwort zurückgegeben werden sollen.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |Bezeichnet die zusätzliche Eigenschaften, die in eine Antwort zurückgegeben.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Definiert eine Anforderung zum Ordner in einem Postfach zu identifizieren.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/FindFolder` <br/> |
|[GetFolder](getfolder.md) <br/> |Definiert eine Anforderung an einen Ordner aus dem Exchange-Speicher abzurufen.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetFolder` <br/> |
|[SyncFolderHierarchy](syncfolderhierarchy.md) <br/> |Definiert eine Anforderung zum Synchronisieren einer Ordnerhierarchie auf einem Client an.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/SyncFolderHierarchy` <br/> |
   
## <a name="remarks"></a>Hinweise

Das **FolderShape** -Element ist ein erforderliches untergeordnetes Element des Elements [FindFolder](findfolder.md) . 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird eine Anforderung veranschaulicht, wie alle Ordner in der ersten Ebene des Ordners Posteingang zu suchen.
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindFolder](findfolder.md)

