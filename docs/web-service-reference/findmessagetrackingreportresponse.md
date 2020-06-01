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
description: Das FindMessageTrackingReportResponse-Element enthält den Status und das Ergebnis einer einzelnen FindMessageTrackingReport-Vorgangsanforderung.
ms.openlocfilehash: a72ae3b20f2cae3d37a90da36b816e6f3265c716
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462915"
---
# <a name="findmessagetrackingreportresponse"></a><span data-ttu-id="d389f-103">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="d389f-103">FindMessageTrackingReportResponse</span></span>

<span data-ttu-id="d389f-104">Das **FindMessageTrackingReportResponse** -Element enthält den Status und das Ergebnis einer einzelnen [FindMessageTrackingReport-Vorgangs](findmessagetrackingreport-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d389f-104">The **FindMessageTrackingReportResponse** element contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span> 
  
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

 <span data-ttu-id="d389f-105">**FindMessageTrackingReportResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="d389f-105">**FindMessageTrackingReportResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d389f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d389f-106">Attributes and elements</span></span>

<span data-ttu-id="d389f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d389f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d389f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d389f-108">Attributes</span></span>

|<span data-ttu-id="d389f-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d389f-109">**Attribute**</span></span>|<span data-ttu-id="d389f-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d389f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d389f-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="d389f-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="d389f-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="d389f-112">Describes the status of the response.</span></span><br/><br/> <span data-ttu-id="d389f-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="d389f-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="d389f-114">-Success</span><span class="sxs-lookup"><span data-stu-id="d389f-114">-  Success</span></span>  <br/><span data-ttu-id="d389f-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="d389f-115">-  Warning</span></span>  <br/><span data-ttu-id="d389f-116">-Error</span><span class="sxs-lookup"><span data-stu-id="d389f-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="d389f-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="d389f-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="d389f-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d389f-118">**Value**</span></span>|<span data-ttu-id="d389f-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d389f-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d389f-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="d389f-120">**Success**</span></span> <br/> |<span data-ttu-id="d389f-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="d389f-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="d389f-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="d389f-122">**Warning**</span></span> <br/> | <span data-ttu-id="d389f-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="d389f-123">Describes a request that was not processed.</span></span> <span data-ttu-id="d389f-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d389f-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="d389f-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="d389f-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="d389f-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="d389f-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="d389f-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="d389f-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="d389f-128">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="d389f-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="d389f-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="d389f-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="d389f-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="d389f-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="d389f-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="d389f-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="d389f-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="d389f-132">**Error**</span></span> <br/> | <span data-ttu-id="d389f-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d389f-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="d389f-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="d389f-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="d389f-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="d389f-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="d389f-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="d389f-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="d389f-137">-Ein unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="d389f-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="d389f-138">-Ein Attribut oder Element, das im Kontext ungültig ist</span><span class="sxs-lookup"><span data-stu-id="d389f-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="d389f-139">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client</span><span class="sxs-lookup"><span data-stu-id="d389f-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="d389f-140">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="d389f-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="d389f-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="d389f-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d389f-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d389f-142">Child elements</span></span>

|<span data-ttu-id="d389f-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="d389f-143">**Element**</span></span>|<span data-ttu-id="d389f-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d389f-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d389f-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="d389f-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="d389f-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="d389f-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="d389f-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d389f-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="d389f-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d389f-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="d389f-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d389f-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="d389f-150">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="d389f-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="d389f-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="d389f-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="d389f-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="d389f-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="d389f-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="d389f-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="d389f-154">Diagnose</span><span class="sxs-lookup"><span data-stu-id="d389f-154">Diagnostics</span></span>](diagnostics.md) <br/> |<span data-ttu-id="d389f-155">Enthält Informationen, die verwendet werden, um verschiedene statistische Berichte für die Überwachungsfunktion in einem Datencenter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d389f-155">Contains information that will be used to produce various statistical reports for the tracking feature in a DataCenter.</span></span>  <br/> |
|[<span data-ttu-id="d389f-156">MessageTrackingSearchResults</span><span class="sxs-lookup"><span data-stu-id="d389f-156">MessageTrackingSearchResults</span></span>](messagetrackingsearchresults.md) <br/> |<span data-ttu-id="d389f-157">Enthält und Array von Nachrichten, die den Suchanforderungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d389f-157">Contains and array of messages that match the search requirements.</span></span>  <br/> |
|[<span data-ttu-id="d389f-158">ExecutedSearchScope</span><span class="sxs-lookup"><span data-stu-id="d389f-158">ExecutedSearchScope</span></span>](executedsearchscope.md) <br/> |<span data-ttu-id="d389f-159">Enthält den Suchbereich, der zum Abrufen der Suchergebnisse ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="d389f-159">Contains the scope of the search that was performed to get the search results.</span></span>  <br/> |
|[<span data-ttu-id="d389f-160">Fehler</span><span class="sxs-lookup"><span data-stu-id="d389f-160">Errors</span></span>](errors-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d389f-161">Enthält einen Eigenschaftenbehälter zum Speichern von Fehlern, die über den Webdienst zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d389f-161">Contains a property bag to store errors that are returned through the Web service.</span></span>  <br/> |
|[<span data-ttu-id="d389f-162">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="d389f-162">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="d389f-163">Enthält eine Liste mit einer oder mehreren Überwachungseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d389f-163">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d389f-164">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d389f-164">Parent elements</span></span>

<span data-ttu-id="d389f-165">Keine.</span><span class="sxs-lookup"><span data-stu-id="d389f-165">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="d389f-166">Textwert</span><span class="sxs-lookup"><span data-stu-id="d389f-166">Text value</span></span>

<span data-ttu-id="d389f-167">Keine.</span><span class="sxs-lookup"><span data-stu-id="d389f-167">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d389f-168">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d389f-168">Remarks</span></span>

<span data-ttu-id="d389f-169">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d389f-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d389f-170">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d389f-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d389f-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="d389f-171">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d389f-172">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d389f-172">Schema Name</span></span>  <br/> |<span data-ttu-id="d389f-173">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d389f-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d389f-174">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d389f-174">Validation File</span></span>  <br/> |<span data-ttu-id="d389f-175">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d389f-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d389f-176">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d389f-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="d389f-177">False</span><span class="sxs-lookup"><span data-stu-id="d389f-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d389f-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d389f-178">See also</span></span>

- [<span data-ttu-id="d389f-179">FindMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d389f-179">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
- [<span data-ttu-id="d389f-180">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d389f-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

