---
title: GetHoldOnMailboxesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f7d0d90-d418-4ce9-8cea-afe8f14728c3
description: Das GetHoldOnMailboxesResponseMessage-Element gibt die Antwortnachricht für eine Anforderung GetHoldOnMailboxes.
ms.openlocfilehash: e1c43f75bfa62b20de9248546e71c92ae5998ed9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758692"
---
# <a name="getholdonmailboxesresponsemessage"></a><span data-ttu-id="8b27a-103">GetHoldOnMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8b27a-103">GetHoldOnMailboxesResponseMessage</span></span>

<span data-ttu-id="8b27a-104">Das **GetHoldOnMailboxesResponseMessage** -Element gibt die Antwortnachricht für eine Anforderung **GetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="8b27a-104">The **GetHoldOnMailboxesResponseMessage** element specifies the response message for a **GetHoldOnMailboxes** request.</span></span> 
  
```XML
<GetHoldOnMailboxesResponseMessage ResponseClass=" Success | Warning | Error ">
    <MailboxHoldResult/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetHoldOnMailboxesResponseMessage>
```

 <span data-ttu-id="8b27a-105">**GetHoldOnMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="8b27a-105">**GetHoldOnMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8b27a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8b27a-106">Attributes and elements</span></span>

<span data-ttu-id="8b27a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8b27a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8b27a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8b27a-108">Attributes</span></span>

|<span data-ttu-id="8b27a-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8b27a-109">**Attribute**</span></span>|<span data-ttu-id="8b27a-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8b27a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8b27a-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="8b27a-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="8b27a-112">Gibt die Klasse der Antwort.</span><span class="sxs-lookup"><span data-stu-id="8b27a-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="8b27a-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="8b27a-113">ResponseClass</span></span>

|<span data-ttu-id="8b27a-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8b27a-114">**Value**</span></span>|<span data-ttu-id="8b27a-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8b27a-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8b27a-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="8b27a-116">Success</span></span>  <br/> |<span data-ttu-id="8b27a-117">Gibt Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="8b27a-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="8b27a-118">Warning</span><span class="sxs-lookup"><span data-stu-id="8b27a-118">Warning</span></span>  <br/> |<span data-ttu-id="8b27a-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="8b27a-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="8b27a-120">Fehler</span><span class="sxs-lookup"><span data-stu-id="8b27a-120">Error</span></span>  <br/> |<span data-ttu-id="8b27a-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="8b27a-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8b27a-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8b27a-122">Child elements</span></span>

|<span data-ttu-id="8b27a-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="8b27a-123">**Element**</span></span>|<span data-ttu-id="8b27a-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8b27a-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8b27a-125">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="8b27a-125">MailboxHoldResult</span></span>](mailboxholdresult.md) <br/> |<span data-ttu-id="8b27a-126">Das Ergebnis der Anforderung **GetHoldOnMailboxes** enthält.</span><span class="sxs-lookup"><span data-stu-id="8b27a-126">Contains the result of the **GetHoldOnMailboxes** request.</span></span>  <br/> |
|[<span data-ttu-id="8b27a-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8b27a-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="8b27a-128">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="8b27a-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="8b27a-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="8b27a-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="8b27a-130">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="8b27a-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="8b27a-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="8b27a-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="8b27a-132">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="8b27a-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="8b27a-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8b27a-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="8b27a-134">Enthält Statusinformationen über die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8b27a-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8b27a-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8b27a-135">Parent elements</span></span>

|<span data-ttu-id="8b27a-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="8b27a-136">**Element**</span></span>|<span data-ttu-id="8b27a-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8b27a-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8b27a-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8b27a-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="8b27a-139">Enthält die Antwortnachrichten für eine Exchange-Webdienste (EWS)-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8b27a-139">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b27a-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8b27a-140">Remarks</span></span>

<span data-ttu-id="8b27a-141">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8b27a-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8b27a-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8b27a-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8b27a-143">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8b27a-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8b27a-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b27a-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8b27a-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8b27a-145">Schema Name</span></span>  <br/> |<span data-ttu-id="8b27a-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8b27a-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="8b27a-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8b27a-147">Validation File</span></span>  <br/> |<span data-ttu-id="8b27a-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8b27a-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8b27a-149">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8b27a-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="8b27a-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b27a-150">See also</span></span>



- [<span data-ttu-id="8b27a-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8b27a-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

