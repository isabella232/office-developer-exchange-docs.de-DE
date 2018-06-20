---
title: GetClientAccessTokenResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45ca2500-ceab-4c98-9576-cb9e158e5896
description: Das GetClientAccessTokenResponseMessage-Element gibt die Antwortnachricht für eine Anforderung GetClientAccessToken.
ms.openlocfilehash: 16fe684dd48f77156ed88d02a6ae7b8f3312cd87
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758598"
---
# <a name="getclientaccesstokenresponsemessage"></a><span data-ttu-id="da6c5-103">GetClientAccessTokenResponseMessage</span><span class="sxs-lookup"><span data-stu-id="da6c5-103">GetClientAccessTokenResponseMessage</span></span>

<span data-ttu-id="da6c5-104">Das **GetClientAccessTokenResponseMessage** -Element gibt die Antwortnachricht für eine Anforderung **GetClientAccessToken** .</span><span class="sxs-lookup"><span data-stu-id="da6c5-104">The **GetClientAccessTokenResponseMessage** element specifies the response message for a **GetClientAccessToken** request.</span></span> 
  
```XML
<GetClientAccessTokenResponseMessage ResponseClass=" Success | Warning | Error ">
    <Token/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetClientAccessTokenResponseMessage>
```

 <span data-ttu-id="da6c5-105">**GetClientAccessTokenResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="da6c5-105">**GetClientAccessTokenResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="da6c5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="da6c5-106">Attributes and elements</span></span>

<span data-ttu-id="da6c5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="da6c5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da6c5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="da6c5-108">Attributes</span></span>

|<span data-ttu-id="da6c5-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="da6c5-109">**Attribute**</span></span>|<span data-ttu-id="da6c5-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da6c5-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="da6c5-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="da6c5-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="da6c5-112">Gibt die Klasse der Antwort.</span><span class="sxs-lookup"><span data-stu-id="da6c5-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="da6c5-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="da6c5-113">ResponseClass</span></span>

|<span data-ttu-id="da6c5-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="da6c5-114">**Value**</span></span>|<span data-ttu-id="da6c5-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da6c5-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="da6c5-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="da6c5-116">Success</span></span>  <br/> |<span data-ttu-id="da6c5-117">Gibt Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="da6c5-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="da6c5-118">Warning</span><span class="sxs-lookup"><span data-stu-id="da6c5-118">Warning</span></span>  <br/> |<span data-ttu-id="da6c5-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="da6c5-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="da6c5-120">Fehler</span><span class="sxs-lookup"><span data-stu-id="da6c5-120">Error</span></span>  <br/> |<span data-ttu-id="da6c5-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="da6c5-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="da6c5-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da6c5-122">Child elements</span></span>

|<span data-ttu-id="da6c5-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="da6c5-123">**Element**</span></span>|<span data-ttu-id="da6c5-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da6c5-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da6c5-125">Token (ClientAccessTokenType)</span><span class="sxs-lookup"><span data-stu-id="da6c5-125">Token (ClientAccessTokenType)</span></span>](token-clientaccesstokentype.md) <br/> |<span data-ttu-id="da6c5-126">Gibt ein Zugriffstoken für den Client an.</span><span class="sxs-lookup"><span data-stu-id="da6c5-126">Specifies a client access token.</span></span>  <br/> |
|[<span data-ttu-id="da6c5-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="da6c5-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="da6c5-128">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="da6c5-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="da6c5-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="da6c5-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="da6c5-130">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="da6c5-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="da6c5-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="da6c5-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="da6c5-132">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="da6c5-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="da6c5-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="da6c5-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="da6c5-134">Enthält Statusinformationen über die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="da6c5-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="da6c5-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da6c5-135">Parent elements</span></span>

|<span data-ttu-id="da6c5-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="da6c5-136">**Element**</span></span>|<span data-ttu-id="da6c5-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da6c5-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da6c5-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="da6c5-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="da6c5-139">Enthält die Antwortnachrichten für eine Exchange-Webdienste (EWS)-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="da6c5-139">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da6c5-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="da6c5-140">Remarks</span></span>

<span data-ttu-id="da6c5-141">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="da6c5-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="da6c5-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="da6c5-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="da6c5-143">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="da6c5-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da6c5-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="da6c5-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="da6c5-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="da6c5-145">Schema Name</span></span>  <br/> |<span data-ttu-id="da6c5-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="da6c5-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="da6c5-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="da6c5-147">Validation File</span></span>  <br/> |<span data-ttu-id="da6c5-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="da6c5-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="da6c5-149">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="da6c5-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="da6c5-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da6c5-150">See also</span></span>



- [<span data-ttu-id="da6c5-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="da6c5-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

