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
ms.openlocfilehash: 1e03cb135b7b2a125da1e29f7293d233f4e20ddb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468677"
---
# <a name="messagetrackingsearchresults"></a><span data-ttu-id="dde39-103">MessageTrackingSearchResults</span><span class="sxs-lookup"><span data-stu-id="dde39-103">MessageTrackingSearchResults</span></span>

<span data-ttu-id="dde39-104">Das **MessageTrackingSearchResults** -Element enthält eine Liste von Datensätzen, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="dde39-104">The **MessageTrackingSearchResults** element contains a list of records that match the search criteria.</span></span> 
  
```XML
<MessageTrackingSearchResults>
   <MessageTrackingSearchResult/>
</MessageTrackingSearchResults>
```

 <span data-ttu-id="dde39-105">**ArrayOfFindMessageTrackingSearchResultType**</span><span class="sxs-lookup"><span data-stu-id="dde39-105">**ArrayOfFindMessageTrackingSearchResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dde39-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dde39-106">Attributes and elements</span></span>

<span data-ttu-id="dde39-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dde39-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dde39-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dde39-108">Attributes</span></span>

<span data-ttu-id="dde39-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="dde39-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dde39-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dde39-110">Child elements</span></span>

|<span data-ttu-id="dde39-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="dde39-111">**Element**</span></span>|<span data-ttu-id="dde39-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dde39-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dde39-113">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="dde39-113">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="dde39-114">Enthält ein einzelnes Nachrichten Ergebnis für ein [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="dde39-114">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dde39-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dde39-115">Parent elements</span></span>

|<span data-ttu-id="dde39-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="dde39-116">**Element**</span></span>|<span data-ttu-id="dde39-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dde39-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dde39-118">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="dde39-118">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="dde39-119">Enthält den Status und das Ergebnis einer einzelnen [FindMessageTrackingReport-Vorgangs](findmessagetrackingreport-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="dde39-119">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dde39-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="dde39-120">Text value</span></span>

<span data-ttu-id="dde39-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="dde39-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dde39-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dde39-122">Remarks</span></span>

<span data-ttu-id="dde39-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="dde39-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dde39-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="dde39-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dde39-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="dde39-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dde39-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dde39-126">Schema Name</span></span>  <br/> |<span data-ttu-id="dde39-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="dde39-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dde39-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dde39-128">Validation File</span></span>  <br/> |<span data-ttu-id="dde39-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="dde39-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dde39-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="dde39-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="dde39-131">False</span><span class="sxs-lookup"><span data-stu-id="dde39-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dde39-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dde39-132">See also</span></span>



- [<span data-ttu-id="dde39-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="dde39-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

