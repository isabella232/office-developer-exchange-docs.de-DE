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
description: Das ConflictResults-Element enthält die Anzahl von Konflikten in einer UpdateItem-Vorgangs Antwort.
ms.openlocfilehash: 923c7950e21039adf28e232486f4df5fc04889d1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460169"
---
# <a name="conflictresults"></a><span data-ttu-id="66729-103">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="66729-103">ConflictResults</span></span>

<span data-ttu-id="66729-104">Das [ConflictResults](conflictresults.md) -Element enthält die Anzahl von Konflikten in einer [UpdateItem-Vorgangs](updateitem-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="66729-104">The [ConflictResults](conflictresults.md) element contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span> 
  
[<span data-ttu-id="66729-105">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="66729-105">UpdateItemResponse</span></span>](updateitemresponse.md)
  
[<span data-ttu-id="66729-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="66729-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="66729-107">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="66729-107">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
  
[<span data-ttu-id="66729-108">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="66729-108">ConflictResults</span></span>](conflictresults.md)
  
```xml
<ConflictResults>
   <Count/>
</ConflictResults>
```

 <span data-ttu-id="66729-109">**ConflictResultsType**</span><span class="sxs-lookup"><span data-stu-id="66729-109">**ConflictResultsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="66729-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="66729-110">Attributes and elements</span></span>

<span data-ttu-id="66729-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="66729-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66729-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="66729-112">Attributes</span></span>

<span data-ttu-id="66729-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="66729-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="66729-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66729-114">Child elements</span></span>

|<span data-ttu-id="66729-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="66729-115">**Element**</span></span>|<span data-ttu-id="66729-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66729-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66729-117">Count</span><span class="sxs-lookup"><span data-stu-id="66729-117">Count</span></span>](count.md) <br/> |<span data-ttu-id="66729-118">Enthält die Anzahl von Konflikten in einer [UpdateItem-Vorgangs](updateitem-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="66729-118">Contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="66729-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66729-119">Parent elements</span></span>

|<span data-ttu-id="66729-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="66729-120">**Element**</span></span>|<span data-ttu-id="66729-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66729-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66729-122">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="66729-122">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md) <br/> |<span data-ttu-id="66729-123">Enthält den Status und das Ergebnis einer einzelnen [UpdateItem-Vorgangs](updateitem-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="66729-123">Contains the status and result of a single [UpdateItem operation](updateitem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66729-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66729-124">Remarks</span></span>

<span data-ttu-id="66729-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server mit installierter Client Zugriffs-Server Rolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="66729-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66729-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="66729-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66729-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="66729-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="66729-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="66729-128">Schema Name</span></span>  <br/> |<span data-ttu-id="66729-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="66729-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="66729-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="66729-130">Validation File</span></span>  <br/> |<span data-ttu-id="66729-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="66729-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="66729-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="66729-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="66729-133">False</span><span class="sxs-lookup"><span data-stu-id="66729-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="66729-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66729-134">See also</span></span>



[<span data-ttu-id="66729-135">UpdateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="66729-135">UpdateItem operation</span></span>](updateitem-operation.md)
  
 <span data-ttu-id="66729-136">**ConflictResultsType**</span><span class="sxs-lookup"><span data-stu-id="66729-136">**ConflictResultsType**</span></span>

