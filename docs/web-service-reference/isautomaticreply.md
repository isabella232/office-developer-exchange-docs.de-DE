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
description: Das IsAutomaticReply-Element gibt an, ob eingehende Nachrichten automatisch beantwortet werden müssen, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 7521dbbb458cf7683b52b2fe4fddacd276b40256
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455562"
---
# <a name="isautomaticreply"></a><span data-ttu-id="3b239-103">IsAutomaticReply</span><span class="sxs-lookup"><span data-stu-id="3b239-103">IsAutomaticReply</span></span>

<span data-ttu-id="3b239-104">Das **IsAutomaticReply** -Element gibt an, ob eingehende Nachrichten automatisch beantwortet werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="3b239-104">The **IsAutomaticReply** element indicates whether incoming messages must be automatic replies in order for the condition or exception to apply.</span></span> 
  
```XML
<IsAutomaticReply> true | false</IsAutomaticReply>
```

 <span data-ttu-id="3b239-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="3b239-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3b239-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3b239-106">Attributes and elements</span></span>

<span data-ttu-id="3b239-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3b239-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b239-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3b239-108">Attributes</span></span>

<span data-ttu-id="3b239-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3b239-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3b239-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b239-110">Child elements</span></span>

<span data-ttu-id="3b239-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3b239-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3b239-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b239-112">Parent elements</span></span>

|<span data-ttu-id="3b239-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3b239-113">**Element**</span></span>|<span data-ttu-id="3b239-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b239-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b239-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="3b239-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="3b239-116">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="3b239-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="3b239-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="3b239-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="3b239-118">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel dar.</span><span class="sxs-lookup"><span data-stu-id="3b239-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3b239-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="3b239-119">Text value</span></span>

<span data-ttu-id="3b239-120">Der Textwert **true** gibt an, dass die Nachricht eine automatische Antwort sein muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="3b239-120">A text value of **true** indicates that the message must be an automatic reply in order for the condition or exception to apply.</span></span> <span data-ttu-id="3b239-121">Der Wert **false** gibt an, dass die Nachricht keine automatische Antwort sein muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="3b239-121">A value of **false** indicates that the message does not have to be an automatic reply in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3b239-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b239-122">Remarks</span></span>

<span data-ttu-id="3b239-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3b239-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3b239-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3b239-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b239-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="3b239-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3b239-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3b239-126">Schema Name</span></span>  <br/> |<span data-ttu-id="3b239-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="3b239-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3b239-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3b239-128">Validation File</span></span>  <br/> |<span data-ttu-id="3b239-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3b239-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3b239-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3b239-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="3b239-131">True</span><span class="sxs-lookup"><span data-stu-id="3b239-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b239-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b239-132">See also</span></span>



- [<span data-ttu-id="3b239-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3b239-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

