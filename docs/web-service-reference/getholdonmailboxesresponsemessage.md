---
title: GetHoldOnMailboxesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f7d0d90-d418-4ce9-8cea-afe8f14728c3
description: Das GetHoldOnMailboxesResponseMessage-Element gibt die Antwortnachricht für eine GetHoldOnMailboxes-Anforderung an.
ms.openlocfilehash: 31832c11181bdca482e88419dd46ff1eacf77ea6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462950"
---
# <a name="getholdonmailboxesresponsemessage"></a><span data-ttu-id="d8649-103">GetHoldOnMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d8649-103">GetHoldOnMailboxesResponseMessage</span></span>

<span data-ttu-id="d8649-104">Das **GetHoldOnMailboxesResponseMessage** -Element gibt die Antwortnachricht für eine **GetHoldOnMailboxes** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="d8649-104">The **GetHoldOnMailboxesResponseMessage** element specifies the response message for a **GetHoldOnMailboxes** request.</span></span> 
  
```XML
<GetHoldOnMailboxesResponseMessage ResponseClass=" Success | Warning | Error ">
    <MailboxHoldResult/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetHoldOnMailboxesResponseMessage>
```

 <span data-ttu-id="d8649-105">**GetHoldOnMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="d8649-105">**GetHoldOnMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d8649-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d8649-106">Attributes and elements</span></span>

<span data-ttu-id="d8649-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d8649-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d8649-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d8649-108">Attributes</span></span>

|<span data-ttu-id="d8649-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d8649-109">**Attribute**</span></span>|<span data-ttu-id="d8649-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d8649-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d8649-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="d8649-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="d8649-112">Gibt die Klasse der Antwort an.</span><span class="sxs-lookup"><span data-stu-id="d8649-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="d8649-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="d8649-113">ResponseClass</span></span>

|<span data-ttu-id="d8649-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d8649-114">**Value**</span></span>|<span data-ttu-id="d8649-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d8649-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d8649-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="d8649-116">Success</span></span>  <br/> |<span data-ttu-id="d8649-117">Gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="d8649-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="d8649-118">Warnung</span><span class="sxs-lookup"><span data-stu-id="d8649-118">Warning</span></span>  <br/> |<span data-ttu-id="d8649-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="d8649-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="d8649-120">Fehler (ungefährer Wortlaut)</span><span class="sxs-lookup"><span data-stu-id="d8649-120">Error</span></span>  <br/> |<span data-ttu-id="d8649-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="d8649-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d8649-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d8649-122">Child elements</span></span>

|<span data-ttu-id="d8649-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="d8649-123">**Element**</span></span>|<span data-ttu-id="d8649-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d8649-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d8649-125">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="d8649-125">MailboxHoldResult</span></span>](mailboxholdresult.md) <br/> |<span data-ttu-id="d8649-126">Enthält das Ergebnis der **GetHoldOnMailboxes** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d8649-126">Contains the result of the **GetHoldOnMailboxes** request.</span></span>  <br/> |
|[<span data-ttu-id="d8649-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d8649-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="d8649-128">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="d8649-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="d8649-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="d8649-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="d8649-130">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="d8649-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="d8649-131">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="d8649-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="d8649-132">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="d8649-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="d8649-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d8649-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="d8649-134">Stellt Statusinformationen zur Anforderung bereit.</span><span class="sxs-lookup"><span data-stu-id="d8649-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d8649-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d8649-135">Parent elements</span></span>

|<span data-ttu-id="d8649-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="d8649-136">**Element**</span></span>|<span data-ttu-id="d8649-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d8649-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d8649-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d8649-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="d8649-139">Enthält die Antwortnachrichten für eine Exchange-Webdienste Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d8649-139">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8649-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8649-140">Remarks</span></span>

<span data-ttu-id="d8649-141">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d8649-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d8649-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d8649-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d8649-143">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d8649-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8649-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8649-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d8649-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d8649-145">Schema Name</span></span>  <br/> |<span data-ttu-id="d8649-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d8649-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="d8649-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d8649-147">Validation File</span></span>  <br/> |<span data-ttu-id="d8649-148">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d8649-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d8649-149">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d8649-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="d8649-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8649-150">See also</span></span>



- [<span data-ttu-id="d8649-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d8649-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

