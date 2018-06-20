---
title: GetSearchableMailboxesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f45865fd-4626-4d80-84f6-7989339fdd85
description: Das GetSearchableMailboxesResponseMessage-Element gibt die Antwortnachricht für eine Anforderung GetSearchableMailboxes.
ms.openlocfilehash: 2a4d1fe357656fe29d8572e7f32a4bc2e4a6131e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758800"
---
# <a name="getsearchablemailboxesresponsemessage"></a><span data-ttu-id="d2241-103">GetSearchableMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d2241-103">GetSearchableMailboxesResponseMessage</span></span>

<span data-ttu-id="d2241-104">Das **GetSearchableMailboxesResponseMessage** -Element gibt die Antwortnachricht für eine Anforderung **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="d2241-104">The **GetSearchableMailboxesResponseMessage** element specifies the response message for a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<GetSearchableMailboxesResponseMessage ResponseClass=" Success | Warning | Error ">
    <SearchableMailboxes/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetSearchablemailboxesResponseMessage>
```

 <span data-ttu-id="d2241-105">**GetSearchableMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="d2241-105">**GetSearchableMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d2241-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d2241-106">Attributes and elements</span></span>

<span data-ttu-id="d2241-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d2241-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d2241-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d2241-108">Attributes</span></span>

|<span data-ttu-id="d2241-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d2241-109">**Attribute**</span></span>|<span data-ttu-id="d2241-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d2241-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d2241-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="d2241-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="d2241-112">Gibt die Klasse der Antwort.</span><span class="sxs-lookup"><span data-stu-id="d2241-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="d2241-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="d2241-113">ResponseClass</span></span>

|<span data-ttu-id="d2241-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d2241-114">**Value**</span></span>|<span data-ttu-id="d2241-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d2241-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d2241-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="d2241-116">Success</span></span>  <br/> |<span data-ttu-id="d2241-117">Gibt Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="d2241-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="d2241-118">Warning</span><span class="sxs-lookup"><span data-stu-id="d2241-118">Warning</span></span>  <br/> |<span data-ttu-id="d2241-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="d2241-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="d2241-120">Fehler</span><span class="sxs-lookup"><span data-stu-id="d2241-120">Error</span></span>  <br/> |<span data-ttu-id="d2241-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="d2241-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d2241-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d2241-122">Child elements</span></span>

|<span data-ttu-id="d2241-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="d2241-123">**Element**</span></span>|<span data-ttu-id="d2241-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d2241-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2241-125">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="d2241-125">SearchableMailboxes</span></span>](searchablemailboxes.md) <br/> |<span data-ttu-id="d2241-126">Enthält ein Array der Postfächer aus einer Anforderung **GetSearchableMailboxes** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d2241-126">Contains an array of the mailboxes returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
|[<span data-ttu-id="d2241-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d2241-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="d2241-128">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="d2241-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="d2241-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="d2241-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="d2241-130">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="d2241-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="d2241-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="d2241-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="d2241-132">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="d2241-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="d2241-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d2241-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="d2241-134">Enthält Statusinformationen über die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d2241-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d2241-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d2241-135">Parent elements</span></span>

|<span data-ttu-id="d2241-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="d2241-136">**Element**</span></span>|<span data-ttu-id="d2241-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d2241-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2241-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d2241-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="d2241-139">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d2241-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2241-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d2241-140">Remarks</span></span>

<span data-ttu-id="d2241-141">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d2241-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d2241-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d2241-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d2241-143">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d2241-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2241-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="d2241-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d2241-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d2241-145">Schema Name</span></span>  <br/> |<span data-ttu-id="d2241-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d2241-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="d2241-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d2241-147">Validation File</span></span>  <br/> |<span data-ttu-id="d2241-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d2241-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d2241-149">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d2241-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="d2241-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2241-150">See also</span></span>



- [<span data-ttu-id="d2241-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d2241-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

