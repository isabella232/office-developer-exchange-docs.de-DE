---
title: SyncFolderItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderItemsResponseMessage
api_type:
- schema
ms.assetid: f58e773f-94a7-4729-90f0-ac4c71b4ba59
description: Das SyncFolderItemsResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung SyncFolderItems Vorgang.
ms.openlocfilehash: 9bb32232143df56ad9de93480e10a5941e68025a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839156"
---
# <a name="syncfolderitemsresponsemessage"></a><span data-ttu-id="5a32c-103">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5a32c-103">SyncFolderItemsResponseMessage</span></span>

<span data-ttu-id="5a32c-104">Das **SyncFolderItemsResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [SyncFolderItems Vorgang](syncfolderitems-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="5a32c-104">The **SyncFolderItemsResponseMessage** element contains the status and result of a single [SyncFolderItems operation](syncfolderitems-operation.md) request.</span></span> 
  
- [<span data-ttu-id="5a32c-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="5a32c-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md) 
- [<span data-ttu-id="5a32c-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5a32c-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="5a32c-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5a32c-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
  
```xml
<SyncFolderItemsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <SyncState/>
   <IncludesLastItemInRange/>
   <Changes/>
</SyncFolderItemsResponseMessage>
```

 <span data-ttu-id="5a32c-108">**SyncFolderItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="5a32c-108">**SyncFolderItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5a32c-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5a32c-109">Attributes and elements</span></span>

<span data-ttu-id="5a32c-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5a32c-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5a32c-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="5a32c-111">Attributes</span></span>

|<span data-ttu-id="5a32c-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5a32c-112">**Attribute**</span></span>|<span data-ttu-id="5a32c-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a32c-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5a32c-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="5a32c-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="5a32c-115">Beschreibt den Status einer Antwort [SyncFolderItems Vorgang](syncfolderitems-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="5a32c-115">Describes the status of a [SyncFolderItems operation](syncfolderitems-operation.md) response.</span></span> <br/><br/><span data-ttu-id="5a32c-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="5a32c-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="5a32c-117">-Success</span><span class="sxs-lookup"><span data-stu-id="5a32c-117">-  Success</span></span>  <br/><span data-ttu-id="5a32c-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="5a32c-118">-  Warning</span></span>  <br/><span data-ttu-id="5a32c-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="5a32c-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="5a32c-120">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="5a32c-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="5a32c-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5a32c-121">**Value**</span></span>|<span data-ttu-id="5a32c-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a32c-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5a32c-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="5a32c-123">**Success**</span></span> <br/> |<span data-ttu-id="5a32c-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="5a32c-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="5a32c-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="5a32c-125">**Warning**</span></span> <br/> | <span data-ttu-id="5a32c-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="5a32c-126">Describes a request that was not processed.</span></span> <span data-ttu-id="5a32c-127">Eine Warnung kann zurückgegeben werden, wenn während der Verarbeitung eines Elements in der Anforderung ist ein Fehler aufgetreten und nachfolgenden Elemente können nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="5a32c-127">A warning may be returned if an error occurred while processing an item in the request and subsequent items cannot be processed.</span></span> <br/><br/><span data-ttu-id="5a32c-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="5a32c-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="5a32c-129">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="5a32c-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="5a32c-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="5a32c-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="5a32c-131">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="5a32c-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="5a32c-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="5a32c-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="5a32c-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="5a32c-133">-  A password has expired.</span></span>  <br/><span data-ttu-id="5a32c-134">-Ein Kontingent überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="5a32c-134">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="5a32c-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="5a32c-135">**Error**</span></span> <br/> | <span data-ttu-id="5a32c-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5a32c-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="5a32c-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="5a32c-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="5a32c-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="5a32c-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="5a32c-139">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="5a32c-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="5a32c-140">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="5a32c-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="5a32c-141">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="5a32c-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="5a32c-142">-Alle Versuch nicht autorisierten Zugriff von jedem client</span><span class="sxs-lookup"><span data-stu-id="5a32c-142">-  Any unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="5a32c-143">-Alle serverseitigen Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="5a32c-143">-  Any server-side failure in response to a valid client-side call</span></span>  <br/>  <br/><span data-ttu-id="5a32c-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="5a32c-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5a32c-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5a32c-145">Child elements</span></span>

|<span data-ttu-id="5a32c-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="5a32c-146">**Element**</span></span>|<span data-ttu-id="5a32c-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a32c-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a32c-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="5a32c-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="5a32c-149">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="5a32c-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="5a32c-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5a32c-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="5a32c-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="5a32c-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="5a32c-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5a32c-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="5a32c-153">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="5a32c-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="5a32c-154">Es enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="5a32c-154">It contains the value of 0.</span></span>  <br/> |
|[<span data-ttu-id="5a32c-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="5a32c-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="5a32c-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="5a32c-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="5a32c-157">Synchronisierungsstatus</span><span class="sxs-lookup"><span data-stu-id="5a32c-157">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5a32c-158">Enthält eine base64-codierten Format von der Synchronisierung von Daten, die nach jeder Anforderung erfolgreich aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5a32c-158">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="5a32c-159">Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5a32c-159">This is used to identify the synchronization state.</span></span>  <br/> |
|[<span data-ttu-id="5a32c-160">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="5a32c-160">IncludesLastItemInRange</span></span>](includeslastiteminrange.md) <br/> |<span data-ttu-id="5a32c-161">Gibt an, ob das letzte Element synchronisieren in der Antwort aufgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="5a32c-161">Indicates whether the last item to synchronize has been included in the response.</span></span>  <br/> |
|[<span data-ttu-id="5a32c-162">Änderungen (Elemente)</span><span class="sxs-lookup"><span data-stu-id="5a32c-162">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="5a32c-163">Enthält ein Array Sequenz von Dateitypen ändern, die die Typen der Unterschiede zwischen den Elementen auf dem Client und der Elemente auf dem Exchange-Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="5a32c-163">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5a32c-164">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5a32c-164">Parent elements</span></span>

|<span data-ttu-id="5a32c-165">**Element**</span><span class="sxs-lookup"><span data-stu-id="5a32c-165">**Element**</span></span>|<span data-ttu-id="5a32c-166">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a32c-166">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a32c-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5a32c-167">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="5a32c-168">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5a32c-168">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a32c-169">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5a32c-169">Remarks</span></span>

<span data-ttu-id="5a32c-170">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="5a32c-170">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5a32c-171">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5a32c-171">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a32c-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="5a32c-172">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5a32c-173">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5a32c-173">Schema Name</span></span>  <br/> |<span data-ttu-id="5a32c-174">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="5a32c-174">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5a32c-175">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5a32c-175">Validation File</span></span>  <br/> |<span data-ttu-id="5a32c-176">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5a32c-176">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5a32c-177">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5a32c-177">Can be Empty</span></span>  <br/> |<span data-ttu-id="5a32c-178">False</span><span class="sxs-lookup"><span data-stu-id="5a32c-178">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a32c-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a32c-179">See also</span></span>

- [<span data-ttu-id="5a32c-180">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5a32c-180">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="5a32c-181">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5a32c-181">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

