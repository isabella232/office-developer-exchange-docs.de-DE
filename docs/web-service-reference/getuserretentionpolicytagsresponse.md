---
title: GetUserRetentionPolicyTagsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 12ba4528-60e9-4c0a-a5b2-eed3a2cb1509
description: Das GetUserRetentionPolicyTagsResponse-Element enthält die Antwort auf eine GetRetentionPolicyTags an.
ms.openlocfilehash: a208bb466725c746a1a7fc60b999ecb1d76dd2d0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829699"
---
# <a name="getuserretentionpolicytagsresponse"></a><span data-ttu-id="5ffa2-103">GetUserRetentionPolicyTagsResponse</span><span class="sxs-lookup"><span data-stu-id="5ffa2-103">GetUserRetentionPolicyTagsResponse</span></span>

<span data-ttu-id="5ffa2-104">Das [GetUserRetentionPolicyTagsResponse](getuserretentionpolicytagsresponse.md) -Element enthält die Antwort auf eine **GetRetentionPolicyTags** an.</span><span class="sxs-lookup"><span data-stu-id="5ffa2-104">The [GetUserRetentionPolicyTagsResponse](getuserretentionpolicytagsresponse.md) element contains the response to a **GetRetentionPolicyTags** request.</span></span> 
  
```XML
<GetUserRetentionPolicyTagsResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RetentionPolicyTags/>
</GetUserRetentionPolicyTagsResponse>
```

 <span data-ttu-id="5ffa2-105">**GetUserRetentionPolicyTagsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="5ffa2-105">**GetUserRetentionPolicyTagsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5ffa2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5ffa2-106">Attributes and elements</span></span>

<span data-ttu-id="5ffa2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5ffa2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5ffa2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5ffa2-108">Attributes</span></span>

<span data-ttu-id="5ffa2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5ffa2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5ffa2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5ffa2-110">Child elements</span></span>

<span data-ttu-id="5ffa2-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [RetentionPolicyTags](retentionpolicytags.md)</span><span class="sxs-lookup"><span data-stu-id="5ffa2-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [RetentionPolicyTags](retentionpolicytags.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5ffa2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5ffa2-112">Parent elements</span></span>

<span data-ttu-id="5ffa2-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="5ffa2-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ffa2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5ffa2-114">Remarks</span></span>

<span data-ttu-id="5ffa2-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5ffa2-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5ffa2-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="5ffa2-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5ffa2-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5ffa2-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5ffa2-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ffa2-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5ffa2-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5ffa2-119">Schema name</span></span>  <br/> |<span data-ttu-id="5ffa2-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="5ffa2-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5ffa2-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5ffa2-121">Validation file</span></span>  <br/> |<span data-ttu-id="5ffa2-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5ffa2-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5ffa2-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="5ffa2-123">Can be empty</span></span>  <br/> |<span data-ttu-id="5ffa2-124">false</span><span class="sxs-lookup"><span data-stu-id="5ffa2-124">false</span></span>  <br/> |
   
