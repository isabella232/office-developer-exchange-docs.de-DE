---
title: DeleteAttachmentResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteAttachmentResponse
api_type:
- schema
ms.assetid: 24099a88-4ab6-4bf3-8ed5-efec8e07b9b9
description: Das DeleteAttachmentResponse definiert eine Antwort auf eine DeleteAttachment--Anforderung.
ms.openlocfilehash: 352318ef54687b0d1d4ce73b075248b79238d555
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457326"
---
# <a name="deleteattachmentresponse"></a><span data-ttu-id="a331a-103">DeleteAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="a331a-103">DeleteAttachmentResponse</span></span>

<span data-ttu-id="a331a-104">Das **DeleteAttachmentResponse** definiert eine Antwort auf eine DeleteAttachment--Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a331a-104">The **DeleteAttachmentResponse** defines a response to a DeleteAttachment request.</span></span> 
  
```xml
<DeleteAttachmentResponse>
   <ResponseMessages/>
</DeleteAttachmentResponse>
```

<span data-ttu-id="a331a-105">**DeleteAttachmentResponseType**</span><span class="sxs-lookup"><span data-stu-id="a331a-105">**DeleteAttachmentResponseType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a331a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a331a-106">Attributes and elements</span></span>

<span data-ttu-id="a331a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a331a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a331a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a331a-108">Attributes</span></span>

<span data-ttu-id="a331a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a331a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a331a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a331a-110">Child elements</span></span>

|<span data-ttu-id="a331a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a331a-111">**Element**</span></span>|<span data-ttu-id="a331a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a331a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a331a-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a331a-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="a331a-114">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a331a-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a331a-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a331a-115">Parent elements</span></span>

<span data-ttu-id="a331a-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="a331a-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a331a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a331a-117">Remarks</span></span>

<span data-ttu-id="a331a-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a331a-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a331a-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a331a-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a331a-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="a331a-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a331a-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a331a-121">Schema name</span></span>  <br/> |<span data-ttu-id="a331a-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a331a-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a331a-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a331a-123">Validation file</span></span>  <br/> |<span data-ttu-id="a331a-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a331a-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a331a-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a331a-125">Can be empty</span></span>  <br/> |<span data-ttu-id="a331a-126">False</span><span class="sxs-lookup"><span data-stu-id="a331a-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a331a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a331a-127">See also</span></span>

- [<span data-ttu-id="a331a-128">DeleteAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a331a-128">DeleteAttachment operation</span></span>](deleteattachment-operation.md)  
- [<span data-ttu-id="a331a-129">DeleteAttachment-</span><span class="sxs-lookup"><span data-stu-id="a331a-129">DeleteAttachment</span></span>](deleteattachment.md)
- [<span data-ttu-id="a331a-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a331a-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

