---
title: BodyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BodyType
api_type:
- schema
ms.assetid: d42ec77b-fb9f-404a-9bf2-1801e8744676
description: Das BodyType-Element identifiziert, wie der Textkörper in der Antwort formatiert ist.
ms.openlocfilehash: f8be2e96390b40faa367cf0d34c533accc3b8afb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757479"
---
# <a name="bodytype"></a>BodyType

Das **BodyType** -Element identifiziert, wie der Textkörper in der Antwort formatiert ist. 
  
```xml
<BodyType>Best or HTML or Text</BodyType>
```

**BodyTypeResponseType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> | Identifiziert die Elementeigenschaften und den Inhalt in einer Antwort GetItem, FindItem oder SyncFolderItems aufzunehmen.  <br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>  `/GetItem/ItemShape`<br/><br/>`/FindItem/ItemShape`<br/><br/>`/SyncFolderItems/ItemShape` <br/> |
|[AttachmentShape](attachmentshape.md) <br/> |Zusätzliche erweiterte Elementeigenschaften in einer Antwort auf eine Anforderung [GetAttachment](getattachment.md) zurückzugebenden identifiziert.  <br/><br/>Es folgt der XPath-Ausdruck, der dieses Element:<br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="text-value"></a>Textwert

Die folgende Tabelle enthält die möglichen Werte für das Element **"BodyType"** . 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Am besten  <br/> |Die Antwort wird den inhaltlich verfügbaren Inhalt des Textkörpers zurückzugeben. Dies ist nützlich, wenn nicht bekannt ist, ob der Inhalt Text "oder" HTML ist.<br/><br/> Der zurückgegebene Text ist Text wird, wenn der gespeicherte Text nur-Text. Andernfalls gibt die Antwort HTML zurück, wenn der gespeicherte Textkörper in HTML oder RTF-Format ist.<br/><br/> Dies ist der Standardwert.  <br/> |
|HTML  <br/> |Die Antwort wird ein Textkörper im HTML-Format zurück.  <br/> |
|Text  <br/> |Die Antwort wird ein Textkörper als nur-Text zurück.  <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können den Typ des Mobilgeräts **BodyType** -Attribut des [Body](body.md) -Elements in der Antwort zurückgegebenen Textkörper identifizieren. Das Attribut **BodyType** erkennt den Text als HTML oder Text. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird eine Anforderung zeigt, wo ein **BodyType** -Element verwendet wird. 
  
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
        <t:BodyType>Best</t:BodyType>
      </AttachmentShape>
      <AttachmentIds>
        <t:AttachmentId Id="ASkAS="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

Das Id-Attribut wurde gekürzt, um die Lesbarkeit zu erhalten.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

