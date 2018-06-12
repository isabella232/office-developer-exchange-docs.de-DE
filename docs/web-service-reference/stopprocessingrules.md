---
title: StopProcessingRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StopProcessingRules
api_type:
- schema
ms.assetid: 5b89a2cb-ab26-444d-b3dd-2b3858872d63
description: Das StopProcessingRules -Element gibt an, ob nachfolgende Regeln sind ausgewertet werden soll.
ms.openlocfilehash: 48799975f8c928bf291fcdcdb83f2ff8768af8b9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831593"
---
# <a name="stopprocessingrules"></a><span data-ttu-id="e3adb-103">StopProcessingRules</span><span class="sxs-lookup"><span data-stu-id="e3adb-103">StopProcessingRules</span></span>

<span data-ttu-id="e3adb-104">Das **StopProcessingRules** -Element gibt an, ob nachfolgende Regeln sind ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3adb-104">The **StopProcessingRules** element indicates whether subsequent rules are to be evaluated.</span></span> 
  
```XML
<StopProcessingRules>true | false</StopProcessingRules>
```

 <span data-ttu-id="e3adb-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e3adb-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e3adb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e3adb-106">Attributes and elements</span></span>

<span data-ttu-id="e3adb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e3adb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3adb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e3adb-108">Attributes</span></span>

<span data-ttu-id="e3adb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e3adb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e3adb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e3adb-110">Child elements</span></span>

<span data-ttu-id="e3adb-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e3adb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e3adb-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e3adb-112">Parent elements</span></span>

|<span data-ttu-id="e3adb-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e3adb-113">**Element**</span></span>|<span data-ttu-id="e3adb-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e3adb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3adb-115">Aktionen</span><span class="sxs-lookup"><span data-stu-id="e3adb-115">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="e3adb-116">Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="e3adb-116">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e3adb-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="e3adb-117">Text value</span></span>

<span data-ttu-id="e3adb-p101">Der Textwert **true** gibt an, dass nachfolgende Regeln nicht verarbeitet werden soll. Der Wert **false** gibt an, dass nachfolgende Regeln ausgewertet wird fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3adb-p101">A text value of **true** indicates that subsequent rules should not be processed. A value of **false** indicates that subsequent rules should continue to be evaluated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e3adb-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e3adb-120">Remarks</span></span>

<span data-ttu-id="e3adb-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e3adb-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e3adb-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e3adb-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3adb-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="e3adb-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e3adb-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e3adb-124">Schema Name</span></span>  <br/> |<span data-ttu-id="e3adb-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="e3adb-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e3adb-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e3adb-126">Validation File</span></span>  <br/> |<span data-ttu-id="e3adb-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e3adb-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e3adb-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e3adb-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="e3adb-129">True</span><span class="sxs-lookup"><span data-stu-id="e3adb-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3adb-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3adb-130">See also</span></span>



- [<span data-ttu-id="e3adb-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e3adb-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

