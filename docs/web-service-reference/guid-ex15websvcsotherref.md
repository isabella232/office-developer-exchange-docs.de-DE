---
title: Guid
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 49dcf69f-bf8d-4be6-a24c-03bbd13f4fe5
description: Das GUID-Element gibt den global eindeutigen Bezeichner des Postfachs an.
ms.openlocfilehash: 4db66b5ae2c67f64f75c69a3d77cfa2b587775be
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530775"
---
# <a name="guid"></a><span data-ttu-id="02e50-103">Guid</span><span class="sxs-lookup"><span data-stu-id="02e50-103">Guid</span></span>

<span data-ttu-id="02e50-104">Das **GUID** -Element gibt den global eindeutigen Bezeichner des Postfachs an.</span><span class="sxs-lookup"><span data-stu-id="02e50-104">The **Guid** element specifies the globally unique identifier of the mailbox.</span></span> 
  
```XML
<Guid></Guid>
```

 <span data-ttu-id="02e50-105">**Guidtype**</span><span class="sxs-lookup"><span data-stu-id="02e50-105">**GuidType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="02e50-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="02e50-106">Attributes and elements</span></span>

<span data-ttu-id="02e50-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="02e50-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02e50-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="02e50-108">Attributes</span></span>

<span data-ttu-id="02e50-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="02e50-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="02e50-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="02e50-110">Child elements</span></span>

<span data-ttu-id="02e50-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="02e50-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="02e50-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="02e50-112">Parent elements</span></span>

|<span data-ttu-id="02e50-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="02e50-113">**Element**</span></span>|<span data-ttu-id="02e50-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="02e50-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02e50-115">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="02e50-115">SearchableMailbox</span></span>](searchablemailbox.md) <br/> |<span data-ttu-id="02e50-116">Gibt ein Postfach an, das von einer **GetSearchableMailboxes** -Anforderung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="02e50-116">Specifies a mailbox returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="02e50-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="02e50-117">Text value</span></span>

<span data-ttu-id="02e50-118">Der Textwert des **GUID** -Elements ist ein GUID-Wert, der ein Postfach eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="02e50-118">The text value of the **Guid** element is a GUID value that uniquely identifies a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="02e50-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02e50-119">Remarks</span></span>

<span data-ttu-id="02e50-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="02e50-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="02e50-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="02e50-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02e50-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="02e50-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02e50-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="02e50-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="02e50-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="02e50-124">Schema Name</span></span>  <br/> |<span data-ttu-id="02e50-125">Typschema</span><span class="sxs-lookup"><span data-stu-id="02e50-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="02e50-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="02e50-126">Validation File</span></span>  <br/> |<span data-ttu-id="02e50-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="02e50-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="02e50-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="02e50-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="02e50-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02e50-129">See also</span></span>



- [<span data-ttu-id="02e50-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="02e50-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

