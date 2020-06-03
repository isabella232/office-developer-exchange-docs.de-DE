---
title: ArchiveItemResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 68109a92-c49e-4c0e-b6ec-e90d38d4be4d
description: Das ArchiveItemResponse-Element gibt die Antwort auf eine ArchiveItem-Anforderung an.
ms.openlocfilehash: 86360846a9a12955e7fa651d5b5027d90b5e56c0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463398"
---
# <a name="archiveitemresponse"></a><span data-ttu-id="73cbc-103">ArchiveItemResponse</span><span class="sxs-lookup"><span data-stu-id="73cbc-103">ArchiveItemResponse</span></span>

<span data-ttu-id="73cbc-104">Das **ArchiveItemResponse** -Element gibt die Antwort auf eine **ArchiveItem** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="73cbc-104">The **ArchiveItemResponse** element specifies the response to an **ArchiveItem** request.</span></span> 
  
```XML
<ArchiveItemResponse>
    <ResponseMessages></ResponseMessages>
</ArchiveItemResponse>
```

 <span data-ttu-id="73cbc-105">**ArchiveItemResponseType**</span><span class="sxs-lookup"><span data-stu-id="73cbc-105">**ArchiveItemResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="73cbc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="73cbc-106">Attributes and elements</span></span>

<span data-ttu-id="73cbc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="73cbc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73cbc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="73cbc-108">Attributes</span></span>

<span data-ttu-id="73cbc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="73cbc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="73cbc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="73cbc-110">Child elements</span></span>

|<span data-ttu-id="73cbc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="73cbc-111">**Element**</span></span>|<span data-ttu-id="73cbc-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73cbc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73cbc-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="73cbc-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="73cbc-114">Enthält die Antwortnachrichten an eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="73cbc-114">Contains the response messages to an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="73cbc-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="73cbc-115">Parent elements</span></span>

<span data-ttu-id="73cbc-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="73cbc-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="73cbc-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73cbc-117">Remarks</span></span>

<span data-ttu-id="73cbc-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="73cbc-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="73cbc-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="73cbc-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="73cbc-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="73cbc-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73cbc-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="73cbc-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="73cbc-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="73cbc-122">Schema Name</span></span>  <br/> |<span data-ttu-id="73cbc-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="73cbc-123">Message schema</span></span>  <br/> |
|<span data-ttu-id="73cbc-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="73cbc-124">Validation File</span></span>  <br/> |<span data-ttu-id="73cbc-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="73cbc-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="73cbc-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="73cbc-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="73cbc-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73cbc-127">See also</span></span>

- [<span data-ttu-id="73cbc-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="73cbc-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

