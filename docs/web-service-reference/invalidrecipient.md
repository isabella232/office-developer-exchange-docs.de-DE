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
description: Das InvalidRecipient-Element enthält die SMTP-Adresse des ungültigen Empfängers sowie Informationen dazu, warum der Empfänger ungültig ist.
ms.openlocfilehash: f301b31c1054625151ce90e41fca5e3efc21f473
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526550"
---
# <a name="invalidrecipient"></a><span data-ttu-id="78e5e-103">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="78e5e-103">InvalidRecipient</span></span>

<span data-ttu-id="78e5e-104">Das **InvalidRecipient** -Element enthält die SMTP-Adresse des ungültigen Empfängers sowie Informationen dazu, warum der Empfänger ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="78e5e-104">The **InvalidRecipient** element contains the SMTP address of the invalid recipient and information about why the recipient is invalid.</span></span> 
  
```XML
<InvalidRecipient>
   <SmtpAddress/>
   <ResponseCode/>
   <MessageText/>
</InvalidRecipient>

```

 <span data-ttu-id="78e5e-105">**InvalidRecipientType**</span><span class="sxs-lookup"><span data-stu-id="78e5e-105">**InvalidRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="78e5e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="78e5e-106">Attributes and elements</span></span>

<span data-ttu-id="78e5e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="78e5e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="78e5e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="78e5e-108">Attributes</span></span>

<span data-ttu-id="78e5e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="78e5e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="78e5e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="78e5e-110">Child elements</span></span>

|<span data-ttu-id="78e5e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="78e5e-111">**Element**</span></span>|<span data-ttu-id="78e5e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78e5e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78e5e-113">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="78e5e-113">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="78e5e-114">Enthält die SMTP-Adresse des ungültigen Empfängers.</span><span class="sxs-lookup"><span data-stu-id="78e5e-114">Contains the SMTP address of the invalid recipient.</span></span> <span data-ttu-id="78e5e-115">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="78e5e-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="78e5e-116">Response Code (InvalidRecipientResponseCodeType)</span><span class="sxs-lookup"><span data-stu-id="78e5e-116">ResponseCode (InvalidRecipientResponseCodeType)</span></span>](responsecode-invalidrecipientresponsecodetype.md) <br/> |<span data-ttu-id="78e5e-117">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="78e5e-117">Provides an error code that identifies the specific error that the request encountered.</span></span> <span data-ttu-id="78e5e-118">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="78e5e-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="78e5e-119">MessageText</span><span class="sxs-lookup"><span data-stu-id="78e5e-119">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="78e5e-120">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="78e5e-120">Provides a text description of the status of the response.</span></span> <span data-ttu-id="78e5e-121">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="78e5e-121">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="78e5e-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="78e5e-122">Parent elements</span></span>

|<span data-ttu-id="78e5e-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="78e5e-123">**Element**</span></span>|<span data-ttu-id="78e5e-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78e5e-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78e5e-125">InvalidRecipients</span><span class="sxs-lookup"><span data-stu-id="78e5e-125">InvalidRecipients</span></span>](invalidrecipients.md) <br/> |<span data-ttu-id="78e5e-126">Stellt die Empfänger einer Anforderung für eine Ordnerfreigabe dar, die ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="78e5e-126">Represents the recipients of a folder sharing request that are invalid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78e5e-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78e5e-127">Remarks</span></span>

<span data-ttu-id="78e5e-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="78e5e-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="78e5e-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="78e5e-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78e5e-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="78e5e-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="78e5e-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="78e5e-131">Schema Name</span></span>  <br/> |<span data-ttu-id="78e5e-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="78e5e-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="78e5e-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="78e5e-133">Validation File</span></span>  <br/> |<span data-ttu-id="78e5e-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="78e5e-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="78e5e-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="78e5e-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="78e5e-136">False</span><span class="sxs-lookup"><span data-stu-id="78e5e-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78e5e-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78e5e-137">See also</span></span>



[<span data-ttu-id="78e5e-138">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="78e5e-138">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="78e5e-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="78e5e-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

