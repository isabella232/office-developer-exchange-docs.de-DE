---
title: PolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa4b1447-dc7b-47ad-a677-78fcee443dc6
description: Das PolicyTag-Element gibt den Bezeichner für die Aufbewahrung auf eines Elements oder Ordners.
ms.openlocfilehash: d6cd5aab1145f6006912541c8f8c1d0a91d1e17e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830835"
---
# <a name="policytag"></a><span data-ttu-id="8d06b-103">PolicyTag</span><span class="sxs-lookup"><span data-stu-id="8d06b-103">PolicyTag</span></span>

<span data-ttu-id="8d06b-104">Das **PolicyTag** -Element gibt den Bezeichner für die Aufbewahrung auf eines Elements oder Ordners.</span><span class="sxs-lookup"><span data-stu-id="8d06b-104">The **PolicyTag** element specifies the retention identifier on an item or folder.</span></span> 
  
```xml
<PolicyTag IsExplicit="true | false"></PolicyTag>
```

 <span data-ttu-id="8d06b-105">**RetentionTagType**</span><span class="sxs-lookup"><span data-stu-id="8d06b-105">**RetentionTagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8d06b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8d06b-106">Attributes and elements</span></span>

<span data-ttu-id="8d06b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8d06b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d06b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8d06b-108">Attributes</span></span>

|<span data-ttu-id="8d06b-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8d06b-109">**Attribute**</span></span>|<span data-ttu-id="8d06b-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d06b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8d06b-111">IsExplicit</span><span class="sxs-lookup"><span data-stu-id="8d06b-111">IsExplicit</span></span>  <br/> |<span data-ttu-id="8d06b-112">Gibt an, ob ein Tag Richtlinie auf eines Elements oder Ordners explizit festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8d06b-112">Indicates whether a policy tag was explicitly set on an item or folder.</span></span>  <br/> <span data-ttu-id="8d06b-113">Der Textwert **true** für das **IsExplicit** -Attribut gibt an, dass das Tag Richtlinie auf des Elements oder Ordners explizit festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8d06b-113">A text value of **true** for the **IsExplicit** attribute indicates that the policy tag was explicitly set on the item or folder.</span></span> <span data-ttu-id="8d06b-114">Der Textwert **false** gibt an, dass das Tag Richtlinie implizit für des Elements oder Ordners basierend auf dem übergeordneten Ordner Policy Tag festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8d06b-114">A text value of **false** indicates that the policy tag was implicitly set on the item or folder based on the parent folder policy tag.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8d06b-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d06b-115">Child elements</span></span>

<span data-ttu-id="8d06b-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="8d06b-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8d06b-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d06b-117">Parent elements</span></span>

<span data-ttu-id="8d06b-118">[SearchPreviewItem](searchpreviewitem.md) | [Element](item.md) | [Kontakt](contact.md) | [Nachricht](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Aufgabe](task.md)</span><span class="sxs-lookup"><span data-stu-id="8d06b-118">[SearchPreviewItem](searchpreviewitem.md) | [Item](item.md) | [Contact](contact.md) | [Message](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="8d06b-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="8d06b-119">Text value</span></span>

<span data-ttu-id="8d06b-120">Der Textwert des **PolicyTag** -Elements ist die Richtlinie Tag-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="8d06b-120">The text value of the **PolicyTag** element is the policy tag identifier.</span></span> <span data-ttu-id="8d06b-121">Die Richtlinie Tag-ID ist eine GUID.</span><span class="sxs-lookup"><span data-stu-id="8d06b-121">The policy tag identifier is a GUID.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8d06b-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d06b-122">Remarks</span></span>

<span data-ttu-id="8d06b-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8d06b-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8d06b-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8d06b-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8d06b-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8d06b-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d06b-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d06b-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8d06b-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8d06b-127">Schema name</span></span>  <br/> |<span data-ttu-id="8d06b-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8d06b-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="8d06b-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8d06b-129">Validation file</span></span>  <br/> |<span data-ttu-id="8d06b-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8d06b-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8d06b-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8d06b-131">Can be empty</span></span>  <br/> ||
   

