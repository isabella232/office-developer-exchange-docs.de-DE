---
title: Item (UploadItemType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ab7058f2-615f-4393-a0d4-af76727f37e9
description: Das Element stellt ein einzelnes Element in einem Postfach hochladen.
ms.openlocfilehash: 8fecef9a2368a44e38633eb9fddaa8197620f6a1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830138"
---
# <a name="item-uploaditemtype"></a>Item (UploadItemType)

**Das Element** stellt ein einzelnes Element in einem Postfach hochladen. 
  
[UploadItems](uploaditems.md)
  
[Elemente (NonEmptyArrayOfUploadItemsType)](items-nonemptyarrayofuploaditemstype.md)
  
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
|**CreateAction** <br/> |Gibt die Aktion für ein Element in einem Postfach hochladen. Dieses Attribut ist erforderlich.  <br/> |
|**IsAssociated** <br/> |Gibt an, ob das hochgeladene Element einem Ordnerelement verknüpft ist. Dieses Attribut ist ein boolescher Wert. Der Wert **true** gibt an, dass das Element einen Ordner, Element verknüpft ist. Dieses Attribut ist optional.  <br/> |
   
#### <a name="createaction-attribute"></a>CreateAction-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**CreateNew** <br/> |Gibt an, dass eine neue Kopie des ursprünglichen Elements an das Postfach hochgeladen werden. Das [ItemId](itemid.md) -Element muss nicht vorhanden, wenn der Wert CreateNew verwendet wird. Der Bezeichner des neuen Elements wird in der Antwort zurückgegeben.  <br/> |
|**Update** <br/> |Gibt an, dass das Element, das vom **ItemId** -Element angegeben werden aktualisiert. Wenn das **ItemId** -Element nicht vorhanden ist oder wenn das Element in den Ordner vom [ParentFolderId](parentfolderid.md) -Element nicht vorhanden ist, wird ein Fehler zurückgegeben.  <br/> |
|**UpdateOrCreate** <br/> |Gibt an, dass zuerst versucht wird, das Element zu aktualisieren. Wenn das Element in der durch das **ParentFolderId** -Element angegebenen Ordner nicht vorhanden ist, wird ein neues Element erstellt.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des übergeordneten Ordners, in dem ein neues Element erstellt wird oder, die zu aktualisierenden Elements enthält.  <br/> |
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und Ändern eines Elements zum Erstellen oder aktualisieren im Exchange-Speicher.  <br/> |
|[Daten (base64Binary)](data-base64binary.md) <br/> |Enthält die Daten eines einzelnen Elements in einem Postfach hochladen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Elemente (NonEmptyArrayOfUploadItemsType)](items-nonemptyarrayofuploaditemstype.md) <br/> |Enthält ein Array von Element in einem Postfach muss hochgeladen werden.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ExportItems-Vorgang](exportitems-operation.md)
  
[UploadItems-Vorgang](uploaditems-operation.md)

