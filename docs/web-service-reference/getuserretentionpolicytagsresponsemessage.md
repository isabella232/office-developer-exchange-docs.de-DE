---
title: GetUserRetentionPolicyTagsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9991d6e0-8c31-4e73-8af3-da4298474b66
description: Das GetUserRetentionPolicyTagsResponseMessage-Element gibt die Antwortnachricht für eine Anforderung GetUserRetentionPolicyTags.
ms.openlocfilehash: db73cb7f1922d845c9565753ff8d4917b82b1259
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829701"
---
# <a name="getuserretentionpolicytagsresponsemessage"></a><span data-ttu-id="80321-103">GetUserRetentionPolicyTagsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="80321-103">GetUserRetentionPolicyTagsResponseMessage</span></span>

<span data-ttu-id="80321-104">Das **GetUserRetentionPolicyTagsResponseMessage** -Element gibt die Antwortnachricht für eine Anforderung **GetUserRetentionPolicyTags** .</span><span class="sxs-lookup"><span data-stu-id="80321-104">The **GetUserRetentionPolicyTagsResponseMessage** element specifies the response message for a **GetUserRetentionPolicyTags** request.</span></span> 
  
```XML
<GetUserRetentionPolicyTagsResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RetentionPolicyTags/>
</GetUserRetentionPolicyTagsResponseMessage>
```

 <span data-ttu-id="80321-105">**GetUserRetentionPolicyTagsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="80321-105">**GetUserRetentionPolicyTagsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="80321-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="80321-106">Attributes and elements</span></span>

<span data-ttu-id="80321-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="80321-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80321-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="80321-108">Attributes</span></span>

<span data-ttu-id="80321-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="80321-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="80321-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="80321-110">Child elements</span></span>

<span data-ttu-id="80321-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [RetentionPolicyTags](retentionpolicytags.md)</span><span class="sxs-lookup"><span data-stu-id="80321-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [RetentionPolicyTags](retentionpolicytags.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="80321-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="80321-112">Parent elements</span></span>

[<span data-ttu-id="80321-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="80321-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="80321-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="80321-114">Remarks</span></span>

<span data-ttu-id="80321-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="80321-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="80321-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="80321-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="80321-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="80321-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80321-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="80321-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="80321-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="80321-119">Schema name</span></span>  <br/> |<span data-ttu-id="80321-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="80321-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="80321-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="80321-121">Validation file</span></span>  <br/> |<span data-ttu-id="80321-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="80321-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="80321-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="80321-123">Can be empty</span></span>  <br/> |<span data-ttu-id="80321-124">false</span><span class="sxs-lookup"><span data-stu-id="80321-124">false</span></span>  <br/> |
   

