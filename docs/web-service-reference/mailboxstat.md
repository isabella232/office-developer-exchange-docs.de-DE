---
title: MailboxStat
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5f24dc30-3ac2-4c82-9dfc-be9dbdb585be
description: Das MailboxStat-Element gibt Statistiken für ein Postfach von Discovery-Suche durchsucht.
ms.openlocfilehash: 692f15904467ce192074b14f7c2a742b3e76de8e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830296"
---
# <a name="mailboxstat"></a><span data-ttu-id="ab9b2-103">MailboxStat</span><span class="sxs-lookup"><span data-stu-id="ab9b2-103">MailboxStat</span></span>

<span data-ttu-id="ab9b2-104">Das **MailboxStat** -Element gibt Statistiken für ein Postfach von Discovery-Suche durchsucht.</span><span class="sxs-lookup"><span data-stu-id="ab9b2-104">The **MailboxStat** element specifies statistics for a mailbox searched by discovery search.</span></span> 
  
```XML
<MailboxStat>
   <MailboxId/>
   <DisplayName/>
   <ItemCount/>
   <Size/>
</MailboxStat>
```

<span data-ttu-id="ab9b2-105">**MailboxStatisticsItemType**</span><span class="sxs-lookup"><span data-stu-id="ab9b2-105">**MailboxStatisticsItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ab9b2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ab9b2-106">Attributes and elements</span></span>

<span data-ttu-id="ab9b2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ab9b2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ab9b2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ab9b2-108">Attributes</span></span>

<span data-ttu-id="ab9b2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ab9b2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ab9b2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ab9b2-110">Child elements</span></span>

<span data-ttu-id="ab9b2-111">[MailboxId](mailboxid.md) | [DisplayName (String)](displayname-string.md) | [ItemCount](itemcount.md) | [Größe (long)](size-long.md)</span><span class="sxs-lookup"><span data-stu-id="ab9b2-111">[MailboxId](mailboxid.md) | [DisplayName (string)](displayname-string.md) | [ItemCount](itemcount.md) | [Size (long)](size-long.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ab9b2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ab9b2-112">Parent elements</span></span>

[<span data-ttu-id="ab9b2-113">MailboxStats</span><span class="sxs-lookup"><span data-stu-id="ab9b2-113">MailboxStats</span></span>](mailboxstats.md)
  
## <a name="remarks"></a><span data-ttu-id="ab9b2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ab9b2-114">Remarks</span></span>

<span data-ttu-id="ab9b2-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ab9b2-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ab9b2-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ab9b2-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ab9b2-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ab9b2-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab9b2-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab9b2-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ab9b2-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ab9b2-119">Schema name</span></span>  <br/> |<span data-ttu-id="ab9b2-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ab9b2-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="ab9b2-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ab9b2-121">Validation file</span></span>  <br/> |<span data-ttu-id="ab9b2-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ab9b2-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ab9b2-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ab9b2-123">Can be empty</span></span>  <br/> |<span data-ttu-id="ab9b2-124">false</span><span class="sxs-lookup"><span data-stu-id="ab9b2-124">false</span></span>  <br/> |
   

