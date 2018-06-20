---
title: GetMailTips
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetMailTips
api_type:
- schema
ms.assetid: 4a24ff79-f1ae-43a1-9ac2-49baf3eaa173
description: Das GetMailTips-Element darstellt, die Empfänger und die Typen der e-Mail-Infos abgerufen.
ms.openlocfilehash: aad3b3d9dd578d0c92bf7d48ee8b78b58c63e23d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758727"
---
# <a name="getmailtips"></a><span data-ttu-id="b76da-103">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="b76da-103">GetMailTips</span></span>

<span data-ttu-id="b76da-104">Das **GetMailTips** -Element darstellt, die Empfänger und die Typen der e-Mail-Infos abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b76da-104">The **GetMailTips** element represents the recipients and types of mail tips to retrieve.</span></span> 
  
```XML
<GetMailTips>
   <SendingAs/>
   <Recipients/>
   <MailTipsRequested/>
</GetMailTips>
```

 <span data-ttu-id="b76da-105">**GetMailTipsType**</span><span class="sxs-lookup"><span data-stu-id="b76da-105">**GetMailTipsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b76da-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b76da-106">Attributes and elements</span></span>

<span data-ttu-id="b76da-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b76da-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b76da-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b76da-108">Attributes</span></span>

<span data-ttu-id="b76da-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b76da-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b76da-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b76da-110">Child elements</span></span>

|<span data-ttu-id="b76da-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b76da-111">**Element**</span></span>|<span data-ttu-id="b76da-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b76da-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b76da-113">SendingAs</span><span class="sxs-lookup"><span data-stu-id="b76da-113">SendingAs</span></span>](sendingas.md) <br/> |<span data-ttu-id="b76da-114">Enthält eine e-Mail-Adresse, der ein Benutzer versucht, als zu senden.</span><span class="sxs-lookup"><span data-stu-id="b76da-114">Contains an e-mail address that a user is trying to send as.</span></span>  <br/> |
|[<span data-ttu-id="b76da-115">Empfänger (ArrayOfRecipientsType)</span><span class="sxs-lookup"><span data-stu-id="b76da-115">Recipients (ArrayOfRecipientsType)</span></span>](recipients-arrayofrecipientstype.md) <br/> |<span data-ttu-id="b76da-116">Enthält eine Liste von Empfängern für e-Mail-Infos zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b76da-116">Contains a list of recipients to check for mail tips.</span></span>  <br/> |
|[<span data-ttu-id="b76da-117">MailTipsRequested</span><span class="sxs-lookup"><span data-stu-id="b76da-117">MailTipsRequested</span></span>](mailtipsrequested.md) <br/> |<span data-ttu-id="b76da-118">Enthält die Typen von e-Mail-Infos aus dem Dienst angefordert.</span><span class="sxs-lookup"><span data-stu-id="b76da-118">Contains the types of mail tips requested from the service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b76da-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b76da-119">Parent elements</span></span>

<span data-ttu-id="b76da-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="b76da-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="b76da-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="b76da-121">Text value</span></span>

<span data-ttu-id="b76da-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="b76da-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b76da-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b76da-123">Remarks</span></span>

<span data-ttu-id="b76da-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b76da-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b76da-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b76da-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b76da-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="b76da-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b76da-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b76da-127">Schema Name</span></span>  <br/> |<span data-ttu-id="b76da-128">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b76da-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b76da-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b76da-129">Validation File</span></span>  <br/> |<span data-ttu-id="b76da-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b76da-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b76da-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b76da-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="b76da-132">False</span><span class="sxs-lookup"><span data-stu-id="b76da-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b76da-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b76da-133">See also</span></span>



- [<span data-ttu-id="b76da-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b76da-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

