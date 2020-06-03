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
description: Das GetMailTips-Element stellt die Empfänger und Typen von e-Mail-Tipps dar, die abgerufen werden sollen.
ms.openlocfilehash: 8ff71ed5d52f713e11188b07c8c93aeee7dfa44d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458635"
---
# <a name="getmailtips"></a><span data-ttu-id="1f660-103">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="1f660-103">GetMailTips</span></span>

<span data-ttu-id="1f660-104">Das **GetMailTips** -Element stellt die Empfänger und Typen von e-Mail-Tipps dar, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1f660-104">The **GetMailTips** element represents the recipients and types of mail tips to retrieve.</span></span> 
  
```XML
<GetMailTips>
   <SendingAs/>
   <Recipients/>
   <MailTipsRequested/>
</GetMailTips>
```

 <span data-ttu-id="1f660-105">**GetMailTipsType**</span><span class="sxs-lookup"><span data-stu-id="1f660-105">**GetMailTipsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1f660-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1f660-106">Attributes and elements</span></span>

<span data-ttu-id="1f660-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1f660-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f660-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1f660-108">Attributes</span></span>

<span data-ttu-id="1f660-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f660-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1f660-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f660-110">Child elements</span></span>

|<span data-ttu-id="1f660-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1f660-111">**Element**</span></span>|<span data-ttu-id="1f660-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1f660-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1f660-113">Absender</span><span class="sxs-lookup"><span data-stu-id="1f660-113">SendingAs</span></span>](sendingas.md) <br/> |<span data-ttu-id="1f660-114">Enthält eine e-Mail-Adresse, die ein Benutzer zu senden versucht.</span><span class="sxs-lookup"><span data-stu-id="1f660-114">Contains an e-mail address that a user is trying to send as.</span></span>  <br/> |
|[<span data-ttu-id="1f660-115">Recipients (ArrayOfRecipientsType)</span><span class="sxs-lookup"><span data-stu-id="1f660-115">Recipients (ArrayOfRecipientsType)</span></span>](recipients-arrayofrecipientstype.md) <br/> |<span data-ttu-id="1f660-116">Enthält eine Liste der Empfänger, die nach e-Mail-Tipps suchen.</span><span class="sxs-lookup"><span data-stu-id="1f660-116">Contains a list of recipients to check for mail tips.</span></span>  <br/> |
|[<span data-ttu-id="1f660-117">MailTipsRequested</span><span class="sxs-lookup"><span data-stu-id="1f660-117">MailTipsRequested</span></span>](mailtipsrequested.md) <br/> |<span data-ttu-id="1f660-118">Enthält die Typen von e-Mail-Tipps, die vom Dienst angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="1f660-118">Contains the types of mail tips requested from the service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1f660-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f660-119">Parent elements</span></span>

<span data-ttu-id="1f660-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f660-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="1f660-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="1f660-121">Text value</span></span>

<span data-ttu-id="1f660-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f660-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1f660-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f660-123">Remarks</span></span>

<span data-ttu-id="1f660-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1f660-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1f660-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1f660-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f660-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f660-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1f660-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1f660-127">Schema Name</span></span>  <br/> |<span data-ttu-id="1f660-128">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="1f660-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1f660-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1f660-129">Validation File</span></span>  <br/> |<span data-ttu-id="1f660-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="1f660-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1f660-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1f660-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="1f660-132">False</span><span class="sxs-lookup"><span data-stu-id="1f660-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1f660-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f660-133">See also</span></span>



- [<span data-ttu-id="1f660-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1f660-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

