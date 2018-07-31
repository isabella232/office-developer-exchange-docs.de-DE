---
title: FindFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindFolder
api_type:
- schema
ms.assetid: b8a59740-d978-454c-9629-a10792385ba0
description: Das FindFolder-Element definiert eine Anforderung zum Suchen von Ordnern in einem Postfach.
ms.openlocfilehash: 69fbaebc5615ac7d19512770658cde83e4d352df
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353532"
---
# <a name="findfolder"></a>FindFolder

Das **FindFolder** -Element definiert eine Anforderung zum Suchen von Ordnern in einem Postfach. 
  
```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <IndexedPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <FractionalPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

**FindFolderType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Durchqueren  <br/> |Definiert, wie eine Suche ausgeführt wird. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="traversal-attribute-values"></a>Traversal Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Flach  <br/> |Weist den FindFolder Vorgang, um nur den identifizierten Ordner suchen und nur den Ordner IDs für Elemente zurückgegeben, die nicht gelöscht wurden. Dies ist eine flache durchqueren bezeichnet.  <br/> |
|Tief  <br/> |Weist den Vorgang FindFolder in alle untergeordneten Ordner des angegebenen übergeordneten Ordners durchsuchen und nur den Ordner IDs für Elemente zurückgegeben, die nicht gelöscht wurden. Dies ist eine umfassende durchqueren bezeichnet.  <br/> |
|SoftDeleted  <br/> |Weist den Vorgang FindFolder flache durchqueren Suchmethode für gelöschte Elemente.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |Gibt die Eigenschaften des Ordners in einer Antwort FindFolder aufzunehmen.  <br/> |
|[IndexedPageFolderView](indexedpagefolderview.md) <br/> |Beschreibt, wie ausgelagerten Elementinformationen in einer FindFolder Antwort zurückgegeben wird. Dieses Element ist optional.  <br/> |
|[FractionalPageFolderView](fractionalpagefolderview.md) <br/> |Beschreibt, in der Seitenansicht startet und die maximale Anzahl von Ordnern in einer Anforderung FindFolder zurückgegeben. Dieses Element ist optional.  <br/> |
|[Einschränkung](restriction.md) <br/> |Definiert eine Einschränkung oder Abfrage, die zum Filtern von Ordnern in einem Vorgang FindFolder verwendet wird. Dieses Element ist optional.  <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Ordner für den Vorgang FindFolder suchen identifiziert.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird eine Anforderung FindFolder veranschaulicht eine Anforderung an alle Ordner befindet sich im Posteingang suchen bilden.
  
```xml
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

- [FindFolder-Vorgang](findfolder-operation.md)

