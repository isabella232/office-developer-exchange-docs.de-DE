---
title: BodyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- BodyType
api_type:
- schema
ms.assetid: d42ec77b-fb9f-404a-9bf2-1801e8744676
description: Das BodyType-Element gibt an, wie der Textkörper in der Antwort formatiert wird.
ms.openlocfilehash: e8952ac2774589e031280ce982ea8671b736a87d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526841"
---
# <a name="bodytype"></a>BodyType

Das **BodyType-Element** gibt an, wie der Textkörper in der Antwort formatiert wird. 
  
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
|[ItemShape](itemshape.md) <br/> | Identifiziert die Elementeigenschaften und -inhalte, die in eine GetItem-, FindItem- oder SyncFolderItems-Antwort eingeschlossen werden sollen.  <br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>  `/GetItem/ItemShape`<br/><br/>`/FindItem/ItemShape`<br/><br/>`/SyncFolderItems/ItemShape` <br/> |
|[AttachmentShape](attachmentshape.md) <br/> |Identifiziert zusätzliche erweiterte Elementeigenschaften, die in einer Antwort auf eine [GetAttachment-Anforderung](getattachment.md) zurückgegeben werden sollen.  <br/><br/>Für dieses Element wird folgender XPath-Ausdruck verwendet: <br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die möglichen Werte für das **BodyType-Element** aufgeführt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Optimal  <br/> |Die Antwort gibt den umfangreichsten verfügbaren Inhalt des Textkörpers zurück. Dies ist nützlich, wenn nicht bekannt ist, ob es sich bei dem Inhalt um Text oder HTML handelt.<br/><br/> Der zurückgegebene Textkörper ist Text, wenn der gespeicherte Text nur Text ist. Andernfalls gibt die Antwort HTML zurück, wenn der gespeicherte Textkörper im HTML- oder RTF-Format vorliegt.<br/><br/> Dies ist der Standardwert.  <br/> |
|HTML  <br/> |Die Antwort gibt einen Elementtext als HTML zurück.  <br/> |
|Text  <br/> |Die Antwort gibt einen Textkörper als Nur-Text zurück.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können den Typ des in der Antwort zurückgegebenen Textkörpers identifizieren, indem Sie das **BodyType-Attribut** des [Body-Elements](body.md) überprüfen. Das **BodyType-Attribut** identifiziert den Text als HTML oder Text. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel einer Anforderung zeigt, wo ein **BodyType-Element** verwendet wird. 
  
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
        <t:BodyType>Best</t:BodyType>
      </AttachmentShape>
      <AttachmentIds>
        <t:AttachmentId Id="ASkAS="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

Das Id-Attribut wurde gekürzt, um die Lesbarkeit zu gewährleisten.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

