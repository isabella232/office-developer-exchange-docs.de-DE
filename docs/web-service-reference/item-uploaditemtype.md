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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830138"
---
# <a name="item-uploaditemtype"></a><span data-ttu-id="4ec99-103">Item (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="4ec99-103">Item (UploadItemType)</span></span>

<span data-ttu-id="4ec99-104">**Das Element** stellt ein einzelnes Element in einem Postfach hochladen.</span><span class="sxs-lookup"><span data-stu-id="4ec99-104">The **Item** element represents a single item to upload into a mailbox.</span></span> 
  
[<span data-ttu-id="4ec99-105">UploadItems</span><span class="sxs-lookup"><span data-stu-id="4ec99-105">UploadItems</span></span>](uploaditems.md)
  
[<span data-ttu-id="4ec99-106">Elemente (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="4ec99-106">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md)
  
[<span data-ttu-id="4ec99-107">Item (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="4ec99-107">Item (UploadItemType)</span></span>](item-uploaditemtype.md)
  
```XML
<Item CreateAction="" IsAssociated="">
   <ParentFolderId/>
   <ItemId/>
   <Data/>
</Item>
```

 <span data-ttu-id="4ec99-108">**UploadItemType**</span><span class="sxs-lookup"><span data-stu-id="4ec99-108">**UploadItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4ec99-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4ec99-109">Attributes and elements</span></span>

<span data-ttu-id="4ec99-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4ec99-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ec99-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="4ec99-111">Attributes</span></span>

|<span data-ttu-id="4ec99-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4ec99-112">**Attribute**</span></span>|<span data-ttu-id="4ec99-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ec99-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4ec99-114">**CreateAction**</span><span class="sxs-lookup"><span data-stu-id="4ec99-114">**CreateAction**</span></span> <br/> |<span data-ttu-id="4ec99-115">Gibt die Aktion für ein Element in einem Postfach hochladen.</span><span class="sxs-lookup"><span data-stu-id="4ec99-115">Specifies the action for uploading an item into a mailbox.</span></span> <span data-ttu-id="4ec99-116">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4ec99-116">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="4ec99-117">**IsAssociated**</span><span class="sxs-lookup"><span data-stu-id="4ec99-117">**IsAssociated**</span></span> <br/> |<span data-ttu-id="4ec99-118">Gibt an, ob das hochgeladene Element einem Ordnerelement verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="4ec99-118">Specifies whether the uploaded item is a folder associated item.</span></span> <span data-ttu-id="4ec99-119">Dieses Attribut ist ein boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="4ec99-119">This attribute is a Boolean value.</span></span> <span data-ttu-id="4ec99-120">Der Wert **true** gibt an, dass das Element einen Ordner, Element verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="4ec99-120">A value of **true** indicates that the item is a folder associated item.</span></span> <span data-ttu-id="4ec99-121">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="4ec99-121">This attribute is optional.</span></span>  <br/> |
   
#### <a name="createaction-attribute"></a><span data-ttu-id="4ec99-122">CreateAction-Attribut</span><span class="sxs-lookup"><span data-stu-id="4ec99-122">CreateAction Attribute</span></span>

|<span data-ttu-id="4ec99-123">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4ec99-123">**Value**</span></span>|<span data-ttu-id="4ec99-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ec99-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4ec99-125">**CreateNew**</span><span class="sxs-lookup"><span data-stu-id="4ec99-125">**CreateNew**</span></span> <br/> |<span data-ttu-id="4ec99-126">Gibt an, dass eine neue Kopie des ursprünglichen Elements an das Postfach hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="4ec99-126">Indicates that a new copy of the original item is uploaded to the mailbox.</span></span> <span data-ttu-id="4ec99-127">Das [ItemId](itemid.md) -Element muss nicht vorhanden, wenn der Wert CreateNew verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4ec99-127">The [ItemId](itemid.md) element must not be present if the CreateNew value is used.</span></span> <span data-ttu-id="4ec99-128">Der Bezeichner des neuen Elements wird in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4ec99-128">The new item identifier is returned in the response.</span></span>  <br/> |
|<span data-ttu-id="4ec99-129">**Update**</span><span class="sxs-lookup"><span data-stu-id="4ec99-129">**Update**</span></span> <br/> |<span data-ttu-id="4ec99-130">Gibt an, dass das Element, das vom **ItemId** -Element angegeben werden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4ec99-130">Specifies that the item indicated by the **ItemId** element will be updated.</span></span> <span data-ttu-id="4ec99-131">Wenn das **ItemId** -Element nicht vorhanden ist oder wenn das Element in den Ordner vom [ParentFolderId](parentfolderid.md) -Element nicht vorhanden ist, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4ec99-131">An error is returned if the **ItemId** element is not present or if the item does not exist in the folder identified by the [ParentFolderId](parentfolderid.md) element.</span></span>  <br/> |
|<span data-ttu-id="4ec99-132">**UpdateOrCreate**</span><span class="sxs-lookup"><span data-stu-id="4ec99-132">**UpdateOrCreate**</span></span> <br/> |<span data-ttu-id="4ec99-133">Gibt an, dass zuerst versucht wird, das Element zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4ec99-133">Indicates that an attempt is first made to update the item.</span></span> <span data-ttu-id="4ec99-134">Wenn das Element in der durch das **ParentFolderId** -Element angegebenen Ordner nicht vorhanden ist, wird ein neues Element erstellt.</span><span class="sxs-lookup"><span data-stu-id="4ec99-134">If the item does not exist in the folder specified by the **ParentFolderId** element, a new item is created.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4ec99-135">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ec99-135">Child elements</span></span>

|<span data-ttu-id="4ec99-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="4ec99-136">**Element**</span></span>|<span data-ttu-id="4ec99-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ec99-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ec99-138">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="4ec99-138">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="4ec99-139">Stellt den Bezeichner des übergeordneten Ordners, in dem ein neues Element erstellt wird oder, die zu aktualisierenden Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="4ec99-139">Represents the identifier of the parent folder where a new item is created or that contains the item to update.</span></span>  <br/> |
|[<span data-ttu-id="4ec99-140">ItemId</span><span class="sxs-lookup"><span data-stu-id="4ec99-140">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="4ec99-141">Enthält den eindeutigen Bezeichner und Ändern eines Elements zum Erstellen oder aktualisieren im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="4ec99-141">Contains the unique identifier and change key of an item to create or update in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4ec99-142">Daten (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="4ec99-142">Data (base64Binary)</span></span>](data-base64binary.md) <br/> |<span data-ttu-id="4ec99-143">Enthält die Daten eines einzelnen Elements in einem Postfach hochladen.</span><span class="sxs-lookup"><span data-stu-id="4ec99-143">Contains the data of a single item to upload into a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4ec99-144">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ec99-144">Parent elements</span></span>

|<span data-ttu-id="4ec99-145">**Element**</span><span class="sxs-lookup"><span data-stu-id="4ec99-145">**Element**</span></span>|<span data-ttu-id="4ec99-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ec99-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ec99-147">Elemente (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="4ec99-147">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md) <br/> |<span data-ttu-id="4ec99-148">Enthält ein Array von Element in einem Postfach muss hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="4ec99-148">Contains an array of item to upload into a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4ec99-149">Textwert</span><span class="sxs-lookup"><span data-stu-id="4ec99-149">Text value</span></span>

<span data-ttu-id="4ec99-150">Keine.</span><span class="sxs-lookup"><span data-stu-id="4ec99-150">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4ec99-151">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4ec99-151">Remarks</span></span>

<span data-ttu-id="4ec99-152">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4ec99-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4ec99-153">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4ec99-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ec99-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ec99-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4ec99-155">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4ec99-155">Schema Name</span></span>  <br/> |<span data-ttu-id="4ec99-156">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4ec99-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="4ec99-157">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4ec99-157">Validation File</span></span>  <br/> |<span data-ttu-id="4ec99-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4ec99-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4ec99-159">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4ec99-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="4ec99-160">False</span><span class="sxs-lookup"><span data-stu-id="4ec99-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4ec99-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ec99-161">See also</span></span>



[<span data-ttu-id="4ec99-162">ExportItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4ec99-162">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="4ec99-163">UploadItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4ec99-163">UploadItems operation</span></span>](uploaditems-operation.md)

