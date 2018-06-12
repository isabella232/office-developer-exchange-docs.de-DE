---
title: ExportItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExportItems
api_type:
- schema
ms.assetid: bbbc56e4-8cc1-43ae-b70a-9a8d6bb0f399
description: Das Element ExportItems stellt eine Anforderung zum Exportieren von Elementen aus einem Postfach.
ms.openlocfilehash: 055012166bb125dfcf86070f2e23496bf0209b51
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758319"
---
# <a name="exportitems"></a><span data-ttu-id="2e90c-103">ExportItems</span><span class="sxs-lookup"><span data-stu-id="2e90c-103">ExportItems</span></span>

<span data-ttu-id="2e90c-104">Das Element **ExportItems** stellt eine Anforderung zum Exportieren von Elementen aus einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="2e90c-104">The **ExportItems** element represents a request to export items from a mailbox.</span></span> 
  
[<span data-ttu-id="2e90c-105">ExportItems</span><span class="sxs-lookup"><span data-stu-id="2e90c-105">ExportItems</span></span>](exportitems.md)
  
```XML
<ExportItems>
   <ItemIds/>
</ExportItems>
```

 <span data-ttu-id="2e90c-106">**ExportItemsType**</span><span class="sxs-lookup"><span data-stu-id="2e90c-106">**ExportItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2e90c-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2e90c-107">Attributes and elements</span></span>

<span data-ttu-id="2e90c-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2e90c-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e90c-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="2e90c-109">Attributes</span></span>

<span data-ttu-id="2e90c-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="2e90c-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2e90c-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2e90c-111">Child elements</span></span>

|<span data-ttu-id="2e90c-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="2e90c-112">**Element**</span></span>|<span data-ttu-id="2e90c-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2e90c-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e90c-114">Artikelnummern ein (NonEmptyArrayOfItemIdsType).</span><span class="sxs-lookup"><span data-stu-id="2e90c-114">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md) <br/> |<span data-ttu-id="2e90c-115">Enthält ein Array der Element-IDs, die die Elemente aus einem Postfach exportieren zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2e90c-115">Contains an array of item identifiers that identify the items to export from a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2e90c-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2e90c-116">Parent elements</span></span>

<span data-ttu-id="2e90c-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="2e90c-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="2e90c-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="2e90c-118">Text value</span></span>

<span data-ttu-id="2e90c-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="2e90c-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e90c-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2e90c-120">Remarks</span></span>

<span data-ttu-id="2e90c-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2e90c-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2e90c-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2e90c-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e90c-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e90c-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2e90c-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2e90c-124">Schema Name</span></span>  <br/> |<span data-ttu-id="2e90c-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2e90c-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="2e90c-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2e90c-126">Validation File</span></span>  <br/> |<span data-ttu-id="2e90c-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2e90c-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2e90c-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2e90c-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="2e90c-129">False</span><span class="sxs-lookup"><span data-stu-id="2e90c-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e90c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e90c-130">See also</span></span>



[<span data-ttu-id="2e90c-131">ExportItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2e90c-131">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="2e90c-132">UploadItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2e90c-132">UploadItems operation</span></span>](uploaditems-operation.md)

