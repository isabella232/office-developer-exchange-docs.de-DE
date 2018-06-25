---
title: ArchiveItemResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 68109a92-c49e-4c0e-b6ec-e90d38d4be4d
description: Das ArchiveItemResponse-Element gibt die Antwort auf eine Anforderung ArchiveItem.
ms.openlocfilehash: bfd1b9d76c2b49e00a82bd8f6f57742007d0adf7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757373"
---
# <a name="archiveitemresponse"></a><span data-ttu-id="e74a8-103">ArchiveItemResponse</span><span class="sxs-lookup"><span data-stu-id="e74a8-103">ArchiveItemResponse</span></span>

<span data-ttu-id="e74a8-104">Das **ArchiveItemResponse** -Element gibt die Antwort auf eine Anforderung **ArchiveItem** .</span><span class="sxs-lookup"><span data-stu-id="e74a8-104">The **ArchiveItemResponse** element specifies the response to an **ArchiveItem** request.</span></span> 
  
```XML
<ArchiveItemResponse>
    <ResponseMessages></ResponseMessages>
</ArchiveItemResponse>
```

 <span data-ttu-id="e74a8-105">**ArchiveItemResponseType**</span><span class="sxs-lookup"><span data-stu-id="e74a8-105">**ArchiveItemResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e74a8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e74a8-106">Attributes and elements</span></span>

<span data-ttu-id="e74a8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e74a8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e74a8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e74a8-108">Attributes</span></span>

<span data-ttu-id="e74a8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e74a8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e74a8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e74a8-110">Child elements</span></span>

|<span data-ttu-id="e74a8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e74a8-111">**Element**</span></span>|<span data-ttu-id="e74a8-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e74a8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e74a8-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e74a8-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="e74a8-114">Enthält die Antwortnachrichten als auf eine Anforderung für die Exchange-Webdienste.</span><span class="sxs-lookup"><span data-stu-id="e74a8-114">Contains the response messages to an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e74a8-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e74a8-115">Parent elements</span></span>

<span data-ttu-id="e74a8-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="e74a8-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e74a8-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e74a8-117">Remarks</span></span>

<span data-ttu-id="e74a8-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e74a8-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e74a8-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e74a8-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e74a8-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e74a8-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e74a8-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="e74a8-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e74a8-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e74a8-122">Schema Name</span></span>  <br/> |<span data-ttu-id="e74a8-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="e74a8-123">Message schema</span></span>  <br/> |
|<span data-ttu-id="e74a8-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e74a8-124">Validation File</span></span>  <br/> |<span data-ttu-id="e74a8-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e74a8-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e74a8-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e74a8-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e74a8-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e74a8-127">See also</span></span>

- [<span data-ttu-id="e74a8-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e74a8-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

