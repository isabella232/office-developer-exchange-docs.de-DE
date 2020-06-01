---
title: ExpandDLResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExpandDLResponseMessage
api_type:
- schema
ms.assetid: 1140601b-98cf-4cb4-a019-321c7f63d5be
description: Das ExpandDLResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen ExpandDL-Vorgangsanforderung.
ms.openlocfilehash: e186c4e14cbb9c922a4d262c85c130b9c33ff939
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460638"
---
# <a name="expanddlresponsemessage"></a><span data-ttu-id="60831-103">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="60831-103">ExpandDLResponseMessage</span></span>

<span data-ttu-id="60831-104">Das **ExpandDLResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [ExpandDL-Vorgangs](expanddl-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="60831-104">The **ExpandDLResponseMessage** element contains the status and result of a single [ExpandDL operation](expanddl-operation.md) request.</span></span> 
  
- [<span data-ttu-id="60831-105">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="60831-105">ExpandDLResponse</span></span>](expanddlresponse.md)  
- [<span data-ttu-id="60831-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="60831-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="60831-107">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="60831-107">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
  
```xml
<ExpandDLResponseMessage ResponseClass="" IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DLExpansion/>
</ExpandDLResponseMessage>
```

<span data-ttu-id="60831-108">**ExpandDLResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="60831-108">**ExpandDLResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="60831-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="60831-109">Attributes and elements</span></span>

<span data-ttu-id="60831-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="60831-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="60831-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="60831-111">Attributes</span></span>

|<span data-ttu-id="60831-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="60831-112">**Attribute**</span></span>|<span data-ttu-id="60831-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60831-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="60831-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="60831-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="60831-115">Beschreibt den Status einer [ExpandDL-Vorgangs](expanddl-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="60831-115">Describes the status of an [ExpandDL operation](expanddl-operation.md) response.</span></span><br/><br/><span data-ttu-id="60831-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="60831-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="60831-117">-Success</span><span class="sxs-lookup"><span data-stu-id="60831-117">-  Success</span></span>  <br/><span data-ttu-id="60831-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="60831-118">-  Warning</span></span>  <br/><span data-ttu-id="60831-119">-Error</span><span class="sxs-lookup"><span data-stu-id="60831-119">-  Error</span></span>  <br/> |
|<span data-ttu-id="60831-120">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="60831-120">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="60831-121">Stellt den nächsten Index dar, der für die nächste Anforderung verwendet werden soll, wenn eine indizierte Auslagerungs Ansicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="60831-121">Represents the next index that should be used for the next request when an indexed paging view is used.</span></span>  <br/> |
|<span data-ttu-id="60831-122">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="60831-122">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="60831-123">Stellt den neuen Zählerwert dar, der für die nächste Anforderung verwendet werden soll, wenn Bruch Seitenansichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60831-123">Represents the new numerator value to use for the next request when fraction page views are used.</span></span>  <br/> |
|<span data-ttu-id="60831-124">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="60831-124">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="60831-125">Stellt den nächsten Nenner dar, der für die nächste Anforderung bei Bruchzahlen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="60831-125">Represents the next denominator to use for the next request when doing fractional paging.</span></span>  <br/> |
|<span data-ttu-id="60831-126">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="60831-126">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="60831-127">Gibt an, dass kein zusätzliches Paging erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="60831-127">Indicates that additional paging is not needed.</span></span> <span data-ttu-id="60831-128">Dieses Attribut ist true, wenn die aktuellen Ergebnisse das letzte Element in der Abfrage enthalten.</span><span class="sxs-lookup"><span data-stu-id="60831-128">This attribute will be true if the current results contain the last item in the query.</span></span>  <br/> |
|<span data-ttu-id="60831-129">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="60831-129">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="60831-130">Stellt die Gesamtzahl der Elemente dar, die die Einschränkung übergeben.</span><span class="sxs-lookup"><span data-stu-id="60831-130">Represents the total number of items that pass the restriction.</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="60831-131">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="60831-131">ResponseClass attribute values</span></span>

|<span data-ttu-id="60831-132">**Wert**</span><span class="sxs-lookup"><span data-stu-id="60831-132">**Value**</span></span>|<span data-ttu-id="60831-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60831-133">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="60831-134">**Success**</span><span class="sxs-lookup"><span data-stu-id="60831-134">**Success**</span></span> <br/> |<span data-ttu-id="60831-135">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="60831-135">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="60831-136">**Warning**</span><span class="sxs-lookup"><span data-stu-id="60831-136">**Warning**</span></span> <br/> | <span data-ttu-id="60831-137">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="60831-137">Describes a request that was not processed.</span></span> <span data-ttu-id="60831-138">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="60831-138">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="60831-139">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="60831-139">The following are examples of sources of warnings:</span></span><br/>  <br/><span data-ttu-id="60831-140">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="60831-140">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="60831-141">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="60831-141">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="60831-142">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="60831-142">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="60831-143">-Die Postfachdatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="60831-143">-  The mailbox database (MDB) is offline.</span></span>  <br/><span data-ttu-id="60831-144">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="60831-144">-  A password is expired.</span></span>  <br/><span data-ttu-id="60831-145">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="60831-145">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="60831-146">**Error**</span><span class="sxs-lookup"><span data-stu-id="60831-146">**Error**</span></span> <br/> | <span data-ttu-id="60831-147">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="60831-147">Describes a request that cannot be fulfilled.</span></span><br/><br/> <span data-ttu-id="60831-148">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="60831-148">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="60831-149">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="60831-149">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="60831-150">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="60831-150">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="60831-151">-Ein unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="60831-151">-  An unknown tag</span></span>  <br/><span data-ttu-id="60831-152">-Ein Attribut oder Element, das im Kontext ungültig ist</span><span class="sxs-lookup"><span data-stu-id="60831-152">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="60831-153">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client</span><span class="sxs-lookup"><span data-stu-id="60831-153">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="60831-154">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="60831-154">-  A server-side failure in response to a valid client-side call</span></span> <br/> <br/>  <span data-ttu-id="60831-155">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="60831-155">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="60831-156">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="60831-156">Child elements</span></span>

|<span data-ttu-id="60831-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="60831-157">**Element**</span></span>|<span data-ttu-id="60831-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60831-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60831-159">MessageText</span><span class="sxs-lookup"><span data-stu-id="60831-159">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="60831-160">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="60831-160">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="60831-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="60831-161">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="60831-162">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="60831-162">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="60831-163">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="60831-163">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="60831-164">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="60831-164">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="60831-165">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="60831-165">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="60831-166">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="60831-166">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="60831-167">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="60831-167">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="60831-168">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="60831-168">DLExpansion</span></span>](dlexpansion.md) <br/> |<span data-ttu-id="60831-169">Enthält eine Reihe von Postfächern, die in einer Verteilerliste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="60831-169">Contains an array of mailboxes that are contained in a distribution list.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="60831-170">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="60831-170">Parent elements</span></span>

|<span data-ttu-id="60831-171">**Element**</span><span class="sxs-lookup"><span data-stu-id="60831-171">**Element**</span></span>|<span data-ttu-id="60831-172">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60831-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60831-173">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="60831-173">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="60831-174">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="60831-174">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60831-175">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60831-175">Remarks</span></span>

<span data-ttu-id="60831-176">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server mit installierter Client Zugriffs-Server Rolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="60831-176">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="60831-177">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="60831-177">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60831-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="60831-178">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="60831-179">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="60831-179">Schema Name</span></span>  <br/> |<span data-ttu-id="60831-180">Schematypen</span><span class="sxs-lookup"><span data-stu-id="60831-180">Types schema</span></span>  <br/> |
|<span data-ttu-id="60831-181">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="60831-181">Validation File</span></span>  <br/> |<span data-ttu-id="60831-182">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="60831-182">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="60831-183">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="60831-183">Can be Empty</span></span>  <br/> |<span data-ttu-id="60831-184">False</span><span class="sxs-lookup"><span data-stu-id="60831-184">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="60831-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60831-185">See also</span></span>

- [<span data-ttu-id="60831-186">ExpandDL-Vorgang</span><span class="sxs-lookup"><span data-stu-id="60831-186">ExpandDL operation</span></span>](expanddl-operation.md)
- [<span data-ttu-id="60831-187">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="60831-187">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="60831-188">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="60831-188">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

