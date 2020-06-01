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
description: Das CreateAttachment-Element definiert eine Anforderung zum Erstellen einer Anlage für ein Element in der Exchange-Informationsspeicher.
ms.openlocfilehash: 4cba1b8865dae5da58b9617b249a29314c67331a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466437"
---
# <a name="createattachment"></a>CreateAttachment

Das **CreateAttachment** -Element definiert eine Anforderung zum Erstellen einer Anlage für ein Element in der Exchange-Informationsspeicher. 
  
```xml
<CreateAttachment>
   <ParentItemId/>
   <Attachments/>
</CreateAttachment>
```

 **Createattachmenttype**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ParentItemId](parentitemid.md) <br/> |Gibt das übergeordnete Exchange-Informationsspeicher Element an, das die erstellte Anlage enthält. Das [ParentItemId](parentitemid.md) -Element muss die ID eines echten Exchange-Informationsspeicher Elements bereitstellen. Reale Speicherelemente können mithilfe des [GetItem-Vorgangs](getitem-operation.md)abgerufen werden; Anlagen werden mithilfe des [GetAttachment-Vorgangs](getattachment-operation.md)abgerufen. Wenn dem [ParentItemId](parentitemid.md) die ID einer Dateianlage übergeben wird, tritt ein Fehler auf. Wenn der [ParentItemId](parentitemid.md) die ID einer vorhandenen Elementanlage darstellt, fügt der CreateAttachment- [Vorgang](createattachment-operation.md) die neue Anlage zu der vorhandenen Anlage hinzu.  <br/> Dieses Element ist für den [CreateAttachment-Vorgang](createattachment-operation.md)erforderlich.  <br/> |
|[Anlagen](attachments-ex15websvcsotherref.md) <br/> |Enthält die Elemente oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt werden sollen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Eine Elementanlage ist nicht als Speicherelement vorhanden. Sie ist nur als Anlage für ein Element oder eine andere Anlage vorhanden. Element Anlagen können nur mithilfe der [GetAttachment](getattachment.md) -Anforderung abgerufen werden. 
  
Die folgenden Element Anlagen können erstellt werden:
  
- Element
    
- Meldung
    
- CalendarItem
    
- Kontakt
    
- Vorgang
    
- MeetingMessage
    
- MeetingRequest
    
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt, wie Sie ein Element erstellen und an ein anderes Element im Exchange-Informationsspeicher anfügen.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[CreateAttachment-Vorgang](createattachment-operation.md)
  
[DeleteAttachment-Vorgang](deleteattachment-operation.md)
  
[GetAttachment-Vorgang](getattachment-operation.md)

