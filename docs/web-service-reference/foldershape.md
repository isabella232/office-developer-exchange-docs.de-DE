---
title: FolderShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FolderShape
api_type:
- schema
ms.assetid: 244f4f46-a33d-4764-92e3-1bddb4dc6a49
description: Das FolderShape-Element identifiziert die Ordnereigenschaften, die in eine GetFolder-, FindFolder- oder SyncFolderHierarchy-Antwort eingeschlossen werden sollen.
ms.openlocfilehash: 530c9f25f17a3eba8549535bf7be37038a58c921
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518358"
---
# <a name="foldershape"></a>FolderShape

Das **FolderShape-Element** identifiziert die Ordnereigenschaften, die in eine [GetFolder-,](getfolder.md) [FindFolder-](findfolder.md)oder [SyncFolderHierarchy-Antwort](syncfolderhierarchy.md) eingeschlossen werden sollen. 
  
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
|[BaseShape](baseshape.md) <br/> |Identifiziert die grundlegende Konfiguration von Eigenschaften, die in einer Antwort zurückgegeben werden sollen.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |Identifiziert zusätzliche Eigenschaften, die in einer Antwort zurückgegeben werden sollen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Definiert eine Anforderung zum Identifizieren von Ordnern in einem Postfach.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/FindFolder` <br/> |
|[GetFolder](getfolder.md) <br/> |Definiert eine Anforderung zum Abrufen eines Ordners aus dem Exchange Speicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetFolder` <br/> |
|[SyncFolderHierarchy](syncfolderhierarchy.md) <br/> |Definiert eine Anforderung zum Synchronisieren einer Ordnerhierarchie auf einem Client.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/SyncFolderHierarchy` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **FolderShape-Element** ist ein erforderliches untergeordnetes Element des [FindFolder-Elements.](findfolder.md) 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel einer Anforderung wird veranschaulicht, wie alle Ordner auf der ersten Ebene des Posteingangsordners gefunden werden.
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindFolder](findfolder.md)

