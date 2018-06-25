---
title: FindMailboxStatisticsByKeywords
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cfe0f0ff-5fea-4db8-ac96-a5724c85ed2f
description: Das FindMailboxStatisticsByKeywords-Element gibt eine Anforderung an die Postfachstatistiken nach Schlüsselwort suchen.
ms.openlocfilehash: e667f13b66e439dca88d73a5e05d74846183928c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758459"
---
# <a name="findmailboxstatisticsbykeywords"></a><span data-ttu-id="ed631-103">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="ed631-103">FindMailboxStatisticsByKeywords</span></span>

<span data-ttu-id="ed631-104">Das **FindMailboxStatisticsByKeywords** -Element gibt eine Anforderung an die Postfachstatistiken nach Schlüsselwort suchen.</span><span class="sxs-lookup"><span data-stu-id="ed631-104">The **FindMailboxStatisticsByKeywords** element specifies a request to search for mailbox statistics by keyword.</span></span> 
  
```XML
<FindMailboxStatisticsByKeywords>
    <Mailboxes/>
    <Keywords/>
    <Language/>
    <Senders/>
    <Recipients/>
    <FromDate/>
    <ToDate/>
    <MessageTypes/>
    <SearchDumpster/>
    <IncludePersonalArchive/>
    <IncludeUnsearchableItems/>
</FindMailboxStatisticsByKeywords>
```

 <span data-ttu-id="ed631-105">**FindMailboxStatisticsByKeywordsType**</span><span class="sxs-lookup"><span data-stu-id="ed631-105">**FindMailboxStatisticsByKeywordsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ed631-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ed631-106">Attributes and elements</span></span>

<span data-ttu-id="ed631-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ed631-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ed631-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ed631-108">Attributes</span></span>

<span data-ttu-id="ed631-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ed631-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ed631-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ed631-110">Child elements</span></span>

|<span data-ttu-id="ed631-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ed631-111">**Element**</span></span>|<span data-ttu-id="ed631-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ed631-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed631-113">Postfächer (ArrayOfUserMailboxesType)</span><span class="sxs-lookup"><span data-stu-id="ed631-113">Mailboxes (ArrayOfUserMailboxesType)</span></span>](mailboxes-arrayofusermailboxestype.md) <br/> |<span data-ttu-id="ed631-114">Enthält ein Array von Postfächern, die von den Haltestatus betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="ed631-114">Contains an array of mailboxes affected by the hold.</span></span>  <br/> |
|[<span data-ttu-id="ed631-115">Keywords</span><span class="sxs-lookup"><span data-stu-id="ed631-115">Keywords</span></span>](keywords-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ed631-116">Gibt die Schlüsselwörter für die Suche.</span><span class="sxs-lookup"><span data-stu-id="ed631-116">Specifies keywords for a search.</span></span>  <br/> |
|[<span data-ttu-id="ed631-117">Language</span><span class="sxs-lookup"><span data-stu-id="ed631-117">Language</span></span>](language.md) <br/> |<span data-ttu-id="ed631-118">Enthält die Sprache für die Suchabfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed631-118">Contains the language used for the search query.</span></span>  <br/> |
|[<span data-ttu-id="ed631-119">Absender</span><span class="sxs-lookup"><span data-stu-id="ed631-119">Senders</span></span>](senders.md) <br/> |<span data-ttu-id="ed631-120">Gibt ein Array von SMTP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="ed631-120">Specifies an array of SMTP addresses.</span></span>  <br/> |
|[<span data-ttu-id="ed631-121">Empfänger (ArrayOfSmtpAddressType)</span><span class="sxs-lookup"><span data-stu-id="ed631-121">Recipients (ArrayOfSmtpAddressType)</span></span>](recipients-arrayofsmtpaddresstype.md) <br/> |<span data-ttu-id="ed631-122">Gibt ein Array von Empfänger einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ed631-122">Specifies an array of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="ed631-123">FromDate</span><span class="sxs-lookup"><span data-stu-id="ed631-123">FromDate</span></span>](fromdate.md) <br/> |<span data-ttu-id="ed631-124">Gibt das Datum, das die Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ed631-124">Specifies the date that the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="ed631-125">ToDate</span><span class="sxs-lookup"><span data-stu-id="ed631-125">ToDate</span></span>](todate.md) <br/> |<span data-ttu-id="ed631-126">Gibt das Datum, das die Nachricht empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="ed631-126">Specifies the date that the message was received.</span></span>  <br/> |
|[<span data-ttu-id="ed631-127">MessageTypes</span><span class="sxs-lookup"><span data-stu-id="ed631-127">MessageTypes</span></span>](messagetypes.md) <br/> |<span data-ttu-id="ed631-128">Gibt ein Array von Nachrichten suchen.</span><span class="sxs-lookup"><span data-stu-id="ed631-128">Specifies an array of messages to search.</span></span>  <br/> |
|[<span data-ttu-id="ed631-129">SearchDumpster</span><span class="sxs-lookup"><span data-stu-id="ed631-129">SearchDumpster</span></span>](searchdumpster.md) <br/> |<span data-ttu-id="ed631-130">Gibt an, ob in gelöschte Elemente durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="ed631-130">Specifies whether to search in deleted items.</span></span>  <br/> |
|[<span data-ttu-id="ed631-131">IncludePersonalArchive</span><span class="sxs-lookup"><span data-stu-id="ed631-131">IncludePersonalArchive</span></span>](includepersonalarchive.md) <br/> |<span data-ttu-id="ed631-132">Gibt an, ob das persönliche Archiv in die Suche einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="ed631-132">Specifies whether to include the personal archive in the search.</span></span>  <br/> |
|[<span data-ttu-id="ed631-133">IncludeUnsearchableItems</span><span class="sxs-lookup"><span data-stu-id="ed631-133">IncludeUnsearchableItems</span></span>](includeunsearchableitems.md) <br/> |<span data-ttu-id="ed631-134">Gibt an, ob Elemente enthalten, die durchsucht werden kann.</span><span class="sxs-lookup"><span data-stu-id="ed631-134">Specifies whether to include items that cannot be searched.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ed631-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ed631-135">Parent elements</span></span>

<span data-ttu-id="ed631-136">Keine.</span><span class="sxs-lookup"><span data-stu-id="ed631-136">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ed631-137">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ed631-137">Remarks</span></span>

<span data-ttu-id="ed631-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ed631-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ed631-139">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ed631-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed631-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed631-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ed631-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ed631-141">Schema Name</span></span>  <br/> |<span data-ttu-id="ed631-142">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ed631-142">Message schema</span></span>  <br/> |
|<span data-ttu-id="ed631-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ed631-143">Validation File</span></span>  <br/> |<span data-ttu-id="ed631-144">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ed631-144">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ed631-145">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ed631-145">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ed631-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed631-146">See also</span></span>



- [<span data-ttu-id="ed631-147">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ed631-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

