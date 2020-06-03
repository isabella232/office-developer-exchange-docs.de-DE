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
description: Das Priority-Element gibt die Reihenfolge an, in der eine Regel ausgeführt werden soll.
ms.openlocfilehash: a5a894bba583618dd04430fc89f125c8920b0202
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462402"
---
# <a name="priority"></a><span data-ttu-id="1f56d-103">Priorität</span><span class="sxs-lookup"><span data-stu-id="1f56d-103">Priority</span></span>

<span data-ttu-id="1f56d-104">Das **Priority** -Element gibt die Reihenfolge an, in der eine Regel ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f56d-104">The **Priority** element indicates the order in which a rule is to be run.</span></span> 
  
```XML
<Priority/>
```

 <span data-ttu-id="1f56d-105">**int**</span><span class="sxs-lookup"><span data-stu-id="1f56d-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1f56d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1f56d-106">Attributes and elements</span></span>

<span data-ttu-id="1f56d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1f56d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f56d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1f56d-108">Attributes</span></span>

<span data-ttu-id="1f56d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f56d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1f56d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f56d-110">Child elements</span></span>

<span data-ttu-id="1f56d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f56d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1f56d-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f56d-112">Parent elements</span></span>

|<span data-ttu-id="1f56d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1f56d-113">**Element**</span></span>|<span data-ttu-id="1f56d-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1f56d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1f56d-115">Regel (RuleType)</span><span class="sxs-lookup"><span data-stu-id="1f56d-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="1f56d-116">Stellt eine Regel im Postfach des Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="1f56d-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1f56d-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="1f56d-117">Text value</span></span>

<span data-ttu-id="1f56d-118">Der Textwert für das **Priority** -Element ist eine ganze Zahl, die die Ausführungsreihenfolge angibt, in der eine Regel ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f56d-118">The text value for the **Priority** element is an integer that indicates the execution order in which a rule should be run.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1f56d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f56d-119">Remarks</span></span>

<span data-ttu-id="1f56d-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1f56d-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1f56d-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1f56d-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f56d-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f56d-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1f56d-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1f56d-123">Schema Name</span></span>  <br/> |<span data-ttu-id="1f56d-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="1f56d-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1f56d-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1f56d-125">Validation File</span></span>  <br/> |<span data-ttu-id="1f56d-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="1f56d-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1f56d-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1f56d-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="1f56d-128">False</span><span class="sxs-lookup"><span data-stu-id="1f56d-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1f56d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f56d-129">See also</span></span>



- [<span data-ttu-id="1f56d-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1f56d-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

