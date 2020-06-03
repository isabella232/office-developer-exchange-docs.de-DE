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
description: Das AcceptSharingInvitation-Element wird verwendet, um eine Einladung zu akzeptieren, die den Zugriff auf die Kalender-oder Kontaktdaten eines anderen Benutzers zulässt.
ms.openlocfilehash: c8cdae707bd122e74fa0e284163d1540d857c3de
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461709"
---
# <a name="acceptsharinginvitation"></a><span data-ttu-id="ebd96-103">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="ebd96-103">AcceptSharingInvitation</span></span>

<span data-ttu-id="ebd96-104">Das **AcceptSharingInvitation** -Element wird verwendet, um eine Einladung zu akzeptieren, die den Zugriff auf die Kalender-oder Kontaktdaten eines anderen Benutzers zulässt.</span><span class="sxs-lookup"><span data-stu-id="ebd96-104">The **AcceptSharingInvitation** element is used to accept an invitation that allows access to another user's calendar or contacts data.</span></span> 
  
```xml
<AcceptSharingInvitation>
   <ReferenceItemId/>
</AcceptSharingInvitation>
```

 <span data-ttu-id="ebd96-105">**AcceptSharingInvitationType**</span><span class="sxs-lookup"><span data-stu-id="ebd96-105">**AcceptSharingInvitationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ebd96-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ebd96-106">Attributes and elements</span></span>

<span data-ttu-id="ebd96-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ebd96-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ebd96-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ebd96-108">Attributes</span></span>

<span data-ttu-id="ebd96-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ebd96-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ebd96-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ebd96-110">Child elements</span></span>

|<span data-ttu-id="ebd96-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ebd96-111">**Element**</span></span>|<span data-ttu-id="ebd96-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ebd96-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ebd96-113">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="ebd96-113">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="ebd96-114">Gibt das Element an, auf das das Response-Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="ebd96-114">Identifies the item to which the response object refers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ebd96-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ebd96-115">Parent elements</span></span>

|<span data-ttu-id="ebd96-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="ebd96-116">**Element**</span></span>|<span data-ttu-id="ebd96-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ebd96-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ebd96-118">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="ebd96-118">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="ebd96-119">Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ebd96-119">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ebd96-120">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="ebd96-120">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="ebd96-121">Enthält ein Array von Elementen, die in dem Ordner erstellt werden sollen, der durch das [parentfolderid (TargetFolderIdType)-](parentfolderid-targetfolderidtype.md) Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="ebd96-121">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ebd96-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebd96-122">Remarks</span></span>

<span data-ttu-id="ebd96-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ebd96-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ebd96-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ebd96-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ebd96-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="ebd96-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ebd96-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ebd96-126">Schema Name</span></span>  <br/> |<span data-ttu-id="ebd96-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ebd96-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="ebd96-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ebd96-128">Validation File</span></span>  <br/> |<span data-ttu-id="ebd96-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ebd96-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ebd96-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ebd96-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="ebd96-131">False</span><span class="sxs-lookup"><span data-stu-id="ebd96-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ebd96-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebd96-132">See also</span></span>

- [<span data-ttu-id="ebd96-133">CreateItem (AcceptSharingInvitation)</span><span class="sxs-lookup"><span data-stu-id="ebd96-133">CreateItem (AcceptSharingInvitation)</span></span>](createitem-acceptsharinginvitation.md)
- [<span data-ttu-id="ebd96-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ebd96-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

