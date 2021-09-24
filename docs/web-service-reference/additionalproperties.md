---
title: AdditionalProperties
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AdditionalProperties
api_type:
- schema
ms.assetid: 7a269aed-dcfd-4c3e-9e14-094e53828101
description: Das AdditionalProperties-Element identifiziert zusätzliche Eigenschaften für die Verwendung in GetItem-, UpdateItem-, CreateItem-, FindItem- oder FindFolder-Anforderungen.
ms.openlocfilehash: 9a6fb98e9a88b1e40bd83559b1836d4122f0f125
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522201"
---
# <a name="additionalproperties"></a>AdditionalProperties

Das **AdditionalProperties-Element** identifiziert zusätzliche Eigenschaften für die Verwendung in [GetItem-,](getitem.md) [UpdateItem-,](updateitem.md) [CreateItem-,](createitem.md) [FindItem-](finditem.md)oder [FindFolder-Anforderungen.](findfolder.md) 
  
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
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifiziert erweiterte MAPI-Eigenschaften, die abgerufen, festgelegt oder erstellt werden sollen.  <br/> |
|[FieldURI](fielduri.md) <br/> |Identifies frequently referenced properties by URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifies frequently referenced dictionary properties by URI.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> | Identifiziert die Ordnereigenschaften, die in eine [GetFolder-,](getfolder.md) [FindFolder-](findfolder.md)oder [SyncFolderHierarchy-Antwort](syncfolderhierarchy.md) eingeschlossen werden sollen.<br/><br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>  `/FindFolder/FolderShape` <br/>  `/GetFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifiziert die Elementeigenschaften und -inhalte, die in eine [GetItem-,](getitem.md) [FindItem-](finditem.md)oder [SyncFolderItems-Antwort](syncfolderitems.md) eingeschlossen werden sollen.<br/><br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
|[AttachmentShape](attachmentshape.md) <br/> |Identifiziert zusätzliche erweiterte Elementeigenschaften, die in einer Antwort auf eine [GetItem-Anforderung](getitem.md) zurückgegeben werden sollen.<br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet: <br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Nicht alle untergeordneten Elemente können mit [GetItem-,](getitem.md) [UpdateItem-,](updateitem.md) [CreateItem-,](createitem.md) [FindItem-](finditem.md)oder [FindFolder-Anforderungen](findfolder.md) verwendet werden. Die Eigenschaft muss auf den Ordner oder das Element anwendbar sein, auf das zugegriffen wird. Verwenden Sie erweiterte Eigenschaften, um auf andere Eigenschaften zuzugreifen. Wenn die Eigenschaft für ein bestimmtes Element nicht vorhanden ist, wird kein entsprechendes Element in den resultierenden XML-Code ausgegeben. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt. 
  
Dieses Element ist optional.
  
## <a name="example"></a>Beispiel

Das folgende Anforderungsbeispiel zeigt, wie Sie einen Elementbeantrager mithilfe des **AdditionalProperties-Elements** abrufen. 
  
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
   

