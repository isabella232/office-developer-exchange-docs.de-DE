---
title: FailedMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f34fb6f6-057e-4ae3-8e10-bc92112eafba
description: Das FailedMailboxes-Element gibt ein Array von Postfächern an, bei denen die Suche fehlgeschlagen ist.
ms.openlocfilehash: 10f10d3f2ac4379d7ddcb3a13019d17a17bb676a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461954"
---
# <a name="failedmailboxes"></a><span data-ttu-id="2e4a3-103">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="2e4a3-103">FailedMailboxes</span></span>

<span data-ttu-id="2e4a3-104">Das **FailedMailboxes** -Element gibt ein Array von Postfächern an, bei denen die Suche fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="2e4a3-104">The **FailedMailboxes** element specifies an array of mailboxes that failed on search.</span></span> 
  
```XML
<FailedMailboxes>
    <FailedMailbox/>
<FailedMailboxes>
```

 <span data-ttu-id="2e4a3-105">**ArrayOfFailedSearchMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="2e4a3-105">**ArrayOfFailedSearchMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2e4a3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2e4a3-106">Attributes and elements</span></span>

<span data-ttu-id="2e4a3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2e4a3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e4a3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2e4a3-108">Attributes</span></span>

<span data-ttu-id="2e4a3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2e4a3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2e4a3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2e4a3-110">Child elements</span></span>

|<span data-ttu-id="2e4a3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2e4a3-111">**Element**</span></span>|<span data-ttu-id="2e4a3-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2e4a3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e4a3-113">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="2e4a3-113">FailedMailbox</span></span>](failedmailbox.md) <br/> |<span data-ttu-id="2e4a3-114">Gibt die Fehlermeldung für ein Postfach an, bei dem die Suche fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="2e4a3-114">Specifies the error message for a mailbox that failed on search.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2e4a3-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2e4a3-115">Parent elements</span></span>

|<span data-ttu-id="2e4a3-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="2e4a3-116">**Element**</span></span>|<span data-ttu-id="2e4a3-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2e4a3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e4a3-118">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="2e4a3-118">SearchMailboxesResult</span></span>](searchmailboxesresult.md) <br/> |<span data-ttu-id="2e4a3-119">Enthält das Ergebnis der **SearchMailboxes** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2e4a3-119">Contains the result of the **SearchMailboxes** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e4a3-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e4a3-120">Remarks</span></span>

<span data-ttu-id="2e4a3-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2e4a3-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2e4a3-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2e4a3-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2e4a3-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2e4a3-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e4a3-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e4a3-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2e4a3-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2e4a3-125">Schema Name</span></span>  <br/> |<span data-ttu-id="2e4a3-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="2e4a3-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="2e4a3-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2e4a3-127">Validation File</span></span>  <br/> |<span data-ttu-id="2e4a3-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="2e4a3-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2e4a3-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2e4a3-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2e4a3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e4a3-130">See also</span></span>



- [<span data-ttu-id="2e4a3-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2e4a3-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

