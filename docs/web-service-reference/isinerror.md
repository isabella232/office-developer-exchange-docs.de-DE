---
title: IsInError
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsInError
api_type:
- schema
ms.assetid: f56e6c31-a566-4761-8755-d90ffe6fe790
description: Das IsInError-Element gibt an, ob sich die Regel in einem Fehlerzustand befindet.
ms.openlocfilehash: 9e642c9f89434bdcad97b0c16dc35f99196051d7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464217"
---
# <a name="isinerror"></a><span data-ttu-id="068ee-103">IsInError</span><span class="sxs-lookup"><span data-stu-id="068ee-103">IsInError</span></span>

<span data-ttu-id="068ee-104">Das **IsInError** -Element gibt an, ob sich die Regel in einem Fehlerzustand befindet.</span><span class="sxs-lookup"><span data-stu-id="068ee-104">The **IsInError** element indicates whether the rule is in an error condition.</span></span> 
  
```XML
<IsInError/>
```

 <span data-ttu-id="068ee-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="068ee-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="068ee-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="068ee-106">Attributes and elements</span></span>

<span data-ttu-id="068ee-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="068ee-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="068ee-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="068ee-108">Attributes</span></span>

<span data-ttu-id="068ee-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="068ee-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="068ee-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="068ee-110">Child elements</span></span>

<span data-ttu-id="068ee-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="068ee-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="068ee-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="068ee-112">Parent elements</span></span>

|<span data-ttu-id="068ee-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="068ee-113">**Element**</span></span>|<span data-ttu-id="068ee-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="068ee-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="068ee-115">Regel (RuleType)</span><span class="sxs-lookup"><span data-stu-id="068ee-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="068ee-116">Stellt eine Regel im Postfach des Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="068ee-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="068ee-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="068ee-117">Text value</span></span>

<span data-ttu-id="068ee-118">Der Textwert **true** gibt an, dass sich die Regel in einem Fehlerzustand befindet.</span><span class="sxs-lookup"><span data-stu-id="068ee-118">A text value of **true** indicates that the rule is in an error condition.</span></span> <span data-ttu-id="068ee-119">Der Wert **false** gibt an, dass sich die Regel nicht in einem Fehlerzustand befindet.</span><span class="sxs-lookup"><span data-stu-id="068ee-119">A value of **false** indicates that the rule is not in an error condition.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="068ee-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="068ee-120">Remarks</span></span>

<span data-ttu-id="068ee-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="068ee-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="068ee-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="068ee-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="068ee-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="068ee-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="068ee-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="068ee-124">Schema Name</span></span>  <br/> |<span data-ttu-id="068ee-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="068ee-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="068ee-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="068ee-126">Validation File</span></span>  <br/> |<span data-ttu-id="068ee-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="068ee-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="068ee-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="068ee-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="068ee-129">True</span><span class="sxs-lookup"><span data-stu-id="068ee-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="068ee-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="068ee-130">See also</span></span>



- [<span data-ttu-id="068ee-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="068ee-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

