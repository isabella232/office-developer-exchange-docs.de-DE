---
title: DLExpansion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DLExpansion
api_type:
- schema
ms.assetid: 9e50278d-fe6a-45e2-a72b-0fb06809e128
description: Das DLExpansion-Element enthält ein Array von Postfächern, die in einer Verteilerliste enthalten sind.
ms.openlocfilehash: 079ad1c0f114d201f5d1b91c3fd9bb45b943cc1a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456997"
---
# <a name="dlexpansion"></a><span data-ttu-id="bb30b-103">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="bb30b-103">DLExpansion</span></span>

<span data-ttu-id="bb30b-104">Das **DLExpansion** -Element enthält ein Array von Postfächern, die in einer Verteilerliste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="bb30b-104">The **DLExpansion** element contains an array of mailboxes that are contained in a distribution list.</span></span> 
  
- [<span data-ttu-id="bb30b-105">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="bb30b-105">ExpandDLResponse</span></span>](expanddlresponse.md) 
- [<span data-ttu-id="bb30b-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="bb30b-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="bb30b-107">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bb30b-107">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
- [<span data-ttu-id="bb30b-108">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="bb30b-108">DLExpansion</span></span>](dlexpansion.md)
  
```xml
<DLExpansion AbsoluteDenominator"" IncludesLastItemInRange="" IndexedPagingOffset="" NumeratorOffset="" TotalItemsInView="">
   <Mailbox/>
</DLExpansion>
```

 <span data-ttu-id="bb30b-109">**ArrayOfDLExpansionType**</span><span class="sxs-lookup"><span data-stu-id="bb30b-109">**ArrayOfDLExpansionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bb30b-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bb30b-110">Attributes and elements</span></span>

<span data-ttu-id="bb30b-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bb30b-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb30b-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="bb30b-112">Attributes</span></span>

|<span data-ttu-id="bb30b-113">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="bb30b-113">**Attribute**</span></span>|<span data-ttu-id="bb30b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bb30b-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bb30b-115">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="bb30b-115">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="bb30b-116">Stellt den nächsten Index dar, der für die nächste Anforderung verwendet werden soll, wenn Sie eine indizierte Seitenansicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="bb30b-116">Represents the next index that should be used for the next request when you are using an indexed page view.</span></span>  <br/> |
|<span data-ttu-id="bb30b-117">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="bb30b-117">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="bb30b-118">Stellt den neuen Zählerwert dar, der für die nächste Anforderung verwendet werden soll, wenn Sie Ansichten mit Bruch Seiten verwenden.</span><span class="sxs-lookup"><span data-stu-id="bb30b-118">Represents the new numerator value to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="bb30b-119">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="bb30b-119">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="bb30b-120">Stellt den nächsten Nenner dar, der für die nächste Anforderung verwendet werden soll, wenn Sie Ansichten mit Bruch Seiten verwenden.</span><span class="sxs-lookup"><span data-stu-id="bb30b-120">Represents the next denominator to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="bb30b-121">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="bb30b-121">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="bb30b-122">Gibt an, ob die aktuellen Ergebnisse das letzte Element in der Abfrage enthalten, sodass kein zusätzliches Paging erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="bb30b-122">Indicates whether the current results contain the last item in the query so that additional paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="bb30b-123">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="bb30b-123">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="bb30b-124">Stellt die Gesamtzahl der Elemente in der Ansicht dar.</span><span class="sxs-lookup"><span data-stu-id="bb30b-124">Represents the total number of items in the view.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bb30b-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bb30b-125">Child elements</span></span>

|<span data-ttu-id="bb30b-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="bb30b-126">**Element**</span></span>|<span data-ttu-id="bb30b-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bb30b-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb30b-128">Postfach</span><span class="sxs-lookup"><span data-stu-id="bb30b-128">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="bb30b-129">Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bb30b-129">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bb30b-130">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bb30b-130">Parent elements</span></span>

|<span data-ttu-id="bb30b-131">**Element**</span><span class="sxs-lookup"><span data-stu-id="bb30b-131">**Element**</span></span>|<span data-ttu-id="bb30b-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bb30b-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb30b-133">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bb30b-133">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md) <br/> |<span data-ttu-id="bb30b-134">Enthält den Status und das Ergebnis einer einzelnen ExpandDL-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="bb30b-134">Contains the status and result of a single ExpandDL request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb30b-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb30b-135">Remarks</span></span>

<span data-ttu-id="bb30b-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="bb30b-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bb30b-137">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="bb30b-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb30b-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="bb30b-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bb30b-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bb30b-139">Schema Name</span></span>  <br/> |<span data-ttu-id="bb30b-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="bb30b-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="bb30b-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bb30b-141">Validation File</span></span>  <br/> |<span data-ttu-id="bb30b-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bb30b-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bb30b-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="bb30b-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="bb30b-144">False</span><span class="sxs-lookup"><span data-stu-id="bb30b-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb30b-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb30b-145">See also</span></span>

- [<span data-ttu-id="bb30b-146">ExpandDL-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bb30b-146">ExpandDL operation</span></span>](expanddl-operation.md)
- [<span data-ttu-id="bb30b-147">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bb30b-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md) 
- [<span data-ttu-id="bb30b-148">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="bb30b-148">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

