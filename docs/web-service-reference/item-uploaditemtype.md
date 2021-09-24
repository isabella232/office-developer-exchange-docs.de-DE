---
title: Item (UploadItemType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ab7058f2-615f-4393-a0d4-af76727f37e9
description: Das Item-Element stellt ein einzelnes Element dar, das in ein Postfach hochgeladen werden soll.
ms.openlocfilehash: bd4681a19df2018db9e54ee39095cd602662650a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514445"
---
# <a name="item-uploaditemtype"></a>Item (UploadItemType)

Das **Item-Element** stellt ein einzelnes Element dar, das in ein Postfach hochgeladen werden soll. 
  
[UploadItems](uploaditems.md)
  
[Items (NonEmptyArrayOfUploadItemsType)](items-nonemptyarrayofuploaditemstype.md)
  
[Item (UploadItemType)](item-uploaditemtype.md)
  
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
|**IsAssociated** <br/> |Gibt an, ob das hochgeladene Element ein zugeordnetes Ordnerelement ist. Dieses Attribut ist ein boolescher Wert. Der Wert **"true"** gibt an, dass es sich bei dem Element um ein dem Ordner zugeordnetes Element handelt. Dieses Attribut ist optional.  <br/> |
   
#### <a name="createaction-attribute"></a>CreateAction-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**CreateNew** <br/> |Gibt an, dass eine neue Kopie des ursprünglichen Elements in das Postfach hochgeladen wird. Das [ItemId-Element](itemid.md) darf nicht vorhanden sein, wenn der CreateNew-Wert verwendet wird. Der neue Elementbezeichner wird in der Antwort zurückgegeben.  <br/> |
|**Update** <br/> |Gibt an, dass das durch das **ItemId-Element** angegebene Element aktualisiert wird. Ein Fehler wird zurückgegeben, wenn das **ItemId-Element** nicht vorhanden ist oder wenn das Element nicht in dem durch das [ParentFolderId-Element identifizierten](parentfolderid.md) Ordner vorhanden ist.  <br/> |
|**UpdateOrCreate** <br/> |Gibt an, dass zuerst versucht wird, das Element zu aktualisieren. Wenn das Element in dem durch das **ParentFolderId-Element** angegebenen Ordner nicht vorhanden ist, wird ein neues Element erstellt.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des übergeordneten Ordners dar, in dem ein neues Element erstellt wird oder das das zu aktualisierende Element enthält.  <br/> |
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements, das im Exchange Speicher erstellt oder aktualisiert werden soll.  <br/> |
|[Daten (base64Binary)](data-base64binary.md) <br/> |Enthält die Daten eines einzelnen Elements, das in ein Postfach hochgeladen werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Items (NonEmptyArrayOfUploadItemsType)](items-nonemptyarrayofuploaditemstype.md) <br/> |Enthält ein Array von Elementen, die in ein Postfach hochgeladen werden sollen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

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

