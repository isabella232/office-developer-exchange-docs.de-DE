---
title: Flag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b47bc74-a60d-4308-8674-5d52444a1753
description: Das Flag-Element gibt ein Flag für ein Postfachelement an.
ms.openlocfilehash: 7229a26181ee9baf80be5c32c0ef99483310ccb3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466262"
---
# <a name="flag"></a><span data-ttu-id="5cb8a-103">Flag</span><span class="sxs-lookup"><span data-stu-id="5cb8a-103">Flag</span></span>

<span data-ttu-id="5cb8a-104">Das **Flag** -Element gibt ein Flag für ein Postfachelement an.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-104">The **Flag** element specifies a flag on a mailbox item.</span></span> 
  
```XML
<Flag>
    <FlagStatus/>
    <StartDate/>
    <DueDate/>
    <CompleteDate/>
</Flag>
```

 <span data-ttu-id="5cb8a-105">**FlagType**</span><span class="sxs-lookup"><span data-stu-id="5cb8a-105">**FlagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5cb8a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5cb8a-106">Attributes and elements</span></span>

<span data-ttu-id="5cb8a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5cb8a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5cb8a-108">Attributes</span></span>

<span data-ttu-id="5cb8a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5cb8a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5cb8a-110">Child elements</span></span>

|<span data-ttu-id="5cb8a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5cb8a-111">**Element**</span></span>|<span data-ttu-id="5cb8a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5cb8a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5cb8a-113">FlagStatus</span><span class="sxs-lookup"><span data-stu-id="5cb8a-113">FlagStatus</span></span>](flagstatus.md) <br/> |<span data-ttu-id="5cb8a-114">Enthält den Status aggregierter Kennzeichen für Elemente im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-114">Contains the aggregated flag status for items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="5cb8a-115">StartDate</span><span class="sxs-lookup"><span data-stu-id="5cb8a-115">StartDate</span></span>](startdate.md) <br/> |<span data-ttu-id="5cb8a-116">Stellt das Anfangsdatum eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-116">Represents the start date of an item.</span></span>  <br/> |
|[<span data-ttu-id="5cb8a-117">DueDate</span><span class="sxs-lookup"><span data-stu-id="5cb8a-117">DueDate</span></span>](duedate.md) <br/> |<span data-ttu-id="5cb8a-118">Stellt das Datum dar, an dem ein Element fällig ist.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-118">Represents the date when an item is due.</span></span>  <br/> |
|[<span data-ttu-id="5cb8a-119">CompleteDate</span><span class="sxs-lookup"><span data-stu-id="5cb8a-119">CompleteDate</span></span>](completedate.md) <br/> |<span data-ttu-id="5cb8a-120">Stellt das Datum dar, an dem ein Element abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-120">Represents the date on which an item was completed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5cb8a-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5cb8a-121">Parent elements</span></span>

|<span data-ttu-id="5cb8a-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="5cb8a-122">**Element**</span></span>|<span data-ttu-id="5cb8a-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5cb8a-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5cb8a-124">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="5cb8a-124">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="5cb8a-125">Enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-125">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="5cb8a-126">Element</span><span class="sxs-lookup"><span data-stu-id="5cb8a-126">Item</span></span>](item.md) <br/> |<span data-ttu-id="5cb8a-127">Stellt ein generisches Element in der Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-127">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5cb8a-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5cb8a-128">Remarks</span></span>

<span data-ttu-id="5cb8a-129">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-129">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5cb8a-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5cb8a-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5cb8a-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5cb8a-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="5cb8a-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5cb8a-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5cb8a-133">Schema Name</span></span>  <br/> |<span data-ttu-id="5cb8a-134">Typschema</span><span class="sxs-lookup"><span data-stu-id="5cb8a-134">Type schema</span></span>  <br/> |
|<span data-ttu-id="5cb8a-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5cb8a-135">Validation File</span></span>  <br/> |<span data-ttu-id="5cb8a-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5cb8a-136">types.xsd</span></span>  <br/> |
|<span data-ttu-id="5cb8a-137">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="5cb8a-137">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="5cb8a-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5cb8a-138">See also</span></span>



- [<span data-ttu-id="5cb8a-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5cb8a-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

