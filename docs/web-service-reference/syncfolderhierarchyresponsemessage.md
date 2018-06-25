---
title: SyncFolderHierarchyResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchyResponseMessage
api_type:
- schema
ms.assetid: ab96c649-1005-401c-9d1c-9917f0b19a60
description: Das SyncFolderHierarchyResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung SyncFolderHierarchy Vorgang.
ms.openlocfilehash: e4141299b128ffb7f67c55bbb09390b77a79e043
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839149"
---
# <a name="syncfolderhierarchyresponsemessage"></a><span data-ttu-id="b301d-103">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b301d-103">SyncFolderHierarchyResponseMessage</span></span>

<span data-ttu-id="b301d-104">Das **SyncFolderHierarchyResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [SyncFolderHierarchy Vorgang](syncfolderhierarchy-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="b301d-104">The **SyncFolderHierarchyResponseMessage** element contains the status and result of a single [SyncFolderHierarchy operation](syncfolderhierarchy-operation.md) request.</span></span> 
  
- [<span data-ttu-id="b301d-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="b301d-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md) 
- [<span data-ttu-id="b301d-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b301d-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="b301d-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b301d-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
```xml
<SyncFolderHierarchyResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <SyncState/>
   <IncludesLastFolderInRange/>
   <Changes/>
</SyncFolderHierarchyResponseMessage>
```

 <span data-ttu-id="b301d-108">**SyncFolderHierarchyResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="b301d-108">**SyncFolderHierarchyResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b301d-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b301d-109">Attributes and elements</span></span>

<span data-ttu-id="b301d-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b301d-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b301d-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="b301d-111">Attributes</span></span>

|<span data-ttu-id="b301d-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b301d-112">**Attribute**</span></span>|<span data-ttu-id="b301d-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b301d-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b301d-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="b301d-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="b301d-115">Beschreibt den Status einer Antwort [SyncFolderHierarchy Vorgang](syncfolderhierarchy-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="b301d-115">Describes the status of a [SyncFolderHierarchy operation](syncfolderhierarchy-operation.md) response.</span></span> <br/><br/><span data-ttu-id="b301d-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="b301d-116">The following values are valid for this attribute:</span></span><br/>  <br/><span data-ttu-id="b301d-117">-Success</span><span class="sxs-lookup"><span data-stu-id="b301d-117">-  Success</span></span>  <br/><span data-ttu-id="b301d-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="b301d-118">-  Warning</span></span>  <br/><span data-ttu-id="b301d-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="b301d-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="b301d-120">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="b301d-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="b301d-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b301d-121">**Value**</span></span>|<span data-ttu-id="b301d-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b301d-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b301d-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="b301d-123">**Success**</span></span> <br/> |<span data-ttu-id="b301d-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="b301d-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="b301d-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="b301d-125">**Warning**</span></span> <br/> | <span data-ttu-id="b301d-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="b301d-126">Describes a request that was not processed.</span></span> <span data-ttu-id="b301d-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="b301d-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="b301d-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="b301d-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="b301d-129">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="b301d-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="b301d-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="b301d-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="b301d-131">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="b301d-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="b301d-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="b301d-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="b301d-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="b301d-133">-  A password has expired.</span></span>  <br/><span data-ttu-id="b301d-134">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="b301d-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="b301d-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="b301d-135">**Error**</span></span> <br/> | <span data-ttu-id="b301d-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b301d-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="b301d-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="b301d-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="b301d-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="b301d-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="b301d-139">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="b301d-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="b301d-140">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="b301d-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="b301d-141">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="b301d-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="b301d-142">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="b301d-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="b301d-143">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="b301d-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="b301d-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="b301d-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b301d-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b301d-145">Child elements</span></span>

|<span data-ttu-id="b301d-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="b301d-146">**Element**</span></span>|<span data-ttu-id="b301d-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b301d-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b301d-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="b301d-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="b301d-149">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="b301d-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="b301d-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b301d-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="b301d-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="b301d-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="b301d-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b301d-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="b301d-153">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="b301d-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="b301d-154">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="b301d-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="b301d-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="b301d-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="b301d-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="b301d-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="b301d-157">Synchronisierungsstatus</span><span class="sxs-lookup"><span data-stu-id="b301d-157">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b301d-158">Enthält eine base64-codierten Format von der Synchronisierung von Daten, die nach jeder Anforderung erfolgreich aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b301d-158">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="b301d-159">Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b301d-159">This is used to identify the synchronization state.</span></span>  <br/> |
|[<span data-ttu-id="b301d-160">IncludesLastFolderInRange</span><span class="sxs-lookup"><span data-stu-id="b301d-160">IncludesLastFolderInRange</span></span>](includeslastfolderinrange.md) <br/> |<span data-ttu-id="b301d-161">Gibt an, ob das letzte Element synchronisieren in der Antwort aufgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="b301d-161">Indicates whether the last item to synchronize has been included in the response.</span></span>  <br/> |
|[<span data-ttu-id="b301d-162">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="b301d-162">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="b301d-163">Enthält ein Array Sequenz von Dateitypen ändern, die die Typen der Unterschiede zwischen den Elementen auf dem Client und der Elemente auf dem Exchange-Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="b301d-163">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b301d-164">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b301d-164">Parent elements</span></span>

|<span data-ttu-id="b301d-165">**Element**</span><span class="sxs-lookup"><span data-stu-id="b301d-165">**Element**</span></span>|<span data-ttu-id="b301d-166">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b301d-166">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b301d-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b301d-167">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="b301d-168">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b301d-168">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b301d-169">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b301d-169">Remarks</span></span>

<span data-ttu-id="b301d-170">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b301d-170">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b301d-171">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b301d-171">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b301d-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="b301d-172">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b301d-173">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b301d-173">Schema Name</span></span>  <br/> |<span data-ttu-id="b301d-174">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b301d-174">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b301d-175">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b301d-175">Validation File</span></span>  <br/> |<span data-ttu-id="b301d-176">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b301d-176">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b301d-177">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b301d-177">Can be Empty</span></span>  <br/> |<span data-ttu-id="b301d-178">False</span><span class="sxs-lookup"><span data-stu-id="b301d-178">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b301d-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b301d-179">See also</span></span>

- [<span data-ttu-id="b301d-180">SyncFolderHierarchy-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b301d-180">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)
- [<span data-ttu-id="b301d-181">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b301d-181">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

