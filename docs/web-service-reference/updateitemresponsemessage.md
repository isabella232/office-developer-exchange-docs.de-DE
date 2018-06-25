---
title: UpdateItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItemResponseMessage
api_type:
- schema
ms.assetid: dc585b05-5afc-4c74-8763-5a54f9a650ec
description: Das UpdateItemResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung UpdateItem Vorgang.
ms.openlocfilehash: c971657813784e68a01539899e8fabea67847325
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839386"
---
# <a name="updateitemresponsemessage"></a><span data-ttu-id="ec94a-103">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ec94a-103">UpdateItemResponseMessage</span></span>

<span data-ttu-id="ec94a-104">Das **UpdateItemResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [UpdateItem Vorgang](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ec94a-104">The **UpdateItemResponseMessage** element contains the status and result of a single [UpdateItem operation](updateitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="ec94a-105">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="ec94a-105">UpdateItemResponse</span></span>](updateitemresponse.md)
- [<span data-ttu-id="ec94a-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ec94a-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="ec94a-107">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ec94a-107">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
  
```xml
<UpdateItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
   <ConflictResults/>
</UpdateItemResponseMessage>
```

 <span data-ttu-id="ec94a-108">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ec94a-108">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ec94a-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ec94a-109">Attributes and elements</span></span>

<span data-ttu-id="ec94a-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ec94a-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec94a-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="ec94a-111">Attributes</span></span>

|<span data-ttu-id="ec94a-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ec94a-112">**Attribute**</span></span>|<span data-ttu-id="ec94a-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec94a-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ec94a-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="ec94a-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="ec94a-115">Beschreibt den Status einer Antwort [UpdateItem Vorgang](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ec94a-115">Describes the status of an [UpdateItem operation](updateitem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="ec94a-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="ec94a-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="ec94a-117">-Success</span><span class="sxs-lookup"><span data-stu-id="ec94a-117">-  Success</span></span>  <br/><span data-ttu-id="ec94a-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="ec94a-118">-  Warning</span></span>  <br/><span data-ttu-id="ec94a-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="ec94a-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="ec94a-120">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="ec94a-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="ec94a-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ec94a-121">**Value**</span></span>|<span data-ttu-id="ec94a-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec94a-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ec94a-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="ec94a-123">**Success**</span></span> <br/> |<span data-ttu-id="ec94a-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ec94a-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="ec94a-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="ec94a-125">**Warning**</span></span> <br/> | <span data-ttu-id="ec94a-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ec94a-126">Describes a request that was not processed.</span></span> <span data-ttu-id="ec94a-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde und nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="ec94a-127">A warning may be returned if an error occurred while an item in the request was processed and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="ec94a-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="ec94a-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="ec94a-129">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="ec94a-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="ec94a-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="ec94a-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="ec94a-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="ec94a-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="ec94a-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="ec94a-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="ec94a-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="ec94a-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="ec94a-134">-Ein Kontingent überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="ec94a-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="ec94a-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="ec94a-135">**Error**</span></span> <br/> | <span data-ttu-id="ec94a-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ec94a-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="ec94a-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="ec94a-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="ec94a-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="ec94a-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="ec94a-139">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="ec94a-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="ec94a-140">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="ec94a-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="ec94a-141">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ec94a-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="ec94a-142">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="ec94a-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="ec94a-143">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="ec94a-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="ec94a-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="ec94a-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ec94a-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec94a-145">Child elements</span></span>

|<span data-ttu-id="ec94a-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="ec94a-146">**Element**</span></span>|<span data-ttu-id="ec94a-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec94a-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec94a-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="ec94a-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ec94a-149">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="ec94a-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ec94a-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ec94a-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ec94a-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="ec94a-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="ec94a-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ec94a-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ec94a-153">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="ec94a-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="ec94a-154">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="ec94a-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="ec94a-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="ec94a-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ec94a-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="ec94a-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="ec94a-157">Elemente</span><span class="sxs-lookup"><span data-stu-id="ec94a-157">Items</span></span>](items.md) <br/> |<span data-ttu-id="ec94a-158">Enthält ein Array von aktualisierten Elemente.</span><span class="sxs-lookup"><span data-stu-id="ec94a-158">Contains an array of updated items.</span></span>  <br/> |
|[<span data-ttu-id="ec94a-159">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="ec94a-159">ConflictResults</span></span>](conflictresults.md) <br/> |<span data-ttu-id="ec94a-160">Enthält die Anzahl der Konflikte in einer Antwort [UpdateItem Vorgang](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ec94a-160">Contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ec94a-161">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec94a-161">Parent elements</span></span>

|<span data-ttu-id="ec94a-162">**Element**</span><span class="sxs-lookup"><span data-stu-id="ec94a-162">**Element**</span></span>|<span data-ttu-id="ec94a-163">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec94a-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec94a-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ec94a-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="ec94a-165">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ec94a-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec94a-166">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ec94a-166">Remarks</span></span>

<span data-ttu-id="ec94a-167">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ec94a-167">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ec94a-168">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ec94a-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec94a-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="ec94a-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ec94a-170">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ec94a-170">Schema Name</span></span>  <br/> |<span data-ttu-id="ec94a-171">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ec94a-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ec94a-172">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ec94a-172">Validation File</span></span>  <br/> |<span data-ttu-id="ec94a-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ec94a-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ec94a-174">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ec94a-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="ec94a-175">False</span><span class="sxs-lookup"><span data-stu-id="ec94a-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec94a-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec94a-176">See also</span></span>

- [<span data-ttu-id="ec94a-177">UpdateItem Operation</span><span class="sxs-lookup"><span data-stu-id="ec94a-177">UpdateItem operation</span></span>](updateitem-operation.md)
- [<span data-ttu-id="ec94a-178">Aktualisierung von Kontakten</span><span class="sxs-lookup"><span data-stu-id="ec94a-178">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
- [<span data-ttu-id="ec94a-179">Aktualisieren der Vorgänge</span><span class="sxs-lookup"><span data-stu-id="ec94a-179">Updating Tasks</span></span>](http://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

