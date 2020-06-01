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
description: Das SentCcMe-Element gibt an, ob der Besitzer des Postfachs in der CcRecipients-Eigenschaft der eingehenden Nachrichten sein muss, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 1fae56a8e7d4e56c56884e5fff051ecd9f138a6d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465478"
---
# <a name="sentccme"></a><span data-ttu-id="fe5d7-103">SentCcMe</span><span class="sxs-lookup"><span data-stu-id="fe5d7-103">SentCcMe</span></span>

<span data-ttu-id="fe5d7-104">Das **SentCcMe** -Element gibt an, ob der Besitzer des Postfachs in der **CcRecipients** -Eigenschaft der eingehenden Nachrichten sein muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="fe5d7-104">The **SentCcMe** element indicates whether the owner of the mailbox has to be in the **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<SentCcMe>true | false</SentCcMe>
```

 <span data-ttu-id="fe5d7-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="fe5d7-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fe5d7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fe5d7-106">Attributes and elements</span></span>

<span data-ttu-id="fe5d7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fe5d7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fe5d7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fe5d7-108">Attributes</span></span>

<span data-ttu-id="fe5d7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="fe5d7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fe5d7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fe5d7-110">Child elements</span></span>

<span data-ttu-id="fe5d7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="fe5d7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fe5d7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fe5d7-112">Parent elements</span></span>

|<span data-ttu-id="fe5d7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fe5d7-113">**Element**</span></span>|<span data-ttu-id="fe5d7-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fe5d7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe5d7-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="fe5d7-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="fe5d7-116">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="fe5d7-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="fe5d7-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="fe5d7-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="fe5d7-118">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel dar.</span><span class="sxs-lookup"><span data-stu-id="fe5d7-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fe5d7-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="fe5d7-119">Text value</span></span>

<span data-ttu-id="fe5d7-120">Der Textwert **true** gibt an, dass der Besitzer des Postfachs in der **CcRecipients** -Eigenschaft der eingehenden Nachrichten sein muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="fe5d7-120">A text value of **true** indicates that the owner of the mailbox must be in the **CcRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> <span data-ttu-id="fe5d7-121">Der Wert **false** gibt an, dass der Besitzer des Postfachs nicht in der **CcRecipients** -Eigenschaft der eingehenden Nachrichten sein darf, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="fe5d7-121">A value of **false** indicates that the owner of the mailbox must not be in the **CcRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fe5d7-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe5d7-122">Remarks</span></span>

<span data-ttu-id="fe5d7-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fe5d7-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fe5d7-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fe5d7-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe5d7-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="fe5d7-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fe5d7-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fe5d7-126">Schema Name</span></span>  <br/> |<span data-ttu-id="fe5d7-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="fe5d7-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fe5d7-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fe5d7-128">Validation File</span></span>  <br/> |<span data-ttu-id="fe5d7-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="fe5d7-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fe5d7-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fe5d7-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="fe5d7-131">True</span><span class="sxs-lookup"><span data-stu-id="fe5d7-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fe5d7-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe5d7-132">See also</span></span>



- [<span data-ttu-id="fe5d7-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fe5d7-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

