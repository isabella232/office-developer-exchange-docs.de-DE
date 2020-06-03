---
title: FindMailboxStatisticsByKeywordsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d3835800-8887-43db-9a8a-fe3cfea7a863
description: Das FindMailboxStatisticsByKeywordsResponseMessage-Element gibt die Antwortnachricht für eine FindMailboxStatisticsByKeywords-Anforderung an.
ms.openlocfilehash: 704eebbf82db2871ab36be8e5b30c88c6959baa5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44525976"
---
# <a name="findmailboxstatisticsbykeywordsresponsemessage"></a><span data-ttu-id="0b817-103">FindMailboxStatisticsByKeywordsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0b817-103">FindMailboxStatisticsByKeywordsResponseMessage</span></span>

<span data-ttu-id="0b817-104">Das **FindMailboxStatisticsByKeywordsResponseMessage** -Element gibt die Antwortnachricht für eine **FindMailboxStatisticsByKeywords** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="0b817-104">The **FindMailboxStatisticsByKeywordsResponseMessage** element specifies the response message for a **FindMailboxStatisticsByKeywords** request.</span></span> 
  
```XML
<FindMailboxStatisticsByKeywordsResponseMessage ResponseClass=" Success | Warning | Error ">
    <MailboxStatisticsSearchResult/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</FindMailboxStatisticsByKeywordsResponseMessage>
```

 <span data-ttu-id="0b817-105">**FindMailboxStatisticsByKeywordsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="0b817-105">**FindMailboxStatisticsByKeywordsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0b817-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0b817-106">Attributes and elements</span></span>

<span data-ttu-id="0b817-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0b817-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0b817-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0b817-108">Attributes</span></span>

|<span data-ttu-id="0b817-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0b817-109">**Attribute**</span></span>|<span data-ttu-id="0b817-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0b817-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0b817-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="0b817-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="0b817-112">Gibt die Antwort Klasse an.</span><span class="sxs-lookup"><span data-stu-id="0b817-112">Specifies the response class.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="0b817-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="0b817-113">ResponseClass</span></span>

|<span data-ttu-id="0b817-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0b817-114">**Value**</span></span>|<span data-ttu-id="0b817-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0b817-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0b817-116">Erfolgreich</span><span class="sxs-lookup"><span data-stu-id="0b817-116">Success</span></span>  <br/> |<span data-ttu-id="0b817-117">Gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="0b817-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="0b817-118">Warnung</span><span class="sxs-lookup"><span data-stu-id="0b817-118">Warning</span></span>  <br/> |<span data-ttu-id="0b817-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="0b817-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="0b817-120">Fehler (ungefährer Wortlaut)</span><span class="sxs-lookup"><span data-stu-id="0b817-120">Error</span></span>  <br/> |<span data-ttu-id="0b817-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="0b817-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0b817-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b817-122">Child elements</span></span>

|<span data-ttu-id="0b817-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="0b817-123">**Element**</span></span>|<span data-ttu-id="0b817-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0b817-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0b817-125">MailboxStatisticsSearchResult</span><span class="sxs-lookup"><span data-stu-id="0b817-125">MailboxStatisticsSearchResult</span></span>](mailboxstatisticssearchresult.md) <br/> |<span data-ttu-id="0b817-126">Gibt das Ergebnis einer Postfachsuche an.</span><span class="sxs-lookup"><span data-stu-id="0b817-126">Specifies the result of a mailbox search.</span></span>  <br/> |
|[<span data-ttu-id="0b817-127">MessageText</span><span class="sxs-lookup"><span data-stu-id="0b817-127">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0b817-128">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="0b817-128">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="0b817-129">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0b817-129">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="0b817-130">Stellt Statusinformationen zur Anforderung bereit.</span><span class="sxs-lookup"><span data-stu-id="0b817-130">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="0b817-131">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0b817-131">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="0b817-132">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="0b817-132">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="0b817-133">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="0b817-133">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="0b817-134">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="0b817-134">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0b817-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b817-135">Parent elements</span></span>

|<span data-ttu-id="0b817-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="0b817-136">**Element**</span></span>|<span data-ttu-id="0b817-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0b817-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0b817-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0b817-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="0b817-139">Gibt ein Array von Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="0b817-139">Specifies an array of response messages.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b817-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b817-140">Remarks</span></span>

<span data-ttu-id="0b817-141">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0b817-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0b817-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0b817-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0b817-143">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0b817-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b817-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b817-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0b817-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0b817-145">Schema Name</span></span>  <br/> |<span data-ttu-id="0b817-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="0b817-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="0b817-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0b817-147">Validation File</span></span>  <br/> |<span data-ttu-id="0b817-148">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0b817-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0b817-149">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="0b817-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0b817-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b817-150">See also</span></span>



- [<span data-ttu-id="0b817-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0b817-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

