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
ms.openlocfilehash: 15ad52c7b7581cce5ca96ba5ff4e8a1c130a02cf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461786"
---
# <a name="hasendtimechanged"></a><span data-ttu-id="3f978-103">HasEndTimeChanged</span><span class="sxs-lookup"><span data-stu-id="3f978-103">HasEndTimeChanged</span></span>

<span data-ttu-id="3f978-104">Das **HasEndTimeChanged** -Element gibt an, ob die Endzeit für eine Besprechung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="3f978-104">The **HasEndTimeChanged** element specifies whether the end time for a meeting has changed.</span></span> 
  
```XML
<HasEndTimeChanged>true | false</HasEndTimeChanged>
```

 <span data-ttu-id="3f978-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="3f978-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3f978-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3f978-106">Attributes and elements</span></span>

<span data-ttu-id="3f978-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3f978-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3f978-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3f978-108">Attributes</span></span>

<span data-ttu-id="3f978-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3f978-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3f978-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3f978-110">Child elements</span></span>

<span data-ttu-id="3f978-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3f978-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3f978-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3f978-112">Parent elements</span></span>

|<span data-ttu-id="3f978-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3f978-113">**Element**</span></span>|<span data-ttu-id="3f978-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3f978-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f978-115">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="3f978-115">ChangeHighlights</span></span>](changehighlights.md) <br/> |<span data-ttu-id="3f978-116">Gibt an, was zwischen zwei Versionen einer Besprechungsanfrage Nachricht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="3f978-116">Specifies what has changed between two versions of a meeting request message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3f978-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="3f978-117">Text value</span></span>

<span data-ttu-id="3f978-118">Der Textwert **true** für das **HasEndTimeChanged** -Element gibt an, dass die Endzeit einer Besprechung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="3f978-118">A text value of **true** for the **HasEndTimeChanged** element indicates that the end time of a meeting has changed.</span></span> <span data-ttu-id="3f978-119">Der Wert **false** gibt an, dass die Endzeit einer Besprechung nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="3f978-119">A value of **false** indicates that the end time of a meeting has not changed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3f978-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f978-120">Remarks</span></span>

<span data-ttu-id="3f978-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3f978-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3f978-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3f978-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3f978-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3f978-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f978-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="3f978-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3f978-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3f978-125">Schema Name</span></span>  <br/> |<span data-ttu-id="3f978-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="3f978-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="3f978-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3f978-127">Validation File</span></span>  <br/> |<span data-ttu-id="3f978-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="3f978-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="3f978-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="3f978-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3f978-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f978-130">See also</span></span>



- [<span data-ttu-id="3f978-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3f978-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

