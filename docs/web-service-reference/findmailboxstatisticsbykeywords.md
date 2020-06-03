---
title: FindMailboxStatisticsByKeywords
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cfe0f0ff-5fea-4db8-ac96-a5724c85ed2f
description: Das FindMailboxStatisticsByKeywords-Element gibt eine Anforderung zum Suchen nach Postfachstatistiken nach Schlüsselwort an.
ms.openlocfilehash: e22c7d8dc849d3fd45d6cb158030cbd82119437e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462528"
---
# <a name="findmailboxstatisticsbykeywords"></a><span data-ttu-id="170b2-103">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="170b2-103">FindMailboxStatisticsByKeywords</span></span>

<span data-ttu-id="170b2-104">Das **FindMailboxStatisticsByKeywords** -Element gibt eine Anforderung zum Suchen nach Postfachstatistiken nach Schlüsselwort an.</span><span class="sxs-lookup"><span data-stu-id="170b2-104">The **FindMailboxStatisticsByKeywords** element specifies a request to search for mailbox statistics by keyword.</span></span> 
  
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

 <span data-ttu-id="170b2-105">**FindMailboxStatisticsByKeywordsType**</span><span class="sxs-lookup"><span data-stu-id="170b2-105">**FindMailboxStatisticsByKeywordsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="170b2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="170b2-106">Attributes and elements</span></span>

<span data-ttu-id="170b2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="170b2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="170b2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="170b2-108">Attributes</span></span>

<span data-ttu-id="170b2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="170b2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="170b2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="170b2-110">Child elements</span></span>

|<span data-ttu-id="170b2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="170b2-111">**Element**</span></span>|<span data-ttu-id="170b2-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="170b2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="170b2-113">Postfächer (ArrayOfUserMailboxesType)</span><span class="sxs-lookup"><span data-stu-id="170b2-113">Mailboxes (ArrayOfUserMailboxesType)</span></span>](mailboxes-arrayofusermailboxestype.md) <br/> |<span data-ttu-id="170b2-114">Enthält ein Array von Postfächern, die vom Haltestatus betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="170b2-114">Contains an array of mailboxes affected by the hold.</span></span>  <br/> |
|[<span data-ttu-id="170b2-115">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="170b2-115">Keywords</span></span>](keywords-ex15websvcsotherref.md) <br/> |<span data-ttu-id="170b2-116">Gibt Stichwörter für eine Suche an.</span><span class="sxs-lookup"><span data-stu-id="170b2-116">Specifies keywords for a search.</span></span>  <br/> |
|[<span data-ttu-id="170b2-117">Sprache</span><span class="sxs-lookup"><span data-stu-id="170b2-117">Language</span></span>](language.md) <br/> |<span data-ttu-id="170b2-118">Enthält die für die Suchabfrage verwendete Sprache.</span><span class="sxs-lookup"><span data-stu-id="170b2-118">Contains the language used for the search query.</span></span>  <br/> |
|[<span data-ttu-id="170b2-119">Absender</span><span class="sxs-lookup"><span data-stu-id="170b2-119">Senders</span></span>](senders.md) <br/> |<span data-ttu-id="170b2-120">Gibt ein Array von SMTP-Adressen an.</span><span class="sxs-lookup"><span data-stu-id="170b2-120">Specifies an array of SMTP addresses.</span></span>  <br/> |
|[<span data-ttu-id="170b2-121">Recipients (ArrayOfSmtpAddressType)</span><span class="sxs-lookup"><span data-stu-id="170b2-121">Recipients (ArrayOfSmtpAddressType)</span></span>](recipients-arrayofsmtpaddresstype.md) <br/> |<span data-ttu-id="170b2-122">Gibt ein Array von Empfängern einer Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="170b2-122">Specifies an array of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="170b2-123">FromDate</span><span class="sxs-lookup"><span data-stu-id="170b2-123">FromDate</span></span>](fromdate.md) <br/> |<span data-ttu-id="170b2-124">Gibt das Datum an, an dem die Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="170b2-124">Specifies the date that the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="170b2-125">ToDate</span><span class="sxs-lookup"><span data-stu-id="170b2-125">ToDate</span></span>](todate.md) <br/> |<span data-ttu-id="170b2-126">Gibt das Datum an, an dem die Nachricht empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="170b2-126">Specifies the date that the message was received.</span></span>  <br/> |
|[<span data-ttu-id="170b2-127">MessageTypes</span><span class="sxs-lookup"><span data-stu-id="170b2-127">MessageTypes</span></span>](messagetypes.md) <br/> |<span data-ttu-id="170b2-128">Gibt ein Array von Nachrichten an, die durchsucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="170b2-128">Specifies an array of messages to search.</span></span>  <br/> |
|[<span data-ttu-id="170b2-129">SearchDumpster</span><span class="sxs-lookup"><span data-stu-id="170b2-129">SearchDumpster</span></span>](searchdumpster.md) <br/> |<span data-ttu-id="170b2-130">Gibt an, ob in gelöschten Elementen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="170b2-130">Specifies whether to search in deleted items.</span></span>  <br/> |
|[<span data-ttu-id="170b2-131">IncludePersonalArchive</span><span class="sxs-lookup"><span data-stu-id="170b2-131">IncludePersonalArchive</span></span>](includepersonalarchive.md) <br/> |<span data-ttu-id="170b2-132">Gibt an, ob das persönliche Archiv in die Suche einbezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="170b2-132">Specifies whether to include the personal archive in the search.</span></span>  <br/> |
|[<span data-ttu-id="170b2-133">Parameter IncludeUnsearchableItems</span><span class="sxs-lookup"><span data-stu-id="170b2-133">IncludeUnsearchableItems</span></span>](includeunsearchableitems.md) <br/> |<span data-ttu-id="170b2-134">Gibt an, ob Elemente eingeschlossen werden sollen, die nicht durchsucht werden können.</span><span class="sxs-lookup"><span data-stu-id="170b2-134">Specifies whether to include items that cannot be searched.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="170b2-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="170b2-135">Parent elements</span></span>

<span data-ttu-id="170b2-136">Keine.</span><span class="sxs-lookup"><span data-stu-id="170b2-136">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="170b2-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="170b2-137">Remarks</span></span>

<span data-ttu-id="170b2-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="170b2-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="170b2-139">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="170b2-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="170b2-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="170b2-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="170b2-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="170b2-141">Schema Name</span></span>  <br/> |<span data-ttu-id="170b2-142">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="170b2-142">Message schema</span></span>  <br/> |
|<span data-ttu-id="170b2-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="170b2-143">Validation File</span></span>  <br/> |<span data-ttu-id="170b2-144">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="170b2-144">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="170b2-145">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="170b2-145">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="170b2-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="170b2-146">See also</span></span>



- [<span data-ttu-id="170b2-147">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="170b2-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

