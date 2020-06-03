---
title: ForwardAsAttachmentToRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ForwardAsAttachmentToRecipients
api_type:
- schema
ms.assetid: 8649ea14-672f-43c9-b10a-a2b02efd5867
description: Das ForwardAsAttachmentToRecipients -Element gibt an, die E-mail-Adressen, an die Nachrichten als Anlage weitergeleitet werden sollen.
ms.openlocfilehash: bf8c3563460eea811602074bf16f9253b4610832
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44453336"
---
# <a name="forwardasattachmenttorecipients"></a><span data-ttu-id="c97a6-103">ForwardAsAttachmentToRecipients</span><span class="sxs-lookup"><span data-stu-id="c97a6-103">ForwardAsAttachmentToRecipients</span></span>

<span data-ttu-id="c97a6-104">Das **ForwardAsAttachmentToRecipients** -Element gibt an, die E-mail-Adressen, an die Nachrichten als Anlage weitergeleitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c97a6-104">The **ForwardAsAttachmentToRecipients** element indicates the e-mail addresses to which messages are to be forwarded as attachments.</span></span> 
  
```XML
<ForwardAsAttachmentToRecipients>
   <Address/>
</ForwardAsAttachmentToRecipients>
```

 <span data-ttu-id="c97a6-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="c97a6-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c97a6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c97a6-106">Attributes and elements</span></span>

<span data-ttu-id="c97a6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c97a6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c97a6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c97a6-108">Attributes</span></span>

<span data-ttu-id="c97a6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c97a6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c97a6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c97a6-110">Child elements</span></span>

|<span data-ttu-id="c97a6-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c97a6-111">**Element**</span></span>|<span data-ttu-id="c97a6-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c97a6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c97a6-113">Adresse (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="c97a6-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="c97a6-114">Stellt eine vollständig aufgelöster E-mail-Adresse dar.</span><span class="sxs-lookup"><span data-stu-id="c97a6-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c97a6-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c97a6-115">Parent elements</span></span>

|<span data-ttu-id="c97a6-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c97a6-116">**Element**</span></span>|<span data-ttu-id="c97a6-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c97a6-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c97a6-118">Aktionen</span><span class="sxs-lookup"><span data-stu-id="c97a6-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="c97a6-119">Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="c97a6-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c97a6-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="c97a6-120">Text value</span></span>

<span data-ttu-id="c97a6-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="c97a6-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c97a6-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c97a6-122">Remarks</span></span>

<span data-ttu-id="c97a6-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c97a6-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c97a6-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c97a6-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c97a6-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="c97a6-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c97a6-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c97a6-126">Schema Name</span></span>  <br/> |<span data-ttu-id="c97a6-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c97a6-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c97a6-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c97a6-128">Validation File</span></span>  <br/> |<span data-ttu-id="c97a6-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c97a6-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c97a6-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c97a6-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="c97a6-131">True</span><span class="sxs-lookup"><span data-stu-id="c97a6-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c97a6-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c97a6-132">See also</span></span>



- [<span data-ttu-id="c97a6-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c97a6-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

