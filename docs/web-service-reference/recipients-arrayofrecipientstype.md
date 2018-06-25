---
title: Empfänger (ArrayOfRecipientsType)
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
description: Das Empfänger-Element stellt eine Sammlung von Empfängern, die eine Kopie der Nachricht erhalten.
ms.openlocfilehash: b24a029bfacd6cc40e85a201b8ca90efd7790e9f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830991"
---
# <a name="recipients-arrayofrecipientstype"></a><span data-ttu-id="ba736-103">Empfänger (ArrayOfRecipientsType)</span><span class="sxs-lookup"><span data-stu-id="ba736-103">Recipients (ArrayOfRecipientsType)</span></span>

<span data-ttu-id="ba736-104">Das **Empfänger** -Element stellt eine Sammlung von Empfängern, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba736-104">The **Recipients** element represents a collection of recipients that receive a copy of the message.</span></span> 
  
```XML
<Recipients>
   <Mailbox/>
</Recipients>
```

 <span data-ttu-id="ba736-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="ba736-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba736-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ba736-106">Attributes and elements</span></span>

<span data-ttu-id="ba736-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ba736-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba736-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ba736-108">Attributes</span></span>

<span data-ttu-id="ba736-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ba736-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba736-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba736-110">Child elements</span></span>

|<span data-ttu-id="ba736-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba736-111">**Element**</span></span>|<span data-ttu-id="ba736-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba736-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba736-113">Postfach</span><span class="sxs-lookup"><span data-stu-id="ba736-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="ba736-114">Eine e-Mail-aktivierte Active Directory-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ba736-114">Identifies a mail-enabled Active Directory object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ba736-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba736-115">Parent elements</span></span>

|<span data-ttu-id="ba736-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba736-116">**Element**</span></span>|<span data-ttu-id="ba736-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba736-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba736-118">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="ba736-118">GetMailTips</span></span>](getmailtips.md) <br/> |<span data-ttu-id="ba736-119">Enthält die Empfänger und Typen von e-Mail-Infos abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ba736-119">Contains the recipients and types of mail tips to retrieve.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ba736-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="ba736-120">Text value</span></span>

<span data-ttu-id="ba736-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="ba736-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ba736-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ba736-122">Remarks</span></span>

<span data-ttu-id="ba736-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ba736-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba736-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ba736-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba736-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba736-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ba736-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ba736-126">Schema Name</span></span>  <br/> |<span data-ttu-id="ba736-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ba736-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="ba736-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ba736-128">Validation File</span></span>  <br/> |<span data-ttu-id="ba736-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ba736-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ba736-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ba736-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="ba736-131">False</span><span class="sxs-lookup"><span data-stu-id="ba736-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba736-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba736-132">See also</span></span>



- [<span data-ttu-id="ba736-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ba736-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

