---
title: SendSMSAlertToRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendSMSAlertToRecipients
api_type:
- schema
ms.assetid: c4dd000b-11b6-4b7b-91e0-dbfeae11d770
description: Das SendSMSAlertToRecipients -Element gibt an, die Mobiltelefonnummer, die ist eine Warnung Short Message Service (SMS) gesendet werden.
ms.openlocfilehash: b28202c71257fccca67879713d5d7df03f69b06d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831347"
---
# <a name="sendsmsalerttorecipients"></a><span data-ttu-id="f2b56-103">SendSMSAlertToRecipients</span><span class="sxs-lookup"><span data-stu-id="f2b56-103">SendSMSAlertToRecipients</span></span>

<span data-ttu-id="f2b56-104">Das **SendSMSAlertToRecipients** -Element gibt an, die Mobiltelefonnummer, die ist eine Warnung Short Message Service (SMS) gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2b56-104">The **SendSMSAlertToRecipients** element indicates the mobile phone numbers to which a Short Message Service (SMS) alert is to be sent.</span></span> 
  
```XML
<SendSMSAlertToRecipients>
   <Address/>
</SendSMSAlertToRecipients>
```

 <span data-ttu-id="f2b56-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="f2b56-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f2b56-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f2b56-106">Attributes and elements</span></span>

<span data-ttu-id="f2b56-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f2b56-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2b56-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f2b56-108">Attributes</span></span>

<span data-ttu-id="f2b56-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f2b56-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f2b56-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f2b56-110">Child elements</span></span>

|<span data-ttu-id="f2b56-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f2b56-111">**Element**</span></span>|<span data-ttu-id="f2b56-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2b56-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2b56-113">Adresse (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="f2b56-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="f2b56-114">Stellt eine vollständig aufgelöster E-mail-Adresse dar.</span><span class="sxs-lookup"><span data-stu-id="f2b56-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f2b56-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f2b56-115">Parent elements</span></span>

|<span data-ttu-id="f2b56-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f2b56-116">**Element**</span></span>|<span data-ttu-id="f2b56-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2b56-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2b56-118">Aktionen</span><span class="sxs-lookup"><span data-stu-id="f2b56-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="f2b56-119">Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="f2b56-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f2b56-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="f2b56-120">Text value</span></span>

<span data-ttu-id="f2b56-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="f2b56-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f2b56-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f2b56-122">Remarks</span></span>

<span data-ttu-id="f2b56-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f2b56-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f2b56-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f2b56-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2b56-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2b56-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f2b56-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f2b56-126">Schema Name</span></span>  <br/> |<span data-ttu-id="f2b56-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f2b56-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f2b56-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f2b56-128">Validation File</span></span>  <br/> |<span data-ttu-id="f2b56-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f2b56-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f2b56-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f2b56-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="f2b56-131">True</span><span class="sxs-lookup"><span data-stu-id="f2b56-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2b56-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2b56-132">See also</span></span>



- [<span data-ttu-id="f2b56-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f2b56-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

