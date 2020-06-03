---
title: ParentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bb7aaa46-3a04-4197-aebb-8881ff10603f
description: Das Parent-ID-Element gibt den Bezeichner des übergeordneten Elements in einer Suchvorschau an.
ms.openlocfilehash: e09b5f9e463c7ecdfc595c87a84584f69cab3f2c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529021"
---
# <a name="parentid"></a><span data-ttu-id="38a36-103">ParentId</span><span class="sxs-lookup"><span data-stu-id="38a36-103">ParentId</span></span>

<span data-ttu-id="38a36-104">Das **Parent** -ID-Element gibt den Bezeichner des übergeordneten Elements in einer Suchvorschau an.</span><span class="sxs-lookup"><span data-stu-id="38a36-104">The **ParentId** element specifies the identifier of the parent item in a search preview.</span></span> 
  
```XML
<ParentId Id="" ChangeKey=""/>
```

<span data-ttu-id="38a36-105">**Itemidtype**</span><span class="sxs-lookup"><span data-stu-id="38a36-105">**ItemIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="38a36-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="38a36-106">Attributes and elements</span></span>

<span data-ttu-id="38a36-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="38a36-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38a36-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="38a36-108">Attributes</span></span>

|<span data-ttu-id="38a36-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="38a36-109">**Attribute**</span></span>|<span data-ttu-id="38a36-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="38a36-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="38a36-111">Id</span><span class="sxs-lookup"><span data-stu-id="38a36-111">Id</span></span>  <br/> |<span data-ttu-id="38a36-112">Der Textwert des **ID-** Attributs ist der Bezeichner des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="38a36-112">The text value of the **Id** attribute is the identifier of the parent item.</span></span>  <br/> |
|<span data-ttu-id="38a36-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="38a36-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="38a36-114">Der Textwert des **ChangeKey** -Attributs ist der Änderungsschlüssel des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="38a36-114">The text value of the **ChangeKey** attribute is the change key of the parent item.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="38a36-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="38a36-115">Child elements</span></span>

<span data-ttu-id="38a36-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="38a36-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="38a36-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="38a36-117">Parent elements</span></span>

[<span data-ttu-id="38a36-118">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="38a36-118">SearchPreviewItem</span></span>](searchpreviewitem.md)
  
## <a name="remarks"></a><span data-ttu-id="38a36-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38a36-119">Remarks</span></span>

<span data-ttu-id="38a36-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="38a36-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="38a36-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="38a36-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="38a36-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="38a36-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38a36-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="38a36-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="38a36-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="38a36-124">Schema name</span></span>  <br/> |<span data-ttu-id="38a36-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="38a36-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="38a36-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="38a36-126">Validation file</span></span>  <br/> |<span data-ttu-id="38a36-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="38a36-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="38a36-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="38a36-128">Can be empty</span></span>  <br/> |<span data-ttu-id="38a36-129">true</span><span class="sxs-lookup"><span data-stu-id="38a36-129">true</span></span>  <br/> |
   

