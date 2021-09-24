---
title: GetNonIndexableItemDetails
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ce3994c1-3bb4-4571-b026-34a6c5705410
description: Das GetNonIndexableItemDetails-Element gibt eine Anforderung zum Abrufen nicht indizierter Elementdetails an.
ms.openlocfilehash: 896b978b9b222454b9e3f016aa0593521e92e33d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533611"
---
# <a name="getnonindexableitemdetails"></a>GetNonIndexableItemDetails

Das **GetNonIndexableItemDetails-Element** gibt eine Anforderung zum Abrufen nicht indizierter Elementdetails an. 
  
```XML
<GetNonIndexableItemDetails>
    <Mailboxes/>
    <PageSize/>
    <PageItemReference/>
    <PageDirection/>
</GetNonIndexableItemDetails>
```

 **GetNonIndexableItemDetailsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Postfächer (NonEmptyArrayOfLegacyDNsType)](mailboxes-nonemptyarrayoflegacydnstype.md) <br/> |Gibt ein Array von **Postfachelementen** an.  <br/> |
|[PageSize](pagesize.md) <br/> |Enthält die Anzahl der Elemente, die auf einer einzelnen Seite für ein Suchergebnis zurückgegeben werden sollen.  <br/> |
|[PageItemReference](pageitemreference.md) <br/> |Gibt den Verweis für ein Seitenelement an.  <br/> |
|[PageDirection](pagedirection.md) <br/> |Enthält die Richtung für die Paginierung im Suchergebnis.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

