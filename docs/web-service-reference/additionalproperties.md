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
description: Das AdditionalProperties-Element identifiziert zusätzliche Eigenschaften für die Verwendung in GetItem-, UpdateItem-, CreateItem-, FindItem-oder FindFolder-Anforderungen.
ms.openlocfilehash: 90a307ba4d5ece10e15d2cec56cf5042c3d38685
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455814"
---
# <a name="additionalproperties"></a>AdditionalProperties

Das **AdditionalProperties** -Element identifiziert zusätzliche Eigenschaften für die Verwendung in [GetItem](getitem.md)-, [UpdateItem](updateitem.md)-, [CreateItem](createitem.md)-, [FindItem](finditem.md)-oder [FindFolder](findfolder.md) -Anforderungen. 
  
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
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifiziert erweiterte MAPI-Eigenschaften zum Abrufen, festlegen oder erstellen.  <br/> |
|[FieldURI](fielduri.md) <br/> |Identifiziert häufig referenzierte Eigenschaften nach URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifiziert häufig referenzierte Wörterbucheigenschaften nach URI.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> | Identifiziert die Ordner Eigenschaften, die in eine [GetFolder](getfolder.md)-, [FindFolder](findfolder.md)-oder [SyncFolderHierarchy](syncfolderhierarchy.md) -Antwort eingeschlossen werden sollen.<br/><br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>  `/FindFolder/FolderShape` <br/>  `/GetFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifiziert die Elementeigenschaften und Inhalte, die in einer [GetItem](getitem.md)-, [FindItem](finditem.md)-oder [SyncFolderItems](syncfolderitems.md) -Antwort enthalten sein sollen.<br/><br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
|[AttachmentShape](attachmentshape.md) <br/> |Identifiziert zusätzliche erweiterte Elementeigenschaften, die in einer Antwort auf eine [GetItem](getitem.md) -Anforderung zurückgegeben werden sollen.<br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet: <br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Nicht alle untergeordneten Elemente können mit [GetItem](getitem.md)-, [UpdateItem](updateitem.md)-, [CreateItem](createitem.md)-, [FindItem](finditem.md)-oder [FindFolder](findfolder.md) -Anforderungen verwendet werden. Die-Eigenschaft muss auf den Ordner oder das Element angewendet werden, auf das zugegriffen wird. Verwenden Sie erweiterte Eigenschaften, um auf andere Eigenschaften zuzugreifen. Wenn die Eigenschaft für ein bestimmtes Element nicht vorhanden ist, wird kein entsprechendes Element in den resultierenden XML-Code ausgegeben. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt. 
  
Dieses Element ist optional.
  
## <a name="example"></a>Beispiel

Im folgenden Anforderungs Beispiel wird gezeigt, wie ein Element Betreff mithilfe des **AdditionalProperties** -Elements abgerufen wird. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

