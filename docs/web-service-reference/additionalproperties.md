---
title: AdditionalProperties
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AdditionalProperties
api_type:
- schema
ms.assetid: 7a269aed-dcfd-4c3e-9e14-094e53828101
description: Das AdditionalProperties-Element identifiziert zusätzliche Eigenschaften für die Verwendung in GetItem, UpdateItem, CreateItem, FindItem oder FindFolder anfordert.
ms.openlocfilehash: 64e4f1ee6b24cf8015b7893dc4a904ca8b32d58e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757230"
---
# <a name="additionalproperties"></a>AdditionalProperties

Das **AdditionalProperties** -Element identifiziert zusätzliche Eigenschaften für die Verwendung in [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md)oder [FindFolder](findfolder.md) anfordert. 
  
```xml
<AdditionalProperties>
   <ExtendedFieldURI/>
   <FieldURI/>
   <IndexedFieldURI/>
</AdditionalProperties>
```

 **NonEmptyArrayOfPathsToElementType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Bezeichnet die extended MAPI-Eigenschaften zum Abrufen oder festlegen, oder erstellen.  <br/> |
|[FieldURI](fielduri.md) <br/> |Identifiziert die Eigenschaften von URI häufig verwiesen wird.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Häufig referenzierten Wörterbucheigenschaften mithilfe von URI identifiziert.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> | Gibt die Eigenschaften des Ordners in einer Antwort [GetFolder](getfolder.md), [FindFolder](findfolder.md)oder [SyncFolderHierarchy](syncfolderhierarchy.md) aufzunehmen.<br/><br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>  `/FindFolder/FolderShape` <br/>  `/GetFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifiziert die Elementeigenschaften und den Inhalt in einer Antwort [GetItem](getitem.md), [FindItem](finditem.md)oder [SyncFolderItems](syncfolderitems.md) aufzunehmen.<br/><br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
|[AttachmentShape](attachmentshape.md) <br/> |Zusätzliche erweiterte Elementeigenschaften in einer Antwort auf eine Anforderung [GetItem](getitem.md) zurückzugebenden identifiziert.<br/><br/> Es folgt der XPath-Ausdruck, der dieses Element:<br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="remarks"></a>Hinweise

Nicht alle untergeordneten Elemente können mit [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md)oder [FindFolder](findfolder.md) Anforderungen verwendet werden. Die Eigenschaft muss auf den Ordner oder das Element, das zugegriffen wird angewendet. Verwenden Sie erweiterte Eigenschaften auf andere Eigenschaften zuzugreifen. Wenn die Eigenschaft für ein bestimmtes Element nicht vorhanden ist, wird kein entsprechendes Element in das resultierende XML ausgegeben werden. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt. 
  
Dieses Element ist optional.
  
## <a name="example"></a>Beispiel

Im folgenden anforderungsbeispiel veranschaulicht einen Betreff des Elements abrufen, indem Sie mithilfe des **AdditionalProperties** -Elements. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="ASkAS="/>
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

