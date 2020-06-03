---
title: GetUserRetentionPolicyTagsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9991d6e0-8c31-4e73-8af3-da4298474b66
description: Das GetUserRetentionPolicyTagsResponseMessage-Element gibt die Antwortnachricht für eine GetUserRetentionPolicyTags-Anforderung an.
ms.openlocfilehash: e65266e72010f42a2052bbb8cfab21ea4059f92b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461807"
---
# <a name="getuserretentionpolicytagsresponsemessage"></a><span data-ttu-id="e7574-103">GetUserRetentionPolicyTagsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e7574-103">GetUserRetentionPolicyTagsResponseMessage</span></span>

<span data-ttu-id="e7574-104">Das **GetUserRetentionPolicyTagsResponseMessage** -Element gibt die Antwortnachricht für eine **GetUserRetentionPolicyTags** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="e7574-104">The **GetUserRetentionPolicyTagsResponseMessage** element specifies the response message for a **GetUserRetentionPolicyTags** request.</span></span> 
  
```XML
<GetUserRetentionPolicyTagsResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RetentionPolicyTags/>
</GetUserRetentionPolicyTagsResponseMessage>
```

 <span data-ttu-id="e7574-105">**GetUserRetentionPolicyTagsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e7574-105">**GetUserRetentionPolicyTagsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e7574-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e7574-106">Attributes and elements</span></span>

<span data-ttu-id="e7574-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e7574-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e7574-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e7574-108">Attributes</span></span>

<span data-ttu-id="e7574-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e7574-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e7574-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e7574-110">Child elements</span></span>

<span data-ttu-id="e7574-111">[MessageText](messagetext.md)  |  [Response Code](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [Messagexml verwendet](messagexml.md)  |  [RetentionPolicyTags](retentionpolicytags.md)</span><span class="sxs-lookup"><span data-stu-id="e7574-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [RetentionPolicyTags](retentionpolicytags.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e7574-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e7574-112">Parent elements</span></span>

[<span data-ttu-id="e7574-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e7574-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="e7574-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7574-114">Remarks</span></span>

<span data-ttu-id="e7574-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e7574-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e7574-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e7574-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e7574-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e7574-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7574-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="e7574-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e7574-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e7574-119">Schema name</span></span>  <br/> |<span data-ttu-id="e7574-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="e7574-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e7574-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e7574-121">Validation file</span></span>  <br/> |<span data-ttu-id="e7574-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e7574-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e7574-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e7574-123">Can be empty</span></span>  <br/> |<span data-ttu-id="e7574-124">False</span><span class="sxs-lookup"><span data-stu-id="e7574-124">false</span></span>  <br/> |
   

