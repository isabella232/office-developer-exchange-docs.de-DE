---
title: FindMessageTrackingReportResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindMessageTrackingReportResponse
api_type:
- schema
ms.assetid: ed4265dc-0e79-4b34-8bf4-88a94875629d
description: Das FindMessageTrackingReportResponse-Element enthält den Status und das Ergebnis einer Anforderung FindMessageTrackingReport Vorgang.
ms.openlocfilehash: fa381f500eac9a46b11aea8c813f1ffc625a3bc3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758472"
---
# <a name="findmessagetrackingreportresponse"></a><span data-ttu-id="5bfac-103">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="5bfac-103">FindMessageTrackingReportResponse</span></span>

<span data-ttu-id="5bfac-104">Das **FindMessageTrackingReportResponse** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [FindMessageTrackingReport Vorgang](findmessagetrackingreport-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="5bfac-104">The **FindMessageTrackingReportResponse** element contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span> 
  
```xml
<FindMessageTrackingReportResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Diagnostics/>
   <MessageTrackingSearchResults/>
   <Errors/>
   <Properties/>
</FindMessageTrackingReportResponse>
```

 <span data-ttu-id="5bfac-105">**FindMessageTrackingReportResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="5bfac-105">**FindMessageTrackingReportResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5bfac-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5bfac-106">Attributes and elements</span></span>

<span data-ttu-id="5bfac-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5bfac-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5bfac-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5bfac-108">Attributes</span></span>

|<span data-ttu-id="5bfac-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5bfac-109">**Attribute**</span></span>|<span data-ttu-id="5bfac-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5bfac-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5bfac-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="5bfac-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="5bfac-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="5bfac-112">Describes the status of the response.</span></span><br/><br/> <span data-ttu-id="5bfac-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="5bfac-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="5bfac-114">-Success</span><span class="sxs-lookup"><span data-stu-id="5bfac-114">-  Success</span></span>  <br/><span data-ttu-id="5bfac-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="5bfac-115">-  Warning</span></span>  <br/><span data-ttu-id="5bfac-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="5bfac-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="5bfac-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="5bfac-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="5bfac-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5bfac-118">**Value**</span></span>|<span data-ttu-id="5bfac-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5bfac-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5bfac-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="5bfac-120">**Success**</span></span> <br/> |<span data-ttu-id="5bfac-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="5bfac-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="5bfac-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="5bfac-122">**Warning**</span></span> <br/> | <span data-ttu-id="5bfac-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="5bfac-123">Describes a request that was not processed.</span></span> <span data-ttu-id="5bfac-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="5bfac-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="5bfac-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="5bfac-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="5bfac-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="5bfac-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="5bfac-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="5bfac-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="5bfac-128">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="5bfac-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="5bfac-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="5bfac-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="5bfac-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="5bfac-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="5bfac-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="5bfac-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="5bfac-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="5bfac-132">**Error**</span></span> <br/> | <span data-ttu-id="5bfac-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5bfac-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="5bfac-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="5bfac-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="5bfac-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="5bfac-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="5bfac-136">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="5bfac-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="5bfac-137">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="5bfac-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="5bfac-138">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="5bfac-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="5bfac-139">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="5bfac-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="5bfac-140">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="5bfac-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="5bfac-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="5bfac-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5bfac-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5bfac-142">Child elements</span></span>

|<span data-ttu-id="5bfac-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="5bfac-143">**Element**</span></span>|<span data-ttu-id="5bfac-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5bfac-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5bfac-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="5bfac-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="5bfac-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="5bfac-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="5bfac-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5bfac-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="5bfac-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="5bfac-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="5bfac-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5bfac-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="5bfac-150">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="5bfac-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="5bfac-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="5bfac-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="5bfac-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="5bfac-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="5bfac-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="5bfac-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="5bfac-154">Diagnose</span><span class="sxs-lookup"><span data-stu-id="5bfac-154">Diagnostics</span></span>](diagnostics.md) <br/> |<span data-ttu-id="5bfac-155">Enthält Informationen, die verwendet wird, um verschiedene statistische Berichte für die Tracking-Feature in einem Datencenter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5bfac-155">Contains information that will be used to produce various statistical reports for the tracking feature in a DataCenter.</span></span>  <br/> |
|[<span data-ttu-id="5bfac-156">MessageTrackingSearchResults</span><span class="sxs-lookup"><span data-stu-id="5bfac-156">MessageTrackingSearchResults</span></span>](messagetrackingsearchresults.md) <br/> |<span data-ttu-id="5bfac-157">Enthält und Array von Nachrichten, die die Suche Anforderungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5bfac-157">Contains and array of messages that match the search requirements.</span></span>  <br/> |
|[<span data-ttu-id="5bfac-158">ExecutedSearchScope</span><span class="sxs-lookup"><span data-stu-id="5bfac-158">ExecutedSearchScope</span></span>](executedsearchscope.md) <br/> |<span data-ttu-id="5bfac-159">Enthält den Bereich der Suche, die ausgeführt wurde, um die Suchergebnisse erhalten.</span><span class="sxs-lookup"><span data-stu-id="5bfac-159">Contains the scope of the search that was performed to get the search results.</span></span>  <br/> |
|[<span data-ttu-id="5bfac-160">Fehler</span><span class="sxs-lookup"><span data-stu-id="5bfac-160">Errors</span></span>](errors-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5bfac-161">Enthält einen Eigenschaftenbehälter zum Speichern von Fehlern, die über den Webdienst zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5bfac-161">Contains a property bag to store errors that are returned through the Web service.</span></span>  <br/> |
|[<span data-ttu-id="5bfac-162">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="5bfac-162">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="5bfac-163">Enthält eine Liste der Eigenschaften für eine oder mehrere Tracking an.</span><span class="sxs-lookup"><span data-stu-id="5bfac-163">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5bfac-164">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5bfac-164">Parent elements</span></span>

<span data-ttu-id="5bfac-165">Keine.</span><span class="sxs-lookup"><span data-stu-id="5bfac-165">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="5bfac-166">Textwert</span><span class="sxs-lookup"><span data-stu-id="5bfac-166">Text value</span></span>

<span data-ttu-id="5bfac-167">Keine.</span><span class="sxs-lookup"><span data-stu-id="5bfac-167">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5bfac-168">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5bfac-168">Remarks</span></span>

<span data-ttu-id="5bfac-169">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="5bfac-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5bfac-170">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5bfac-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5bfac-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="5bfac-171">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5bfac-172">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5bfac-172">Schema Name</span></span>  <br/> |<span data-ttu-id="5bfac-173">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="5bfac-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5bfac-174">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5bfac-174">Validation File</span></span>  <br/> |<span data-ttu-id="5bfac-175">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5bfac-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5bfac-176">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5bfac-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="5bfac-177">False</span><span class="sxs-lookup"><span data-stu-id="5bfac-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5bfac-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bfac-178">See also</span></span>

- [<span data-ttu-id="5bfac-179">FindMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5bfac-179">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
- [<span data-ttu-id="5bfac-180">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5bfac-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

