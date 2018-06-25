---
title: FindItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindItemResponseMessage
api_type:
- schema
ms.assetid: fb2cd399-8a04-4f26-9091-993134ed1d15
description: Das FindItemResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung FindItem Vorgang.
ms.openlocfilehash: 0a4bfb3ba8d85b0bff0d03f043be865ce7276229
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758462"
---
# <a name="finditemresponsemessage"></a><span data-ttu-id="f4c29-103">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f4c29-103">FindItemResponseMessage</span></span>

<span data-ttu-id="f4c29-104">Das **FindItemResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [FindItem Vorgang](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="f4c29-104">The **FindItemResponseMessage** element contains the status and result of a single [FindItem operation](finditem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="f4c29-105">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="f4c29-105">FindItemResponse</span></span>](finditemresponse.md) 
- [<span data-ttu-id="f4c29-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f4c29-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="f4c29-107">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f4c29-107">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
  
```xml
<FindItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RootFolder/>
</FindItemResponseMessage>
```

 <span data-ttu-id="f4c29-108">**FindItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f4c29-108">**FindItemResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f4c29-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f4c29-109">Attributes and elements</span></span>

<span data-ttu-id="f4c29-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f4c29-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4c29-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="f4c29-111">Attributes</span></span>

|<span data-ttu-id="f4c29-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f4c29-112">**Attribute**</span></span>|<span data-ttu-id="f4c29-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f4c29-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f4c29-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="f4c29-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="f4c29-115">Beschreibt den Status einer Antwort [FindItem Vorgang](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="f4c29-115">Describes the status of a [FindItem operation](finditem-operation.md) response.</span></span><br/><br/> <span data-ttu-id="f4c29-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="f4c29-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="f4c29-117">-Success</span><span class="sxs-lookup"><span data-stu-id="f4c29-117">-  Success</span></span>  <br/><span data-ttu-id="f4c29-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="f4c29-118">-  Warning</span></span>  <br/><span data-ttu-id="f4c29-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="f4c29-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="f4c29-120">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="f4c29-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="f4c29-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f4c29-121">**Value**</span></span>|<span data-ttu-id="f4c29-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f4c29-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f4c29-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="f4c29-123">**Success**</span></span> <br/> |<span data-ttu-id="f4c29-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="f4c29-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="f4c29-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="f4c29-125">**Warning**</span></span> <br/> | <span data-ttu-id="f4c29-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="f4c29-126">Describes a request that was not processed.</span></span> <span data-ttu-id="f4c29-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler während der Verarbeitung eines Elements in der Anforderung verarbeitet hat, und die nachfolgenden Elemente konnte nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="f4c29-127">A warning may be returned if an error occurred while processing an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="f4c29-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="f4c29-128">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="f4c29-129">-Der Exchange-Speicher wird während der Batchaktualisierung offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="f4c29-129">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="f4c29-130">-Active Directory-Domänendienste (AD DS) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="f4c29-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="f4c29-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="f4c29-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="f4c29-132">-Die Nachrichtendatenbank (MDB) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="f4c29-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="f4c29-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="f4c29-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="f4c29-134">-Ein Kontingent überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="f4c29-134">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="f4c29-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="f4c29-135">**Error**</span></span> <br/> | <span data-ttu-id="f4c29-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f4c29-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="f4c29-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="f4c29-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="f4c29-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="f4c29-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="f4c29-139">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="f4c29-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="f4c29-140">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="f4c29-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="f4c29-141">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="f4c29-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="f4c29-142">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="f4c29-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="f4c29-143">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="f4c29-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="f4c29-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="f4c29-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f4c29-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f4c29-145">Child elements</span></span>

|<span data-ttu-id="f4c29-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="f4c29-146">**Element**</span></span>|<span data-ttu-id="f4c29-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f4c29-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4c29-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="f4c29-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="f4c29-149">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="f4c29-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="f4c29-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f4c29-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="f4c29-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="f4c29-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="f4c29-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f4c29-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="f4c29-153">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f4c29-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="f4c29-154">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="f4c29-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="f4c29-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="f4c29-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="f4c29-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="f4c29-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="f4c29-157">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="f4c29-157">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md) <br/> |<span data-ttu-id="f4c29-158">Enthält die Ergebnisse einer Suche in einer einzelnen Stammordner während einer [FindItem Vorgang](finditem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="f4c29-158">Contains the results from a search of a single root folder during a [FindItem operation](finditem-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f4c29-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f4c29-159">Parent elements</span></span>

|<span data-ttu-id="f4c29-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="f4c29-160">**Element**</span></span>|<span data-ttu-id="f4c29-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f4c29-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4c29-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f4c29-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="f4c29-163">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f4c29-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4c29-164">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f4c29-164">Remarks</span></span>

<span data-ttu-id="f4c29-165">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f4c29-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f4c29-166">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f4c29-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4c29-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="f4c29-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f4c29-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f4c29-168">Schema name</span></span>  <br/> |<span data-ttu-id="f4c29-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f4c29-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f4c29-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f4c29-170">Validation file</span></span>  <br/> |<span data-ttu-id="f4c29-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f4c29-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f4c29-172">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f4c29-172">Can be empty</span></span>  <br/> |<span data-ttu-id="f4c29-173">False</span><span class="sxs-lookup"><span data-stu-id="f4c29-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4c29-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4c29-174">See also</span></span>

- [<span data-ttu-id="f4c29-175">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f4c29-175">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="f4c29-176">Finding Items</span><span class="sxs-lookup"><span data-stu-id="f4c29-176">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

