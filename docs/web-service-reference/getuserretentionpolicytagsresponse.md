---
title: GetUserRetentionPolicyTagsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 12ba4528-60e9-4c0a-a5b2-eed3a2cb1509
description: Das GetUserRetentionPolicyTagsResponse-Element enthält die Antwort auf eine GetRetentionPolicyTags-Anforderung.
ms.openlocfilehash: a8cfdc1aaaf47f3a66e541537381edf92bb024a9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530825"
---
# <a name="getuserretentionpolicytagsresponse"></a><span data-ttu-id="a298b-103">GetUserRetentionPolicyTagsResponse</span><span class="sxs-lookup"><span data-stu-id="a298b-103">GetUserRetentionPolicyTagsResponse</span></span>

<span data-ttu-id="a298b-104">Das [GetUserRetentionPolicyTagsResponse](getuserretentionpolicytagsresponse.md) -Element enthält die Antwort auf eine **GetRetentionPolicyTags** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a298b-104">The [GetUserRetentionPolicyTagsResponse](getuserretentionpolicytagsresponse.md) element contains the response to a **GetRetentionPolicyTags** request.</span></span> 
  
```XML
<GetUserRetentionPolicyTagsResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RetentionPolicyTags/>
</GetUserRetentionPolicyTagsResponse>
```

 <span data-ttu-id="a298b-105">**GetUserRetentionPolicyTagsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="a298b-105">**GetUserRetentionPolicyTagsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a298b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a298b-106">Attributes and elements</span></span>

<span data-ttu-id="a298b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a298b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a298b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a298b-108">Attributes</span></span>

<span data-ttu-id="a298b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a298b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a298b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a298b-110">Child elements</span></span>

<span data-ttu-id="a298b-111">[MessageText](messagetext.md)  |  [Response Code](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [Messagexml verwendet](messagexml.md)  |  [RetentionPolicyTags](retentionpolicytags.md)</span><span class="sxs-lookup"><span data-stu-id="a298b-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [RetentionPolicyTags](retentionpolicytags.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a298b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a298b-112">Parent elements</span></span>

<span data-ttu-id="a298b-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a298b-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a298b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a298b-114">Remarks</span></span>

<span data-ttu-id="a298b-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a298b-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a298b-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a298b-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a298b-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a298b-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a298b-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="a298b-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a298b-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a298b-119">Schema name</span></span>  <br/> |<span data-ttu-id="a298b-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a298b-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a298b-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a298b-121">Validation file</span></span>  <br/> |<span data-ttu-id="a298b-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a298b-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a298b-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a298b-123">Can be empty</span></span>  <br/> |<span data-ttu-id="a298b-124">False</span><span class="sxs-lookup"><span data-stu-id="a298b-124">false</span></span>  <br/> |
   

