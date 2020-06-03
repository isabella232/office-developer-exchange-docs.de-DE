---
title: Parameter IncludeUnsearchableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9a9bd2dc-f5b9-4b82-a6a0-f643d2951080
description: Das Parameter IncludeUnsearchableItems-Element gibt an, ob Elemente einbezogen werden, die nicht durchsucht werden können.
ms.openlocfilehash: 19fe450f5b1647be2df75138dbe67dd9e1c05c21
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465702"
---
# <a name="includeunsearchableitems"></a><span data-ttu-id="68b02-103">Parameter IncludeUnsearchableItems</span><span class="sxs-lookup"><span data-stu-id="68b02-103">IncludeUnsearchableItems</span></span>

<span data-ttu-id="68b02-104">Das **Parameter IncludeUnsearchableItems** -Element gibt an, ob Elemente einbezogen werden, die nicht durchsucht werden können.</span><span class="sxs-lookup"><span data-stu-id="68b02-104">The **IncludeUnsearchableItems** element specifies whether to include items that cannot be searched.</span></span> 
  
```XML
<IncludeUnsearchableItems>true | false</IncludeUnsearchableItems>
```

 <span data-ttu-id="68b02-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="68b02-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="68b02-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="68b02-106">Attributes and elements</span></span>

<span data-ttu-id="68b02-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="68b02-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="68b02-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="68b02-108">Attributes</span></span>

<span data-ttu-id="68b02-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="68b02-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="68b02-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68b02-110">Child elements</span></span>

<span data-ttu-id="68b02-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="68b02-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="68b02-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68b02-112">Parent elements</span></span>

|<span data-ttu-id="68b02-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="68b02-113">**Element**</span></span>|<span data-ttu-id="68b02-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68b02-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68b02-115">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="68b02-115">FindMailboxStatisticsByKeywords</span></span>](findmailboxstatisticsbykeywords.md) <br/> |<span data-ttu-id="68b02-116">Gibt eine Anforderung an, nach Postfachstatistiken nach Stichwort zu suchen.</span><span class="sxs-lookup"><span data-stu-id="68b02-116">Specifies a request to search for mailbox statistics by keyword.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="68b02-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="68b02-117">Text value</span></span>

<span data-ttu-id="68b02-118">Der Textwert **true** für das **Parameter IncludeUnsearchableItems** -Element gibt an, dass Statistiken nicht für Elemente enthalten sind, die nicht durchsuchbar sind.</span><span class="sxs-lookup"><span data-stu-id="68b02-118">A text value of **true** for the **IncludeUnsearchableItems** element indicates that statistics are not included for items that are not searchable.</span></span> <span data-ttu-id="68b02-119">Der Wert **false** gibt an, dass Statistiken für Elemente enthalten sind, die nicht durchsuchbar sind.</span><span class="sxs-lookup"><span data-stu-id="68b02-119">A value of **false** indicates that statistics are included for items that are not searchable.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="68b02-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68b02-120">Remarks</span></span>

<span data-ttu-id="68b02-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="68b02-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="68b02-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="68b02-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="68b02-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="68b02-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68b02-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="68b02-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="68b02-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="68b02-125">Schema Name</span></span>  <br/> |<span data-ttu-id="68b02-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="68b02-126">Message schema</span></span>  <br/> |
|<span data-ttu-id="68b02-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="68b02-127">Validation File</span></span>  <br/> |<span data-ttu-id="68b02-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="68b02-128">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="68b02-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="68b02-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="68b02-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68b02-130">See also</span></span>



- [<span data-ttu-id="68b02-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="68b02-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

