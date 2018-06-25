---
title: AttachmentIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttachmentIds
api_type:
- schema
ms.assetid: 46ce3ad7-4b20-43ae-8c63-39f1e3c2666b
description: Das AttachmentIds-Element enthält ein Array mit den IDs der Anlage.
ms.openlocfilehash: f205aefe6a7dc4ec208e8a96b8a6b47094aa741b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757396"
---
# <a name="attachmentids"></a><span data-ttu-id="7d5fc-103">AttachmentIds</span><span class="sxs-lookup"><span data-stu-id="7d5fc-103">AttachmentIds</span></span>

<span data-ttu-id="7d5fc-104">Das **AttachmentIds** -Element enthält ein Array mit den IDs der Anlage.</span><span class="sxs-lookup"><span data-stu-id="7d5fc-104">The **AttachmentIds** element contains an array of attachment identifiers.</span></span> 
  
```xml
<AttachmentIds>
   <AttachmentId Id=""/>
</AttachmentIds>
```

 <span data-ttu-id="7d5fc-105">**NonEmptyArrayOfRequestAttachmentIdsType**</span><span class="sxs-lookup"><span data-stu-id="7d5fc-105">**NonEmptyArrayOfRequestAttachmentIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7d5fc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7d5fc-106">Attributes and elements</span></span>

<span data-ttu-id="7d5fc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7d5fc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7d5fc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7d5fc-108">Attributes</span></span>

<span data-ttu-id="7d5fc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7d5fc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7d5fc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7d5fc-110">Child elements</span></span>

|<span data-ttu-id="7d5fc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7d5fc-111">**Element**</span></span>|<span data-ttu-id="7d5fc-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7d5fc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7d5fc-113">AttachmentId (GetAttachment und DeleteAttachment)</span><span class="sxs-lookup"><span data-stu-id="7d5fc-113">AttachmentId (GetAttachment and DeleteAttachment)</span></span>](attachmentid-getattachment-and-deleteattachment.md) <br/> |<span data-ttu-id="7d5fc-114">Das Element, das eine Anlage identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7d5fc-114">The element that identifies a single attachment.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7d5fc-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7d5fc-115">Parent elements</span></span>

|<span data-ttu-id="7d5fc-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="7d5fc-116">**Element**</span></span>|<span data-ttu-id="7d5fc-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7d5fc-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7d5fc-118">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="7d5fc-118">DeleteAttachment</span></span>](deleteattachment.md) <br/> |<span data-ttu-id="7d5fc-119">Das Element, das eine Anforderung zum Löschen einer Anlage aus dem Exchange-Speicher definiert.</span><span class="sxs-lookup"><span data-stu-id="7d5fc-119">The element that defines a request to delete an attachment from the Exchange store.</span></span>  <br/> <span data-ttu-id="7d5fc-120">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="7d5fc-120">The following is the XPath expression to this element:</span></span>  <br/>  `/DeleteAttachment` <br/> |
|[<span data-ttu-id="7d5fc-121">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="7d5fc-121">GetAttachment</span></span>](getattachment.md) <br/> |<span data-ttu-id="7d5fc-122">Das Element, das eine Anforderung an eine Anlage aus dem Exchange-Speicher abrufen definiert.</span><span class="sxs-lookup"><span data-stu-id="7d5fc-122">The element that defines a request to get an attachment from the Exchange store.</span></span>  <br/> <span data-ttu-id="7d5fc-123">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="7d5fc-123">The following is the XPath expression to this element:</span></span>  <br/>  `/GetAttachment` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d5fc-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7d5fc-124">Remarks</span></span>

<span data-ttu-id="7d5fc-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="7d5fc-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7d5fc-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7d5fc-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d5fc-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d5fc-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7d5fc-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7d5fc-128">Schema Name</span></span>  <br/> |<span data-ttu-id="7d5fc-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7d5fc-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7d5fc-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7d5fc-130">Validation File</span></span>  <br/> |<span data-ttu-id="7d5fc-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7d5fc-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7d5fc-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7d5fc-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="7d5fc-133">False</span><span class="sxs-lookup"><span data-stu-id="7d5fc-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d5fc-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d5fc-134">See also</span></span>

- [<span data-ttu-id="7d5fc-135">DeleteAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7d5fc-135">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
- [<span data-ttu-id="7d5fc-136">GetAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7d5fc-136">GetAttachment operation</span></span>](getattachment-operation.md)

