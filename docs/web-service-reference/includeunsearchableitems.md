---
title: IncludeUnsearchableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9a9bd2dc-f5b9-4b82-a6a0-f643d2951080
description: Das IncludeUnsearchableItems-Element gibt an, ob Elemente enthalten, die durchsucht werden kann.
ms.openlocfilehash: 4c6b9b3752330bf914c9901d2e8f69e93546fec6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829907"
---
# <a name="includeunsearchableitems"></a><span data-ttu-id="bf823-103">IncludeUnsearchableItems</span><span class="sxs-lookup"><span data-stu-id="bf823-103">IncludeUnsearchableItems</span></span>

<span data-ttu-id="bf823-104">Das **IncludeUnsearchableItems** -Element gibt an, ob Elemente enthalten, die durchsucht werden kann.</span><span class="sxs-lookup"><span data-stu-id="bf823-104">The **IncludeUnsearchableItems** element specifies whether to include items that cannot be searched.</span></span> 
  
```XML
<IncludeUnsearchableItems>true | false</IncludeUnsearchableItems>
```

 <span data-ttu-id="bf823-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="bf823-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bf823-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bf823-106">Attributes and elements</span></span>

<span data-ttu-id="bf823-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bf823-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bf823-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="bf823-108">Attributes</span></span>

<span data-ttu-id="bf823-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="bf823-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bf823-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bf823-110">Child elements</span></span>

<span data-ttu-id="bf823-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="bf823-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bf823-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bf823-112">Parent elements</span></span>

|<span data-ttu-id="bf823-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bf823-113">**Element**</span></span>|<span data-ttu-id="bf823-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bf823-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bf823-115">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="bf823-115">FindMailboxStatisticsByKeywords</span></span>](findmailboxstatisticsbykeywords.md) <br/> |<span data-ttu-id="bf823-116">Gibt eine Anforderung an die Postfachstatistiken nach Schlüsselwort suchen.</span><span class="sxs-lookup"><span data-stu-id="bf823-116">Specifies a request to search for mailbox statistics by keyword.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bf823-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="bf823-117">Text value</span></span>

<span data-ttu-id="bf823-118">Der Textwert **true** für das **IncludeUnsearchableItems** -Element gibt an, dass Statistiken nicht für Elemente enthalten sind, die nicht durchsuchbar sind.</span><span class="sxs-lookup"><span data-stu-id="bf823-118">A text value of **true** for the **IncludeUnsearchableItems** element indicates that statistics are not included for items that are not searchable.</span></span> <span data-ttu-id="bf823-119">Der Wert **false** gibt an, dass Statistiken für Elemente enthalten sind, die nicht durchsuchbar sind.</span><span class="sxs-lookup"><span data-stu-id="bf823-119">A value of **false** indicates that statistics are included for items that are not searchable.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bf823-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bf823-120">Remarks</span></span>

<span data-ttu-id="bf823-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bf823-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="bf823-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="bf823-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bf823-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bf823-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf823-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="bf823-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bf823-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bf823-125">Schema Name</span></span>  <br/> |<span data-ttu-id="bf823-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="bf823-126">Message schema</span></span>  <br/> |
|<span data-ttu-id="bf823-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bf823-127">Validation File</span></span>  <br/> |<span data-ttu-id="bf823-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bf823-128">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bf823-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="bf823-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="bf823-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf823-130">See also</span></span>



- [<span data-ttu-id="bf823-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bf823-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

