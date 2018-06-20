---
title: ApplyConversationActionResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ApplyConversationActionResponseMessage
api_type:
- schema
ms.assetid: a09edc89-7f2f-4846-a3a5-06694c97b9f6
description: Das ApplyConversationActionResponseMessage-Element enthält den Status und die Ergebnisse einer ApplyConversationAction Vorgang Anforderung.
ms.openlocfilehash: d8c5571cfc9c2ea6aaf09cb26a0e47e4abfc3f40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757356"
---
# <a name="applyconversationactionresponsemessage"></a><span data-ttu-id="b823b-103">ApplyConversationActionResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b823b-103">ApplyConversationActionResponseMessage</span></span>

<span data-ttu-id="b823b-104">Das **ApplyConversationActionResponseMessage** -Element enthält den Status und die Ergebnisse einer Anforderung [ApplyConversationAction Vorgang](applyconversationaction-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="b823b-104">The **ApplyConversationActionResponseMessage** element contains the status and results of an [ApplyConversationAction operation](applyconversationaction-operation.md) request.</span></span>  
  
- [<span data-ttu-id="b823b-105">ApplyConversationActionResponse</span><span class="sxs-lookup"><span data-stu-id="b823b-105">ApplyConversationActionResponse</span></span>](applyconversationactionresponse.md)
- [<span data-ttu-id="b823b-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b823b-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="b823b-107">ApplyConversationActionResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b823b-107">ApplyConversationActionResponseMessage</span></span>](applyconversationactionresponsemessage.md)
  
```XML
<ApplyConversationActionResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</ApplyConversationActionResponseMessage>
```

 <span data-ttu-id="b823b-108">**ApplyConversationActionResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="b823b-108">**ApplyConversationActionResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b823b-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b823b-109">Attributes and elements</span></span>

<span data-ttu-id="b823b-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b823b-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b823b-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="b823b-111">Attributes</span></span>

|<span data-ttu-id="b823b-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b823b-112">**Attribute**</span></span>|<span data-ttu-id="b823b-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b823b-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b823b-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="b823b-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="b823b-115">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="b823b-115">Describes the status of the response.</span></span><br/><br/><span data-ttu-id="b823b-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="b823b-116">The following values are valid for this attribute:</span></span><ul><li><span data-ttu-id="b823b-117">Erfolg</span><span class="sxs-lookup"><span data-stu-id="b823b-117">Success</span></span></li><li><span data-ttu-id="b823b-118">Warning</span><span class="sxs-lookup"><span data-stu-id="b823b-118">Warning</span></span></li><li><span data-ttu-id="b823b-119">Fehler</span><span class="sxs-lookup"><span data-stu-id="b823b-119">Error</span></span></li></ul> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="b823b-120">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="b823b-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="b823b-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b823b-121">**Value**</span></span>|<span data-ttu-id="b823b-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b823b-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b823b-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="b823b-123">**Success**</span></span> <br/> |<span data-ttu-id="b823b-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="b823b-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="b823b-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="b823b-125">**Warning**</span></span> <br/> | <span data-ttu-id="b823b-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="b823b-126">Describes a request that was not processed.</span></span> <span data-ttu-id="b823b-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="b823b-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="b823b-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="b823b-128">The following are examples of sources of warnings:</span></span><ul><li><span data-ttu-id="b823b-129">Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="b823b-129">The Exchange store is offline during the batch.</span></span></li><li><span data-ttu-id="b823b-130">Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="b823b-130">Active Directory Domain Services (AD DS) is offline.</span></span></li><li><span data-ttu-id="b823b-131">Postfächer verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="b823b-131">Mailboxes were moved.</span></span></li><li><span data-ttu-id="b823b-132">Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="b823b-132">The message database (MDB) is offline.</span></span></li><li><span data-ttu-id="b823b-133">Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="b823b-133">A password is expired.</span></span></li><li><span data-ttu-id="b823b-134">Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="b823b-134">A quota has been exceeded.</span></span></li></ul> |
|<span data-ttu-id="b823b-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="b823b-135">**Error**</span></span> <br/> | <span data-ttu-id="b823b-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b823b-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="b823b-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="b823b-137">The following are examples of sources of errors:</span></span>  <ul><li><span data-ttu-id="b823b-138">Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="b823b-138">Invalid attributes or elements</span></span></li><li><span data-ttu-id="b823b-139">Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="b823b-139">Attributes or elements that are out of range</span></span></li><li><span data-ttu-id="b823b-140">Ein unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="b823b-140">An unknown tag</span></span>  </li><li><span data-ttu-id="b823b-141">Ein Attribut oder ein Element, das nicht im Kontext gültig ist</span><span class="sxs-lookup"><span data-stu-id="b823b-141">An attribute or element that is not valid in the context</span></span></li><li><span data-ttu-id="b823b-142">Ein Versuch nicht autorisierten Zugriff von jedem client</span><span class="sxs-lookup"><span data-stu-id="b823b-142">An unauthorized access attempt by any client</span></span></li><li><span data-ttu-id="b823b-143">Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="b823b-143">A server-side failure in response to a valid client-side call</span></span></li></ul><span data-ttu-id="b823b-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="b823b-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b823b-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b823b-145">Child elements</span></span>

|<span data-ttu-id="b823b-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="b823b-146">**Element**</span></span>|<span data-ttu-id="b823b-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b823b-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b823b-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="b823b-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="b823b-149">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="b823b-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="b823b-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b823b-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="b823b-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="b823b-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="b823b-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b823b-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="b823b-153">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="b823b-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="b823b-154">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="b823b-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="b823b-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="b823b-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="b823b-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="b823b-156">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b823b-157">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b823b-157">Parent elements</span></span>

|<span data-ttu-id="b823b-158">**Element**</span><span class="sxs-lookup"><span data-stu-id="b823b-158">**Element**</span></span>|<span data-ttu-id="b823b-159">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b823b-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b823b-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b823b-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="b823b-161">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b823b-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b823b-162">Textwert</span><span class="sxs-lookup"><span data-stu-id="b823b-162">Text value</span></span>

<span data-ttu-id="b823b-163">Keine.</span><span class="sxs-lookup"><span data-stu-id="b823b-163">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b823b-164">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b823b-164">Remarks</span></span>

<span data-ttu-id="b823b-165">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b823b-165">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="b823b-166">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="b823b-166">Version differences</span></span>

<span data-ttu-id="b823b-167">In Versionen von Exchange, beginnend mit Build 15.00.0986.00 ist das **ApplyConversationActionResponseMessage** -Element vom Typ **ApplyConversationActionResponseMessageType**.</span><span class="sxs-lookup"><span data-stu-id="b823b-167">In versions of Exchange starting with build 15.00.0986.00, the **ApplyConversationActionResponseMessage** element is of type **ApplyConversationActionResponseMessageType**.</span></span> <span data-ttu-id="b823b-168">In früheren Versionen ist das Element vom Typ **ResponseMessageType**.</span><span class="sxs-lookup"><span data-stu-id="b823b-168">In previous versions, the element is of type **ResponseMessageType**.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b823b-169">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b823b-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b823b-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="b823b-170">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b823b-171">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b823b-171">Schema Name</span></span>  <br/> |<span data-ttu-id="b823b-172">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b823b-172">Message schema</span></span>  <br/> |
|<span data-ttu-id="b823b-173">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b823b-173">Validation File</span></span>  <br/> |<span data-ttu-id="b823b-174">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b823b-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b823b-175">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b823b-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="b823b-176">False</span><span class="sxs-lookup"><span data-stu-id="b823b-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b823b-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b823b-177">See also</span></span>

- [<span data-ttu-id="b823b-178">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b823b-178">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="b823b-179">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b823b-179">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

