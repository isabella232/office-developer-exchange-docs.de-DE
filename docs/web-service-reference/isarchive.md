---
title: IsArchive
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b89d8a78-5c18-4547-aaf4-4b16a93190a7
description: Das IsArchive-Element gibt einen Boolean-Wert, der angibt, ob das Postfach ein Archivpostfach ist.
ms.openlocfilehash: 417afd1afc25e5872d1f511feff34494fe6b7b62
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829990"
---
# <a name="isarchive"></a><span data-ttu-id="a0387-103">IsArchive</span><span class="sxs-lookup"><span data-stu-id="a0387-103">IsArchive</span></span>

<span data-ttu-id="a0387-104">Das **IsArchive** -Element gibt einen Boolean-Wert, der angibt, ob das Postfach ein Archivpostfach ist.</span><span class="sxs-lookup"><span data-stu-id="a0387-104">The **IsArchive** element specifies a Boolean value that indicates whether the mailbox is an archive mailbox.</span></span> 
  
```XML
<IsArchive>true | false</IsArchive>
```

 <span data-ttu-id="a0387-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a0387-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a0387-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a0387-106">Attributes and elements</span></span>

<span data-ttu-id="a0387-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a0387-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a0387-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a0387-108">Attributes</span></span>

<span data-ttu-id="a0387-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a0387-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a0387-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a0387-110">Child elements</span></span>

<span data-ttu-id="a0387-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="a0387-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a0387-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a0387-112">Parent elements</span></span>

<span data-ttu-id="a0387-113">[FailedMailbox](failedmailbox.md) | [RetentionPolicyTag](retentionpolicytag.md)</span><span class="sxs-lookup"><span data-stu-id="a0387-113">[FailedMailbox](failedmailbox.md) | [RetentionPolicyTag](retentionpolicytag.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="a0387-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="a0387-114">Text value</span></span>

<span data-ttu-id="a0387-115">Der Textwert **true** für das Element **IsArchive** gibt an, dass das Zielpostfach ein Archivpostfach ist.</span><span class="sxs-lookup"><span data-stu-id="a0387-115">A text value of **true** for the **IsArchive** element indicates that the target mailbox is an archive mailbox.</span></span> <span data-ttu-id="a0387-116">Der Wert **false** gibt an, dass das Zielpostfach ein Archivpostfach nicht ist.</span><span class="sxs-lookup"><span data-stu-id="a0387-116">A value of **false** indicates that the target mailbox is not an archive mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a0387-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a0387-117">Remarks</span></span>

<span data-ttu-id="a0387-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a0387-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a0387-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a0387-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a0387-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a0387-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a0387-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="a0387-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a0387-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a0387-122">Schema Name</span></span>  <br/> |<span data-ttu-id="a0387-123">Typschema</span><span class="sxs-lookup"><span data-stu-id="a0387-123">Type schema</span></span>  <br/> |
|<span data-ttu-id="a0387-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a0387-124">Validation File</span></span>  <br/> |<span data-ttu-id="a0387-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a0387-125">types.xsd</span></span>  <br/> |
|<span data-ttu-id="a0387-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a0387-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="a0387-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0387-127">See also</span></span>



- [<span data-ttu-id="a0387-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a0387-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

