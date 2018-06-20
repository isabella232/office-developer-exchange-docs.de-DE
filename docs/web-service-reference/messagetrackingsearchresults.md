---
title: MessageTrackingSearchResults
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageTrackingSearchResults
api_type:
- schema
ms.assetid: 6bf36f37-c2b3-40c1-a4df-31573ed8642a
description: Das MessageTrackingSearchResults-Element enthält eine Liste von Datensätzen, die den Suchkriterien entsprechen.
ms.openlocfilehash: 866cc8d4e9afa8347eb7bd0d9e9acaddc616c396
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830454"
---
# <a name="messagetrackingsearchresults"></a><span data-ttu-id="bddba-103">MessageTrackingSearchResults</span><span class="sxs-lookup"><span data-stu-id="bddba-103">MessageTrackingSearchResults</span></span>

<span data-ttu-id="bddba-104">Das **MessageTrackingSearchResults** -Element enthält eine Liste von Datensätzen, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bddba-104">The **MessageTrackingSearchResults** element contains a list of records that match the search criteria.</span></span> 
  
```XML
<MessageTrackingSearchResults>
   <MessageTrackingSearchResult/>
</MessageTrackingSearchResults>
```

 <span data-ttu-id="bddba-105">**ArrayOfFindMessageTrackingSearchResultType**</span><span class="sxs-lookup"><span data-stu-id="bddba-105">**ArrayOfFindMessageTrackingSearchResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bddba-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bddba-106">Attributes and elements</span></span>

<span data-ttu-id="bddba-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bddba-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bddba-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="bddba-108">Attributes</span></span>

<span data-ttu-id="bddba-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="bddba-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bddba-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bddba-110">Child elements</span></span>

|<span data-ttu-id="bddba-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="bddba-111">**Element**</span></span>|<span data-ttu-id="bddba-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bddba-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bddba-113">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="bddba-113">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="bddba-114">Ein einzelnes Nachricht Ergebnis für ein [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) -Element enthält.</span><span class="sxs-lookup"><span data-stu-id="bddba-114">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bddba-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bddba-115">Parent elements</span></span>

|<span data-ttu-id="bddba-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="bddba-116">**Element**</span></span>|<span data-ttu-id="bddba-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bddba-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bddba-118">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="bddba-118">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="bddba-119">Enthält den Status und das Ergebnis einer einzelnen Anforderung [FindMessageTrackingReport Vorgang](findmessagetrackingreport-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="bddba-119">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bddba-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="bddba-120">Text value</span></span>

<span data-ttu-id="bddba-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="bddba-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bddba-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bddba-122">Remarks</span></span>

<span data-ttu-id="bddba-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="bddba-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bddba-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bddba-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bddba-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="bddba-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bddba-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bddba-126">Schema Name</span></span>  <br/> |<span data-ttu-id="bddba-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="bddba-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bddba-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bddba-128">Validation File</span></span>  <br/> |<span data-ttu-id="bddba-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bddba-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bddba-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="bddba-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="bddba-131">False</span><span class="sxs-lookup"><span data-stu-id="bddba-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bddba-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bddba-132">See also</span></span>



- [<span data-ttu-id="bddba-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bddba-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

