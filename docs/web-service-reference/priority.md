---
title: Priorität
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Priority
api_type:
- schema
ms.assetid: e1adb8b9-e3d5-469a-b188-822733d2503e
description: Element mit der Priorität Gibt die Reihenfolge an, in der ist eine Regel ausgeführt werden.
ms.openlocfilehash: 49e9bda063d8766ff49c8a2e9574c986bcfdbeb2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830888"
---
# <a name="priority"></a><span data-ttu-id="176a8-103">Priorität</span><span class="sxs-lookup"><span data-stu-id="176a8-103">Priority</span></span>

<span data-ttu-id="176a8-104">Element mit der **Priorität** gibt die Reihenfolge an, in der ist eine Regel ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="176a8-104">The **Priority** element indicates the order in which a rule is to be run.</span></span> 
  
```XML
<Priority/>
```

 <span data-ttu-id="176a8-105">**int**</span><span class="sxs-lookup"><span data-stu-id="176a8-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="176a8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="176a8-106">Attributes and elements</span></span>

<span data-ttu-id="176a8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="176a8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="176a8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="176a8-108">Attributes</span></span>

<span data-ttu-id="176a8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="176a8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="176a8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="176a8-110">Child elements</span></span>

<span data-ttu-id="176a8-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="176a8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="176a8-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="176a8-112">Parent elements</span></span>

|<span data-ttu-id="176a8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="176a8-113">**Element**</span></span>|<span data-ttu-id="176a8-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="176a8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="176a8-115">Regel (RuleType)</span><span class="sxs-lookup"><span data-stu-id="176a8-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="176a8-116">Stellt eine Regel in das Postfach des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="176a8-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="176a8-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="176a8-117">Text value</span></span>

<span data-ttu-id="176a8-118">Der Textwert für das Element der **Priorität** ist eine ganze Zahl, die die Reihenfolge der Ausführung gibt an, in der eine Regel ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="176a8-118">The text value for the **Priority** element is an integer that indicates the execution order in which a rule should be run.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="176a8-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="176a8-119">Remarks</span></span>

<span data-ttu-id="176a8-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="176a8-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="176a8-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="176a8-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="176a8-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="176a8-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="176a8-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="176a8-123">Schema Name</span></span>  <br/> |<span data-ttu-id="176a8-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="176a8-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="176a8-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="176a8-125">Validation File</span></span>  <br/> |<span data-ttu-id="176a8-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="176a8-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="176a8-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="176a8-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="176a8-128">False</span><span class="sxs-lookup"><span data-stu-id="176a8-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="176a8-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="176a8-129">See also</span></span>



- [<span data-ttu-id="176a8-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="176a8-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

