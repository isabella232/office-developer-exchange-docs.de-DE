---
title: Recipients (ArrayOfRecipientsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Recipients
api_type:
- schema
ms.assetid: f4b71403-cbae-4176-8b2e-3597048c057b
description: Das Recipients-Element stellt eine Auflistung von Empfängern dar, die eine Kopie der Nachricht erhalten.
ms.openlocfilehash: 0e18152a8143b888ad27f48137c06613694f5713
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463874"
---
# <a name="recipients-arrayofrecipientstype"></a><span data-ttu-id="af1a0-103">Recipients (ArrayOfRecipientsType)</span><span class="sxs-lookup"><span data-stu-id="af1a0-103">Recipients (ArrayOfRecipientsType)</span></span>

<span data-ttu-id="af1a0-104">Das **Recipients** -Element stellt eine Auflistung von Empfängern dar, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="af1a0-104">The **Recipients** element represents a collection of recipients that receive a copy of the message.</span></span> 
  
```XML
<Recipients>
   <Mailbox/>
</Recipients>
```

 <span data-ttu-id="af1a0-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="af1a0-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="af1a0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="af1a0-106">Attributes and elements</span></span>

<span data-ttu-id="af1a0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="af1a0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af1a0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="af1a0-108">Attributes</span></span>

<span data-ttu-id="af1a0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="af1a0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="af1a0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="af1a0-110">Child elements</span></span>

|<span data-ttu-id="af1a0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="af1a0-111">**Element**</span></span>|<span data-ttu-id="af1a0-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="af1a0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af1a0-113">Postfach</span><span class="sxs-lookup"><span data-stu-id="af1a0-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="af1a0-114">Identifiziert ein e-Mail-aktiviertes Active Directory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="af1a0-114">Identifies a mail-enabled Active Directory object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="af1a0-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="af1a0-115">Parent elements</span></span>

|<span data-ttu-id="af1a0-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="af1a0-116">**Element**</span></span>|<span data-ttu-id="af1a0-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="af1a0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af1a0-118">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="af1a0-118">GetMailTips</span></span>](getmailtips.md) <br/> |<span data-ttu-id="af1a0-119">Enthält die Empfänger und Typen von e-Mail-Tipps, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="af1a0-119">Contains the recipients and types of mail tips to retrieve.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="af1a0-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="af1a0-120">Text value</span></span>

<span data-ttu-id="af1a0-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="af1a0-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="af1a0-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af1a0-122">Remarks</span></span>

<span data-ttu-id="af1a0-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="af1a0-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="af1a0-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="af1a0-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af1a0-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="af1a0-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="af1a0-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="af1a0-126">Schema Name</span></span>  <br/> |<span data-ttu-id="af1a0-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="af1a0-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="af1a0-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="af1a0-128">Validation File</span></span>  <br/> |<span data-ttu-id="af1a0-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="af1a0-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="af1a0-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="af1a0-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="af1a0-131">False</span><span class="sxs-lookup"><span data-stu-id="af1a0-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af1a0-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af1a0-132">See also</span></span>



- [<span data-ttu-id="af1a0-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="af1a0-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

