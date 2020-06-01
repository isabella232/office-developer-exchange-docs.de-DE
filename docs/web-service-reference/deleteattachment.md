---
title: DeleteAttachment-
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteAttachment
api_type:
- schema
ms.assetid: 43d0c1cb-92ca-4399-9b3a-acb2b5c22624
description: Das DeleteAttachment--Element ist das Stammelement in einer Anforderung zum Löschen einer Anlage aus dem Exchange-Informationsspeicher.
ms.openlocfilehash: ae8dd5abc1dced2645e579a62f1f57a66cbc9877
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457347"
---
# <a name="deleteattachment"></a><span data-ttu-id="a5d0c-103">DeleteAttachment-</span><span class="sxs-lookup"><span data-stu-id="a5d0c-103">DeleteAttachment</span></span>

<span data-ttu-id="a5d0c-104">Das **DeleteAttachment-** -Element ist das Stammelement in einer Anforderung zum Löschen einer Anlage aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a5d0c-104">The **DeleteAttachment** element is the root element in a request to delete an attachment from the Exchange store.</span></span> 
  
```xml
<DeleteAttachment>
   <AttachmentIds/>
</DeleteAttachment>
```

<span data-ttu-id="a5d0c-105">**DeleteAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="a5d0c-105">**DeleteAttachmentType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a5d0c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a5d0c-106">Attributes and elements</span></span>

<span data-ttu-id="a5d0c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a5d0c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a5d0c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a5d0c-108">Attributes</span></span>

<span data-ttu-id="a5d0c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a5d0c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a5d0c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a5d0c-110">Child elements</span></span>

|<span data-ttu-id="a5d0c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a5d0c-111">**Element**</span></span>|<span data-ttu-id="a5d0c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a5d0c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a5d0c-113">AttachmentIds</span><span class="sxs-lookup"><span data-stu-id="a5d0c-113">AttachmentIds</span></span>](attachmentids.md) <br/> |<span data-ttu-id="a5d0c-114">Enthält ein Array von Anlagen Bezeichnern, die zum Löschen der Anlagen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5d0c-114">Contains an array of attachment identifiers that are used to delete the attachments.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a5d0c-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a5d0c-115">Parent elements</span></span>

<span data-ttu-id="a5d0c-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="a5d0c-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a5d0c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5d0c-117">Remarks</span></span>

<span data-ttu-id="a5d0c-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a5d0c-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a5d0c-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a5d0c-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a5d0c-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="a5d0c-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a5d0c-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a5d0c-121">Schema Name</span></span>  <br/> |<span data-ttu-id="a5d0c-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a5d0c-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a5d0c-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a5d0c-123">Validation File</span></span>  <br/> |<span data-ttu-id="a5d0c-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a5d0c-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a5d0c-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a5d0c-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="a5d0c-126">False</span><span class="sxs-lookup"><span data-stu-id="a5d0c-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a5d0c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5d0c-127">See also</span></span>

- [<span data-ttu-id="a5d0c-128">DeleteAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a5d0c-128">DeleteAttachment operation</span></span>](deleteattachment-operation.md)

