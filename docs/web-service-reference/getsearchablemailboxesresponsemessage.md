---
title: GetSearchableMailboxesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f45865fd-4626-4d80-84f6-7989339fdd85
description: Das GetSearchableMailboxesResponseMessage-Element gibt die Antwortnachricht für eine GetSearchableMailboxes-Anforderung an.
ms.openlocfilehash: 69f45d87cfbd398013d021cdd39b55497d78ae04
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458257"
---
# <a name="getsearchablemailboxesresponsemessage"></a><span data-ttu-id="85dbc-103">GetSearchableMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="85dbc-103">GetSearchableMailboxesResponseMessage</span></span>

<span data-ttu-id="85dbc-104">Das **GetSearchableMailboxesResponseMessage** -Element gibt die Antwortnachricht für eine **GetSearchableMailboxes** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="85dbc-104">The **GetSearchableMailboxesResponseMessage** element specifies the response message for a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<GetSearchableMailboxesResponseMessage ResponseClass=" Success | Warning | Error ">
    <SearchableMailboxes/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetSearchablemailboxesResponseMessage>
```

 <span data-ttu-id="85dbc-105">**GetSearchableMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="85dbc-105">**GetSearchableMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85dbc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="85dbc-106">Attributes and elements</span></span>

<span data-ttu-id="85dbc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="85dbc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85dbc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="85dbc-108">Attributes</span></span>

|<span data-ttu-id="85dbc-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="85dbc-109">**Attribute**</span></span>|<span data-ttu-id="85dbc-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85dbc-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85dbc-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="85dbc-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="85dbc-112">Gibt die Klasse der Antwort an.</span><span class="sxs-lookup"><span data-stu-id="85dbc-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="85dbc-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="85dbc-113">ResponseClass</span></span>

|<span data-ttu-id="85dbc-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="85dbc-114">**Value**</span></span>|<span data-ttu-id="85dbc-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85dbc-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85dbc-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="85dbc-116">Success</span></span>  <br/> |<span data-ttu-id="85dbc-117">Gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="85dbc-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="85dbc-118">Warnung</span><span class="sxs-lookup"><span data-stu-id="85dbc-118">Warning</span></span>  <br/> |<span data-ttu-id="85dbc-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="85dbc-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="85dbc-120">Fehler (ungefährer Wortlaut)</span><span class="sxs-lookup"><span data-stu-id="85dbc-120">Error</span></span>  <br/> |<span data-ttu-id="85dbc-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="85dbc-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="85dbc-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="85dbc-122">Child elements</span></span>

|<span data-ttu-id="85dbc-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="85dbc-123">**Element**</span></span>|<span data-ttu-id="85dbc-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85dbc-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85dbc-125">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="85dbc-125">SearchableMailboxes</span></span>](searchablemailboxes.md) <br/> |<span data-ttu-id="85dbc-126">Enthält ein Array der Postfächer, die von einer **GetSearchableMailboxes** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="85dbc-126">Contains an array of the mailboxes returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
|[<span data-ttu-id="85dbc-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="85dbc-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="85dbc-128">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="85dbc-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="85dbc-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="85dbc-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="85dbc-130">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="85dbc-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="85dbc-131">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="85dbc-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="85dbc-132">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="85dbc-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="85dbc-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="85dbc-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="85dbc-134">Stellt Statusinformationen zur Anforderung bereit.</span><span class="sxs-lookup"><span data-stu-id="85dbc-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="85dbc-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="85dbc-135">Parent elements</span></span>

|<span data-ttu-id="85dbc-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="85dbc-136">**Element**</span></span>|<span data-ttu-id="85dbc-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85dbc-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85dbc-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="85dbc-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="85dbc-139">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="85dbc-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85dbc-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85dbc-140">Remarks</span></span>

<span data-ttu-id="85dbc-141">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="85dbc-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="85dbc-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="85dbc-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85dbc-143">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="85dbc-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85dbc-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="85dbc-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="85dbc-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="85dbc-145">Schema Name</span></span>  <br/> |<span data-ttu-id="85dbc-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="85dbc-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="85dbc-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="85dbc-147">Validation File</span></span>  <br/> |<span data-ttu-id="85dbc-148">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="85dbc-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="85dbc-149">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="85dbc-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="85dbc-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85dbc-150">See also</span></span>



- [<span data-ttu-id="85dbc-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="85dbc-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

