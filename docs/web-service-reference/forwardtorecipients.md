---
title: ForwardToRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ForwardToRecipients
api_type:
- schema
ms.assetid: dd58fd72-591d-4891-b226-465bcf12c19b
description: Das ForwardToRecipients -Element gibt an, die E-mail-Adressen, werden Nachrichten weitergeleitet werden.
ms.openlocfilehash: f2538f62bb9d837ef64bdc742b01d26d3d7d77f5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758527"
---
# <a name="forwardtorecipients"></a><span data-ttu-id="3dd06-103">ForwardToRecipients</span><span class="sxs-lookup"><span data-stu-id="3dd06-103">ForwardToRecipients</span></span>

<span data-ttu-id="3dd06-104">Das **ForwardToRecipients** -Element gibt an, die E-mail-Adressen, werden Nachrichten weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="3dd06-104">The **ForwardToRecipients** element indicates the e-mail addresses to which messages are to be forwarded.</span></span> 
  
```XML
<ForwardToRecipients>
   <Address/>
</ForwardToRecipients>
```

 <span data-ttu-id="3dd06-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="3dd06-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3dd06-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3dd06-106">Attributes and elements</span></span>

<span data-ttu-id="3dd06-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3dd06-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3dd06-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3dd06-108">Attributes</span></span>

<span data-ttu-id="3dd06-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3dd06-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3dd06-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3dd06-110">Child elements</span></span>

|<span data-ttu-id="3dd06-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3dd06-111">**Element**</span></span>|<span data-ttu-id="3dd06-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3dd06-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3dd06-113">Adresse (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="3dd06-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="3dd06-114">Stellt eine vollständig aufgelöster E-mail-Adresse dar.</span><span class="sxs-lookup"><span data-stu-id="3dd06-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3dd06-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3dd06-115">Parent elements</span></span>

|<span data-ttu-id="3dd06-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="3dd06-116">**Element**</span></span>|<span data-ttu-id="3dd06-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3dd06-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3dd06-118">Aktionen</span><span class="sxs-lookup"><span data-stu-id="3dd06-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="3dd06-119">Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="3dd06-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3dd06-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="3dd06-120">Text value</span></span>

<span data-ttu-id="3dd06-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="3dd06-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3dd06-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3dd06-122">Remarks</span></span>

<span data-ttu-id="3dd06-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3dd06-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3dd06-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3dd06-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3dd06-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="3dd06-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3dd06-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3dd06-126">Schema Name</span></span>  <br/> |<span data-ttu-id="3dd06-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="3dd06-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3dd06-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3dd06-128">Validation File</span></span>  <br/> |<span data-ttu-id="3dd06-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3dd06-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3dd06-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3dd06-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="3dd06-131">True</span><span class="sxs-lookup"><span data-stu-id="3dd06-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3dd06-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dd06-132">See also</span></span>



- [<span data-ttu-id="3dd06-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3dd06-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

