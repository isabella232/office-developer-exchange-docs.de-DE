---
title: ContainsSubjectStrings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContainsSubjectStrings
api_type:
- schema
ms.assetid: c6ec1d8d-8dd8-4c9a-a3e1-50e24958eb0d
description: Das ContainsSubjectStrings-Element gibt an, die Zeichenfolgen, die den Betreff der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende vorhanden sein müssen.
ms.openlocfilehash: a266855effaeb34aa232305db970f97c309a2e4c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757670"
---
# <a name="containssubjectstrings"></a><span data-ttu-id="42ad8-103">ContainsSubjectStrings</span><span class="sxs-lookup"><span data-stu-id="42ad8-103">ContainsSubjectStrings</span></span>

<span data-ttu-id="42ad8-104">Das **ContainsSubjectStrings** -Element gibt an, die Zeichenfolgen, die den Betreff der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende vorhanden sein müssen.</span><span class="sxs-lookup"><span data-stu-id="42ad8-104">The **ContainsSubjectStrings** element indicates the strings that must appear in the subject of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ContainsSubjectStrings>
    <String/>
</ContainsSubjectStrings>
```

 <span data-ttu-id="42ad8-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="42ad8-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="42ad8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="42ad8-106">Attributes and elements</span></span>

<span data-ttu-id="42ad8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="42ad8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="42ad8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="42ad8-108">Attributes</span></span>

<span data-ttu-id="42ad8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="42ad8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="42ad8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="42ad8-110">Child elements</span></span>

|<span data-ttu-id="42ad8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="42ad8-111">**Element**</span></span>|<span data-ttu-id="42ad8-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="42ad8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42ad8-113">String</span><span class="sxs-lookup"><span data-stu-id="42ad8-113">String</span></span>](string.md) <br/> |<span data-ttu-id="42ad8-114">Stellt eine Zeichenfolge, die den Betreff der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende vorhanden sein muss.</span><span class="sxs-lookup"><span data-stu-id="42ad8-114">Represents a string that must appear in the subject of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="42ad8-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="42ad8-115">Parent elements</span></span>

|<span data-ttu-id="42ad8-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="42ad8-116">**Element**</span></span>|<span data-ttu-id="42ad8-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="42ad8-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42ad8-118">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="42ad8-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="42ad8-119">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="42ad8-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="42ad8-120">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="42ad8-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="42ad8-121">Stellt die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen.</span><span class="sxs-lookup"><span data-stu-id="42ad8-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="42ad8-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="42ad8-122">Text value</span></span>

<span data-ttu-id="42ad8-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="42ad8-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="42ad8-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="42ad8-124">Remarks</span></span>

<span data-ttu-id="42ad8-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="42ad8-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="42ad8-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="42ad8-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="42ad8-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="42ad8-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="42ad8-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="42ad8-128">Schema Name</span></span>  <br/> |<span data-ttu-id="42ad8-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="42ad8-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="42ad8-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="42ad8-130">Validation File</span></span>  <br/> |<span data-ttu-id="42ad8-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="42ad8-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="42ad8-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="42ad8-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="42ad8-133">True</span><span class="sxs-lookup"><span data-stu-id="42ad8-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42ad8-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42ad8-134">See also</span></span>



- [<span data-ttu-id="42ad8-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="42ad8-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

