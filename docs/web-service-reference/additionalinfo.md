---
title: AdditionalInfo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 50bebbab-2fef-4a27-a5a9-32d7200820b6
description: Das AdditionalInfo-Element gibt zusätzliche Informationen zum Aufbewahrungs Status eines Postfachs an.
ms.openlocfilehash: 1911ff3ac0baf7a8854c0609e08959a54cc27b6d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455821"
---
# <a name="additionalinfo"></a><span data-ttu-id="50a63-103">AdditionalInfo</span><span class="sxs-lookup"><span data-stu-id="50a63-103">AdditionalInfo</span></span>

<span data-ttu-id="50a63-104">Das **AdditionalInfo** -Element gibt zusätzliche Informationen zum Aufbewahrungs Status eines Postfachs an.</span><span class="sxs-lookup"><span data-stu-id="50a63-104">The **AdditionalInfo** element specifies additional information about the hold status of a mailbox.</span></span> 
  
```XML
<AdditionalInfo></AdditionalInfo>
```

 <span data-ttu-id="50a63-105">**xs: Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50a63-105">**xs:string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="50a63-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="50a63-106">Attributes and elements</span></span>

<span data-ttu-id="50a63-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="50a63-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="50a63-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="50a63-108">Attributes</span></span>

<span data-ttu-id="50a63-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="50a63-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="50a63-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="50a63-110">Child elements</span></span>

<span data-ttu-id="50a63-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="50a63-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="50a63-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="50a63-112">Parent elements</span></span>

|<span data-ttu-id="50a63-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="50a63-113">**Element**</span></span>|<span data-ttu-id="50a63-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="50a63-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50a63-115">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="50a63-115">MailboxHoldStatus</span></span>](mailboxholdstatus.md) <br/> |<span data-ttu-id="50a63-116">Gibt den Aufbewahrungs Status des Postfachs an.</span><span class="sxs-lookup"><span data-stu-id="50a63-116">Specifies the hold status of the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="50a63-117">NonIndexableItemDetail</span><span class="sxs-lookup"><span data-stu-id="50a63-117">NonIndexableItemDetail</span></span>](nonindexableitemdetail.md) <br/> |<span data-ttu-id="50a63-118">Gibt Details für ein Element an, das nicht indiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="50a63-118">Specifies detail for an item that cannot be indexed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="50a63-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="50a63-119">Text value</span></span>

<span data-ttu-id="50a63-120">Der Textwert des AdditionalInfo-Elements ist zusätzliche Informationen zum Aufbewahrungs Status eines Postfachs.</span><span class="sxs-lookup"><span data-stu-id="50a63-120">The text value of the AdditionalInfo element is additional information about the hold status of a mailbox.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="50a63-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50a63-121">Remarks</span></span>

<span data-ttu-id="50a63-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="50a63-122">This element is optional.</span></span>
  
<span data-ttu-id="50a63-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="50a63-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="50a63-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="50a63-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="50a63-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="50a63-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50a63-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="50a63-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="50a63-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="50a63-127">Schema Name</span></span>  <br/> |<span data-ttu-id="50a63-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="50a63-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="50a63-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="50a63-129">Validation File</span></span>  <br/> |<span data-ttu-id="50a63-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="50a63-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="50a63-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="50a63-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="50a63-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50a63-132">See also</span></span>

- [<span data-ttu-id="50a63-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="50a63-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

