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
description: Das SyncFolderHierarchyResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen SyncFolderHierarchy-Vorgangsanforderung.
ms.openlocfilehash: fda0a37178f89ba0fd5ef860f8b009f335a11391
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465345"
---
# <a name="syncfolderhierarchyresponsemessage"></a><span data-ttu-id="8e2e8-103">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8e2e8-103">SyncFolderHierarchyResponseMessage</span></span>

<span data-ttu-id="8e2e8-104">Das **SyncFolderHierarchyResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [SyncFolderHierarchy-Vorgangs](syncfolderhierarchy-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-104">The **SyncFolderHierarchyResponseMessage** element contains the status and result of a single [SyncFolderHierarchy operation](syncfolderhierarchy-operation.md) request.</span></span> 
  
- [<span data-ttu-id="8e2e8-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="8e2e8-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md) 
- [<span data-ttu-id="8e2e8-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8e2e8-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="8e2e8-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8e2e8-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
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

 <span data-ttu-id="8e2e8-108">**SyncFolderHierarchyResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="8e2e8-108">**SyncFolderHierarchyResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8e2e8-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8e2e8-109">Attributes and elements</span></span>

<span data-ttu-id="8e2e8-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8e2e8-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="8e2e8-111">Attributes</span></span>

|<span data-ttu-id="8e2e8-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8e2e8-112">**Attribute**</span></span>|<span data-ttu-id="8e2e8-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8e2e8-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8e2e8-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="8e2e8-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="8e2e8-115">Beschreibt den Status einer [SyncFolderHierarchy-Vorgangs](syncfolderhierarchy-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-115">Describes the status of a [SyncFolderHierarchy operation](syncfolderhierarchy-operation.md) response.</span></span> <br/><br/><span data-ttu-id="8e2e8-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="8e2e8-116">The following values are valid for this attribute:</span></span><br/>  <br/><span data-ttu-id="8e2e8-117">-Success</span><span class="sxs-lookup"><span data-stu-id="8e2e8-117">-  Success</span></span>  <br/><span data-ttu-id="8e2e8-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="8e2e8-118">-  Warning</span></span>  <br/><span data-ttu-id="8e2e8-119">-Error</span><span class="sxs-lookup"><span data-stu-id="8e2e8-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="8e2e8-120">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="8e2e8-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="8e2e8-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8e2e8-121">**Value**</span></span>|<span data-ttu-id="8e2e8-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8e2e8-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8e2e8-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="8e2e8-123">**Success**</span></span> <br/> |<span data-ttu-id="8e2e8-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="8e2e8-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="8e2e8-125">**Warning**</span></span> <br/> | <span data-ttu-id="8e2e8-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-126">Describes a request that was not processed.</span></span> <span data-ttu-id="8e2e8-127">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="8e2e8-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="8e2e8-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="8e2e8-129">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="8e2e8-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="8e2e8-131">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="8e2e8-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="8e2e8-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-133">-  A password has expired.</span></span>  <br/><span data-ttu-id="8e2e8-134">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="8e2e8-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="8e2e8-135">**Error**</span></span> <br/> | <span data-ttu-id="8e2e8-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="8e2e8-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="8e2e8-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="8e2e8-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="8e2e8-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="8e2e8-139">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="8e2e8-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="8e2e8-140">-Ein unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="8e2e8-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="8e2e8-141">-Ein Attribut oder Element, das im Kontext ungültig ist</span><span class="sxs-lookup"><span data-stu-id="8e2e8-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="8e2e8-142">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client</span><span class="sxs-lookup"><span data-stu-id="8e2e8-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="8e2e8-143">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="8e2e8-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="8e2e8-144">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="8e2e8-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8e2e8-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8e2e8-145">Child elements</span></span>

|<span data-ttu-id="8e2e8-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="8e2e8-146">**Element**</span></span>|<span data-ttu-id="8e2e8-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8e2e8-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e2e8-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="8e2e8-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="8e2e8-149">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="8e2e8-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8e2e8-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="8e2e8-151">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="8e2e8-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8e2e8-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="8e2e8-153">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="8e2e8-154">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="8e2e8-155">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="8e2e8-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="8e2e8-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="8e2e8-157">Von "SyncState</span><span class="sxs-lookup"><span data-stu-id="8e2e8-157">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="8e2e8-158">Enthält eine Base64-codierte Form der Synchronisierungsdaten, die nach jeder erfolgreichen Anforderung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-158">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="8e2e8-159">Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-159">This is used to identify the synchronization state.</span></span>  <br/> |
|[<span data-ttu-id="8e2e8-160">IncludesLastFolderInRange</span><span class="sxs-lookup"><span data-stu-id="8e2e8-160">IncludesLastFolderInRange</span></span>](includeslastfolderinrange.md) <br/> |<span data-ttu-id="8e2e8-161">Gibt an, ob das letzte zu synchronisierende Element in die Antwort eingeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-161">Indicates whether the last item to synchronize has been included in the response.</span></span>  <br/> |
|[<span data-ttu-id="8e2e8-162">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="8e2e8-162">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="8e2e8-163">Enthält ein Sequenz Array von Änderungstypen, die die Arten von Unterschieden zwischen den Elementen auf dem Client und den Elementen auf dem Exchange-Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-163">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8e2e8-164">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8e2e8-164">Parent elements</span></span>

|<span data-ttu-id="8e2e8-165">**Element**</span><span class="sxs-lookup"><span data-stu-id="8e2e8-165">**Element**</span></span>|<span data-ttu-id="8e2e8-166">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8e2e8-166">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e2e8-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8e2e8-167">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="8e2e8-168">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-168">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e2e8-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e2e8-169">Remarks</span></span>

<span data-ttu-id="8e2e8-170">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8e2e8-170">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8e2e8-171">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8e2e8-171">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e2e8-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e2e8-172">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8e2e8-173">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8e2e8-173">Schema Name</span></span>  <br/> |<span data-ttu-id="8e2e8-174">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8e2e8-174">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8e2e8-175">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8e2e8-175">Validation File</span></span>  <br/> |<span data-ttu-id="8e2e8-176">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="8e2e8-176">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8e2e8-177">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8e2e8-177">Can be Empty</span></span>  <br/> |<span data-ttu-id="8e2e8-178">False</span><span class="sxs-lookup"><span data-stu-id="8e2e8-178">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e2e8-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e2e8-179">See also</span></span>

- [<span data-ttu-id="8e2e8-180">SyncFolderHierarchy-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8e2e8-180">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)
- [<span data-ttu-id="8e2e8-181">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8e2e8-181">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

