---
title: GetServerTimeZonesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServerTimeZonesResponseMessage
api_type:
- schema
ms.assetid: eb2592b2-144f-4c33-8df7-8e70dce7ab55
description: Das GetServerTimeZonesResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen GetServerTimeZones-Vorgangsanforderung.
ms.openlocfilehash: de032c961f6fffa5b4f0607a17fe48630510fda9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460918"
---
# <a name="getservertimezonesresponsemessage"></a><span data-ttu-id="9b024-103">GetServerTimeZonesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9b024-103">GetServerTimeZonesResponseMessage</span></span>

<span data-ttu-id="9b024-104">Das **GetServerTimeZonesResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [GetServerTimeZones-Vorgangs](getservertimezones-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9b024-104">The **GetServerTimeZonesResponseMessage** element contains the status and result of a single [GetServerTimeZones operation](getservertimezones-operation.md) request.</span></span> 
  
```XML
<GetServerTimeZonesResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <TimeZoneDefinitions/>
</GetServerTimeZonesResponseMessage>
```

 <span data-ttu-id="9b024-105">**GetServerTimeZonesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="9b024-105">**GetServerTimeZonesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9b024-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9b024-106">Attributes and elements</span></span>

<span data-ttu-id="9b024-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9b024-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9b024-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9b024-108">Attributes</span></span>

|<span data-ttu-id="9b024-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9b024-109">**Attribute**</span></span>|<span data-ttu-id="9b024-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b024-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b024-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="9b024-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="9b024-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="9b024-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="9b024-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="9b024-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="9b024-114">-Success</span><span class="sxs-lookup"><span data-stu-id="9b024-114">-  Success</span></span>  <br/><span data-ttu-id="9b024-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="9b024-115">-  Warning</span></span>  <br/><span data-ttu-id="9b024-116">-Error</span><span class="sxs-lookup"><span data-stu-id="9b024-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="9b024-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="9b024-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="9b024-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9b024-118">**Value**</span></span>|<span data-ttu-id="9b024-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b024-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b024-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="9b024-120">**Success**</span></span> <br/> |<span data-ttu-id="9b024-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="9b024-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="9b024-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="9b024-122">**Warning**</span></span> <br/> | <span data-ttu-id="9b024-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="9b024-123">Describes a request that was not processed.</span></span> <span data-ttu-id="9b024-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="9b024-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="9b024-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="9b024-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="9b024-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="9b024-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="9b024-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="9b024-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="9b024-128">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="9b024-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="9b024-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="9b024-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="9b024-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="9b024-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="9b024-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="9b024-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="9b024-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="9b024-132">**Error**</span></span> <br/> | <span data-ttu-id="9b024-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9b024-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="9b024-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="9b024-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="9b024-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="9b024-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="9b024-136">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="9b024-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="9b024-137">-Ein unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="9b024-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="9b024-138">-Ein Attribut oder Element, das im Kontext ungültig ist</span><span class="sxs-lookup"><span data-stu-id="9b024-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="9b024-139">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client</span><span class="sxs-lookup"><span data-stu-id="9b024-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="9b024-140">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="9b024-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="9b024-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="9b024-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9b024-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9b024-142">Child elements</span></span>

|<span data-ttu-id="9b024-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="9b024-143">**Element**</span></span>|<span data-ttu-id="9b024-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b024-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b024-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="9b024-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="9b024-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="9b024-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="9b024-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9b024-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="9b024-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="9b024-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="9b024-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9b024-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="9b024-150">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="9b024-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="9b024-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="9b024-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="9b024-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="9b024-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="9b024-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="9b024-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="9b024-154">TimeZoneDefinitions</span><span class="sxs-lookup"><span data-stu-id="9b024-154">TimeZoneDefinitions</span></span>](timezonedefinitions.md) <br/> |<span data-ttu-id="9b024-155">Enthält ein Array von Zeitzonendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9b024-155">Contains an array of time zone definitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9b024-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9b024-156">Parent elements</span></span>

|<span data-ttu-id="9b024-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="9b024-157">**Element**</span></span>|<span data-ttu-id="9b024-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b024-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b024-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9b024-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="9b024-160">Enthält die Antwortnachrichten für eine Exchange-Webdienste Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9b024-160">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b024-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b024-161">Remarks</span></span>

<span data-ttu-id="9b024-162">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9b024-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9b024-163">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9b024-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b024-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b024-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9b024-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9b024-165">Schema Name</span></span>  <br/> |<span data-ttu-id="9b024-166">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="9b024-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9b024-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9b024-167">Validation File</span></span>  <br/> |<span data-ttu-id="9b024-168">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9b024-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9b024-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9b024-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="9b024-170">False</span><span class="sxs-lookup"><span data-stu-id="9b024-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b024-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b024-171">See also</span></span>

- [<span data-ttu-id="9b024-172">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9b024-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

