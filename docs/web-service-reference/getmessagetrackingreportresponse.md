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
description: Das GetMessageTrackingReportResponse-Element enthält die Antwort für den GetMessageTrackingReport-Vorgang.
ms.openlocfilehash: 15e1f5c91c07dbaad224fb0cd3bc89f444a18087
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460568"
---
# <a name="getmessagetrackingreportresponse"></a><span data-ttu-id="4cf9a-103">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="4cf9a-103">GetMessageTrackingReportResponse</span></span>

<span data-ttu-id="4cf9a-104">Das **GetMessageTrackingReportResponse** -Element enthält die Antwort für den [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="4cf9a-104">The **GetMessageTrackingReportResponse** element contains the response for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>
  
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

 <span data-ttu-id="4cf9a-105">**GetMessageTrackingReportResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="4cf9a-105">**GetMessageTrackingReportResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4cf9a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4cf9a-106">Attributes and elements</span></span>

<span data-ttu-id="4cf9a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4cf9a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4cf9a-108">Attributes</span></span>

|<span data-ttu-id="4cf9a-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4cf9a-109">**Attribute**</span></span>|<span data-ttu-id="4cf9a-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4cf9a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4cf9a-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="4cf9a-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="4cf9a-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="4cf9a-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="4cf9a-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="4cf9a-114">-Success</span><span class="sxs-lookup"><span data-stu-id="4cf9a-114">-  Success</span></span>  <br/><span data-ttu-id="4cf9a-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="4cf9a-115">-  Warning</span></span>  <br/><span data-ttu-id="4cf9a-116">-Error</span><span class="sxs-lookup"><span data-stu-id="4cf9a-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="4cf9a-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="4cf9a-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="4cf9a-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4cf9a-118">**Value**</span></span>|<span data-ttu-id="4cf9a-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4cf9a-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4cf9a-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="4cf9a-120">**Success**</span></span> <br/> |<span data-ttu-id="4cf9a-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="4cf9a-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="4cf9a-122">**Warning**</span></span> <br/> | <span data-ttu-id="4cf9a-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-123">Describes a request that was not processed.</span></span> <span data-ttu-id="4cf9a-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="4cf9a-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="4cf9a-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="4cf9a-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="4cf9a-127">-Active Directory Domäne dient (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-127">-  Active Directory Domain Serves (AD DS) is offline.</span></span>  <br/><span data-ttu-id="4cf9a-128">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="4cf9a-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="4cf9a-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="4cf9a-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="4cf9a-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="4cf9a-132">**Error**</span></span> <br/> | <span data-ttu-id="4cf9a-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="4cf9a-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="4cf9a-134">The following are examples of sources of errors:</span></span>  <br/>  <span data-ttu-id="4cf9a-135">Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="4cf9a-135">Invalid attributes or elements</span></span>  <br/><br/><span data-ttu-id="4cf9a-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="4cf9a-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="4cf9a-137">-Ein unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="4cf9a-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="4cf9a-138">-Ein Attribut oder Element, das im Kontext ungültig ist</span><span class="sxs-lookup"><span data-stu-id="4cf9a-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="4cf9a-139">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client</span><span class="sxs-lookup"><span data-stu-id="4cf9a-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="4cf9a-140">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="4cf9a-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="4cf9a-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="4cf9a-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4cf9a-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4cf9a-142">Child elements</span></span>

|<span data-ttu-id="4cf9a-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="4cf9a-143">**Element**</span></span>|<span data-ttu-id="4cf9a-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4cf9a-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4cf9a-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="4cf9a-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="4cf9a-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="4cf9a-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4cf9a-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="4cf9a-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="4cf9a-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="4cf9a-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="4cf9a-150">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="4cf9a-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="4cf9a-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="4cf9a-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="4cf9a-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="4cf9a-154">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="4cf9a-154">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="4cf9a-155">Enthält eine Nachricht, die in einem [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-155">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="4cf9a-156">Diagnose</span><span class="sxs-lookup"><span data-stu-id="4cf9a-156">Diagnostics</span></span>](diagnostics.md) <br/> |<span data-ttu-id="4cf9a-157">Enthält Informationen zu Timing und Leistung, die für die Berichterstellung in einem Datencenter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-157">Provides timing and performance information that is used for reporting in a DataCenter.</span></span>  <br/> |
|[<span data-ttu-id="4cf9a-158">Fehler</span><span class="sxs-lookup"><span data-stu-id="4cf9a-158">Errors</span></span>](errors-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4cf9a-159">Enthält einen Eigenschaftenbehälter zum Speichern von Fehlern, die über den Webdienst zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-159">Contains a property bag to store errors that are returned through the Web service.</span></span>  <br/> |
|[<span data-ttu-id="4cf9a-160">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="4cf9a-160">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="4cf9a-161">Enthält eine Liste mit einer oder mehreren Überwachungseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-161">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4cf9a-162">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4cf9a-162">Parent elements</span></span>

<span data-ttu-id="4cf9a-163">Keine.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-163">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="4cf9a-164">Textwert</span><span class="sxs-lookup"><span data-stu-id="4cf9a-164">Text value</span></span>

<span data-ttu-id="4cf9a-165">Keine.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4cf9a-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4cf9a-166">Remarks</span></span>

<span data-ttu-id="4cf9a-167">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4cf9a-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4cf9a-168">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4cf9a-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4cf9a-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="4cf9a-169">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4cf9a-170">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4cf9a-170">Schema Name</span></span>  <br/> |<span data-ttu-id="4cf9a-171">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4cf9a-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4cf9a-172">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4cf9a-172">Validation File</span></span>  <br/> |<span data-ttu-id="4cf9a-173">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4cf9a-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4cf9a-174">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4cf9a-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="4cf9a-175">False</span><span class="sxs-lookup"><span data-stu-id="4cf9a-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4cf9a-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cf9a-176">See also</span></span>

- [<span data-ttu-id="4cf9a-177">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4cf9a-177">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="4cf9a-178">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4cf9a-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

