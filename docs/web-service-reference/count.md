---
title: Anzahl
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Count
api_type:
- schema
ms.assetid: 68314b4a-1e17-4e21-9c2e-224d70ef7a32
description: Das count-Element enthält die Anzahl von Konflikten in einer UpdateItem-Vorgangs Antwort.
ms.openlocfilehash: a43896a1b8b6a9d96ab02afe64f9e553639e478e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466759"
---
# <a name="count"></a><span data-ttu-id="f1f4f-103">Anzahl</span><span class="sxs-lookup"><span data-stu-id="f1f4f-103">Count</span></span>

<span data-ttu-id="f1f4f-104">Das [count](count.md) -Element enthält die Anzahl von Konflikten in einer [UpdateItem-Vorgangs](updateitem-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="f1f4f-104">The [Count](count.md) element contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span> 
  
[<span data-ttu-id="f1f4f-105">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="f1f4f-105">UpdateItemResponse</span></span>](updateitemresponse.md)
  
[<span data-ttu-id="f1f4f-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f1f4f-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="f1f4f-107">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f1f4f-107">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
  
[<span data-ttu-id="f1f4f-108">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="f1f4f-108">ConflictResults</span></span>](conflictresults.md)
  
[<span data-ttu-id="f1f4f-109">Count</span><span class="sxs-lookup"><span data-stu-id="f1f4f-109">Count</span></span>](count.md)
  
```xml
<Count/>
```

 <span data-ttu-id="f1f4f-110">**int**</span><span class="sxs-lookup"><span data-stu-id="f1f4f-110">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f1f4f-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f1f4f-111">Attributes and elements</span></span>

<span data-ttu-id="f1f4f-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f1f4f-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1f4f-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="f1f4f-113">Attributes</span></span>

<span data-ttu-id="f1f4f-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="f1f4f-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f1f4f-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f1f4f-115">Child elements</span></span>

<span data-ttu-id="f1f4f-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="f1f4f-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f1f4f-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f1f4f-117">Parent elements</span></span>

|<span data-ttu-id="f1f4f-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="f1f4f-118">**Element**</span></span>|<span data-ttu-id="f1f4f-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f1f4f-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f1f4f-120">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="f1f4f-120">ConflictResults</span></span>](conflictresults.md) <br/> |<span data-ttu-id="f1f4f-121">Enthält die Anzahl von Konflikten in einer [UpdateItem-Vorgangs](updateitem-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="f1f4f-121">Contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f1f4f-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="f1f4f-122">Text value</span></span>

<span data-ttu-id="f1f4f-123">Der Textwert ist eine ganze Zahl, die die Anzahl der Konflikte in einer [UpdateItem-Vorgangs](updateitem-operation.md) Antwort darstellt.</span><span class="sxs-lookup"><span data-stu-id="f1f4f-123">The text value is an integer that represents the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f1f4f-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1f4f-124">Remarks</span></span>

<span data-ttu-id="f1f4f-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f1f4f-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f1f4f-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f1f4f-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1f4f-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1f4f-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f1f4f-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f1f4f-128">Schema Name</span></span>  <br/> |<span data-ttu-id="f1f4f-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f1f4f-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="f1f4f-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f1f4f-130">Validation File</span></span>  <br/> |<span data-ttu-id="f1f4f-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f1f4f-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f1f4f-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f1f4f-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="f1f4f-133">False</span><span class="sxs-lookup"><span data-stu-id="f1f4f-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f1f4f-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1f4f-134">See also</span></span>



[<span data-ttu-id="f1f4f-135">UpdateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f1f4f-135">UpdateItem operation</span></span>](updateitem-operation.md)
  
 <span data-ttu-id="f1f4f-136">**ConflictResultsType**</span><span class="sxs-lookup"><span data-stu-id="f1f4f-136">**ConflictResultsType**</span></span>

