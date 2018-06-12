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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758527"
---
# <a name="forwardtorecipients"></a><span data-ttu-id="91c37-103">ForwardToRecipients</span><span class="sxs-lookup"><span data-stu-id="91c37-103">ForwardToRecipients</span></span>

<span data-ttu-id="91c37-104">Das **ForwardToRecipients** -Element gibt an, die E-mail-Adressen, werden Nachrichten weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="91c37-104">The **ForwardToRecipients** element indicates the e-mail addresses to which messages are to be forwarded.</span></span> 
  
```XML
<ForwardToRecipients>
   <Address/>
</ForwardToRecipients>
```

 <span data-ttu-id="91c37-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="91c37-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="91c37-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="91c37-106">Attributes and elements</span></span>

<span data-ttu-id="91c37-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="91c37-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91c37-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="91c37-108">Attributes</span></span>

<span data-ttu-id="91c37-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="91c37-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="91c37-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91c37-110">Child elements</span></span>

|<span data-ttu-id="91c37-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="91c37-111">**Element**</span></span>|<span data-ttu-id="91c37-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91c37-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91c37-113">Adresse (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="91c37-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="91c37-114">Stellt eine vollständig aufgelöster E-mail-Adresse dar.</span><span class="sxs-lookup"><span data-stu-id="91c37-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="91c37-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91c37-115">Parent elements</span></span>

|<span data-ttu-id="91c37-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="91c37-116">**Element**</span></span>|<span data-ttu-id="91c37-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91c37-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91c37-118">Aktionen</span><span class="sxs-lookup"><span data-stu-id="91c37-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="91c37-119">Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="91c37-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="91c37-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="91c37-120">Text value</span></span>

<span data-ttu-id="91c37-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="91c37-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="91c37-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="91c37-122">Remarks</span></span>

<span data-ttu-id="91c37-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="91c37-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="91c37-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="91c37-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91c37-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="91c37-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="91c37-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="91c37-126">Schema Name</span></span>  <br/> |<span data-ttu-id="91c37-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="91c37-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="91c37-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="91c37-128">Validation File</span></span>  <br/> |<span data-ttu-id="91c37-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="91c37-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="91c37-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="91c37-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="91c37-131">True</span><span class="sxs-lookup"><span data-stu-id="91c37-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91c37-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91c37-132">See also</span></span>



- [<span data-ttu-id="91c37-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="91c37-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

