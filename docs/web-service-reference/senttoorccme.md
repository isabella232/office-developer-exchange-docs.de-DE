---
title: SentToOrCcMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SentToOrCcMe
api_type:
- schema
ms.assetid: ca43e05d-df37-485b-9276-34678025f2b7
description: Das SentToOrCcMe-Element gibt an, ob der Besitzer des Postfachs entweder eine torecipients-oder eine CcRecipients-Eigenschaft eingehender Nachrichten sein muss, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 906e5d9fd405b9aa6f772bcedbd1869b5023a05e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462080"
---
# <a name="senttoorccme"></a><span data-ttu-id="d0c7c-103">SentToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="d0c7c-103">SentToOrCcMe</span></span>

<span data-ttu-id="d0c7c-104">Das **SentToOrCcMe** -Element gibt an, ob der Besitzer des Postfachs entweder eine **torecipients** -oder eine **CcRecipients** -Eigenschaft eingehender Nachrichten sein muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="d0c7c-104">The **SentToOrCcMe** element indicates whether the owner of the mailbox has to be in either a **ToRecipients** or **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<SentToOrCcMe>true | false</SentToOrCcMe>
```

 <span data-ttu-id="d0c7c-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="d0c7c-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0c7c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d0c7c-106">Attributes and elements</span></span>

<span data-ttu-id="d0c7c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d0c7c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0c7c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d0c7c-108">Attributes</span></span>

<span data-ttu-id="d0c7c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d0c7c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0c7c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0c7c-110">Child elements</span></span>

<span data-ttu-id="d0c7c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d0c7c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d0c7c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0c7c-112">Parent elements</span></span>

|<span data-ttu-id="d0c7c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d0c7c-113">**Element**</span></span>|<span data-ttu-id="d0c7c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d0c7c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0c7c-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="d0c7c-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="d0c7c-116">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="d0c7c-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="d0c7c-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="d0c7c-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="d0c7c-118">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel dar.</span><span class="sxs-lookup"><span data-stu-id="d0c7c-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d0c7c-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="d0c7c-119">Text value</span></span>

<span data-ttu-id="d0c7c-120">Der Textwert **true** gibt an, dass der Besitzer des Postfachs in der **torecipients** -oder der **CcRecipients** -Eigenschaft der eingehenden Nachrichten sein muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="d0c7c-120">A text value of **true** indicates that the owner of the mailbox must be in the **ToRecipients** or **CcRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> <span data-ttu-id="d0c7c-121">Der Wert **false** gibt an, dass der Besitzer des Postfachs nicht in der **torecipients** -oder der **CcRecipients** -Eigenschaft der eingehenden Nachrichten sein darf, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="d0c7c-121">A value of **false** indicates that the owner of the mailbox must not be in the **ToRecipients** or **CcRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d0c7c-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0c7c-122">Remarks</span></span>

<span data-ttu-id="d0c7c-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d0c7c-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0c7c-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d0c7c-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0c7c-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0c7c-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d0c7c-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d0c7c-126">Schema Name</span></span>  <br/> |<span data-ttu-id="d0c7c-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d0c7c-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d0c7c-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d0c7c-128">Validation File</span></span>  <br/> |<span data-ttu-id="d0c7c-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d0c7c-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d0c7c-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d0c7c-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="d0c7c-131">True</span><span class="sxs-lookup"><span data-stu-id="d0c7c-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0c7c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0c7c-132">See also</span></span>



- [<span data-ttu-id="d0c7c-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d0c7c-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

