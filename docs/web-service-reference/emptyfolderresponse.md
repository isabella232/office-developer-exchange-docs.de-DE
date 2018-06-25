---
title: EmptyFolderResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c900be49-3c90-41aa-aba5-bcf1116ec2aa
description: Das EmptyFolderResponse-Element definiert eine Antwort auf eine Anforderung des EmptyFolder-Vorgang.
ms.openlocfilehash: ab753351a1eb7deba83823875989816ba75b9809
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758209"
---
# <a name="emptyfolderresponse"></a><span data-ttu-id="ede1b-103">EmptyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="ede1b-103">EmptyFolderResponse</span></span>

<span data-ttu-id="ede1b-104">Das **EmptyFolderResponse** -Element definiert eine Antwort auf eine Anforderung [EmptyFolder-Vorgang](emptyfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ede1b-104">The **EmptyFolderResponse** element defines a response to an [EmptyFolder operation](emptyfolder-operation.md) request.</span></span> 
  
```XML
<EmptyFolderResponse>
   <ResponseMessages/>
</EmptyFolderResponse>
```

 <span data-ttu-id="ede1b-105">**EmptyFolderResponseType**</span><span class="sxs-lookup"><span data-stu-id="ede1b-105">**EmptyFolderResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ede1b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ede1b-106">Attributes and elements</span></span>

<span data-ttu-id="ede1b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ede1b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ede1b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ede1b-108">Attributes</span></span>

<span data-ttu-id="ede1b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ede1b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ede1b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ede1b-110">Child elements</span></span>

|<span data-ttu-id="ede1b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ede1b-111">**Element**</span></span>|<span data-ttu-id="ede1b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ede1b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ede1b-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ede1b-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="ede1b-114">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ede1b-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ede1b-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ede1b-115">Parent elements</span></span>

<span data-ttu-id="ede1b-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="ede1b-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ede1b-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ede1b-117">Remarks</span></span>

<span data-ttu-id="ede1b-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ede1b-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ede1b-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ede1b-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ede1b-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="ede1b-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ede1b-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ede1b-121">Schema name</span></span>  <br/> |<span data-ttu-id="ede1b-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ede1b-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ede1b-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ede1b-123">Validation file</span></span>  <br/> |<span data-ttu-id="ede1b-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ede1b-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ede1b-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ede1b-125">Can be empty</span></span>  <br/> |<span data-ttu-id="ede1b-126">False</span><span class="sxs-lookup"><span data-stu-id="ede1b-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ede1b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ede1b-127">See also</span></span>



[<span data-ttu-id="ede1b-128">EmptyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ede1b-128">EmptyFolder operation</span></span>](emptyfolder-operation.md)
  
[<span data-ttu-id="ede1b-129">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="ede1b-129">EmptyFolder</span></span>](emptyfolder.md)


- [<span data-ttu-id="ede1b-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ede1b-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

