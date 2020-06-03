---
title: Bereich (NonEmptyStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Scope
api_type:
- schema
ms.assetid: 7efb6fd9-1615-469e-96f6-0f7846ad9b44
description: Das Scope-Element gibt den Bereich des Nachrichtenverfolgungsberichts an.
ms.openlocfilehash: f86f6198e84e094e61ee569f6d005549316bbb9b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466941"
---
# <a name="scope-nonemptystringtype"></a><span data-ttu-id="7906a-103">Bereich (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="7906a-103">Scope (NonEmptyStringType)</span></span>

<span data-ttu-id="7906a-104">Das **Scope** -Element gibt den Bereich des Nachrichtenverfolgungsberichts an.</span><span class="sxs-lookup"><span data-stu-id="7906a-104">The **Scope** element specifies the scope of the message tracking report.</span></span> 
  
```XML
<Scope>Organization | Forest | Site</Scope>
```

 <span data-ttu-id="7906a-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="7906a-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7906a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7906a-106">Attributes and elements</span></span>

<span data-ttu-id="7906a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7906a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7906a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7906a-108">Attributes</span></span>

<span data-ttu-id="7906a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7906a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7906a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7906a-110">Child elements</span></span>

<span data-ttu-id="7906a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="7906a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7906a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7906a-112">Parent elements</span></span>

<span data-ttu-id="7906a-113">[FindMessageTrackingReport](findmessagetrackingreport.md)  |  [GetMessageTrackingReport](getmessagetrackingreport.md)</span><span class="sxs-lookup"><span data-stu-id="7906a-113">[FindMessageTrackingReport](findmessagetrackingreport.md) | [GetMessageTrackingReport](getmessagetrackingreport.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="7906a-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="7906a-114">Text value</span></span>

<span data-ttu-id="7906a-115">In der folgenden Tabelle sind die möglichen Werte für das **Scope** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7906a-115">The following table lists the possible values for the **Scope** element.</span></span> 
  
|<span data-ttu-id="7906a-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7906a-116">**Value**</span></span>|<span data-ttu-id="7906a-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7906a-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7906a-118">Organisation</span><span class="sxs-lookup"><span data-stu-id="7906a-118">Organization</span></span>  <br/> |<span data-ttu-id="7906a-119">Die Nachrichten Verfolgungs Bereiche umfassen die gesamte Organisation.</span><span class="sxs-lookup"><span data-stu-id="7906a-119">The message tracking scopes spans across an organization.</span></span>  <br/> |
|<span data-ttu-id="7906a-120">Gesamtstruktur</span><span class="sxs-lookup"><span data-stu-id="7906a-120">Forest</span></span>  <br/> |<span data-ttu-id="7906a-121">Die Nachrichten Verfolgungs Bereiche umfassen über eine Gesamtstruktur hinweg.</span><span class="sxs-lookup"><span data-stu-id="7906a-121">The message tracking scopes spans across a forest.</span></span>  <br/> |
|<span data-ttu-id="7906a-122">Website</span><span class="sxs-lookup"><span data-stu-id="7906a-122">Site</span></span>  <br/> |<span data-ttu-id="7906a-123">Die Nachrichten Verfolgungs Bereiche umfassen über einen Standort hinweg.</span><span class="sxs-lookup"><span data-stu-id="7906a-123">The message tracking scopes spans across a site.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7906a-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7906a-124">Remarks</span></span>

<span data-ttu-id="7906a-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7906a-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7906a-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7906a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7906a-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="7906a-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7906a-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7906a-128">Schema Name</span></span>  <br/> |<span data-ttu-id="7906a-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7906a-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7906a-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7906a-130">Validation File</span></span>  <br/> |<span data-ttu-id="7906a-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7906a-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7906a-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7906a-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="7906a-133">False</span><span class="sxs-lookup"><span data-stu-id="7906a-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7906a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7906a-134">See also</span></span>



- [<span data-ttu-id="7906a-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7906a-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

