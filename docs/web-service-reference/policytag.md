---
title: PolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa4b1447-dc7b-47ad-a677-78fcee443dc6
description: Das PolicyTag-Element gibt die Aufbewahrungs-ID für ein Element oder einen Ordner an.
ms.openlocfilehash: ddc4d890d1e514586ba5ea7f6a8b541b2e4786c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460897"
---
# <a name="policytag"></a><span data-ttu-id="b9e58-103">PolicyTag</span><span class="sxs-lookup"><span data-stu-id="b9e58-103">PolicyTag</span></span>

<span data-ttu-id="b9e58-104">Das **PolicyTag** -Element gibt die Aufbewahrungs-ID für ein Element oder einen Ordner an.</span><span class="sxs-lookup"><span data-stu-id="b9e58-104">The **PolicyTag** element specifies the retention identifier on an item or folder.</span></span> 
  
```xml
<PolicyTag IsExplicit="true | false"></PolicyTag>
```

 <span data-ttu-id="b9e58-105">**RetentionTagType**</span><span class="sxs-lookup"><span data-stu-id="b9e58-105">**RetentionTagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b9e58-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b9e58-106">Attributes and elements</span></span>

<span data-ttu-id="b9e58-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b9e58-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b9e58-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b9e58-108">Attributes</span></span>

|<span data-ttu-id="b9e58-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b9e58-109">**Attribute**</span></span>|<span data-ttu-id="b9e58-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b9e58-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9e58-111">Isexplicit</span><span class="sxs-lookup"><span data-stu-id="b9e58-111">IsExplicit</span></span>  <br/> |<span data-ttu-id="b9e58-112">Gibt an, ob ein Richtlinien Tag explizit für ein Element oder einen Ordner festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="b9e58-112">Indicates whether a policy tag was explicitly set on an item or folder.</span></span>  <br/> <span data-ttu-id="b9e58-113">Der Textwert **true** für das Attribut **isexplicit** gibt an, dass das richtlinientag explizit für das Element oder den Ordner festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="b9e58-113">A text value of **true** for the **IsExplicit** attribute indicates that the policy tag was explicitly set on the item or folder.</span></span> <span data-ttu-id="b9e58-114">Der Textwert **false** gibt an, dass das richtlinientag für das Element oder den Ordner basierend auf dem richtlinientag des übergeordneten Ordners implizit festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="b9e58-114">A text value of **false** indicates that the policy tag was implicitly set on the item or folder based on the parent folder policy tag.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b9e58-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b9e58-115">Child elements</span></span>

<span data-ttu-id="b9e58-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="b9e58-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b9e58-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b9e58-117">Parent elements</span></span>

<span data-ttu-id="b9e58-118">[SearchPreviewItem](searchpreviewitem.md)  |  [Element](item.md)  |  [Kontaktinformationen](contact.md)  |  [Nachricht](message-ex15websvcsotherref.md)  |  [Verteilerliste](distributionlist.md)  |  [CalendarItem](calendaritem.md)  |  [PostItem](postitem.md)  |  [Aufgabe](task.md)</span><span class="sxs-lookup"><span data-stu-id="b9e58-118">[SearchPreviewItem](searchpreviewitem.md) | [Item](item.md) | [Contact](contact.md) | [Message](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="b9e58-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="b9e58-119">Text value</span></span>

<span data-ttu-id="b9e58-120">Der Textwert des **PolicyTag** -Elements ist der Bezeichner des Richtlinien Tags.</span><span class="sxs-lookup"><span data-stu-id="b9e58-120">The text value of the **PolicyTag** element is the policy tag identifier.</span></span> <span data-ttu-id="b9e58-121">Der Bezeichner des Richtlinien Tags ist eine GUID.</span><span class="sxs-lookup"><span data-stu-id="b9e58-121">The policy tag identifier is a GUID.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b9e58-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9e58-122">Remarks</span></span>

<span data-ttu-id="b9e58-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b9e58-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b9e58-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b9e58-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b9e58-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b9e58-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9e58-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9e58-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b9e58-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b9e58-127">Schema name</span></span>  <br/> |<span data-ttu-id="b9e58-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b9e58-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="b9e58-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b9e58-129">Validation file</span></span>  <br/> |<span data-ttu-id="b9e58-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b9e58-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b9e58-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b9e58-131">Can be empty</span></span>  <br/> ||
   

