---
title: IsAutomaticReply
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsAutomaticReply
api_type:
- schema
ms.assetid: 280e9baf-199d-422c-8fdf-1d0751a3e77d
description: Das IsAutomaticReply-Element gibt an, ob eingehende Nachrichten automatische Antworten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.
ms.openlocfilehash: 3f26b947313b8c53f70e2a89b9a6bdd17840a055
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829995"
---
# <a name="isautomaticreply"></a><span data-ttu-id="04c47-103">IsAutomaticReply</span><span class="sxs-lookup"><span data-stu-id="04c47-103">IsAutomaticReply</span></span>

<span data-ttu-id="04c47-104">Das **IsAutomaticReply** -Element gibt an, ob eingehende Nachrichten automatische Antworten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="04c47-104">The **IsAutomaticReply** element indicates whether incoming messages must be automatic replies in order for the condition or exception to apply.</span></span> 
  
```XML
<IsAutomaticReply> true | false</IsAutomaticReply>
```

 <span data-ttu-id="04c47-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="04c47-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="04c47-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="04c47-106">Attributes and elements</span></span>

<span data-ttu-id="04c47-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="04c47-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04c47-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="04c47-108">Attributes</span></span>

<span data-ttu-id="04c47-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="04c47-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="04c47-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="04c47-110">Child elements</span></span>

<span data-ttu-id="04c47-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="04c47-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="04c47-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="04c47-112">Parent elements</span></span>

|<span data-ttu-id="04c47-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="04c47-113">**Element**</span></span>|<span data-ttu-id="04c47-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="04c47-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="04c47-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="04c47-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="04c47-116">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="04c47-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="04c47-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="04c47-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="04c47-118">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel an.</span><span class="sxs-lookup"><span data-stu-id="04c47-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="04c47-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="04c47-119">Text value</span></span>

<span data-ttu-id="04c47-120">Der Textwert **true** gibt an, dass die Nachricht eine automatische Antwort in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="04c47-120">A text value of **true** indicates that the message must be an automatic reply in order for the condition or exception to apply.</span></span> <span data-ttu-id="04c47-121">Der Wert **false** gibt an, dass die Nachricht nicht vorhanden ist, um eine automatische Antwort in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="04c47-121">A value of **false** indicates that the message does not have to be an automatic reply in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="04c47-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="04c47-122">Remarks</span></span>

<span data-ttu-id="04c47-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="04c47-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="04c47-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="04c47-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04c47-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="04c47-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="04c47-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="04c47-126">Schema Name</span></span>  <br/> |<span data-ttu-id="04c47-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="04c47-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="04c47-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="04c47-128">Validation File</span></span>  <br/> |<span data-ttu-id="04c47-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="04c47-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="04c47-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="04c47-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="04c47-131">True</span><span class="sxs-lookup"><span data-stu-id="04c47-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="04c47-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04c47-132">See also</span></span>



- [<span data-ttu-id="04c47-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="04c47-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

