---
title: CreateAttachment-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CreateAttachment
api_type:
- schema
ms.assetid: e066db95-6963-4507-a8d0-8efad287f550
description: Der CreateAttachment-Vorgang erstellt entweder ein Element oder eine Dateianlage und fügt es an das angegebene Element an.
ms.openlocfilehash: 0c75e8c73bf4352e2703a6ca6ac06e261e8f37c9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511881"
---
# <a name="createattachment-operation"></a>CreateAttachment-Vorgang

Der CreateAttachment-Vorgang erstellt entweder ein Element oder eine Dateianlage und fügt es an das angegebene Element an.
  
## <a name="file-createattachment-request-example"></a>Beispiel für datei createAttachment-Anforderung

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer CreateAttachment-Anforderung zeigt, wie Sie eine Dateianlage erstellen.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
<soap:Body>
  <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
    <ParentItemId Id="AAAtAE..." ChangeKey="CQAAABYA..."/>
    <Attachments>
      <t:FileAttachment>
        <t:Name>SomeFile</t:Name>
        <t:Content>AQIDBAU=</t:Content>
      </t:FileAttachment>
    </Attachments>
  </CreateAttachment>
</soap:Body>
</soap:Envelope>
```

### <a name="comment"></a>Kommentar

Ein Name für die Anlage muss angegeben werden.
  
> [!NOTE]
> Der Bezeichner des übergeordneten Elements und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu gewährleisten. 
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [CreateAttachment](createattachment.md)
    
- [ParentItemId](parentitemid.md)
    
- [Anhänge](attachments-ex15websvcsotherref.md)
    
- [FileAttachment](fileattachment.md)
    
- [Name (AttachmentType)](name-attachmenttype.md)
    
- [Inhalt](content.md)
    
## <a name="successful-file-createattachment-response-example"></a>Beispiel für erfolgreiche "File CreateAttachment"-Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die CreateAttachment-Anforderung.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="AAAtAE=" RootItemId="AAAtAEFk=" RootItemChangeKey="CQAAAB"/>
            </t:FileAttachment>
          </m:Attachments>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </CreateAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a>Kommentar

Die Antwort enthält den Bezeichner der angefügten Datei. Es enthält auch den Bezeichner und den Änderungsschlüssel des Stammelements. Die Elementbezeichner und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu gewährleisten.
  
### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateAttachmentResponse](createattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateAttachmentResponseMessage](createattachmentresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Anhänge](attachments-ex15websvcsotherref.md)
    
- [FileAttachment](fileattachment.md)
    
- [AttachmentId](attachmentid.md)
    
## <a name="item-createattachment-request-example"></a>Beispiel für eine Item CreateAttachment-Anforderung

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer CreateAttachment-Anforderung zeigt, wie Sie eine Elementanlage erstellen.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <ParentItemId Id="AAAtAE=" ChangeKey="CQAAABYA"/>
      <Attachments>
        <t:ItemAttachment>
          <t:Name>An item attachment</t:Name>
          <t:Message>
            <t:Subject>A message to attach</t:Subject>
          </t:Message>
        </t:ItemAttachment>
      </Attachments>
    </CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a>Kommentar

Ein Name für die Anlage muss angegeben werden.
  
 **Hinweis** Der Bezeichner des übergeordneten Elements und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu gewährleisten. 
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [CreateAttachment](createattachment.md)
    
- [ParentItemId](parentitemid.md)
    
- [Anhänge](attachments-ex15websvcsotherref.md)
    
- [ItemAttachment](itemattachment.md)
    
- [Name (AttachmentType)](name-attachmenttype.md)
    
- [Meldung](message-ex15websvcsotherref.md)
    
- [Betreff](subject.md)
    
## <a name="successful-item-createattachment-response-example"></a>Beispiel für erfolgreiches CreateAttachment-Element

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die CreateAttachment-Anforderung.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:ItemAttachment>
              <t:AttachmentId Id="AAAtAEFk=" RootItemId="AAAtAEFkb=" RootItemChangeKey="CQAAABYA"/>
            </t:ItemAttachment>
          </m:Attachments>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </CreateAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a>Kommentar

Die Antwort enthält den Bezeichner der neuen Anlage. Es enthält auch den Bezeichner und den Änderungsschlüssel des Stammelements. Das Stammelement ist das Element, das die Anlage enthält. Die Elementbezeichner und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu gewährleisten.
  
### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateAttachmentResponse](createattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateAttachmentResponseMessage](createattachmentresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Anhänge](attachments-ex15websvcsotherref.md)
    
- [ItemAttachment](itemattachment.md)
    
- [AttachmentId](attachmentid.md)
    
## <a name="createattachment-error-response-example"></a>Beispiel für CreateAttachment-Fehlerantwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort auf die CreateAttachment-Anforderung. Der Fehler ist darauf zurückzuführen, dass der Name der Anlage nicht angegeben wurde.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Error">
          <m:MessageText>Required property is missing.</m:MessageText>
          <m:ResponseCode>ErrorRequiredPropertyMissing</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:MessageXml>
            <t:ExceptionFieldURI FieldURI="attachment:Name"/>
          </m:MessageXml>
          <m:Attachments/>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </CreateAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Fehlerantwortelemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateAttachmentResponse](createattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateAttachmentResponseMessage](createattachmentresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [MessageXml](messagexml.md)
    
- [ExceptionFieldURI](exceptionfielduri.md)
    
- [Anhänge](attachments-ex15websvcsotherref.md)
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn an ein Element in einem einzelnen Roundtrip mehrere Anlagen angefügt sind, ist rootItemChangeKey in der letzten Antwortnachricht diejenige, die den neuen Änderungsschlüssel des Elements darstellt, das die Anlagen enthält.
  
## <a name="see-also"></a>Siehe auch



[DeleteAttachment-Vorgang](deleteattachment-operation.md)
  
[GetAttachment-Vorgang](getattachment-operation.md)

