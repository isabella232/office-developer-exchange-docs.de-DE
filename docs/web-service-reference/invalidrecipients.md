---
title: InvalidRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InvalidRecipients
api_type:
- schema
ms.assetid: e4e7b50e-2fa9-4649-94a6-6002f341ecc4
description: Das InvalidRecipients -Element darstellt, die Empfänger eines Ordners Freigabeanfrage, die ungültig sind.
ms.openlocfilehash: 02ad8935bde347c563875bf5bfb31968b70d81b6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829966"
---
# <a name="invalidrecipients"></a><span data-ttu-id="4ad4d-103">InvalidRecipients</span><span class="sxs-lookup"><span data-stu-id="4ad4d-103">InvalidRecipients</span></span>

<span data-ttu-id="4ad4d-104">Das **InvalidRecipients** -Element darstellt, die Empfänger eines Ordners Freigabeanfrage, die ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="4ad4d-104">The **InvalidRecipients** element represents the recipients of a folder sharing request that are invalid.</span></span> 
  
```XML
<InvalidRecipients>
   <InvalidRecipient/>
</InvalidRecipients>
```

 <span data-ttu-id="4ad4d-105">**ArrayOfInvalidRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="4ad4d-105">**ArrayOfInvalidRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4ad4d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4ad4d-106">Attributes and elements</span></span>

<span data-ttu-id="4ad4d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4ad4d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ad4d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4ad4d-108">Attributes</span></span>

<span data-ttu-id="4ad4d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4ad4d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4ad4d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ad4d-110">Child elements</span></span>

|<span data-ttu-id="4ad4d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4ad4d-111">**Element**</span></span>|<span data-ttu-id="4ad4d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ad4d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ad4d-113">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="4ad4d-113">InvalidRecipient</span></span>](invalidrecipient.md) <br/> |<span data-ttu-id="4ad4d-114">Enthält die SMTP-Adresse des ungültige Empfänger und Informationen dazu, warum der Empfänger ungültig.</span><span class="sxs-lookup"><span data-stu-id="4ad4d-114">Contains the SMTP address of the invalid recipient and information about why the recipient is invalid.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4ad4d-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ad4d-115">Parent elements</span></span>

|<span data-ttu-id="4ad4d-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="4ad4d-116">**Element**</span></span>|<span data-ttu-id="4ad4d-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ad4d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ad4d-118">GetSharingMetadataResponse</span><span class="sxs-lookup"><span data-stu-id="4ad4d-118">GetSharingMetadataResponse</span></span>](getsharingmetadataresponse.md) <br/> |<span data-ttu-id="4ad4d-119">Definiert eine Antwort auf eine [GetSharingMetadata-Vorgang](getsharingmetadata-operation.md) an.</span><span class="sxs-lookup"><span data-stu-id="4ad4d-119">Defines a response to a [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="4ad4d-120">GetSharingMetadataResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4ad4d-120">GetSharingMetadataResponseMessage</span></span>](getsharingmetadataresponsemessage.md) <br/> |<span data-ttu-id="4ad4d-121">Enthält den Status und das Ergebnis einer einzelnen [GetSharingMetadata-Vorgang](getsharingmetadata-operation.md) -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4ad4d-121">Contains the status and result of a single [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ad4d-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4ad4d-122">Remarks</span></span>

<span data-ttu-id="4ad4d-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4ad4d-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4ad4d-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4ad4d-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ad4d-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ad4d-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4ad4d-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4ad4d-126">Schema Name</span></span>  <br/> |<span data-ttu-id="4ad4d-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4ad4d-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4ad4d-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4ad4d-128">Validation File</span></span>  <br/> |<span data-ttu-id="4ad4d-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4ad4d-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4ad4d-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4ad4d-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="4ad4d-131">False</span><span class="sxs-lookup"><span data-stu-id="4ad4d-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4ad4d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ad4d-132">See also</span></span>



[<span data-ttu-id="4ad4d-133">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4ad4d-133">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="4ad4d-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4ad4d-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

