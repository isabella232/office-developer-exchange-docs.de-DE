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
# <a name="item-uploaditemtype"></a><span data-ttu-id="18fc9-103">Element (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="18fc9-103">Item (UploadItemType)</span></span>

<span data-ttu-id="18fc9-104">Das **Item** -Element stellt ein einzelnes Element dar, das in ein Postfach hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="18fc9-104">The **Item** element represents a single item to upload into a mailbox.</span></span> 
  
[<span data-ttu-id="18fc9-105">UploadItems</span><span class="sxs-lookup"><span data-stu-id="18fc9-105">UploadItems</span></span>](uploaditems.md)
  
[<span data-ttu-id="18fc9-106">Elemente (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="18fc9-106">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md)
  
[<span data-ttu-id="18fc9-107">Element (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="18fc9-107">Item (UploadItemType)</span></span>](item-uploaditemtype.md)
  
```XML
<Item CreateAction="" IsAssociated="">
   <ParentFolderId/>
   <ItemId/>
   <Data/>
</Item>
```

 <span data-ttu-id="18fc9-108">**UploadItemType**</span><span class="sxs-lookup"><span data-stu-id="18fc9-108">**UploadItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="18fc9-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="18fc9-109">Attributes and elements</span></span>

<span data-ttu-id="18fc9-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="18fc9-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18fc9-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="18fc9-111">Attributes</span></span>

|<span data-ttu-id="18fc9-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="18fc9-112">**Attribute**</span></span>|<span data-ttu-id="18fc9-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18fc9-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18fc9-114">**CreateAction**</span><span class="sxs-lookup"><span data-stu-id="18fc9-114">**CreateAction**</span></span> <br/> |<span data-ttu-id="18fc9-115">Gibt die Aktion zum Hochladen eines Elements in ein Postfach an.</span><span class="sxs-lookup"><span data-stu-id="18fc9-115">Specifies the action for uploading an item into a mailbox.</span></span> <span data-ttu-id="18fc9-116">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="18fc9-116">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="18fc9-117">**Isassociated**</span><span class="sxs-lookup"><span data-stu-id="18fc9-117">**IsAssociated**</span></span> <br/> |<span data-ttu-id="18fc9-118">Gibt an, ob das hochgeladene Element ein Ordner zugeordnetes Element ist.</span><span class="sxs-lookup"><span data-stu-id="18fc9-118">Specifies whether the uploaded item is a folder associated item.</span></span> <span data-ttu-id="18fc9-119">Dieses Attribut ist ein boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="18fc9-119">This attribute is a Boolean value.</span></span> <span data-ttu-id="18fc9-120">Der Wert **true** gibt an, dass das Element ein Ordner zugeordnetes Element ist.</span><span class="sxs-lookup"><span data-stu-id="18fc9-120">A value of **true** indicates that the item is a folder associated item.</span></span> <span data-ttu-id="18fc9-121">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="18fc9-121">This attribute is optional.</span></span>  <br/> |
   
#### <a name="createaction-attribute"></a><span data-ttu-id="18fc9-122">Create-Attribut</span><span class="sxs-lookup"><span data-stu-id="18fc9-122">CreateAction Attribute</span></span>

|<span data-ttu-id="18fc9-123">**Wert**</span><span class="sxs-lookup"><span data-stu-id="18fc9-123">**Value**</span></span>|<span data-ttu-id="18fc9-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18fc9-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18fc9-125">**CreateNew**</span><span class="sxs-lookup"><span data-stu-id="18fc9-125">**CreateNew**</span></span> <br/> |<span data-ttu-id="18fc9-126">Gibt an, dass eine neue Kopie des ursprünglichen Elements in das Postfach hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="18fc9-126">Indicates that a new copy of the original item is uploaded to the mailbox.</span></span> <span data-ttu-id="18fc9-127">Das [ItemID](itemid.md) -Element darf nicht vorhanden sein, wenn der CreateNew-Wert verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="18fc9-127">The [ItemId](itemid.md) element must not be present if the CreateNew value is used.</span></span> <span data-ttu-id="18fc9-128">Der neue Elementbezeichner wird in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18fc9-128">The new item identifier is returned in the response.</span></span>  <br/> |
|<span data-ttu-id="18fc9-129">**Update**</span><span class="sxs-lookup"><span data-stu-id="18fc9-129">**Update**</span></span> <br/> |<span data-ttu-id="18fc9-130">Gibt an, dass das Element, das durch das Element **ItemID** angegeben wird, aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="18fc9-130">Specifies that the item indicated by the **ItemId** element will be updated.</span></span> <span data-ttu-id="18fc9-131">Ein Fehler wird zurückgegeben, wenn das **ItemID** -Element nicht vorhanden ist oder wenn das Element nicht in dem durch das [parentfolderid](parentfolderid.md) -Element identifizierten Ordner vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="18fc9-131">An error is returned if the **ItemId** element is not present or if the item does not exist in the folder identified by the [ParentFolderId](parentfolderid.md) element.</span></span>  <br/> |
|<span data-ttu-id="18fc9-132">**UpdateOrCreate**</span><span class="sxs-lookup"><span data-stu-id="18fc9-132">**UpdateOrCreate**</span></span> <br/> |<span data-ttu-id="18fc9-133">Gibt an, dass zunächst versucht wurde, das Element zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="18fc9-133">Indicates that an attempt is first made to update the item.</span></span> <span data-ttu-id="18fc9-134">Wenn das Element nicht in dem durch das **parentfolderid** -Element angegebenen Ordner vorhanden ist, wird ein neues Element erstellt.</span><span class="sxs-lookup"><span data-stu-id="18fc9-134">If the item does not exist in the folder specified by the **ParentFolderId** element, a new item is created.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="18fc9-135">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="18fc9-135">Child elements</span></span>

|<span data-ttu-id="18fc9-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="18fc9-136">**Element**</span></span>|<span data-ttu-id="18fc9-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18fc9-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18fc9-138">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="18fc9-138">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="18fc9-139">Stellt den Bezeichner des übergeordneten Ordners dar, in dem ein neues Element erstellt wird oder das zu aktualisierende Element enthält.</span><span class="sxs-lookup"><span data-stu-id="18fc9-139">Represents the identifier of the parent folder where a new item is created or that contains the item to update.</span></span>  <br/> |
|[<span data-ttu-id="18fc9-140">ItemId</span><span class="sxs-lookup"><span data-stu-id="18fc9-140">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="18fc9-141">Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements, das in der Exchange-Informationsspeicher erstellt oder aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="18fc9-141">Contains the unique identifier and change key of an item to create or update in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="18fc9-142">Data (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="18fc9-142">Data (base64Binary)</span></span>](data-base64binary.md) <br/> |<span data-ttu-id="18fc9-143">Enthält die Daten eines einzelnen Elements, das in ein Postfach hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="18fc9-143">Contains the data of a single item to upload into a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="18fc9-144">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="18fc9-144">Parent elements</span></span>

|<span data-ttu-id="18fc9-145">**Element**</span><span class="sxs-lookup"><span data-stu-id="18fc9-145">**Element**</span></span>|<span data-ttu-id="18fc9-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18fc9-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18fc9-147">Elemente (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="18fc9-147">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md) <br/> |<span data-ttu-id="18fc9-148">Enthält ein Array von Elementen, das in ein Postfach hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="18fc9-148">Contains an array of item to upload into a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="18fc9-149">Textwert</span><span class="sxs-lookup"><span data-stu-id="18fc9-149">Text value</span></span>

<span data-ttu-id="18fc9-150">Keine.</span><span class="sxs-lookup"><span data-stu-id="18fc9-150">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="18fc9-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18fc9-151">Remarks</span></span>

<span data-ttu-id="18fc9-152">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="18fc9-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18fc9-153">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="18fc9-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18fc9-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="18fc9-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="18fc9-155">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="18fc9-155">Schema Name</span></span>  <br/> |<span data-ttu-id="18fc9-156">Schematypen</span><span class="sxs-lookup"><span data-stu-id="18fc9-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="18fc9-157">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="18fc9-157">Validation File</span></span>  <br/> |<span data-ttu-id="18fc9-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="18fc9-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="18fc9-159">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="18fc9-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="18fc9-160">False</span><span class="sxs-lookup"><span data-stu-id="18fc9-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18fc9-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18fc9-161">See also</span></span>



[<span data-ttu-id="18fc9-162">ExportItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="18fc9-162">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="18fc9-163">UploadItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="18fc9-163">UploadItems operation</span></span>](uploaditems-operation.md)

