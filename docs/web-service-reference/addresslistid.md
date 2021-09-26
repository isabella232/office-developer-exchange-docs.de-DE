---
title: AddressListId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a3334bb2-90dc-4fe1-96d9-890b13d9ff30
description: Das AddressListId-Element gibt den Bezeichner einer Adressliste an.
ms.openlocfilehash: 5348c6877e24fcc0c8873df1098f8a8e30fe4c1c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541560"
---
# <a name="addresslistid"></a>AddressListId

Das **AddressListId-Element** gibt den Bezeichner einer Adressliste an. 
  
```XML
<AddressListId Id="">
</AddressListId>
```

 **AddressListIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Id** <br/> |Eine Zeichenfolgenadresslisten-ID. Dieses Attribut ist erforderlich.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |Gibt den Ordner an, der für Aktionen bestimmt ist, die Ordner verwenden. Dieses Element muss beim Kopieren, Löschen, Verschieben und Festlegen des Lesestatus von Unterhaltungselementen in einem Zielordner vorhanden sein.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Gibt den Bezeichner des Ordners an, in den E-Mail-Elemente kopiert werden.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Gibt den Zielordner für Kopier- und Verschiebungsaktionen an.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Gibt den Bezeichner des Ordners an, in den E-Mail-Elemente verschoben werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

