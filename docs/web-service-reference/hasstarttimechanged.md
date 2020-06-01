---
title: HasStartTimeChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 04a6968d-7fb5-47ee-b66e-dc99c35dbb63
description: Das HasStartTimeChanged-Element gibt an, ob die Startzeit für eine Besprechung geändert wurde.
ms.openlocfilehash: 1355917005d956d05064bfc095055fb72aa16c57
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462745"
---
# <a name="hasstarttimechanged"></a><span data-ttu-id="78c0b-103">HasStartTimeChanged</span><span class="sxs-lookup"><span data-stu-id="78c0b-103">HasStartTimeChanged</span></span>

<span data-ttu-id="78c0b-104">Das **HasStartTimeChanged** -Element gibt an, ob die Startzeit für eine Besprechung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="78c0b-104">The **HasStartTimeChanged** element specifies whether the start time for a meeting has changed.</span></span> 
  
```XML
<HasStartTimeChanged> true | false </HasStartTimeChanged>
```

 <span data-ttu-id="78c0b-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="78c0b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="78c0b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="78c0b-106">Attributes and elements</span></span>

<span data-ttu-id="78c0b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="78c0b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="78c0b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="78c0b-108">Attributes</span></span>

<span data-ttu-id="78c0b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="78c0b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="78c0b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="78c0b-110">Child elements</span></span>

<span data-ttu-id="78c0b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="78c0b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="78c0b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="78c0b-112">Parent elements</span></span>

|<span data-ttu-id="78c0b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="78c0b-113">**Element**</span></span>|<span data-ttu-id="78c0b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78c0b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78c0b-115">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="78c0b-115">ChangeHighlights</span></span>](changehighlights.md) <br/> |<span data-ttu-id="78c0b-116">Gibt an, was zwischen zwei Versionen einer Besprechungsanfrage Nachricht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="78c0b-116">Specifies what has changed between two versions of a meeting request message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="78c0b-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="78c0b-117">Text value</span></span>

<span data-ttu-id="78c0b-118">Der Textwert **true** für das **HasStartTimeChanged** -Element gibt an, dass die Startzeit für eine Besprechung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="78c0b-118">A text value of **true** for the **HasStartTimeChanged** element indicates that the start time for a meeting has changed.</span></span> <span data-ttu-id="78c0b-119">Der Wert **false** gibt an, dass die Startzeit nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="78c0b-119">A value of **false** indicates that the start time has not changed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="78c0b-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78c0b-120">Remarks</span></span>

<span data-ttu-id="78c0b-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="78c0b-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="78c0b-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="78c0b-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="78c0b-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="78c0b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78c0b-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="78c0b-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="78c0b-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="78c0b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="78c0b-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="78c0b-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="78c0b-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="78c0b-127">Validation File</span></span>  <br/> |<span data-ttu-id="78c0b-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="78c0b-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="78c0b-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="78c0b-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="78c0b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78c0b-130">See also</span></span>



- [<span data-ttu-id="78c0b-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="78c0b-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

