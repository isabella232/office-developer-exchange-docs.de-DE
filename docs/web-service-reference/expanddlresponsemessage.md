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
description: Das ExpandDLResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung der ExpandDL-Vorgang.
ms.openlocfilehash: 62a81574f9c513b905a92876b3d757c635b4f07b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758322"
---
# <a name="expanddlresponsemessage"></a><span data-ttu-id="7bd65-103">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7bd65-103">ExpandDLResponseMessage</span></span>

<span data-ttu-id="7bd65-104">Das **ExpandDLResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [der ExpandDL-Vorgang](expanddl-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="7bd65-104">The **ExpandDLResponseMessage** element contains the status and result of a single [ExpandDL operation](expanddl-operation.md) request.</span></span> 
  
- [<span data-ttu-id="7bd65-105">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="7bd65-105">ExpandDLResponse</span></span>](expanddlresponse.md)  
- [<span data-ttu-id="7bd65-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7bd65-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="7bd65-107">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7bd65-107">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
  
```xml
<ExpandDLResponseMessage ResponseClass="" IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DLExpansion/>
</ExpandDLResponseMessage>
```

<span data-ttu-id="7bd65-108">**ExpandDLResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="7bd65-108">**ExpandDLResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="7bd65-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7bd65-109">Attributes and elements</span></span>

<span data-ttu-id="7bd65-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7bd65-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7bd65-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="7bd65-111">Attributes</span></span>

|<span data-ttu-id="7bd65-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7bd65-112">**Attribute**</span></span>|<span data-ttu-id="7bd65-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7bd65-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7bd65-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="7bd65-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="7bd65-115">Beschreibt den Status einer Antwort [der ExpandDL-Vorgang](expanddl-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="7bd65-115">Describes the status of an [ExpandDL operation](expanddl-operation.md) response.</span></span><br/><br/><span data-ttu-id="7bd65-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="7bd65-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="7bd65-117">-Success</span><span class="sxs-lookup"><span data-stu-id="7bd65-117">-  Success</span></span>  <br/><span data-ttu-id="7bd65-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="7bd65-118">-  Warning</span></span>  <br/><span data-ttu-id="7bd65-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="7bd65-119">-  Error</span></span>  <br/> |
|<span data-ttu-id="7bd65-120">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="7bd65-120">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="7bd65-121">Stellt den Index, der für die nächste Anforderung verwendet werden soll, wenn eine indizierte Sicht Paging verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7bd65-121">Represents the next index that should be used for the next request when an indexed paging view is used.</span></span>  <br/> |
|<span data-ttu-id="7bd65-122">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="7bd65-122">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="7bd65-123">Steht für den neuen Zähler-Wert für die nächste Anforderung verwendet werden soll, wenn Teiler Seitenansichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7bd65-123">Represents the new numerator value to use for the next request when fraction page views are used.</span></span>  <br/> |
|<span data-ttu-id="7bd65-124">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="7bd65-124">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="7bd65-125">Verwenden Sie für die nächste Anforderung bei Bruchzahlen Paging die nächste Nenner darstellt.</span><span class="sxs-lookup"><span data-stu-id="7bd65-125">Represents the next denominator to use for the next request when doing fractional paging.</span></span>  <br/> |
|<span data-ttu-id="7bd65-126">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="7bd65-126">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="7bd65-127">Gibt an, dass zusätzliche Paging nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="7bd65-127">Indicates that additional paging is not needed.</span></span> <span data-ttu-id="7bd65-128">Dieses Attribut wird true, wenn die aktuellen Ergebnisse das letzte Element in der Abfrage enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="7bd65-128">This attribute will be true if the current results contain the last item in the query.</span></span>  <br/> |
|<span data-ttu-id="7bd65-129">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="7bd65-129">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="7bd65-130">Stellt die Gesamtzahl der Elemente, die die Einschränkung übergeben.</span><span class="sxs-lookup"><span data-stu-id="7bd65-130">Represents the total number of items that pass the restriction.</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="7bd65-131">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="7bd65-131">ResponseClass attribute values</span></span>

|<span data-ttu-id="7bd65-132">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7bd65-132">**Value**</span></span>|<span data-ttu-id="7bd65-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7bd65-133">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7bd65-134">**Success**</span><span class="sxs-lookup"><span data-stu-id="7bd65-134">**Success**</span></span> <br/> |<span data-ttu-id="7bd65-135">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="7bd65-135">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="7bd65-136">**Warning**</span><span class="sxs-lookup"><span data-stu-id="7bd65-136">**Warning**</span></span> <br/> | <span data-ttu-id="7bd65-137">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="7bd65-137">Describes a request that was not processed.</span></span> <span data-ttu-id="7bd65-138">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="7bd65-138">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="7bd65-139">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="7bd65-139">The following are examples of sources of warnings:</span></span><br/>  <br/><span data-ttu-id="7bd65-140">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="7bd65-140">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="7bd65-141">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="7bd65-141">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="7bd65-142">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="7bd65-142">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="7bd65-143">-Die Postfachdatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="7bd65-143">-  The mailbox database (MDB) is offline.</span></span>  <br/><span data-ttu-id="7bd65-144">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="7bd65-144">-  A password is expired.</span></span>  <br/><span data-ttu-id="7bd65-145">-Ein Kontingent überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="7bd65-145">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="7bd65-146">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="7bd65-146">**Error**</span></span> <br/> | <span data-ttu-id="7bd65-147">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7bd65-147">Describes a request that cannot be fulfilled.</span></span><br/><br/> <span data-ttu-id="7bd65-148">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="7bd65-148">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="7bd65-149">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="7bd65-149">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="7bd65-150">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="7bd65-150">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="7bd65-151">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="7bd65-151">-  An unknown tag</span></span>  <br/><span data-ttu-id="7bd65-152">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="7bd65-152">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="7bd65-153">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="7bd65-153">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="7bd65-154">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="7bd65-154">-  A server-side failure in response to a valid client-side call</span></span> <br/> <br/>  <span data-ttu-id="7bd65-155">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="7bd65-155">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7bd65-156">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7bd65-156">Child elements</span></span>

|<span data-ttu-id="7bd65-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="7bd65-157">**Element**</span></span>|<span data-ttu-id="7bd65-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7bd65-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7bd65-159">MessageText</span><span class="sxs-lookup"><span data-stu-id="7bd65-159">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="7bd65-160">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="7bd65-160">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="7bd65-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7bd65-161">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="7bd65-162">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="7bd65-162">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="7bd65-163">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="7bd65-163">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="7bd65-164">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="7bd65-164">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="7bd65-165">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="7bd65-165">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="7bd65-166">MessageXml</span><span class="sxs-lookup"><span data-stu-id="7bd65-166">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="7bd65-167">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="7bd65-167">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="7bd65-168">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="7bd65-168">DLExpansion</span></span>](dlexpansion.md) <br/> |<span data-ttu-id="7bd65-169">Enthält eine Reihe von Postfächern, die in einer Verteilerliste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7bd65-169">Contains an array of mailboxes that are contained in a distribution list.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7bd65-170">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7bd65-170">Parent elements</span></span>

|<span data-ttu-id="7bd65-171">**Element**</span><span class="sxs-lookup"><span data-stu-id="7bd65-171">**Element**</span></span>|<span data-ttu-id="7bd65-172">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7bd65-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7bd65-173">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7bd65-173">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="7bd65-174">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="7bd65-174">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7bd65-175">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7bd65-175">Remarks</span></span>

<span data-ttu-id="7bd65-176">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, der Exchange-Server, mit die Clientzugriffs-Serverrolle installiert ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bd65-176">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7bd65-177">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7bd65-177">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7bd65-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="7bd65-178">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7bd65-179">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7bd65-179">Schema Name</span></span>  <br/> |<span data-ttu-id="7bd65-180">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7bd65-180">Types schema</span></span>  <br/> |
|<span data-ttu-id="7bd65-181">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7bd65-181">Validation File</span></span>  <br/> |<span data-ttu-id="7bd65-182">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7bd65-182">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7bd65-183">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7bd65-183">Can be Empty</span></span>  <br/> |<span data-ttu-id="7bd65-184">False</span><span class="sxs-lookup"><span data-stu-id="7bd65-184">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7bd65-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bd65-185">See also</span></span>

- [<span data-ttu-id="7bd65-186">Der ExpandDL-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7bd65-186">ExpandDL operation</span></span>](expanddl-operation.md)
- [<span data-ttu-id="7bd65-187">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="7bd65-187">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="7bd65-188">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7bd65-188">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

