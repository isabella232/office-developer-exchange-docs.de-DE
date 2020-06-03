---
title: Referenten
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 01057872-4f1a-4246-86ba-73d10ef854a0
description: Das presenters-Element gibt die Referenten für eine Onlinebesprechung an.
ms.openlocfilehash: 0236457020dfc4684569e84d3d54e357af00d102
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529910"
---
# <a name="presenters"></a><span data-ttu-id="c7e53-103">Referenten</span><span class="sxs-lookup"><span data-stu-id="c7e53-103">Presenters</span></span>

<span data-ttu-id="c7e53-104">Das **Presenters** -Element gibt die Referenten für eine Onlinebesprechung an.</span><span class="sxs-lookup"><span data-stu-id="c7e53-104">The **Presenters** element specifies the presenters for an online meeting.</span></span> 
  
```XML
<Presenters> Disabled | Internal | Everyone </Presenters>
```

 <span data-ttu-id="c7e53-105">**PresentersType**</span><span class="sxs-lookup"><span data-stu-id="c7e53-105">**PresentersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c7e53-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c7e53-106">Attributes and elements</span></span>

<span data-ttu-id="c7e53-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c7e53-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7e53-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c7e53-108">Attributes</span></span>

<span data-ttu-id="c7e53-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c7e53-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c7e53-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c7e53-110">Child elements</span></span>

<span data-ttu-id="c7e53-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c7e53-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c7e53-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c7e53-112">Parent elements</span></span>

[<span data-ttu-id="c7e53-113">OnlineMeetingSettings</span><span class="sxs-lookup"><span data-stu-id="c7e53-113">OnlineMeetingSettings</span></span>](onlinemeetingsettings.md)
  
## <a name="text-value"></a><span data-ttu-id="c7e53-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="c7e53-114">Text value</span></span>

<span data-ttu-id="c7e53-115">Der Textwert des **Presenters** -Elements ist der Typ von Benutzern, die als Referent für eine Onlinebesprechung fungieren können.</span><span class="sxs-lookup"><span data-stu-id="c7e53-115">The text value of **Presenters** element is the type of users that can be a presenter for an online meeting.</span></span> <span data-ttu-id="c7e53-116">Die Textwerte für das **Presenters** -Element werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c7e53-116">The text values for the **Presenters** element are described in the following table.</span></span> 
  
<span data-ttu-id="c7e53-117">**Textwerte des Presenters-Elements**</span><span class="sxs-lookup"><span data-stu-id="c7e53-117">**Presenters element text values**</span></span>

|<span data-ttu-id="c7e53-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c7e53-118">**Value**</span></span>|<span data-ttu-id="c7e53-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c7e53-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c7e53-120">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="c7e53-120">Disabled</span></span>  <br/> |<span data-ttu-id="c7e53-121">Referenten sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c7e53-121">Presenters are disabled.</span></span>  <br/> |
|<span data-ttu-id="c7e53-122">Intern</span><span class="sxs-lookup"><span data-stu-id="c7e53-122">Internal</span></span>  <br/> |<span data-ttu-id="c7e53-123">Nur interne Teilnehmer können Referenten sein.</span><span class="sxs-lookup"><span data-stu-id="c7e53-123">Only internal participants can be presenters.</span></span>  <br/> |
|<span data-ttu-id="c7e53-124">Alle</span><span class="sxs-lookup"><span data-stu-id="c7e53-124">Everyone</span></span>  <br/> |<span data-ttu-id="c7e53-125">Jeder Teilnehmer kann ein Referent sein.</span><span class="sxs-lookup"><span data-stu-id="c7e53-125">Any participant can be a presenter.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7e53-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7e53-126">Remarks</span></span>

<span data-ttu-id="c7e53-127">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c7e53-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c7e53-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c7e53-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c7e53-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c7e53-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7e53-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7e53-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c7e53-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c7e53-131">Schema name</span></span>  <br/> |<span data-ttu-id="c7e53-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c7e53-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="c7e53-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c7e53-133">Validation file</span></span>  <br/> |<span data-ttu-id="c7e53-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c7e53-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c7e53-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c7e53-135">Can be empty</span></span>  <br/> ||
   

