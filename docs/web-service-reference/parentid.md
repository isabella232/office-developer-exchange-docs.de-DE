---
title: ParentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bb7aaa46-3a04-4197-aebb-8881ff10603f
description: Das ParentId-Element gibt den Bezeichner des übergeordneten Elements in einer Vorschau für die Suche.
ms.openlocfilehash: ddc76320b1c482e3518a98fb63fc2296143d163c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830698"
---
# <a name="parentid"></a><span data-ttu-id="630ed-103">ParentId</span><span class="sxs-lookup"><span data-stu-id="630ed-103">ParentId</span></span>

<span data-ttu-id="630ed-104">Das **ParentId** -Element gibt den Bezeichner des übergeordneten Elements in einer Vorschau für die Suche.</span><span class="sxs-lookup"><span data-stu-id="630ed-104">The **ParentId** element specifies the identifier of the parent item in a search preview.</span></span> 
  
```XML
<ParentId Id="" ChangeKey=""/>
```

<span data-ttu-id="630ed-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="630ed-105">**ItemIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="630ed-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="630ed-106">Attributes and elements</span></span>

<span data-ttu-id="630ed-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="630ed-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="630ed-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="630ed-108">Attributes</span></span>

|<span data-ttu-id="630ed-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="630ed-109">**Attribute**</span></span>|<span data-ttu-id="630ed-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="630ed-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="630ed-111">Id</span><span class="sxs-lookup"><span data-stu-id="630ed-111">Id</span></span>  <br/> |<span data-ttu-id="630ed-112">Der Textwert des **Id** -Attributs ist der Bezeichner des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="630ed-112">The text value of the **Id** attribute is the identifier of the parent item.</span></span>  <br/> |
|<span data-ttu-id="630ed-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="630ed-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="630ed-114">Der Textwert des **ChangeKey** -Attributs ist der Key ändern des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="630ed-114">The text value of the **ChangeKey** attribute is the change key of the parent item.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="630ed-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="630ed-115">Child elements</span></span>

<span data-ttu-id="630ed-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="630ed-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="630ed-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="630ed-117">Parent elements</span></span>

[<span data-ttu-id="630ed-118">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="630ed-118">SearchPreviewItem</span></span>](searchpreviewitem.md)
  
## <a name="remarks"></a><span data-ttu-id="630ed-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="630ed-119">Remarks</span></span>

<span data-ttu-id="630ed-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="630ed-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="630ed-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="630ed-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="630ed-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="630ed-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="630ed-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="630ed-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="630ed-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="630ed-124">Schema name</span></span>  <br/> |<span data-ttu-id="630ed-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="630ed-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="630ed-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="630ed-126">Validation file</span></span>  <br/> |<span data-ttu-id="630ed-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="630ed-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="630ed-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="630ed-128">Can be empty</span></span>  <br/> |<span data-ttu-id="630ed-129">true</span><span class="sxs-lookup"><span data-stu-id="630ed-129">true</span></span>  <br/> |
   

