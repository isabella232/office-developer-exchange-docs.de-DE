---
title: ConflictResults
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConflictResults
api_type:
- schema
ms.assetid: 08cdd547-4de7-4c7a-b60f-e618dc217d20
description: Das ConflictResults-Element enthält die Anzahl der Konflikte in einer Antwort ein UpdateItem Vorgang.
ms.openlocfilehash: faa6dc6c5fbbe874438a89c810a12fa675e8a1c9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757599"
---
# <a name="conflictresults"></a><span data-ttu-id="55861-103">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="55861-103">ConflictResults</span></span>

<span data-ttu-id="55861-104">Das [ConflictResults](conflictresults.md) -Element enthält die Anzahl der Konflikte in einer Antwort [UpdateItem Vorgang](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="55861-104">The [ConflictResults](conflictresults.md) element contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span> 
  
[<span data-ttu-id="55861-105">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="55861-105">UpdateItemResponse</span></span>](updateitemresponse.md)
  
[<span data-ttu-id="55861-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="55861-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="55861-107">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="55861-107">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
  
[<span data-ttu-id="55861-108">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="55861-108">ConflictResults</span></span>](conflictresults.md)
  
```xml
<ConflictResults>
   <Count/>
</ConflictResults>
```

 <span data-ttu-id="55861-109">**ConflictResultsType**</span><span class="sxs-lookup"><span data-stu-id="55861-109">**ConflictResultsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="55861-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="55861-110">Attributes and elements</span></span>

<span data-ttu-id="55861-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="55861-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="55861-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="55861-112">Attributes</span></span>

<span data-ttu-id="55861-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="55861-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="55861-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55861-114">Child elements</span></span>

|<span data-ttu-id="55861-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="55861-115">**Element**</span></span>|<span data-ttu-id="55861-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55861-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55861-117">Count</span><span class="sxs-lookup"><span data-stu-id="55861-117">Count</span></span>](count.md) <br/> |<span data-ttu-id="55861-118">Enthält die Anzahl der Konflikte in einer Antwort [UpdateItem Vorgang](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="55861-118">Contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="55861-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55861-119">Parent elements</span></span>

|<span data-ttu-id="55861-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="55861-120">**Element**</span></span>|<span data-ttu-id="55861-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55861-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55861-122">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="55861-122">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md) <br/> |<span data-ttu-id="55861-123">Enthält den Status und das Ergebnis einer einzelnen Anforderung [UpdateItem Vorgang](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="55861-123">Contains the status and result of a single [UpdateItem operation](updateitem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55861-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="55861-124">Remarks</span></span>

<span data-ttu-id="55861-125">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, der Exchange-Server, mit die Clientzugriffs-Serverrolle installiert ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55861-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="55861-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="55861-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55861-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="55861-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="55861-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="55861-128">Schema Name</span></span>  <br/> |<span data-ttu-id="55861-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="55861-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="55861-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="55861-130">Validation File</span></span>  <br/> |<span data-ttu-id="55861-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="55861-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="55861-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="55861-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="55861-133">False</span><span class="sxs-lookup"><span data-stu-id="55861-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55861-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55861-134">See also</span></span>



[<span data-ttu-id="55861-135">UpdateItem Operation</span><span class="sxs-lookup"><span data-stu-id="55861-135">UpdateItem operation</span></span>](updateitem-operation.md)
  
 <span data-ttu-id="55861-136">**ConflictResultsType**</span><span class="sxs-lookup"><span data-stu-id="55861-136">**ConflictResultsType**</span></span>

