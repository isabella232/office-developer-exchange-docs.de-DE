---
title: HasEndTimeChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0eb444d-8e2e-478b-b785-2b9787ffb226
description: Das HasEndTimeChanged-Element gibt an, ob die Endzeit für eine Besprechung geändert wurde.
ms.openlocfilehash: 046bb302d6f7052c6f1757ce393583b305311e2f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829805"
---
# <a name="hasendtimechanged"></a><span data-ttu-id="79b40-103">HasEndTimeChanged</span><span class="sxs-lookup"><span data-stu-id="79b40-103">HasEndTimeChanged</span></span>

<span data-ttu-id="79b40-104">Das **HasEndTimeChanged** -Element gibt an, ob die Endzeit für eine Besprechung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="79b40-104">The **HasEndTimeChanged** element specifies whether the end time for a meeting has changed.</span></span> 
  
```XML
<HasEndTimeChanged>true | false</HasEndTimeChanged>
```

 <span data-ttu-id="79b40-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="79b40-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="79b40-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="79b40-106">Attributes and elements</span></span>

<span data-ttu-id="79b40-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="79b40-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="79b40-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="79b40-108">Attributes</span></span>

<span data-ttu-id="79b40-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="79b40-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="79b40-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="79b40-110">Child elements</span></span>

<span data-ttu-id="79b40-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="79b40-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="79b40-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="79b40-112">Parent elements</span></span>

|<span data-ttu-id="79b40-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="79b40-113">**Element**</span></span>|<span data-ttu-id="79b40-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="79b40-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="79b40-115">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="79b40-115">ChangeHighlights</span></span>](changehighlights.md) <br/> |<span data-ttu-id="79b40-116">Gibt an, was sich zwischen zwei Versionen einer Besprechung geändert hat Request-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="79b40-116">Specifies what has changed between two versions of a meeting request message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="79b40-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="79b40-117">Text value</span></span>

<span data-ttu-id="79b40-118">Der Textwert **true** für das **HasEndTimeChanged** -Element gibt an, dass die Zeit für das Ende einer Besprechung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="79b40-118">A text value of **true** for the **HasEndTimeChanged** element indicates that the end time of a meeting has changed.</span></span> <span data-ttu-id="79b40-119">Der Wert **false** gibt an, dass die Endzeit der Besprechung nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="79b40-119">A value of **false** indicates that the end time of a meeting has not changed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="79b40-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="79b40-120">Remarks</span></span>

<span data-ttu-id="79b40-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="79b40-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="79b40-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="79b40-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="79b40-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="79b40-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79b40-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="79b40-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="79b40-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="79b40-125">Schema Name</span></span>  <br/> |<span data-ttu-id="79b40-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="79b40-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="79b40-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="79b40-127">Validation File</span></span>  <br/> |<span data-ttu-id="79b40-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="79b40-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="79b40-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="79b40-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="79b40-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79b40-130">See also</span></span>



- [<span data-ttu-id="79b40-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="79b40-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

