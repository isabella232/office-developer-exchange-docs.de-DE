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
description: Das FindItemResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen FindItem-Vorgangsanforderung.
ms.openlocfilehash: ca941e0c7e5b9b08f6f495ccae0d634d72b8f429
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462535"
---
# <a name="finditemresponsemessage"></a><span data-ttu-id="d6d55-103">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d6d55-103">FindItemResponseMessage</span></span>

<span data-ttu-id="d6d55-104">Das **FindItemResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [FindItem-Vorgangs](finditem-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d6d55-104">The **FindItemResponseMessage** element contains the status and result of a single [FindItem operation](finditem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="d6d55-105">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="d6d55-105">FindItemResponse</span></span>](finditemresponse.md) 
- [<span data-ttu-id="d6d55-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d6d55-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="d6d55-107">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d6d55-107">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
  
```xml
<FindItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RootFolder/>
</FindItemResponseMessage>
```

 <span data-ttu-id="d6d55-108">**FindItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="d6d55-108">**FindItemResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d6d55-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d6d55-109">Attributes and elements</span></span>

<span data-ttu-id="d6d55-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d6d55-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d6d55-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="d6d55-111">Attributes</span></span>

|<span data-ttu-id="d6d55-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d6d55-112">**Attribute**</span></span>|<span data-ttu-id="d6d55-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6d55-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6d55-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="d6d55-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="d6d55-115">Beschreibt den Status einer [FindItem-Vorgangs](finditem-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="d6d55-115">Describes the status of a [FindItem operation](finditem-operation.md) response.</span></span><br/><br/> <span data-ttu-id="d6d55-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="d6d55-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="d6d55-117">-Success</span><span class="sxs-lookup"><span data-stu-id="d6d55-117">-  Success</span></span>  <br/><span data-ttu-id="d6d55-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="d6d55-118">-  Warning</span></span>  <br/><span data-ttu-id="d6d55-119">-Error</span><span class="sxs-lookup"><span data-stu-id="d6d55-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="d6d55-120">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="d6d55-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="d6d55-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d6d55-121">**Value**</span></span>|<span data-ttu-id="d6d55-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6d55-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6d55-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="d6d55-123">**Success**</span></span> <br/> |<span data-ttu-id="d6d55-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="d6d55-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="d6d55-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="d6d55-125">**Warning**</span></span> <br/> | <span data-ttu-id="d6d55-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="d6d55-126">Describes a request that was not processed.</span></span> <span data-ttu-id="d6d55-127">Es kann eine Warnung zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d6d55-127">A warning may be returned if an error occurred while processing an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="d6d55-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="d6d55-128">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="d6d55-129">– Der Exchange-Informationsspeicher wird während des Batches offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="d6d55-129">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="d6d55-130">-Active Directory-Domänendienste (AD DS) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="d6d55-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="d6d55-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="d6d55-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="d6d55-132">-Die Nachrichtendatenbank (MDB) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="d6d55-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="d6d55-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="d6d55-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="d6d55-134">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="d6d55-134">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="d6d55-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="d6d55-135">**Error**</span></span> <br/> | <span data-ttu-id="d6d55-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d6d55-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="d6d55-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="d6d55-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="d6d55-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="d6d55-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="d6d55-139">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="d6d55-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="d6d55-140">-Ein unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="d6d55-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="d6d55-141">-Ein Attribut oder Element, das im Kontext ungültig ist</span><span class="sxs-lookup"><span data-stu-id="d6d55-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="d6d55-142">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client</span><span class="sxs-lookup"><span data-stu-id="d6d55-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="d6d55-143">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="d6d55-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="d6d55-144">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="d6d55-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d6d55-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6d55-145">Child elements</span></span>

|<span data-ttu-id="d6d55-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6d55-146">**Element**</span></span>|<span data-ttu-id="d6d55-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6d55-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d6d55-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="d6d55-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="d6d55-149">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="d6d55-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="d6d55-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d6d55-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="d6d55-151">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d6d55-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="d6d55-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d6d55-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="d6d55-153">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="d6d55-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="d6d55-154">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="d6d55-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="d6d55-155">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="d6d55-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="d6d55-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="d6d55-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="d6d55-157">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="d6d55-157">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md) <br/> |<span data-ttu-id="d6d55-158">Enthält die Ergebnisse einer Suche eines einzelnen Stammordners während eines FindItem- [Vorgangs](finditem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="d6d55-158">Contains the results from a search of a single root folder during a [FindItem operation](finditem-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d6d55-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6d55-159">Parent elements</span></span>

|<span data-ttu-id="d6d55-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6d55-160">**Element**</span></span>|<span data-ttu-id="d6d55-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6d55-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d6d55-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d6d55-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="d6d55-163">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d6d55-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6d55-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6d55-164">Remarks</span></span>

<span data-ttu-id="d6d55-165">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d6d55-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d6d55-166">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d6d55-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6d55-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="d6d55-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d6d55-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d6d55-168">Schema name</span></span>  <br/> |<span data-ttu-id="d6d55-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d6d55-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d6d55-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d6d55-170">Validation file</span></span>  <br/> |<span data-ttu-id="d6d55-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d6d55-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d6d55-172">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d6d55-172">Can be empty</span></span>  <br/> |<span data-ttu-id="d6d55-173">False</span><span class="sxs-lookup"><span data-stu-id="d6d55-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6d55-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6d55-174">See also</span></span>

- [<span data-ttu-id="d6d55-175">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d6d55-175">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="d6d55-176">Suchen von Elementen</span><span class="sxs-lookup"><span data-stu-id="d6d55-176">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

