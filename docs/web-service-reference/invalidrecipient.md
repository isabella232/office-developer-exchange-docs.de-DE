---
title: InvalidRecipient
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InvalidRecipient
api_type:
- schema
ms.assetid: 9e2d3433-22d7-444b-9883-e5649297d8fe
description: Das InvalidRecipient-Element enthält die SMTP-Adresse des ungültige Empfänger und Informationen dazu, warum der Empfänger ungültig.
ms.openlocfilehash: 800056666e486e9337dcd1c2786f7e6db1e060bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829961"
---
# <a name="invalidrecipient"></a><span data-ttu-id="6f8bd-103">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="6f8bd-103">InvalidRecipient</span></span>

<span data-ttu-id="6f8bd-104">Das **InvalidRecipient** -Element enthält die SMTP-Adresse des ungültige Empfänger und Informationen dazu, warum der Empfänger ungültig.</span><span class="sxs-lookup"><span data-stu-id="6f8bd-104">The **InvalidRecipient** element contains the SMTP address of the invalid recipient and information about why the recipient is invalid.</span></span> 
  
```XML
<InvalidRecipient>
   <SmtpAddress/>
   <ResponseCode/>
   <MessageText/>
</InvalidRecipient>

```

 <span data-ttu-id="6f8bd-105">**InvalidRecipientType**</span><span class="sxs-lookup"><span data-stu-id="6f8bd-105">**InvalidRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f8bd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6f8bd-106">Attributes and elements</span></span>

<span data-ttu-id="6f8bd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6f8bd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f8bd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6f8bd-108">Attributes</span></span>

<span data-ttu-id="6f8bd-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6f8bd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f8bd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6f8bd-110">Child elements</span></span>

|<span data-ttu-id="6f8bd-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6f8bd-111">**Element**</span></span>|<span data-ttu-id="6f8bd-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6f8bd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f8bd-113">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="6f8bd-113">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="6f8bd-114">Enthält die SMTP-Adresse des Empfängers ungültig.</span><span class="sxs-lookup"><span data-stu-id="6f8bd-114">Contains the SMTP address of the invalid recipient.</span></span> <span data-ttu-id="6f8bd-115">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6f8bd-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="6f8bd-116">ResponseCode (InvalidRecipientResponseCodeType)</span><span class="sxs-lookup"><span data-stu-id="6f8bd-116">ResponseCode (InvalidRecipientResponseCodeType)</span></span>](responsecode-invalidrecipientresponsecodetype.md) <br/> |<span data-ttu-id="6f8bd-117">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="6f8bd-117">Provides an error code that identifies the specific error that the request encountered.</span></span> <span data-ttu-id="6f8bd-118">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6f8bd-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="6f8bd-119">MessageText</span><span class="sxs-lookup"><span data-stu-id="6f8bd-119">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="6f8bd-120">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="6f8bd-120">Provides a text description of the status of the response.</span></span> <span data-ttu-id="6f8bd-121">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="6f8bd-121">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6f8bd-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6f8bd-122">Parent elements</span></span>

|<span data-ttu-id="6f8bd-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="6f8bd-123">**Element**</span></span>|<span data-ttu-id="6f8bd-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6f8bd-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f8bd-125">InvalidRecipients</span><span class="sxs-lookup"><span data-stu-id="6f8bd-125">InvalidRecipients</span></span>](invalidrecipients.md) <br/> |<span data-ttu-id="6f8bd-126">Stellt die Empfänger eines Ordners Freigabeanfrage, die ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="6f8bd-126">Represents the recipients of a folder sharing request that are invalid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f8bd-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6f8bd-127">Remarks</span></span>

<span data-ttu-id="6f8bd-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6f8bd-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f8bd-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6f8bd-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f8bd-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="6f8bd-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6f8bd-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6f8bd-131">Schema Name</span></span>  <br/> |<span data-ttu-id="6f8bd-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6f8bd-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="6f8bd-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6f8bd-133">Validation File</span></span>  <br/> |<span data-ttu-id="6f8bd-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6f8bd-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6f8bd-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6f8bd-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="6f8bd-136">False</span><span class="sxs-lookup"><span data-stu-id="6f8bd-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f8bd-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f8bd-137">See also</span></span>



[<span data-ttu-id="6f8bd-138">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6f8bd-138">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="6f8bd-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6f8bd-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

