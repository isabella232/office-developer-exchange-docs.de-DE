---
title: SentCcMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SentCcMe
api_type:
- schema
ms.assetid: bf5044e4-cbdf-4e24-a16f-b6454a51fcd5
description: Das SentCcMe-Element gibt an, ob der Besitzer des Postfachs in die CcRecipients-Eigenschaft des eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden.
ms.openlocfilehash: 634a83d477efbe8683255c4fab71e3f7f1ab2191
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831354"
---
# <a name="sentccme"></a><span data-ttu-id="58571-103">SentCcMe</span><span class="sxs-lookup"><span data-stu-id="58571-103">SentCcMe</span></span>

<span data-ttu-id="58571-104">Das **SentCcMe** -Element gibt an, ob der Besitzer des Postfachs in die **CcRecipients** -Eigenschaft des eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="58571-104">The **SentCcMe** element indicates whether the owner of the mailbox has to be in the **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<SentCcMe>true | false</SentCcMe>
```

 <span data-ttu-id="58571-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="58571-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="58571-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="58571-106">Attributes and elements</span></span>

<span data-ttu-id="58571-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="58571-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58571-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="58571-108">Attributes</span></span>

<span data-ttu-id="58571-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="58571-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="58571-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="58571-110">Child elements</span></span>

<span data-ttu-id="58571-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="58571-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="58571-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="58571-112">Parent elements</span></span>

|<span data-ttu-id="58571-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="58571-113">**Element**</span></span>|<span data-ttu-id="58571-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="58571-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58571-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="58571-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="58571-116">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="58571-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="58571-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="58571-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="58571-118">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel an.</span><span class="sxs-lookup"><span data-stu-id="58571-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="58571-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="58571-119">Text value</span></span>

<span data-ttu-id="58571-120">Der Textwert **true** gibt an, dass der Besitzer des Postfachs in der **CcRecipients** -Eigenschaft der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="58571-120">A text value of **true** indicates that the owner of the mailbox must be in the **CcRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> <span data-ttu-id="58571-121">Der Wert **false** gibt an, dass der Besitzer des Postfachs nicht in der **CcRecipients** -Eigenschaft der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="58571-121">A value of **false** indicates that the owner of the mailbox must not be in the **CcRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="58571-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="58571-122">Remarks</span></span>

<span data-ttu-id="58571-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="58571-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="58571-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="58571-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58571-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="58571-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="58571-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="58571-126">Schema Name</span></span>  <br/> |<span data-ttu-id="58571-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="58571-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="58571-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="58571-128">Validation File</span></span>  <br/> |<span data-ttu-id="58571-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="58571-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="58571-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="58571-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="58571-131">True</span><span class="sxs-lookup"><span data-stu-id="58571-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58571-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58571-132">See also</span></span>



- [<span data-ttu-id="58571-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="58571-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

