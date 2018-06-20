---
title: IsEncrypted
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsEncrypted
api_type:
- schema
ms.assetid: 68a30e92-c2b1-4af5-bb16-ba38afb80c43
description: Das IsEncrypted-Element gibt an, ob eingehende Nachrichten S/MIME verschlüsselt in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.
ms.openlocfilehash: 582a1f197d4ee6b60af91b1a178d79163b50052c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830003"
---
# <a name="isencrypted"></a><span data-ttu-id="c2892-103">IsEncrypted</span><span class="sxs-lookup"><span data-stu-id="c2892-103">IsEncrypted</span></span>

<span data-ttu-id="c2892-104">Das **IsEncrypted** -Element gibt an, ob eingehende Nachrichten S/MIME verschlüsselt in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c2892-104">The **IsEncrypted** element indicates whether incoming messages must be S/MIME encrypted in order for the condition or exception to apply.</span></span> 
  
```XML
<IsEncrypted>true | false</IsEncrypted>
```

 <span data-ttu-id="c2892-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c2892-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c2892-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c2892-106">Attributes and elements</span></span>

<span data-ttu-id="c2892-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c2892-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c2892-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c2892-108">Attributes</span></span>

<span data-ttu-id="c2892-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c2892-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c2892-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c2892-110">Child elements</span></span>

<span data-ttu-id="c2892-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c2892-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c2892-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c2892-112">Parent elements</span></span>

|<span data-ttu-id="c2892-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c2892-113">**Element**</span></span>|<span data-ttu-id="c2892-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c2892-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c2892-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="c2892-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="c2892-116">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="c2892-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="c2892-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="c2892-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="c2892-118">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel an.</span><span class="sxs-lookup"><span data-stu-id="c2892-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c2892-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="c2892-119">Text value</span></span>

<span data-ttu-id="c2892-120">Der Textwert **true** gibt an, dass die Nachricht S/MIME verschlüsselt in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="c2892-120">A text value of **true** indicates that the message must be S/MIME encrypted in order for the condition or exception to apply.</span></span> <span data-ttu-id="c2892-121">Der Wert **false** gibt an, dass die Nachricht nicht S/MIME in Reihenfolge für die Bedingung oder Ausnahme angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2892-121">A value of **false** indicates that the message does not have to be S/MIME in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c2892-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c2892-122">Remarks</span></span>

<span data-ttu-id="c2892-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c2892-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c2892-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c2892-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2892-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2892-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c2892-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c2892-126">Schema Name</span></span>  <br/> |<span data-ttu-id="c2892-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c2892-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c2892-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c2892-128">Validation File</span></span>  <br/> |<span data-ttu-id="c2892-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c2892-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c2892-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c2892-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="c2892-131">True</span><span class="sxs-lookup"><span data-stu-id="c2892-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c2892-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2892-132">See also</span></span>



- [<span data-ttu-id="c2892-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c2892-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

