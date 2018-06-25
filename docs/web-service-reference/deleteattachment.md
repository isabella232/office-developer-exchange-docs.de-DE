---
title: DeleteAttachment
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
description: Das DeleteAttachment-Element ist das Stammelement im eine Anforderung an eine Anlage aus dem Exchange-Speicher zu löschen.
ms.openlocfilehash: 2beedd647febf025f6e3140ec37b196c9aeb7611
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757902"
---
# <a name="deleteattachment"></a><span data-ttu-id="a997e-103">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="a997e-103">DeleteAttachment</span></span>

<span data-ttu-id="a997e-104">Das **DeleteAttachment** -Element ist das Stammelement im eine Anforderung an eine Anlage aus dem Exchange-Speicher zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a997e-104">The **DeleteAttachment** element is the root element in a request to delete an attachment from the Exchange store.</span></span> 
  
```xml
<DeleteAttachment>
   <AttachmentIds/>
</DeleteAttachment>
```

<span data-ttu-id="a997e-105">**DeleteAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="a997e-105">**DeleteAttachmentType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a997e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a997e-106">Attributes and elements</span></span>

<span data-ttu-id="a997e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a997e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a997e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a997e-108">Attributes</span></span>

<span data-ttu-id="a997e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a997e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a997e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a997e-110">Child elements</span></span>

|<span data-ttu-id="a997e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a997e-111">**Element**</span></span>|<span data-ttu-id="a997e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a997e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a997e-113">AttachmentIds</span><span class="sxs-lookup"><span data-stu-id="a997e-113">AttachmentIds</span></span>](attachmentids.md) <br/> |<span data-ttu-id="a997e-114">Enthält ein Array mit Anlage Bezeichner, die verwendet werden, um die Anlagen löschen.</span><span class="sxs-lookup"><span data-stu-id="a997e-114">Contains an array of attachment identifiers that are used to delete the attachments.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a997e-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a997e-115">Parent elements</span></span>

<span data-ttu-id="a997e-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="a997e-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a997e-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a997e-117">Remarks</span></span>

<span data-ttu-id="a997e-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a997e-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a997e-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a997e-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a997e-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="a997e-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a997e-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a997e-121">Schema Name</span></span>  <br/> |<span data-ttu-id="a997e-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a997e-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a997e-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a997e-123">Validation File</span></span>  <br/> |<span data-ttu-id="a997e-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a997e-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a997e-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a997e-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="a997e-126">False</span><span class="sxs-lookup"><span data-stu-id="a997e-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a997e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a997e-127">See also</span></span>

- [<span data-ttu-id="a997e-128">DeleteAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a997e-128">DeleteAttachment operation</span></span>](deleteattachment-operation.md)

