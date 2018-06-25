---
title: AcceptSharingInvitation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AcceptSharingInvitation
api_type:
- schema
ms.assetid: 3c2a47d6-490d-425b-8893-089a4f8882cd
description: Das Element AcceptSharingInvitation wird verwendet, um eine Einladung annehmen, die Zugriff auf einen anderen Benutzer Kalender oder Kontaktdaten ermöglicht.
ms.openlocfilehash: 06439739e6cc544d5039ac9d18e0452b1d42a0ed
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758365"
---
# <a name="acceptsharinginvitation"></a><span data-ttu-id="db3b0-103">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="db3b0-103">AcceptSharingInvitation</span></span>

<span data-ttu-id="db3b0-104">Das Element **AcceptSharingInvitation** wird verwendet, um eine Einladung annehmen, die Zugriff auf einen anderen Benutzer Kalender oder Kontaktdaten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="db3b0-104">The **AcceptSharingInvitation** element is used to accept an invitation that allows access to another user's calendar or contacts data.</span></span> 
  
```xml
<AcceptSharingInvitation>
   <ReferenceItemId/>
</AcceptSharingInvitation>
```

 <span data-ttu-id="db3b0-105">**AcceptSharingInvitationType**</span><span class="sxs-lookup"><span data-stu-id="db3b0-105">**AcceptSharingInvitationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="db3b0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="db3b0-106">Attributes and elements</span></span>

<span data-ttu-id="db3b0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="db3b0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="db3b0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="db3b0-108">Attributes</span></span>

<span data-ttu-id="db3b0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="db3b0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="db3b0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="db3b0-110">Child elements</span></span>

|<span data-ttu-id="db3b0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="db3b0-111">**Element**</span></span>|<span data-ttu-id="db3b0-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="db3b0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="db3b0-113">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="db3b0-113">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="db3b0-114">Identifiziert das Element auf dem im Response-Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="db3b0-114">Identifies the item to which the response object refers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="db3b0-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="db3b0-115">Parent elements</span></span>

|<span data-ttu-id="db3b0-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="db3b0-116">**Element**</span></span>|<span data-ttu-id="db3b0-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="db3b0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="db3b0-118">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="db3b0-118">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="db3b0-119">Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="db3b0-119">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="db3b0-120">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="db3b0-120">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="db3b0-121">Enthält ein Array von Elementen im Ordner zu erstellen, die durch das Element [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="db3b0-121">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db3b0-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="db3b0-122">Remarks</span></span>

<span data-ttu-id="db3b0-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="db3b0-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="db3b0-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="db3b0-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db3b0-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="db3b0-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="db3b0-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="db3b0-126">Schema Name</span></span>  <br/> |<span data-ttu-id="db3b0-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="db3b0-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="db3b0-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="db3b0-128">Validation File</span></span>  <br/> |<span data-ttu-id="db3b0-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="db3b0-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="db3b0-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="db3b0-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="db3b0-131">False</span><span class="sxs-lookup"><span data-stu-id="db3b0-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="db3b0-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db3b0-132">See also</span></span>

- [<span data-ttu-id="db3b0-133">CreateItem (AcceptSharingInvitation)</span><span class="sxs-lookup"><span data-stu-id="db3b0-133">CreateItem (AcceptSharingInvitation)</span></span>](createitem-acceptsharinginvitation.md)
- [<span data-ttu-id="db3b0-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="db3b0-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

