---
title: RedirectToRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RedirectToRecipients
api_type:
- schema
ms.assetid: 00ef4a84-76d2-4669-b597-f52abbbc34f5
description: Das RedirectToRecipients -Element gibt an, die E-mail-Adressen, werden Nachrichten weitergeleitet werden.
ms.openlocfilehash: ebc0e0abe88d1e364dee94cc24313879458778d0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462192"
---
# <a name="redirecttorecipients"></a><span data-ttu-id="18579-103">RedirectToRecipients</span><span class="sxs-lookup"><span data-stu-id="18579-103">RedirectToRecipients</span></span>

<span data-ttu-id="18579-104">Das **RedirectToRecipients** -Element gibt an, die E-mail-Adressen, werden Nachrichten weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="18579-104">The **RedirectToRecipients** element indicates the e-mail addresses to which messages are to be redirected.</span></span> 
  
```XML
<RedirectToRecipients>
   <Address/>
</RedirectToRecipients>
```

 <span data-ttu-id="18579-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="18579-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="18579-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="18579-106">Attributes and elements</span></span>

<span data-ttu-id="18579-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="18579-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18579-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="18579-108">Attributes</span></span>

<span data-ttu-id="18579-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="18579-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="18579-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="18579-110">Child elements</span></span>

|<span data-ttu-id="18579-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="18579-111">**Element**</span></span>|<span data-ttu-id="18579-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18579-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18579-113">Adresse (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="18579-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="18579-114">Stellt eine vollständig aufgelöster E-mail-Adresse dar.</span><span class="sxs-lookup"><span data-stu-id="18579-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="18579-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="18579-115">Parent elements</span></span>

|<span data-ttu-id="18579-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="18579-116">**Element**</span></span>|<span data-ttu-id="18579-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18579-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18579-118">Aktionen</span><span class="sxs-lookup"><span data-stu-id="18579-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="18579-119">Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="18579-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="18579-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="18579-120">Text value</span></span>

<span data-ttu-id="18579-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="18579-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="18579-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18579-122">Remarks</span></span>

<span data-ttu-id="18579-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="18579-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18579-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="18579-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18579-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="18579-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="18579-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="18579-126">Schema Name</span></span>  <br/> |<span data-ttu-id="18579-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="18579-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="18579-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="18579-128">Validation File</span></span>  <br/> |<span data-ttu-id="18579-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="18579-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="18579-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="18579-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="18579-131">True</span><span class="sxs-lookup"><span data-stu-id="18579-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18579-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18579-132">See also</span></span>



- [<span data-ttu-id="18579-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="18579-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

