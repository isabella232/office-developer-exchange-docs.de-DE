---
title: Element (UploadItemType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ab7058f2-615f-4393-a0d4-af76727f37e9
description: Das Item-Element stellt ein einzelnes Element dar, das in ein Postfach hochgeladen werden soll.
ms.openlocfilehash: 82c0fdf89c06ddfb812c2b2f1899b589eedeb7d8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467550"
---
# <a name="item-uploaditemtype"></a>Element (UploadItemType)

Das **Item** -Element stellt ein einzelnes Element dar, das in ein Postfach hochgeladen werden soll. 
  
[UploadItems](uploaditems.md)
  
[Elemente (NonEmptyArrayOfUploadItemsType)](items-nonemptyarrayofuploaditemstype.md)
  
[Element (UploadItemType)](item-uploaditemtype.md)
  
```XML
<Item CreateAction="" IsAssociated="">
   <ParentFolderId/>
   <ItemId/>
   <Data/>
</Item>
```

 **UploadItemType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**CreateAction** <br/> |Gibt die Aktion zum Hochladen eines Elements in ein Postfach an. Dieses Attribut ist erforderlich.  <br/> |
|**Isassociated** <br/> |Gibt an, ob das hochgeladene Element ein Ordner zugeordnetes Element ist. Dieses Attribut ist ein boolescher Wert. Der Wert **true** gibt an, dass das Element ein Ordner zugeordnetes Element ist. Dieses Attribut ist optional.  <br/> |
   
#### <a name="createaction-attribute"></a>Create-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**CreateNew** <br/> |Gibt an, dass eine neue Kopie des ursprünglichen Elements in das Postfach hochgeladen wird. Das [ItemID](itemid.md) -Element darf nicht vorhanden sein, wenn der CreateNew-Wert verwendet wird. Der neue Elementbezeichner wird in der Antwort zurückgegeben.  <br/> |
|**Update** <br/> |Gibt an, dass das Element, das durch das Element **ItemID** angegeben wird, aktualisiert wird. Ein Fehler wird zurückgegeben, wenn das **ItemID** -Element nicht vorhanden ist oder wenn das Element nicht in dem durch das [parentfolderid](parentfolderid.md) -Element identifizierten Ordner vorhanden ist.  <br/> |
|**UpdateOrCreate** <br/> |Gibt an, dass zunächst versucht wurde, das Element zu aktualisieren. Wenn das Element nicht in dem durch das **parentfolderid** -Element angegebenen Ordner vorhanden ist, wird ein neues Element erstellt.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des übergeordneten Ordners dar, in dem ein neues Element erstellt wird oder das zu aktualisierende Element enthält.  <br/> |
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements, das in der Exchange-Informationsspeicher erstellt oder aktualisiert werden soll.  <br/> |
|[Data (base64Binary)](data-base64binary.md) <br/> |Enthält die Daten eines einzelnen Elements, das in ein Postfach hochgeladen werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Elemente (NonEmptyArrayOfUploadItemsType)](items-nonemptyarrayofuploaditemstype.md) <br/> |Enthält ein Array von Elementen, das in ein Postfach hochgeladen werden soll.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ExportItems-Vorgang](exportitems-operation.md)
  
[UploadItems-Vorgang](uploaditems-operation.md)

