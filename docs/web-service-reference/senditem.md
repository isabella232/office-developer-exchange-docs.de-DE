---
title: SendItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendItem
api_type:
- schema
ms.assetid: a966da19-b05a-4504-ac98-91acc1667b9a
description: Das SendItem-Element ist das Stammelement in einer Anforderung, ein Element im Exchange-Informationsspeicher zu senden.
ms.openlocfilehash: 28f0d484dd079146c998cb7317bd2d80c6739e19
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530565"
---
# <a name="senditem"></a><span data-ttu-id="f534f-103">SendItem</span><span class="sxs-lookup"><span data-stu-id="f534f-103">SendItem</span></span>

<span data-ttu-id="f534f-104">Das **SendItem** -Element ist das Stammelement in einer Anforderung, ein Element im Exchange-Informationsspeicher zu senden.</span><span class="sxs-lookup"><span data-stu-id="f534f-104">The **SendItem** element is the root element in a request to send an item in the Exchange store.</span></span> 
  
```xml
<SendItem SaveItemToFolder="">
   <ItemIds/>
   <SavedItemFolderId/>
</SendItem>
```

 <span data-ttu-id="f534f-105">**SendItemType**</span><span class="sxs-lookup"><span data-stu-id="f534f-105">**SendItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f534f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f534f-106">Attributes and elements</span></span>

<span data-ttu-id="f534f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f534f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f534f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f534f-108">Attributes</span></span>

|<span data-ttu-id="f534f-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f534f-109">**Attribute**</span></span>|<span data-ttu-id="f534f-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f534f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f534f-111">**SaveItemToFolder**</span><span class="sxs-lookup"><span data-stu-id="f534f-111">**SaveItemToFolder**</span></span> <br/> |<span data-ttu-id="f534f-112">Gibt an, ob eine Kopie des gesendeten Elements gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="f534f-112">Identifies whether a copy of the sent item is saved.</span></span> <span data-ttu-id="f534f-113">Die Save-Aktion hängt vom Wert von **SaveItemToFolder** und davon ab, ob ein [SavedItemFolderId](saveditemfolderid.md) -Element in der Anforderung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f534f-113">The save action depends on the value of **SaveItemToFolder** and whether a [SavedItemFolderId](saveditemfolderid.md) element is present in the request.</span></span> <span data-ttu-id="f534f-114">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f534f-114">This element is required.</span></span>  <br/> |
   
#### <a name="saveitemtofolder-attribute"></a><span data-ttu-id="f534f-115">SaveItemToFolder-Attribut</span><span class="sxs-lookup"><span data-stu-id="f534f-115">SaveItemToFolder Attribute</span></span>

|<span data-ttu-id="f534f-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f534f-116">**Value**</span></span>|<span data-ttu-id="f534f-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f534f-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f534f-118">**true**</span><span class="sxs-lookup"><span data-stu-id="f534f-118">**true**</span></span> <br/> |<span data-ttu-id="f534f-119">Wenn das [SavedItemFolderId](saveditemfolderid.md) -Element nicht vorhanden ist, wird das Element im Ordner "Gesendete Elemente" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f534f-119">If the [SavedItemFolderId](saveditemfolderid.md) element is not present, the item is saved in the Sent Items folder.</span></span> <span data-ttu-id="f534f-120">Wenn das [SavedItemFolderId](saveditemfolderid.md) -Element vorhanden ist, wird das Element in dem Ordner gespeichert, der durch das [SavedItemFolderId](saveditemfolderid.md) -Element angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f534f-120">If the [SavedItemFolderId](saveditemfolderid.md) element is present, the item is saved in the folder that is specified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
|<span data-ttu-id="f534f-121">**False**</span><span class="sxs-lookup"><span data-stu-id="f534f-121">**false**</span></span> <br/> |<span data-ttu-id="f534f-122">Wenn das [SavedItemFolderId](saveditemfolderid.md) -Element nicht vorhanden ist, wird das Element nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f534f-122">If the [SavedItemFolderId](saveditemfolderid.md) element is not present, the item is not saved.</span></span> <span data-ttu-id="f534f-123">Wenn das [SavedItemFolderId](saveditemfolderid.md) -Element vorhanden ist, wird eine Fehlerantwort mit einem [Response Code](responsecode.md) -Element zurückgegeben, das den **ErrorInvalidSendItemSaveSettings** -Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="f534f-123">If the [SavedItemFolderId](saveditemfolderid.md) element is present, an error response will be returned with a [ResponseCode](responsecode.md) element that contains the **ErrorInvalidSendItemSaveSettings** value.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f534f-124">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f534f-124">Child elements</span></span>

|<span data-ttu-id="f534f-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="f534f-125">**Element**</span></span>|<span data-ttu-id="f534f-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f534f-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f534f-127">ItemIds</span><span class="sxs-lookup"><span data-stu-id="f534f-127">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="f534f-128">Enthält die eindeutigen Identitäten von Elementen, Element Elementen und wiederkehrenden Hauptelementen, die zum Löschen, senden, abrufen, verlagern oder Kopieren von Elementen in der Exchange-Informationsspeicher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f534f-128">Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f534f-129">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="f534f-129">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> |<span data-ttu-id="f534f-130">Identifiziert den Zielordner für Vorgänge, die Elemente im Exchange-Informationsspeicher aktualisieren, senden und erstellen.</span><span class="sxs-lookup"><span data-stu-id="f534f-130">Identifies the target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f534f-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f534f-131">Parent elements</span></span>

<span data-ttu-id="f534f-132">Keine.</span><span class="sxs-lookup"><span data-stu-id="f534f-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f534f-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f534f-133">Remarks</span></span>

<span data-ttu-id="f534f-134">Wenn ein Element im Ordner "Gesendete Elemente" gesendet wird, wird das gesendete Element gelöscht, und eine Kopie davon wird im Ordner "Gesendete Elemente" abgelegt.</span><span class="sxs-lookup"><span data-stu-id="f534f-134">If an item in the Sent Items folder is sent, the sent item is deleted and a copy of it is put in the Sent Items folder.</span></span>
  
<span data-ttu-id="f534f-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f534f-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f534f-136">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f534f-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f534f-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="f534f-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f534f-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f534f-138">Schema Name</span></span>  <br/> |<span data-ttu-id="f534f-139">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f534f-139">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f534f-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f534f-140">Validation File</span></span>  <br/> |<span data-ttu-id="f534f-141">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f534f-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f534f-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f534f-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="f534f-143">False</span><span class="sxs-lookup"><span data-stu-id="f534f-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f534f-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f534f-144">See also</span></span>



[<span data-ttu-id="f534f-145">SendItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f534f-145">SendItem operation</span></span>](senditem-operation.md)

