---
title: NotSentToMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NotSentToMe
api_type:
- schema
ms.assetid: 7cb63269-622c-4198-9a21-f5a021bf6901
description: Das NotSentToMe-Element gibt an, ob der Besitzer des Postfachs nicht in der torecipients-Eigenschaft der eingehenden Nachrichten sein darf, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 58efe4381fe0c9f5bd0645a9eba471a13b5e4064
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462612"
---
# <a name="notsenttome"></a><span data-ttu-id="6e5a2-103">NotSentToMe</span><span class="sxs-lookup"><span data-stu-id="6e5a2-103">NotSentToMe</span></span>

<span data-ttu-id="6e5a2-104">Das **NotSentToMe** -Element gibt an, ob der Besitzer des Postfachs nicht in der **torecipients** -Eigenschaft der eingehenden Nachrichten sein darf, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="6e5a2-104">The **NotSentToMe** element indicates whether the owner of the mailbox must not be in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> 
  
```xml
<NotSentToMe>true | false</NotSentToMe>
```

 <span data-ttu-id="6e5a2-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="6e5a2-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6e5a2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6e5a2-106">Attributes and elements</span></span>

<span data-ttu-id="6e5a2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6e5a2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6e5a2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6e5a2-108">Attributes</span></span>

<span data-ttu-id="6e5a2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6e5a2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6e5a2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6e5a2-110">Child elements</span></span>

<span data-ttu-id="6e5a2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="6e5a2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6e5a2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6e5a2-112">Parent elements</span></span>

|<span data-ttu-id="6e5a2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6e5a2-113">**Element**</span></span>|<span data-ttu-id="6e5a2-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6e5a2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6e5a2-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="6e5a2-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="6e5a2-116">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="6e5a2-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="6e5a2-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="6e5a2-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="6e5a2-118">Stellt die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen.</span><span class="sxs-lookup"><span data-stu-id="6e5a2-118">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6e5a2-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="6e5a2-119">Text value</span></span>

<span data-ttu-id="6e5a2-120">Der Textwert **true** gibt an, dass der Besitzer des Postfachs nicht in der **torecipients** -Eigenschaft der eingehenden Nachrichten sein darf, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="6e5a2-120">A text value of **true** indicates that the owner of the mailbox must not be in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> <span data-ttu-id="6e5a2-121">Der Wert **false** gibt an, dass der Besitzer des Postfachs in der **torecipients** -Eigenschaft der eingehenden Nachricht sein muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="6e5a2-121">A value of **false** indicates that the owner of the mailbox must be in the **ToRecipients** property of the incoming message in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6e5a2-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e5a2-122">Remarks</span></span>

<span data-ttu-id="6e5a2-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6e5a2-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6e5a2-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6e5a2-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e5a2-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e5a2-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6e5a2-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6e5a2-126">Schema Name</span></span>  <br/> |<span data-ttu-id="6e5a2-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="6e5a2-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6e5a2-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6e5a2-128">Validation File</span></span>  <br/> |<span data-ttu-id="6e5a2-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6e5a2-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6e5a2-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6e5a2-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="6e5a2-131">True</span><span class="sxs-lookup"><span data-stu-id="6e5a2-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6e5a2-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e5a2-132">See also</span></span>



- [<span data-ttu-id="6e5a2-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6e5a2-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

