---
title: FailedMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f34fb6f6-057e-4ae3-8e10-bc92112eafba
description: Das FailedMailboxes-Element gibt ein Array von Postfächern, die nicht auf Suche.
ms.openlocfilehash: f68cc29dc9da3b1b74369aa21cde65866e42f3b8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758405"
---
# <a name="failedmailboxes"></a><span data-ttu-id="3e6ba-103">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="3e6ba-103">FailedMailboxes</span></span>

<span data-ttu-id="3e6ba-104">Das **FailedMailboxes** -Element gibt ein Array von Postfächern, die nicht auf Suche.</span><span class="sxs-lookup"><span data-stu-id="3e6ba-104">The **FailedMailboxes** element specifies an array of mailboxes that failed on search.</span></span> 
  
```XML
<FailedMailboxes>
    <FailedMailbox/>
<FailedMailboxes>
```

 <span data-ttu-id="3e6ba-105">**ArrayOfFailedSearchMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="3e6ba-105">**ArrayOfFailedSearchMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3e6ba-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3e6ba-106">Attributes and elements</span></span>

<span data-ttu-id="3e6ba-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3e6ba-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3e6ba-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3e6ba-108">Attributes</span></span>

<span data-ttu-id="3e6ba-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3e6ba-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3e6ba-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e6ba-110">Child elements</span></span>

|<span data-ttu-id="3e6ba-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3e6ba-111">**Element**</span></span>|<span data-ttu-id="3e6ba-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3e6ba-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e6ba-113">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="3e6ba-113">FailedMailbox</span></span>](failedmailbox.md) <br/> |<span data-ttu-id="3e6ba-114">Gibt die Fehlermeldung für ein Postfach, die nicht auf die Suche an.</span><span class="sxs-lookup"><span data-stu-id="3e6ba-114">Specifies the error message for a mailbox that failed on search.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3e6ba-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e6ba-115">Parent elements</span></span>

|<span data-ttu-id="3e6ba-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="3e6ba-116">**Element**</span></span>|<span data-ttu-id="3e6ba-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3e6ba-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e6ba-118">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="3e6ba-118">SearchMailboxesResult</span></span>](searchmailboxesresult.md) <br/> |<span data-ttu-id="3e6ba-119">Das Ergebnis der Anforderung **SearchMailboxes** enthält.</span><span class="sxs-lookup"><span data-stu-id="3e6ba-119">Contains the result of the **SearchMailboxes** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e6ba-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3e6ba-120">Remarks</span></span>

<span data-ttu-id="3e6ba-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3e6ba-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3e6ba-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3e6ba-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3e6ba-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3e6ba-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e6ba-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e6ba-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3e6ba-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3e6ba-125">Schema Name</span></span>  <br/> |<span data-ttu-id="3e6ba-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="3e6ba-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="3e6ba-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3e6ba-127">Validation File</span></span>  <br/> |<span data-ttu-id="3e6ba-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3e6ba-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="3e6ba-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="3e6ba-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3e6ba-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e6ba-130">See also</span></span>



- [<span data-ttu-id="3e6ba-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3e6ba-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

