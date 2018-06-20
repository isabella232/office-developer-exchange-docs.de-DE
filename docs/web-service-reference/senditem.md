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
description: Das SendItem-Element ist das Stammelement im eine Anforderung zum Senden eines Elements im Exchange-Speicher.
ms.openlocfilehash: c5ce52ee4643219aa31ae59e8b7d40d7a904c8ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831340"
---
# <a name="senditem"></a><span data-ttu-id="98365-103">SendItem</span><span class="sxs-lookup"><span data-stu-id="98365-103">SendItem</span></span>

<span data-ttu-id="98365-104">Das **SendItem** -Element ist das Stammelement im eine Anforderung zum Senden eines Elements im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="98365-104">The **SendItem** element is the root element in a request to send an item in the Exchange store.</span></span> 
  
```xml
<SendItem SaveItemToFolder="">
   <ItemIds/>
   <SavedItemFolderId/>
</SendItem>
```

 <span data-ttu-id="98365-105">**SendItemType**</span><span class="sxs-lookup"><span data-stu-id="98365-105">**SendItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="98365-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="98365-106">Attributes and elements</span></span>

<span data-ttu-id="98365-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="98365-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="98365-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="98365-108">Attributes</span></span>

|<span data-ttu-id="98365-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="98365-109">**Attribute**</span></span>|<span data-ttu-id="98365-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="98365-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="98365-111">**SaveItemToFolder**</span><span class="sxs-lookup"><span data-stu-id="98365-111">**SaveItemToFolder**</span></span> <br/> |<span data-ttu-id="98365-112">Bestimmt, ob eine Kopie der das gesendete Element gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="98365-112">Identifies whether a copy of the sent item is saved.</span></span> <span data-ttu-id="98365-113">Speichern in Aktion hängt vom Wert der **SaveItemToFolder** und gibt an, ob ein Element [des SavedItemFolderId](saveditemfolderid.md) in der Anforderung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="98365-113">The save action depends on the value of **SaveItemToFolder** and whether a [SavedItemFolderId](saveditemfolderid.md) element is present in the request.</span></span> <span data-ttu-id="98365-114">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="98365-114">This element is required.</span></span>  <br/> |
   
#### <a name="saveitemtofolder-attribute"></a><span data-ttu-id="98365-115">SaveItemToFolder-Attributs</span><span class="sxs-lookup"><span data-stu-id="98365-115">SaveItemToFolder Attribute</span></span>

|<span data-ttu-id="98365-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="98365-116">**Value**</span></span>|<span data-ttu-id="98365-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="98365-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="98365-118">**"true"**</span><span class="sxs-lookup"><span data-stu-id="98365-118">**true**</span></span> <br/> |<span data-ttu-id="98365-119">Wenn das Element [des SavedItemFolderId](saveditemfolderid.md) nicht vorhanden ist, wird das Element im Ordner "Gesendete Elemente" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="98365-119">If the [SavedItemFolderId](saveditemfolderid.md) element is not present, the item is saved in the Sent Items folder.</span></span> <span data-ttu-id="98365-120">Wenn das Element [des SavedItemFolderId](saveditemfolderid.md) vorhanden ist, wird das Element im Ordner gespeichert, die durch das Element [des SavedItemFolderId](saveditemfolderid.md) angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="98365-120">If the [SavedItemFolderId](saveditemfolderid.md) element is present, the item is saved in the folder that is specified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
|<span data-ttu-id="98365-121">**false**</span><span class="sxs-lookup"><span data-stu-id="98365-121">**false**</span></span> <br/> |<span data-ttu-id="98365-122">Wenn das Element [des SavedItemFolderId](saveditemfolderid.md) nicht vorhanden ist, wird das Element nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="98365-122">If the [SavedItemFolderId](saveditemfolderid.md) element is not present, the item is not saved.</span></span> <span data-ttu-id="98365-123">Wenn das Element [des SavedItemFolderId](saveditemfolderid.md) vorhanden ist, wird eine Fehlerantwort mit einem [ResponseCode](responsecode.md) -Element zurückgegeben werden soll, die den **ErrorInvalidSendItemSaveSettings** -Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="98365-123">If the [SavedItemFolderId](saveditemfolderid.md) element is present, an error response will be returned with a [ResponseCode](responsecode.md) element that contains the **ErrorInvalidSendItemSaveSettings** value.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="98365-124">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="98365-124">Child elements</span></span>

|<span data-ttu-id="98365-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="98365-125">**Element**</span></span>|<span data-ttu-id="98365-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="98365-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98365-127">Artikelnummern ein.</span><span class="sxs-lookup"><span data-stu-id="98365-127">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="98365-128">Enthält die eindeutigen Identitäten der Elemente, Vorkommen Elemente und Terminserien der Master-Shape, mit denen löschen, senden, abrufen, verschieben oder Kopieren von Elementen in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="98365-128">Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="98365-129">Des SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="98365-129">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> |<span data-ttu-id="98365-130">Identifiziert den Zielordner für Vorgänge, die zu aktualisieren, senden und Elemente im Exchange-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="98365-130">Identifies the target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="98365-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="98365-131">Parent elements</span></span>

<span data-ttu-id="98365-132">Keine.</span><span class="sxs-lookup"><span data-stu-id="98365-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98365-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="98365-133">Remarks</span></span>

<span data-ttu-id="98365-134">Wenn ein Element im Ordner "Gesendete Elemente" gesendet wird, wird das gesendete Element gelöscht, und eine Kopie davon hört im Ordner "Gesendete Elemente".</span><span class="sxs-lookup"><span data-stu-id="98365-134">If an item in the Sent Items folder is sent, the sent item is deleted and a copy of it is put in the Sent Items folder.</span></span>
  
<span data-ttu-id="98365-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="98365-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="98365-136">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="98365-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98365-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="98365-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="98365-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="98365-138">Schema Name</span></span>  <br/> |<span data-ttu-id="98365-139">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="98365-139">Messages schema</span></span>  <br/> |
|<span data-ttu-id="98365-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="98365-140">Validation File</span></span>  <br/> |<span data-ttu-id="98365-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="98365-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="98365-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="98365-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="98365-143">False</span><span class="sxs-lookup"><span data-stu-id="98365-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="98365-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98365-144">See also</span></span>



[<span data-ttu-id="98365-145">SendItem Operation</span><span class="sxs-lookup"><span data-stu-id="98365-145">SendItem operation</span></span>](senditem-operation.md)

