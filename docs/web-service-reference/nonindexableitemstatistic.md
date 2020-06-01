---
title: NonIndexableItemStatistic
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 593e0c79-9ec2-4040-a6a3-3c5c61cbdf7c
description: Das NonIndexableItemStatistic-Element enthält eine einzelne Statistik für ein Element, das nicht indiziert werden konnte.
ms.openlocfilehash: cc7bee9fd2759a16dd16538d6712e40ceb005fec
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462682"
---
# <a name="nonindexableitemstatistic"></a><span data-ttu-id="b86c7-103">NonIndexableItemStatistic</span><span class="sxs-lookup"><span data-stu-id="b86c7-103">NonIndexableItemStatistic</span></span>

<span data-ttu-id="b86c7-104">Das **NonIndexableItemStatistic** -Element enthält eine einzelne Statistik für ein Element, das nicht indiziert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="b86c7-104">The **NonIndexableItemStatistic** element contains a single statistic for an item that could not be indexed</span></span> 
  
```XML
<NonIndexableItemStatistic>
   <Mailbox/>
   <ItemCount/>
   <ErrorMessage/>
</NonIndexableItemStatistic>
```

 <span data-ttu-id="b86c7-105">**NonIndexableItemStatisticType**</span><span class="sxs-lookup"><span data-stu-id="b86c7-105">**NonIndexableItemStatisticType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b86c7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b86c7-106">Attributes and elements</span></span>

<span data-ttu-id="b86c7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b86c7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b86c7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b86c7-108">Attributes</span></span>

<span data-ttu-id="b86c7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b86c7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b86c7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b86c7-110">Child elements</span></span>

<span data-ttu-id="b86c7-111">[Postfach (Zeichenfolge)](mailbox-string.md)  |  [ItemCount](itemcount.md)  |  [ErrorMessage](errormessage.md)</span><span class="sxs-lookup"><span data-stu-id="b86c7-111">[Mailbox (string)](mailbox-string.md) | [ItemCount](itemcount.md) | [ErrorMessage](errormessage.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b86c7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b86c7-112">Parent elements</span></span>

[<span data-ttu-id="b86c7-113">NonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="b86c7-113">NonIndexableItemStatistics</span></span>](nonindexableitemstatistics.md)
  
## <a name="remarks"></a><span data-ttu-id="b86c7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b86c7-114">Remarks</span></span>

<span data-ttu-id="b86c7-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b86c7-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b86c7-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b86c7-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b86c7-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b86c7-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b86c7-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="b86c7-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b86c7-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b86c7-119">Schema name</span></span>  <br/> |<span data-ttu-id="b86c7-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b86c7-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b86c7-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b86c7-121">Validation file</span></span>  <br/> |<span data-ttu-id="b86c7-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b86c7-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b86c7-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b86c7-123">Can be empty</span></span>  <br/> |<span data-ttu-id="b86c7-124">False</span><span class="sxs-lookup"><span data-stu-id="b86c7-124">False</span></span>  <br/> |
   

