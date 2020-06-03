---
title: BccRecipient
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BccRecipient
api_type:
- schema
ms.assetid: 4ef0cff5-8a5a-4d76-9d2b-938774d8fc1b
description: Das BccRecipient-Element stellt einen Empfänger dar, der eine Blindkopie (BCC) einer e-Mail-Nachricht empfängt.
ms.openlocfilehash: 8296af1d74338bdfb1f4cb7bc7449ad91a9cd531
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461527"
---
# <a name="bccrecipient"></a><span data-ttu-id="d891f-103">BccRecipient</span><span class="sxs-lookup"><span data-stu-id="d891f-103">BccRecipient</span></span>

<span data-ttu-id="d891f-104">Das **BccRecipient** -Element stellt einen Empfänger dar, der eine Blindkopie (BCC) einer e-Mail-Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="d891f-104">The **BccRecipient** element represents a recipient to receive a blind carbon copy (Bcc) of an e-mail message.</span></span> 
  
```XML
<BccRecipient>true | false</BccRecipient>
```

 <span data-ttu-id="d891f-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="d891f-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d891f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d891f-106">Attributes and elements</span></span>

<span data-ttu-id="d891f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d891f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d891f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d891f-108">Attributes</span></span>

<span data-ttu-id="d891f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d891f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d891f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d891f-110">Child elements</span></span>

<span data-ttu-id="d891f-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d891f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d891f-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d891f-112">Parent elements</span></span>

|<span data-ttu-id="d891f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d891f-113">**Element**</span></span>|<span data-ttu-id="d891f-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d891f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d891f-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="d891f-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="d891f-116">Enthält Informationen zu einem einzelnen Ereignis für einen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="d891f-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d891f-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="d891f-117">Text value</span></span>

<span data-ttu-id="d891f-118">Dieses Element kann entweder **true** oder **false**sein.</span><span class="sxs-lookup"><span data-stu-id="d891f-118">This element can be either **true** or **false**.</span></span> <span data-ttu-id="d891f-119">Der Wert **true** gibt an, dass der Empfänger Blind Kohlenstoff kopiert ist; der Wert **false** gibt an, dass der Empfänger nicht Blind Carbon kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="d891f-119">A value of **true** indicates that the recipient is blind carbon copied; a value of **false** indicates that the recipient is not blind carbon copied.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d891f-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d891f-120">Remarks</span></span>

<span data-ttu-id="d891f-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d891f-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d891f-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d891f-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d891f-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="d891f-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d891f-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d891f-124">Schema Name</span></span>  <br/> |<span data-ttu-id="d891f-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d891f-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="d891f-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d891f-126">Validation File</span></span>  <br/> |<span data-ttu-id="d891f-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d891f-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d891f-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d891f-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="d891f-129">False</span><span class="sxs-lookup"><span data-stu-id="d891f-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d891f-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d891f-130">See also</span></span>



- [<span data-ttu-id="d891f-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d891f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

