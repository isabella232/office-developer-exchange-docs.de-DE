---
title: IsArchive
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b89d8a78-5c18-4547-aaf4-4b16a93190a7
description: Das isarchive-Element gibt einen booleschen Wert an, der angibt, ob es sich bei dem Postfach um ein Archivpostfach handelt.
ms.openlocfilehash: 6d0be0eb283de3f4d8f786ff96f4a0d4f49e2009
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526515"
---
# <a name="isarchive"></a><span data-ttu-id="dce8c-103">IsArchive</span><span class="sxs-lookup"><span data-stu-id="dce8c-103">IsArchive</span></span>

<span data-ttu-id="dce8c-104">Das **isarchive** -Element gibt einen booleschen Wert an, der angibt, ob es sich bei dem Postfach um ein Archivpostfach handelt.</span><span class="sxs-lookup"><span data-stu-id="dce8c-104">The **IsArchive** element specifies a Boolean value that indicates whether the mailbox is an archive mailbox.</span></span> 
  
```XML
<IsArchive>true | false</IsArchive>
```

 <span data-ttu-id="dce8c-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="dce8c-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dce8c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dce8c-106">Attributes and elements</span></span>

<span data-ttu-id="dce8c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dce8c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dce8c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dce8c-108">Attributes</span></span>

<span data-ttu-id="dce8c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="dce8c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dce8c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dce8c-110">Child elements</span></span>

<span data-ttu-id="dce8c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="dce8c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dce8c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dce8c-112">Parent elements</span></span>

<span data-ttu-id="dce8c-113">[FailedMailbox](failedmailbox.md)  |  [RetentionPolicyTag](retentionpolicytag.md)</span><span class="sxs-lookup"><span data-stu-id="dce8c-113">[FailedMailbox](failedmailbox.md) | [RetentionPolicyTag](retentionpolicytag.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="dce8c-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="dce8c-114">Text value</span></span>

<span data-ttu-id="dce8c-115">Der Textwert **true** für das **isarchive** -Element gibt an, dass das Zielpostfach ein Archivpostfach ist.</span><span class="sxs-lookup"><span data-stu-id="dce8c-115">A text value of **true** for the **IsArchive** element indicates that the target mailbox is an archive mailbox.</span></span> <span data-ttu-id="dce8c-116">Der Wert **false** gibt an, dass das Zielpostfach kein Archivpostfach ist.</span><span class="sxs-lookup"><span data-stu-id="dce8c-116">A value of **false** indicates that the target mailbox is not an archive mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dce8c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dce8c-117">Remarks</span></span>

<span data-ttu-id="dce8c-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="dce8c-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dce8c-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="dce8c-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dce8c-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="dce8c-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dce8c-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="dce8c-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dce8c-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dce8c-122">Schema Name</span></span>  <br/> |<span data-ttu-id="dce8c-123">Typschema</span><span class="sxs-lookup"><span data-stu-id="dce8c-123">Type schema</span></span>  <br/> |
|<span data-ttu-id="dce8c-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dce8c-124">Validation File</span></span>  <br/> |<span data-ttu-id="dce8c-125">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="dce8c-125">types.xsd</span></span>  <br/> |
|<span data-ttu-id="dce8c-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="dce8c-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="dce8c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dce8c-127">See also</span></span>



- [<span data-ttu-id="dce8c-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="dce8c-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

