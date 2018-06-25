---
title: IncludePersonalArchive
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b373bb1a-6b1d-4959-98a1-4c4ea62973bc
description: Das IncludePersonalArchive-Element gibt an, ob das persönliche Archiv in die Suche einzubeziehen.
ms.openlocfilehash: ba2dcaae3befd3595815c7281858e4fa8a738e0a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829905"
---
# <a name="includepersonalarchive"></a><span data-ttu-id="e832b-103">IncludePersonalArchive</span><span class="sxs-lookup"><span data-stu-id="e832b-103">IncludePersonalArchive</span></span>

<span data-ttu-id="e832b-104">Das **IncludePersonalArchive** -Element gibt an, ob das persönliche Archiv in die Suche einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="e832b-104">The **IncludePersonalArchive** element specifies whether to include the personal archive in the search.</span></span> 
  
```XML
<IncludePersonalArchive>true | false</IncludePersonalArchive>
```

 <span data-ttu-id="e832b-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e832b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e832b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e832b-106">Attributes and elements</span></span>

<span data-ttu-id="e832b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e832b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e832b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e832b-108">Attributes</span></span>

<span data-ttu-id="e832b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e832b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e832b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e832b-110">Child elements</span></span>

<span data-ttu-id="e832b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e832b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e832b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e832b-112">Parent elements</span></span>

|<span data-ttu-id="e832b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e832b-113">**Element**</span></span>|<span data-ttu-id="e832b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e832b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e832b-115">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="e832b-115">FindMailboxStatisticsByKeywords</span></span>](findmailboxstatisticsbykeywords.md) <br/> |<span data-ttu-id="e832b-116">Gibt eine Anforderung an die Postfachstatistiken nach Schlüsselwort suchen.</span><span class="sxs-lookup"><span data-stu-id="e832b-116">Specifies a request to search for mailbox statistics by keyword.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e832b-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="e832b-117">Text value</span></span>

<span data-ttu-id="e832b-118">Der Textwert **true** für das **IncludePersonalArchive** -Element gibt an, dass das persönliche Archiv in die Suche einbezogen wird.</span><span class="sxs-lookup"><span data-stu-id="e832b-118">A text value of **true** for the **IncludePersonalArchive** element indicates that the personal archive is included in the search.</span></span> <span data-ttu-id="e832b-119">Der Wert **false** gibt an, dass das persönliche Archiv in die Suche nicht enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e832b-119">A value of **false** indicates that the personal archive is not included in the search.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e832b-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e832b-120">Remarks</span></span>

<span data-ttu-id="e832b-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e832b-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e832b-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e832b-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e832b-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="e832b-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e832b-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e832b-124">Schema Name</span></span>  <br/> |<span data-ttu-id="e832b-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="e832b-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="e832b-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e832b-126">Validation File</span></span>  <br/> |<span data-ttu-id="e832b-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e832b-127">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e832b-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e832b-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e832b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e832b-129">See also</span></span>



- [<span data-ttu-id="e832b-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e832b-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

