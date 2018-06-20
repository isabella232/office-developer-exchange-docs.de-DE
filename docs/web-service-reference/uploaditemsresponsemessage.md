---
title: UploadItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UploadItemsResponseMessage
api_type:
- schema
ms.assetid: 03febd08-c015-4009-b291-1b4296182ffe
description: Das UploadItemsResponseMessage-Element enthält den Status und die Ergebnisse einer Anforderung für ein einzelnes Postfach Element hochladen.
ms.openlocfilehash: 9a1a33011aa1e240ab7e15794e2e89401238ffda
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839422"
---
# <a name="uploaditemsresponsemessage"></a><span data-ttu-id="e8184-103">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e8184-103">UploadItemsResponseMessage</span></span>

<span data-ttu-id="e8184-104">Das **UploadItemsResponseMessage** -Element enthält den Status und die Ergebnisse einer Anforderung für ein einzelnes Postfach Element hochladen.</span><span class="sxs-lookup"><span data-stu-id="e8184-104">The **UploadItemsResponseMessage** element contains the status and results of a request to upload a single mailbox item.</span></span> 
  
- [<span data-ttu-id="e8184-105">UploadItemsResponse</span><span class="sxs-lookup"><span data-stu-id="e8184-105">UploadItemsResponse</span></span>](uploaditemsresponse.md) 
- [<span data-ttu-id="e8184-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e8184-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="e8184-107">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e8184-107">UploadItemsResponseMessage</span></span>](uploaditemsresponsemessage.md)
  
```XML
<UploadItemsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ItemId/>
</UploadItemsResponseMessage>
```

 <span data-ttu-id="e8184-108">**UploadItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e8184-108">**UploadItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e8184-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e8184-109">Attributes and elements</span></span>

<span data-ttu-id="e8184-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e8184-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8184-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="e8184-111">Attributes</span></span>

|<span data-ttu-id="e8184-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e8184-112">**Attribute**</span></span>|<span data-ttu-id="e8184-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e8184-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8184-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="e8184-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="e8184-115">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="e8184-115">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="e8184-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="e8184-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="e8184-117">-Success</span><span class="sxs-lookup"><span data-stu-id="e8184-117">-  Success</span></span>  <br/><span data-ttu-id="e8184-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="e8184-118">-  Warning</span></span>  <br/><span data-ttu-id="e8184-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="e8184-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="e8184-120">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="e8184-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="e8184-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e8184-121">**Value**</span></span>|<span data-ttu-id="e8184-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e8184-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8184-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="e8184-123">**Success**</span></span> <br/> |<span data-ttu-id="e8184-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="e8184-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="e8184-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="e8184-125">**Warning**</span></span> <br/> | <span data-ttu-id="e8184-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="e8184-126">Describes a request that was not processed.</span></span> <span data-ttu-id="e8184-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="e8184-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="e8184-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="e8184-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="e8184-129">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="e8184-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="e8184-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="e8184-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="e8184-131">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="e8184-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="e8184-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="e8184-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="e8184-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="e8184-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="e8184-134">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="e8184-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="e8184-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="e8184-135">**Error**</span></span> <br/> | <span data-ttu-id="e8184-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e8184-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="e8184-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="e8184-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="e8184-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="e8184-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="e8184-139">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="e8184-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="e8184-140">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="e8184-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="e8184-141">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="e8184-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="e8184-142">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="e8184-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="e8184-143">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="e8184-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="e8184-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="e8184-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e8184-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e8184-145">Child elements</span></span>

|<span data-ttu-id="e8184-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="e8184-146">**Element**</span></span>|<span data-ttu-id="e8184-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e8184-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8184-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="e8184-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="e8184-149">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="e8184-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="e8184-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e8184-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="e8184-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="e8184-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="e8184-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e8184-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="e8184-153">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="e8184-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="e8184-154">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="e8184-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="e8184-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="e8184-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="e8184-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="e8184-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="e8184-157">ItemId</span><span class="sxs-lookup"><span data-stu-id="e8184-157">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="e8184-158">Enthält die Element-ID eines Elements hochgeladenen.</span><span class="sxs-lookup"><span data-stu-id="e8184-158">Contains the item identifier of an uploaded item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e8184-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e8184-159">Parent elements</span></span>

|<span data-ttu-id="e8184-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="e8184-160">**Element**</span></span>|<span data-ttu-id="e8184-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e8184-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8184-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e8184-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="e8184-163">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e8184-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e8184-164">Textwert</span><span class="sxs-lookup"><span data-stu-id="e8184-164">Text value</span></span>

<span data-ttu-id="e8184-165">Keine.</span><span class="sxs-lookup"><span data-stu-id="e8184-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e8184-166">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e8184-166">Remarks</span></span>

<span data-ttu-id="e8184-167">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e8184-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e8184-168">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e8184-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8184-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="e8184-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e8184-170">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e8184-170">Schema Name</span></span>  <br/> |<span data-ttu-id="e8184-171">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="e8184-171">Message schema</span></span>  <br/> |
|<span data-ttu-id="e8184-172">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e8184-172">Validation File</span></span>  <br/> |<span data-ttu-id="e8184-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e8184-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e8184-174">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e8184-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="e8184-175">False</span><span class="sxs-lookup"><span data-stu-id="e8184-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8184-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8184-176">See also</span></span>

- [<span data-ttu-id="e8184-177">ExportItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e8184-177">ExportItems operation</span></span>](exportitems-operation.md)
- [<span data-ttu-id="e8184-178">UploadItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e8184-178">UploadItems operation</span></span>](uploaditems-operation.md)
- [<span data-ttu-id="e8184-179">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e8184-179">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

