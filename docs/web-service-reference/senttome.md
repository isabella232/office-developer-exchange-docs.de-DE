---
title: SentToMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SentToMe
api_type:
- schema
ms.assetid: f18aecd1-ad33-41c3-b275-4ca648ce1da0
description: Das SentToMe-Element gibt an, ob der Besitzer des Postfachs in der torecipients-Eigenschaft der eingehenden Nachrichten sein muss, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 830125f03ad91a3e6f2beaf11e41be5e940ed48b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44439924"
---
# <a name="senttome"></a><span data-ttu-id="dd8d8-103">SentToMe</span><span class="sxs-lookup"><span data-stu-id="dd8d8-103">SentToMe</span></span>

<span data-ttu-id="dd8d8-104">Das **SentToMe** -Element gibt an, ob der Besitzer des Postfachs in der **torecipients** -Eigenschaft der eingehenden Nachrichten sein muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="dd8d8-104">The **SentToMe** element indicates whether the owner of the mailbox has to be in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<SentToMe>true | false</SentToMe>
```

 <span data-ttu-id="dd8d8-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="dd8d8-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dd8d8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dd8d8-106">Attributes and elements</span></span>

<span data-ttu-id="dd8d8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dd8d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dd8d8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dd8d8-108">Attributes</span></span>

<span data-ttu-id="dd8d8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="dd8d8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dd8d8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dd8d8-110">Child elements</span></span>

<span data-ttu-id="dd8d8-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="dd8d8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dd8d8-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dd8d8-112">Parent elements</span></span>

|<span data-ttu-id="dd8d8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd8d8-113">**Element**</span></span>|<span data-ttu-id="dd8d8-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd8d8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd8d8-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="dd8d8-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="dd8d8-116">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="dd8d8-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="dd8d8-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="dd8d8-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="dd8d8-118">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel dar.</span><span class="sxs-lookup"><span data-stu-id="dd8d8-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dd8d8-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="dd8d8-119">Text value</span></span>

<span data-ttu-id="dd8d8-120">Der Textwert **true** gibt an, dass der Besitzer des Postfachs in der **torecipients** -Eigenschaft der eingehenden Nachrichten sein muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="dd8d8-120">A text value of **true** indicates that the owner of the mailbox must be in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> <span data-ttu-id="dd8d8-121">Der Wert **false** gibt an, dass der Besitzer des Postfachs nicht in der **torecipients** -Eigenschaft der eingehenden Nachrichten sein darf, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="dd8d8-121">A value of **false** indicates that the owner of the mailbox must not be in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dd8d8-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd8d8-122">Remarks</span></span>

<span data-ttu-id="dd8d8-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="dd8d8-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dd8d8-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="dd8d8-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd8d8-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd8d8-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dd8d8-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dd8d8-126">Schema Name</span></span>  <br/> |<span data-ttu-id="dd8d8-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="dd8d8-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dd8d8-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dd8d8-128">Validation File</span></span>  <br/> |<span data-ttu-id="dd8d8-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="dd8d8-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dd8d8-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="dd8d8-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="dd8d8-131">True</span><span class="sxs-lookup"><span data-stu-id="dd8d8-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dd8d8-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd8d8-132">See also</span></span>



- [<span data-ttu-id="dd8d8-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="dd8d8-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

