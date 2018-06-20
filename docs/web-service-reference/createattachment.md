---
title: CreateAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAttachment
api_type:
- schema
ms.assetid: e33b403a-b7d3-48ee-8d24-6b7abf0d70bc
description: Das CreateAttachment-Element definiert eine Anforderung an eine Anlage zu einem Element in der Exchange-Speicher zu erstellen.
ms.openlocfilehash: d403eb5ca15623d3a973f7b224dbcde5529cf1bc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757741"
---
# <a name="createattachment"></a>CreateAttachment

Das **CreateAttachment** -Element definiert eine Anforderung an eine Anlage zu einem Element in der Exchange-Speicher zu erstellen. 
  
```xml
<CreateAttachment>
   <ParentItemId/>
   <Attachments/>
</CreateAttachment>
```

 **CreateAttachmentType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ParentItemId](parentitemid.md) <br/> |Gibt das übergeordnete Exchange Store-Element, das die erstellte Anlage enthält. Das [ParentItemId](parentitemid.md) -Element muss die ID des einer realen Exchange-Datenspeicherelement bereitstellen. Echte Store Elemente können mithilfe der [GetItem Operation](getitem-operation.md)abgerufen werden. Anlagen werden mithilfe des [Vorgangs GetAttachment](getattachment-operation.md)abgerufen. Ein Fehler tritt auf, wenn die [ParentItemId](parentitemid.md) die ID der Dateianlage zu einer übergeben wird. Wenn die [ParentItemId](parentitemid.md) die ID der Elementanlage vorhandenes darstellt, fügt den [CreateAttachment Vorgang](createattachment-operation.md) die neue Anlage in die vorhandene Anlage.  <br/> Dieses Element ist für den [Vorgang CreateAttachment](createattachment-operation.md)erforderlich.  <br/> |
|[Anlagen](attachments-ex15websvcsotherref.md) <br/> |Enthält die Elemente oder Dateien eines Elements in der Exchange-Speicher an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Elementanlage ist nicht als Store Element vorhanden. Es ist nur als Anlage zu einem Element oder eine andere Anlage vorhanden. Anlagen können nur mithilfe der [GetAttachment](getattachment.md) -Anforderung abgerufen werden. 
  
Die folgenden elementanlagen können erstellt werden:
  
- Element
    
- Nachricht
    
- CalendarItem
    
- Kontakt
    
- Aufgabe
    
- MeetingMessage
    
- MeetingRequest
    
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird gezeigt, wie zu erstellen, und fügen Sie ein Element mit einem anderen Element im Exchange-Speicher.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <ParentItemId Id="ASkAS"/>
      <Attachments>
        <t:ItemAttachment>
          <t:Name>MyAttachment</t:Name>
          <t:Message>
            <t:ItemClass>IPM>Note</t:ItemClass>
            <t:Subject>My attachment subject</t:Subject>
            <t:Body BodyType="Text">My attachment body</t:Body>
          </t:Message>
        </t:ItemAttachment>
      </Attachments>
    </CreateAttachment>
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



[CreateAttachment-Vorgang](createattachment-operation.md)
  
[DeleteAttachment-Vorgang](deleteattachment-operation.md)
  
[GetAttachment-Vorgang](getattachment-operation.md)

