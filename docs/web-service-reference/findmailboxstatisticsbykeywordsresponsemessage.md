---
title: FindMailboxStatisticsByKeywordsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d3835800-8887-43db-9a8a-fe3cfea7a863
description: Das FindMailboxStatisticsByKeywordsResponseMessage-Element gibt die Antwortnachricht für eine Anforderung FindMailboxStatisticsByKeywords.
ms.openlocfilehash: 9479252ed53335d07a6402707bc69e5eaadfa7c8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758466"
---
# <a name="findmailboxstatisticsbykeywordsresponsemessage"></a><span data-ttu-id="94fbc-103">FindMailboxStatisticsByKeywordsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="94fbc-103">FindMailboxStatisticsByKeywordsResponseMessage</span></span>

<span data-ttu-id="94fbc-104">Das **FindMailboxStatisticsByKeywordsResponseMessage** -Element gibt die Antwortnachricht für eine Anforderung **FindMailboxStatisticsByKeywords** .</span><span class="sxs-lookup"><span data-stu-id="94fbc-104">The **FindMailboxStatisticsByKeywordsResponseMessage** element specifies the response message for a **FindMailboxStatisticsByKeywords** request.</span></span> 
  
```XML
<FindMailboxStatisticsByKeywordsResponseMessage ResponseClass=" Success | Warning | Error ">
    <MailboxStatisticsSearchResult/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</FindMailboxStatisticsByKeywordsResponseMessage>
```

 <span data-ttu-id="94fbc-105">**FindMailboxStatisticsByKeywordsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="94fbc-105">**FindMailboxStatisticsByKeywordsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="94fbc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="94fbc-106">Attributes and elements</span></span>

<span data-ttu-id="94fbc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="94fbc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="94fbc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="94fbc-108">Attributes</span></span>

|<span data-ttu-id="94fbc-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="94fbc-109">**Attribute**</span></span>|<span data-ttu-id="94fbc-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="94fbc-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="94fbc-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="94fbc-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="94fbc-112">Gibt die Antwort-Klasse.</span><span class="sxs-lookup"><span data-stu-id="94fbc-112">Specifies the response class.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="94fbc-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="94fbc-113">ResponseClass</span></span>

|<span data-ttu-id="94fbc-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="94fbc-114">**Value**</span></span>|<span data-ttu-id="94fbc-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="94fbc-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="94fbc-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="94fbc-116">Success</span></span>  <br/> |<span data-ttu-id="94fbc-117">Gibt Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="94fbc-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="94fbc-118">Warning</span><span class="sxs-lookup"><span data-stu-id="94fbc-118">Warning</span></span>  <br/> |<span data-ttu-id="94fbc-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="94fbc-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="94fbc-120">Fehler</span><span class="sxs-lookup"><span data-stu-id="94fbc-120">Error</span></span>  <br/> |<span data-ttu-id="94fbc-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="94fbc-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="94fbc-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="94fbc-122">Child elements</span></span>

|<span data-ttu-id="94fbc-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="94fbc-123">**Element**</span></span>|<span data-ttu-id="94fbc-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="94fbc-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="94fbc-125">MailboxStatisticsSearchResult</span><span class="sxs-lookup"><span data-stu-id="94fbc-125">MailboxStatisticsSearchResult</span></span>](mailboxstatisticssearchresult.md) <br/> |<span data-ttu-id="94fbc-126">Gibt das Ergebnis einer postfachsuche an.</span><span class="sxs-lookup"><span data-stu-id="94fbc-126">Specifies the result of a mailbox search.</span></span>  <br/> |
|[<span data-ttu-id="94fbc-127">MessageText</span><span class="sxs-lookup"><span data-stu-id="94fbc-127">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="94fbc-128">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="94fbc-128">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="94fbc-129">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="94fbc-129">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="94fbc-130">Enthält Statusinformationen über die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="94fbc-130">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="94fbc-131">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="94fbc-131">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="94fbc-132">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="94fbc-132">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="94fbc-133">MessageXml</span><span class="sxs-lookup"><span data-stu-id="94fbc-133">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="94fbc-134">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="94fbc-134">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="94fbc-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="94fbc-135">Parent elements</span></span>

|<span data-ttu-id="94fbc-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="94fbc-136">**Element**</span></span>|<span data-ttu-id="94fbc-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="94fbc-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="94fbc-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="94fbc-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="94fbc-139">Gibt ein Array von Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="94fbc-139">Specifies an array of response messages.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94fbc-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="94fbc-140">Remarks</span></span>

<span data-ttu-id="94fbc-141">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="94fbc-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="94fbc-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="94fbc-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="94fbc-143">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="94fbc-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94fbc-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="94fbc-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="94fbc-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="94fbc-145">Schema Name</span></span>  <br/> |<span data-ttu-id="94fbc-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="94fbc-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="94fbc-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="94fbc-147">Validation File</span></span>  <br/> |<span data-ttu-id="94fbc-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="94fbc-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="94fbc-149">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="94fbc-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="94fbc-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94fbc-150">See also</span></span>



- [<span data-ttu-id="94fbc-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="94fbc-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

