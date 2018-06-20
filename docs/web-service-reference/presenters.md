---
title: Referenten
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 01057872-4f1a-4246-86ba-73d10ef854a0
description: Das Referenten-Element gibt die Referenten für eine onlinebesprechung umwandeln.
ms.openlocfilehash: f62b458759e0d8199c98827602d6c3fe16aebeea
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830875"
---
# <a name="presenters"></a><span data-ttu-id="53066-103">Referenten</span><span class="sxs-lookup"><span data-stu-id="53066-103">Presenters</span></span>

<span data-ttu-id="53066-104">Das **Referenten** -Element gibt die Referenten für eine onlinebesprechung umwandeln.</span><span class="sxs-lookup"><span data-stu-id="53066-104">The **Presenters** element specifies the presenters for an online meeting.</span></span> 
  
```XML
<Presenters> Disabled | Internal | Everyone </Presenters>
```

 <span data-ttu-id="53066-105">**PresentersType**</span><span class="sxs-lookup"><span data-stu-id="53066-105">**PresentersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="53066-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="53066-106">Attributes and elements</span></span>

<span data-ttu-id="53066-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="53066-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53066-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="53066-108">Attributes</span></span>

<span data-ttu-id="53066-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="53066-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="53066-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53066-110">Child elements</span></span>

<span data-ttu-id="53066-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="53066-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="53066-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53066-112">Parent elements</span></span>

[<span data-ttu-id="53066-113">OnlineMeetingSettings</span><span class="sxs-lookup"><span data-stu-id="53066-113">OnlineMeetingSettings</span></span>](onlinemeetingsettings.md)
  
## <a name="text-value"></a><span data-ttu-id="53066-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="53066-114">Text value</span></span>

<span data-ttu-id="53066-115">Der Textwert der **Referenten** -Element ist der Typ der Benutzer, die für eine onlinebesprechung umwandeln Referent sein kann.</span><span class="sxs-lookup"><span data-stu-id="53066-115">The text value of **Presenters** element is the type of users that can be a presenter for an online meeting.</span></span> <span data-ttu-id="53066-116">In der folgenden Tabelle werden die Textwerte für das Element **Referenten** beschrieben.</span><span class="sxs-lookup"><span data-stu-id="53066-116">The text values for the **Presenters** element are described in the following table.</span></span> 
  
<span data-ttu-id="53066-117">**Text-Elementwerte Referenten**</span><span class="sxs-lookup"><span data-stu-id="53066-117">**Presenters element text values**</span></span>

|<span data-ttu-id="53066-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="53066-118">**Value**</span></span>|<span data-ttu-id="53066-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="53066-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53066-120">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="53066-120">Disabled</span></span>  <br/> |<span data-ttu-id="53066-121">Referenten sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="53066-121">Presenters are disabled.</span></span>  <br/> |
|<span data-ttu-id="53066-122">Interne</span><span class="sxs-lookup"><span data-stu-id="53066-122">Internal</span></span>  <br/> |<span data-ttu-id="53066-123">Nur interne Teilnehmer können als Referenten.</span><span class="sxs-lookup"><span data-stu-id="53066-123">Only internal participants can be presenters.</span></span>  <br/> |
|<span data-ttu-id="53066-124">Jeder</span><span class="sxs-lookup"><span data-stu-id="53066-124">Everyone</span></span>  <br/> |<span data-ttu-id="53066-125">Alle Teilnehmer kann als Referenten fungieren.</span><span class="sxs-lookup"><span data-stu-id="53066-125">Any participant can be a presenter.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53066-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="53066-126">Remarks</span></span>

<span data-ttu-id="53066-127">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="53066-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="53066-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="53066-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="53066-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="53066-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53066-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="53066-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="53066-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="53066-131">Schema name</span></span>  <br/> |<span data-ttu-id="53066-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="53066-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="53066-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="53066-133">Validation file</span></span>  <br/> |<span data-ttu-id="53066-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="53066-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="53066-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="53066-135">Can be empty</span></span>  <br/> ||
   

