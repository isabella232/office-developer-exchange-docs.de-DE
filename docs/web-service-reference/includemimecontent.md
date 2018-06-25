---
title: IncludeMimeContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IncludeMimeContent
api_type:
- schema
ms.assetid: 3f3c2300-55cd-41c0-900e-b470b290d52f
description: Das IncludeMimeContent-Element gibt an, ob der Inhalt Multipurpose Internet Mail Extensions (MIME) eines Elements oder die Anlage in der Antwort zurückgegeben wird.
ms.openlocfilehash: ddd6988be93231ac7c574a2e19c9ba4b562c7d0e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829903"
---
# <a name="includemimecontent"></a>IncludeMimeContent

Das **IncludeMimeContent** -Element gibt an, ob der Inhalt Multipurpose Internet Mail Extensions (MIME) eines Elements oder die Anlage in der Antwort zurückgegeben wird. 
  
```xml
<IncludeMimeContent>true or false</IncludeMimeContent>
```

 **boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AttachmentShape](attachmentshape.md) <br/> | Bezeichnet die zusätzliche Eigenschaften in einer Antwort auf eine Anforderung [GetAttachment](getattachment.md) zurückgegeben werden sollen.  <br/> <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifiziert die Elementeigenschaften und den Inhalt in einer Antwort GetItem, FindItem oder SyncFolderItems aufzunehmen.  <br/> <br/> Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/>  <br/>  `/GetItem/ItemShape` <br/><br/>  `/FindItem/ItemShape` <br/><br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a>Textwert

Dieses Element kann **true** oder **false**sein. Der Standardwert ist **false**. Dies ist ein Boolean-Datentyp.
  
## <a name="remarks"></a>Hinweise

Dieses Element ist optional.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird eine Anforderung gezeigt, wie das **IncludeMimeContent** -Element festlegen. 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape>
        <t:IncludeMimeContent>true</t:IncludeMimeContent>
        <t:BodyType>Best</t:BodyType>
      </AttachmentShape>
      <AttachmentIds>
        <t:AttachmentId Id="ASkAS="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

Das Anlage-Id-Attribut werden abgeschnitten, um die Lesbarkeit zu erhalten.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

