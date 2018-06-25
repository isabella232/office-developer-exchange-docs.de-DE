---
title: NonIndexableItemStatistic
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 593e0c79-9ec2-4040-a6a3-3c5c61cbdf7c
description: Das NonIndexableItemStatistic-Element enthält eine einzelne Statistik für ein Element, das nicht indiziert werden konnten
ms.openlocfilehash: e604f73216aab4cca259bc6cb7eb80a2fd36cd23
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830540"
---
# <a name="nonindexableitemstatistic"></a><span data-ttu-id="562c6-103">NonIndexableItemStatistic</span><span class="sxs-lookup"><span data-stu-id="562c6-103">NonIndexableItemStatistic</span></span>

<span data-ttu-id="562c6-104">Das **NonIndexableItemStatistic** -Element enthält eine einzelne Statistik für ein Element, das nicht indiziert werden konnten</span><span class="sxs-lookup"><span data-stu-id="562c6-104">The **NonIndexableItemStatistic** element contains a single statistic for an item that could not be indexed</span></span> 
  
```XML
<NonIndexableItemStatistic>
   <Mailbox/>
   <ItemCount/>
   <ErrorMessage/>
</NonIndexableItemStatistic>
```

 <span data-ttu-id="562c6-105">**NonIndexableItemStatisticType**</span><span class="sxs-lookup"><span data-stu-id="562c6-105">**NonIndexableItemStatisticType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="562c6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="562c6-106">Attributes and elements</span></span>

<span data-ttu-id="562c6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="562c6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="562c6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="562c6-108">Attributes</span></span>

<span data-ttu-id="562c6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="562c6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="562c6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="562c6-110">Child elements</span></span>

<span data-ttu-id="562c6-111">[Postfach (String)](mailbox-string.md) | [ItemCount](itemcount.md) | [ErrorMessage](errormessage.md)</span><span class="sxs-lookup"><span data-stu-id="562c6-111">[Mailbox (string)](mailbox-string.md) | [ItemCount](itemcount.md) | [ErrorMessage](errormessage.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="562c6-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="562c6-112">Parent elements</span></span>

[<span data-ttu-id="562c6-113">NonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="562c6-113">NonIndexableItemStatistics</span></span>](nonindexableitemstatistics.md)
  
## <a name="remarks"></a><span data-ttu-id="562c6-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="562c6-114">Remarks</span></span>

<span data-ttu-id="562c6-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="562c6-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="562c6-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="562c6-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="562c6-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="562c6-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="562c6-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="562c6-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="562c6-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="562c6-119">Schema name</span></span>  <br/> |<span data-ttu-id="562c6-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="562c6-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="562c6-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="562c6-121">Validation file</span></span>  <br/> |<span data-ttu-id="562c6-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="562c6-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="562c6-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="562c6-123">Can be empty</span></span>  <br/> |<span data-ttu-id="562c6-124">False</span><span class="sxs-lookup"><span data-stu-id="562c6-124">False</span></span>  <br/> |
   

