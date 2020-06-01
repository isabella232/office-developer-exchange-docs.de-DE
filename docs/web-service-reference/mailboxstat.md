---
title: MailboxStat
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5f24dc30-3ac2-4c82-9dfc-be9dbdb585be
description: Das MailboxStat-Element gibt die Statistik für ein Postfach an, das von der Ermittlungs Suche durchsucht wurde.
ms.openlocfilehash: 417f63f5e1aa34c2157b1d5ad868461113afec7b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44451432"
---
# <a name="mailboxstat"></a><span data-ttu-id="ef623-103">MailboxStat</span><span class="sxs-lookup"><span data-stu-id="ef623-103">MailboxStat</span></span>

<span data-ttu-id="ef623-104">Das **MailboxStat** -Element gibt die Statistik für ein Postfach an, das von der Ermittlungs Suche durchsucht wurde.</span><span class="sxs-lookup"><span data-stu-id="ef623-104">The **MailboxStat** element specifies statistics for a mailbox searched by discovery search.</span></span> 
  
```XML
<MailboxStat>
   <MailboxId/>
   <DisplayName/>
   <ItemCount/>
   <Size/>
</MailboxStat>
```

<span data-ttu-id="ef623-105">**MailboxStatisticsItemType**</span><span class="sxs-lookup"><span data-stu-id="ef623-105">**MailboxStatisticsItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ef623-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ef623-106">Attributes and elements</span></span>

<span data-ttu-id="ef623-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ef623-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef623-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ef623-108">Attributes</span></span>

<span data-ttu-id="ef623-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ef623-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef623-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef623-110">Child elements</span></span>

<span data-ttu-id="ef623-111">[Post Fach-Nr](mailboxid.md)  |  [DisplayName (Zeichenfolge)](displayname-string.md)  |  [ItemCount](itemcount.md)  |  [Größe (lang)](size-long.md)</span><span class="sxs-lookup"><span data-stu-id="ef623-111">[MailboxId](mailboxid.md) | [DisplayName (string)](displayname-string.md) | [ItemCount](itemcount.md) | [Size (long)](size-long.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ef623-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef623-112">Parent elements</span></span>

[<span data-ttu-id="ef623-113">MailboxStats</span><span class="sxs-lookup"><span data-stu-id="ef623-113">MailboxStats</span></span>](mailboxstats.md)
  
## <a name="remarks"></a><span data-ttu-id="ef623-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef623-114">Remarks</span></span>

<span data-ttu-id="ef623-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ef623-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ef623-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ef623-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef623-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ef623-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef623-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef623-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ef623-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ef623-119">Schema name</span></span>  <br/> |<span data-ttu-id="ef623-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ef623-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="ef623-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ef623-121">Validation file</span></span>  <br/> |<span data-ttu-id="ef623-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ef623-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ef623-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ef623-123">Can be empty</span></span>  <br/> |<span data-ttu-id="ef623-124">false</span><span class="sxs-lookup"><span data-stu-id="ef623-124">false</span></span>  <br/> |
   

