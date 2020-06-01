---
title: FailedMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3d4c9816-54bb-4932-b4ba-f057c9173a1a
description: Das FailedMailbox -Element gibt die Fehlermeldung für ein Postfach, die nicht auf Suchen.
ms.openlocfilehash: 404084bc342eb555db61c4216e936bee6ced9c36
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461961"
---
# <a name="failedmailbox"></a><span data-ttu-id="1123d-103">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="1123d-103">FailedMailbox</span></span>

<span data-ttu-id="1123d-104">Das **FailedMailbox** -Element gibt die Fehlermeldung für ein Postfach, die nicht auf Suchen.</span><span class="sxs-lookup"><span data-stu-id="1123d-104">The **FailedMailbox** element specifies the error message for a mailbox that failed on search.</span></span> 
  
```XML
<FailedMailbox>
    <Mailbox/>
    <ErrorCode/>
    <ErrorMessage/>
    <IsArchive/>
</FailedMailbox>
```

 <span data-ttu-id="1123d-105">**FailedSearchMailboxType**</span><span class="sxs-lookup"><span data-stu-id="1123d-105">**FailedSearchMailboxType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1123d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1123d-106">Attributes and elements</span></span>

<span data-ttu-id="1123d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1123d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1123d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1123d-108">Attributes</span></span>

<span data-ttu-id="1123d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1123d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1123d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1123d-110">Child elements</span></span>

|<span data-ttu-id="1123d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1123d-111">**Element**</span></span>|<span data-ttu-id="1123d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1123d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1123d-113">Postfach (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="1123d-113">Mailbox (string)</span></span>](mailbox-string.md) <br/> |<span data-ttu-id="1123d-114">Enthält einen Bezeichner für das Postfach.</span><span class="sxs-lookup"><span data-stu-id="1123d-114">Contains an identifier for the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="1123d-115">ErrorCode (Int)</span><span class="sxs-lookup"><span data-stu-id="1123d-115">ErrorCode (int)</span></span>](errorcode-int.md) <br/> |<span data-ttu-id="1123d-116">Gibt den Fehlercode des Postfachs an, die die Suche ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="1123d-116">Specifies the error code of the mailbox that failed the search.</span></span>  <br/> |
|[<span data-ttu-id="1123d-117">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="1123d-117">ErrorMessage</span></span>](errormessage.md) <br/> |<span data-ttu-id="1123d-118">Stellt den Grund für die Überprüfungsfehler.</span><span class="sxs-lookup"><span data-stu-id="1123d-118">Represents the reason for the validation error.</span></span>  <br/> |
|[<span data-ttu-id="1123d-119">IsArchive</span><span class="sxs-lookup"><span data-stu-id="1123d-119">IsArchive</span></span>](isarchive.md) <br/> |<span data-ttu-id="1123d-120">Gibt einen Boolean-Wert, der angibt, ob das Postfach ein Archiv ist.</span><span class="sxs-lookup"><span data-stu-id="1123d-120">Specifies a Boolean value that indicates whether the mailbox is an archive.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1123d-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1123d-121">Parent elements</span></span>

|<span data-ttu-id="1123d-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="1123d-122">**Element**</span></span>|<span data-ttu-id="1123d-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1123d-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1123d-124">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="1123d-124">FailedMailboxes</span></span>](failedmailboxes.md) <br/> |<span data-ttu-id="1123d-125">Gibt ein Array von Postfächer mit Fehlern.</span><span class="sxs-lookup"><span data-stu-id="1123d-125">Specifies an array of failed mailboxes.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1123d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1123d-126">Remarks</span></span>

<span data-ttu-id="1123d-127">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1123d-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1123d-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1123d-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1123d-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1123d-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1123d-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="1123d-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1123d-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1123d-131">Schema Name</span></span>  <br/> |<span data-ttu-id="1123d-132">Typschema</span><span class="sxs-lookup"><span data-stu-id="1123d-132">Type schema</span></span>  <br/> |
|<span data-ttu-id="1123d-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1123d-133">Validation File</span></span>  <br/> |<span data-ttu-id="1123d-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1123d-134">types.xsd</span></span>  <br/> |
|<span data-ttu-id="1123d-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="1123d-135">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="1123d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1123d-136">See also</span></span>



- [<span data-ttu-id="1123d-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1123d-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

