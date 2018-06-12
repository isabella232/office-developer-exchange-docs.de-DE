---
title: GetAppManifestsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 86cf88f4-09c4-436a-a100-ac5cba0c4388
description: Das GetAppManifestsResponse-Element definiert die Antwort auf die Anforderung einer GetAppManifests Vorgang.
ms.openlocfilehash: b5eac7c06c39c0ed80a362080db6b0cb37f8f4ca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758572"
---
# <a name="getappmanifestsresponse"></a><span data-ttu-id="8bbcf-103">GetAppManifestsResponse</span><span class="sxs-lookup"><span data-stu-id="8bbcf-103">GetAppManifestsResponse</span></span>

<span data-ttu-id="8bbcf-104">Das **GetAppManifestsResponse** -Element definiert die Antwort auf die Anforderung einer **GetAppManifests** Vorgang.</span><span class="sxs-lookup"><span data-stu-id="8bbcf-104">The **GetAppManifestsResponse** element defines the response for a **GetAppManifests** operation request.</span></span> 
  
```XML
<GetAppManifestsResponse>
    <ResponseCode/>
    <Manifests/>
</GetAppManifestsResponse>
```

 <span data-ttu-id="8bbcf-105">**GetAppManifestsResponseType**</span><span class="sxs-lookup"><span data-stu-id="8bbcf-105">**GetAppManifestsResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8bbcf-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8bbcf-106">Attributes and elements</span></span>

<span data-ttu-id="8bbcf-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8bbcf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8bbcf-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8bbcf-108">Attributes</span></span>

<span data-ttu-id="8bbcf-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8bbcf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8bbcf-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8bbcf-110">Child elements</span></span>

<span data-ttu-id="8bbcf-111">[ResponseCode](responsecode.md) | [-Manifeste](manifests.md) | [Apps](apps.md)</span><span class="sxs-lookup"><span data-stu-id="8bbcf-111">[ResponseCode](responsecode.md) | [Manifests](manifests.md) | [Apps](apps.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8bbcf-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8bbcf-112">Parent elements</span></span>

<span data-ttu-id="8bbcf-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="8bbcf-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8bbcf-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8bbcf-114">Remarks</span></span>

<span data-ttu-id="8bbcf-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8bbcf-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8bbcf-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8bbcf-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8bbcf-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8bbcf-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8bbcf-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="8bbcf-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8bbcf-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8bbcf-119">Schema Name</span></span>  <br/> |<span data-ttu-id="8bbcf-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8bbcf-120">Message schema</span></span>  <br/> |
|<span data-ttu-id="8bbcf-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8bbcf-121">Validation File</span></span>  <br/> |<span data-ttu-id="8bbcf-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8bbcf-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8bbcf-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8bbcf-123">Can Be Empty</span></span>  <br/> |<span data-ttu-id="8bbcf-124">False</span><span class="sxs-lookup"><span data-stu-id="8bbcf-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8bbcf-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bbcf-125">See also</span></span>



- [<span data-ttu-id="8bbcf-126">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8bbcf-126">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
