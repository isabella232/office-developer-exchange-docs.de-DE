---
title: SearchPreviewItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 59b0b2db-a0ae-4162-a2cb-5f37f42fe872
description: Das SearchPreviewItem-Element gibt die Elementvorschau für eine Ermittlungssuche an.
ms.openlocfilehash: 7ecc034de3386ed35f0071403c013e91b79d13c5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59534301"
---
# <a name="searchpreviewitem"></a>SearchPreviewItem

Das **SearchPreviewItem-Element** gibt die Elementvorschau für eine Ermittlungssuche an. 
  
```XML
<SearchPreviewItem>
   <Id/>
   <Mailbox/>
   <ParentId/>
   <ItemClass/>
   <UniqueHash/>
   <SortValue/>
   <OwaLink/>
   <Sender/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <CreatedTime/>
   <ReceivedTime/>
   <SentTime/>
   <Subject/>
   <Size/>
   <Preview/>
   <Importance/>
   <Read/>
   <HasAttachment/>
   <ExtendedProperties/>
</SearchPreviewItem>
```

 **SearchPreviewItemType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[ID (ItemIdType)](id-itemidtype.md)  |  [Postfach (PreviewItemMailboxType)](mailbox-previewitemmailboxtype.md)  |  [ParentId](parentid.md)  |  [ItemClass](itemclass.md)  |  [UniqueHash](uniquehash.md)  |  [SortValue](sortvalue.md)  |  [OwaLink](owalink.md)  |  [Sender (Zeichenfolge)](sender-string.md)  |  [ToRecipients (ArrayOfSmtpAddressType)](torecipients-arrayofsmtpaddresstype.md)  |  [CcRecipients](ccrecipients.md)  |  [BccRecipients](bccrecipients.md)  |  [CreatedTime](createdtime.md)  |  [ReceivedTime](receivedtime.md)  |  [SentTime](senttime.md)  |  [Betreff](subject.md)  |  [Größe (lang)](size-long.md)  |  [Vorschau](preview-ex15websvcsotherref.md)  |  [Wichtigkeit](importance.md)  |  [Lesen](read.md)  |  [HasAttachment](hasattachment.md)  |  [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Items (ArrayOfSearchPreviewItemsType)](items-arrayofsearchpreviewitemstype.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

