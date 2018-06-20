---
title: Löschen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Delete
api_type:
- schema
ms.assetid: aa45f0c1-a80d-4b6c-8a85-375b6de515f4
description: Das Delete-Element gibt an, ob ein Client eines Ordners oder Elements löschen kann.
ms.openlocfilehash: 8a00a24ea63fa564ecefb96a5caed3a9199690eb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757901"
---
# <a name="delete"></a><span data-ttu-id="f9437-103">Löschen</span><span class="sxs-lookup"><span data-stu-id="f9437-103">Delete</span></span>

<span data-ttu-id="f9437-104">Das Element **Löschen** gibt an, ob ein Client eines Ordners oder Elements löschen kann.</span><span class="sxs-lookup"><span data-stu-id="f9437-104">The **Delete** element indicates whether a client can delete a folder or item.</span></span> 
  
```XML
<Delete>true or false</Delete>
```

<span data-ttu-id="f9437-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="f9437-105">**boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f9437-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f9437-106">Attributes and elements</span></span>

<span data-ttu-id="f9437-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f9437-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f9437-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f9437-108">Attributes</span></span>

<span data-ttu-id="f9437-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f9437-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f9437-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9437-110">Child elements</span></span>

<span data-ttu-id="f9437-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f9437-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f9437-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9437-112">Parent elements</span></span>

|<span data-ttu-id="f9437-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f9437-113">**Element**</span></span>|<span data-ttu-id="f9437-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f9437-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9437-115">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="f9437-115">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="f9437-116">Die Rechte des Clients basierend auf die berechtigungseinstellungen für das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="f9437-116">Contains the rights of the client based on the permission settings for the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="f9437-117">Aktionen</span><span class="sxs-lookup"><span data-stu-id="f9437-117">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="f9437-118">Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="f9437-118">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f9437-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="f9437-119">Text value</span></span>

<span data-ttu-id="f9437-120">Der Textwert **true** gibt an, dass ein Client eines Elements oder Ordners löschen kann.</span><span class="sxs-lookup"><span data-stu-id="f9437-120">A text value of **true** indicates that a client can delete an item or folder.</span></span> <span data-ttu-id="f9437-121">Der Wert **false** gibt an, dass ein Client eines Elements oder Ordners gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="f9437-121">A value of **false** indicates that a client cannot delete an item or folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f9437-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f9437-122">Remarks</span></span>

<span data-ttu-id="f9437-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f9437-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f9437-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f9437-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9437-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="f9437-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f9437-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f9437-126">Schema Name</span></span>  <br/> |<span data-ttu-id="f9437-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f9437-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="f9437-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f9437-128">Validation File</span></span>  <br/> |<span data-ttu-id="f9437-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f9437-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f9437-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f9437-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="f9437-131">False</span><span class="sxs-lookup"><span data-stu-id="f9437-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f9437-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9437-132">See also</span></span>

- [<span data-ttu-id="f9437-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f9437-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="f9437-134">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="f9437-134">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

