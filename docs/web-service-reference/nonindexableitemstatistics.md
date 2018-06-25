---
title: NonIndexableItemStatistics
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 12f2934a-008c-4236-b8b3-7c7b6b5707e2
description: Das NonIndexableItemStatistics-Element enthält ein Array von Statistiken für Elemente, die nicht indiziert werden konnten.
ms.openlocfilehash: 1414053b6d39f4cd08ccfd1a11faaf1b13c2052b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830544"
---
# <a name="nonindexableitemstatistics"></a><span data-ttu-id="804b3-103">NonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="804b3-103">NonIndexableItemStatistics</span></span>

<span data-ttu-id="804b3-104">Das **NonIndexableItemStatistics** -Element enthält ein Array von Statistiken für Elemente, die nicht indiziert werden konnten.</span><span class="sxs-lookup"><span data-stu-id="804b3-104">The **NonIndexableItemStatistics** element contains an array of statistics for items that could not be indexed.</span></span> 
  
```XML
<NonIndexableItemStatistics>
   <NonIndexableItemStatistic/>
</NonIndexableItemStatistics>
```

 <span data-ttu-id="804b3-105">**ArrayOfNonIndexableItemStatisticsType**</span><span class="sxs-lookup"><span data-stu-id="804b3-105">**ArrayOfNonIndexableItemStatisticsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="804b3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="804b3-106">Attributes and elements</span></span>

<span data-ttu-id="804b3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="804b3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="804b3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="804b3-108">Attributes</span></span>

<span data-ttu-id="804b3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="804b3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="804b3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="804b3-110">Child elements</span></span>

[<span data-ttu-id="804b3-111">NonIndexableItemStatistic</span><span class="sxs-lookup"><span data-stu-id="804b3-111">NonIndexableItemStatistic</span></span>](nonindexableitemstatistic.md)
  
### <a name="parent-elements"></a><span data-ttu-id="804b3-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="804b3-112">Parent elements</span></span>

<span data-ttu-id="804b3-113">[GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md) , [GetNonIndexableItemStatisticsResponseMessage](getnonindexableitemstatisticsresponsemessage.md)</span><span class="sxs-lookup"><span data-stu-id="804b3-113">[GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md) , [GetNonIndexableItemStatisticsResponseMessage](getnonindexableitemstatisticsresponsemessage.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="804b3-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="804b3-114">Remarks</span></span>

<span data-ttu-id="804b3-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="804b3-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="804b3-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="804b3-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="804b3-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="804b3-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="804b3-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="804b3-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="804b3-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="804b3-119">Schema name</span></span>  <br/> |<span data-ttu-id="804b3-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="804b3-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="804b3-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="804b3-121">Validation file</span></span>  <br/> |<span data-ttu-id="804b3-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="804b3-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="804b3-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="804b3-123">Can be empty</span></span>  <br/> |<span data-ttu-id="804b3-124">False</span><span class="sxs-lookup"><span data-stu-id="804b3-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="804b3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="804b3-125">See also</span></span>



[<span data-ttu-id="804b3-126">GetNonIndexableItemStatistics-Vorgang</span><span class="sxs-lookup"><span data-stu-id="804b3-126">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)


- [<span data-ttu-id="804b3-127">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="804b3-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

