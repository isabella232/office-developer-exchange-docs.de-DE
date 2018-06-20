---
title: GetMessageTrackingReportResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetMessageTrackingReportResponse
api_type:
- schema
ms.assetid: 41177894-2008-44a6-86f8-bc34c0a48e36
description: Das GetMessageTrackingReportResponse-Element enthält die Antwort für den Vorgang GetMessageTrackingReport.
ms.openlocfilehash: bdb8b97e57f92a32cbdc498d09297920366b58bd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758736"
---
# <a name="getmessagetrackingreportresponse"></a><span data-ttu-id="1ee28-103">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="1ee28-103">GetMessageTrackingReportResponse</span></span>

<span data-ttu-id="1ee28-104">Das **GetMessageTrackingReportResponse** -Element enthält die Antwort für den [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="1ee28-104">The **GetMessageTrackingReportResponse** element contains the response for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>
  
```xml
<GetMessageTrackingReportResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MessageTrackingReport/>
   <Diagnostics/>
   <Errors/>
   <Properties/>
</GetMessageTrackingReportResponse>
```

 <span data-ttu-id="1ee28-105">**GetMessageTrackingReportResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="1ee28-105">**GetMessageTrackingReportResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1ee28-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1ee28-106">Attributes and elements</span></span>

<span data-ttu-id="1ee28-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1ee28-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ee28-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1ee28-108">Attributes</span></span>

|<span data-ttu-id="1ee28-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1ee28-109">**Attribute**</span></span>|<span data-ttu-id="1ee28-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ee28-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ee28-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="1ee28-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="1ee28-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="1ee28-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="1ee28-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="1ee28-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="1ee28-114">-Success</span><span class="sxs-lookup"><span data-stu-id="1ee28-114">-  Success</span></span>  <br/><span data-ttu-id="1ee28-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="1ee28-115">-  Warning</span></span>  <br/><span data-ttu-id="1ee28-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="1ee28-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="1ee28-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="1ee28-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="1ee28-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1ee28-118">**Value**</span></span>|<span data-ttu-id="1ee28-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ee28-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ee28-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="1ee28-120">**Success**</span></span> <br/> |<span data-ttu-id="1ee28-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="1ee28-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="1ee28-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="1ee28-122">**Warning**</span></span> <br/> | <span data-ttu-id="1ee28-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="1ee28-123">Describes a request that was not processed.</span></span> <span data-ttu-id="1ee28-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="1ee28-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="1ee28-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="1ee28-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="1ee28-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="1ee28-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="1ee28-127">-Active Directory-Domäne fungiert (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="1ee28-127">-  Active Directory Domain Serves (AD DS) is offline.</span></span>  <br/><span data-ttu-id="1ee28-128">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="1ee28-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="1ee28-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="1ee28-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="1ee28-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="1ee28-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="1ee28-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="1ee28-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="1ee28-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="1ee28-132">**Error**</span></span> <br/> | <span data-ttu-id="1ee28-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1ee28-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="1ee28-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="1ee28-134">The following are examples of sources of errors:</span></span>  <br/>  <span data-ttu-id="1ee28-135">Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="1ee28-135">Invalid attributes or elements</span></span>  <br/><br/><span data-ttu-id="1ee28-136">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="1ee28-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="1ee28-137">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="1ee28-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="1ee28-138">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="1ee28-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="1ee28-139">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="1ee28-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="1ee28-140">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="1ee28-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="1ee28-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="1ee28-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1ee28-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ee28-142">Child elements</span></span>

|<span data-ttu-id="1ee28-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ee28-143">**Element**</span></span>|<span data-ttu-id="1ee28-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ee28-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ee28-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="1ee28-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="1ee28-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="1ee28-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="1ee28-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1ee28-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="1ee28-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="1ee28-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="1ee28-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="1ee28-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="1ee28-150">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="1ee28-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="1ee28-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="1ee28-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="1ee28-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="1ee28-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="1ee28-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="1ee28-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="1ee28-154">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="1ee28-154">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="1ee28-155">Enthält eine Nachricht, die in einem [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1ee28-155">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="1ee28-156">Diagnose</span><span class="sxs-lookup"><span data-stu-id="1ee28-156">Diagnostics</span></span>](diagnostics.md) <br/> |<span data-ttu-id="1ee28-157">Enthält Timing und Leistung Informationen, die für die berichterstellung in einem Rechenzentrum verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ee28-157">Provides timing and performance information that is used for reporting in a DataCenter.</span></span>  <br/> |
|[<span data-ttu-id="1ee28-158">Fehler</span><span class="sxs-lookup"><span data-stu-id="1ee28-158">Errors</span></span>](errors-ex15websvcsotherref.md) <br/> |<span data-ttu-id="1ee28-159">Enthält einen Eigenschaftenbehälter zum Speichern von Fehlern, die über den Webdienst zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1ee28-159">Contains a property bag to store errors that are returned through the Web service.</span></span>  <br/> |
|[<span data-ttu-id="1ee28-160">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="1ee28-160">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="1ee28-161">Enthält eine Liste der Eigenschaften für eine oder mehrere Tracking an.</span><span class="sxs-lookup"><span data-stu-id="1ee28-161">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1ee28-162">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ee28-162">Parent elements</span></span>

<span data-ttu-id="1ee28-163">Keine.</span><span class="sxs-lookup"><span data-stu-id="1ee28-163">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="1ee28-164">Textwert</span><span class="sxs-lookup"><span data-stu-id="1ee28-164">Text value</span></span>

<span data-ttu-id="1ee28-165">Keine.</span><span class="sxs-lookup"><span data-stu-id="1ee28-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1ee28-166">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1ee28-166">Remarks</span></span>

<span data-ttu-id="1ee28-167">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1ee28-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1ee28-168">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1ee28-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ee28-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ee28-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1ee28-170">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1ee28-170">Schema Name</span></span>  <br/> |<span data-ttu-id="1ee28-171">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="1ee28-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1ee28-172">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1ee28-172">Validation File</span></span>  <br/> |<span data-ttu-id="1ee28-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1ee28-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1ee28-174">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1ee28-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="1ee28-175">False</span><span class="sxs-lookup"><span data-stu-id="1ee28-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ee28-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ee28-176">See also</span></span>

- [<span data-ttu-id="1ee28-177">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1ee28-177">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="1ee28-178">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1ee28-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

