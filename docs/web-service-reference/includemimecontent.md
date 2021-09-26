---
title: IncludeMimeContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IncludeMimeContent
api_type:
- schema
ms.assetid: 3f3c2300-55cd-41c0-900e-b470b290d52f
description: Das IncludeMimeContent-Element gibt an, ob der MIME-Inhalt (Multipurpose Internet Mail Extensions) eines Elements oder einer Anlage in der Antwort zurückgegeben wird.
ms.openlocfilehash: 04d015ea450907f3968200dcbb6f411eb6343681
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542176"
---
# <a name="includemimecontent"></a>IncludeMimeContent

Das **IncludeMimeContent-Element** gibt an, ob der MIME-Inhalt (Multipurpose Internet Mail Extensions) eines Elements oder einer Anlage in der Antwort zurückgegeben wird. 
  
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
|[AttachmentShape](attachmentshape.md) <br/> | Identifiziert zusätzliche Eigenschaften, die in einer Antwort auf eine [GetAttachment-Anforderung](getattachment.md) zurückgegeben werden sollen.  <br/> <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifiziert die Elementeigenschaften und -inhalte, die in eine GetItem-, FindItem- oder SyncFolderItems-Antwort eingeschlossen werden sollen.  <br/> <br/> Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/>  <br/>  `/GetItem/ItemShape` <br/><br/>  `/FindItem/ItemShape` <br/><br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a>Textwert

Dieses Element kann entweder **"true"** oder **"false" sein.** Der Standardwert ist **false**. Dies ist ein boolescher Datentyp.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element ist optional.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel einer Anforderung veranschaulicht, wie das **IncludeMimeContent-Element** festgelegt wird. 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

Das Anlagen-ID-Attribut wird abgeschnitten, um die Lesbarkeit zu gewährleisten.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

