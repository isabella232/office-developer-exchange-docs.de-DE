---
title: IncludePersonalArchive
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b373bb1a-6b1d-4959-98a1-4c4ea62973bc
description: Das IncludePersonalArchive-Element gibt an, ob das persönliche Archiv in die Suche einbezogen werden soll.
ms.openlocfilehash: a25dd45bc0717af8f949d14b88793af3821ca69f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458250"
---
# <a name="includepersonalarchive"></a><span data-ttu-id="63a06-103">IncludePersonalArchive</span><span class="sxs-lookup"><span data-stu-id="63a06-103">IncludePersonalArchive</span></span>

<span data-ttu-id="63a06-104">Das **IncludePersonalArchive** -Element gibt an, ob das persönliche Archiv in die Suche einbezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="63a06-104">The **IncludePersonalArchive** element specifies whether to include the personal archive in the search.</span></span> 
  
```XML
<IncludePersonalArchive>true | false</IncludePersonalArchive>
```

 <span data-ttu-id="63a06-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="63a06-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="63a06-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="63a06-106">Attributes and elements</span></span>

<span data-ttu-id="63a06-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="63a06-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="63a06-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="63a06-108">Attributes</span></span>

<span data-ttu-id="63a06-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="63a06-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="63a06-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="63a06-110">Child elements</span></span>

<span data-ttu-id="63a06-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="63a06-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="63a06-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="63a06-112">Parent elements</span></span>

|<span data-ttu-id="63a06-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="63a06-113">**Element**</span></span>|<span data-ttu-id="63a06-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="63a06-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="63a06-115">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="63a06-115">FindMailboxStatisticsByKeywords</span></span>](findmailboxstatisticsbykeywords.md) <br/> |<span data-ttu-id="63a06-116">Gibt eine Anforderung an, nach Postfachstatistiken nach Stichwort zu suchen.</span><span class="sxs-lookup"><span data-stu-id="63a06-116">Specifies a request to search for mailbox statistics by keyword.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="63a06-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="63a06-117">Text value</span></span>

<span data-ttu-id="63a06-118">Der Textwert **true** für das **IncludePersonalArchive** -Element gibt an, dass das persönliche Archiv in die Suche einbezogen wird.</span><span class="sxs-lookup"><span data-stu-id="63a06-118">A text value of **true** for the **IncludePersonalArchive** element indicates that the personal archive is included in the search.</span></span> <span data-ttu-id="63a06-119">Der Wert **false** gibt an, dass das persönliche Archiv nicht in die Suche einbezogen wird.</span><span class="sxs-lookup"><span data-stu-id="63a06-119">A value of **false** indicates that the personal archive is not included in the search.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="63a06-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63a06-120">Remarks</span></span>

<span data-ttu-id="63a06-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="63a06-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="63a06-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="63a06-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63a06-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="63a06-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="63a06-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="63a06-124">Schema Name</span></span>  <br/> |<span data-ttu-id="63a06-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="63a06-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="63a06-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="63a06-126">Validation File</span></span>  <br/> |<span data-ttu-id="63a06-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="63a06-127">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="63a06-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="63a06-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="63a06-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63a06-129">See also</span></span>



- [<span data-ttu-id="63a06-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="63a06-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

