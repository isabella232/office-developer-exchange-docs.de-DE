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
description: Das GetServerTimeZonesResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung GetServerTimeZones Vorgang.
ms.openlocfilehash: 594b194f7c73e8880b83db6e20bb447e682a525c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829665"
---
# <a name="getservertimezonesresponsemessage"></a><span data-ttu-id="27891-103">GetServerTimeZonesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="27891-103">GetServerTimeZonesResponseMessage</span></span>

<span data-ttu-id="27891-104">Das **GetServerTimeZonesResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [GetServerTimeZones Vorgang](getservertimezones-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="27891-104">The **GetServerTimeZonesResponseMessage** element contains the status and result of a single [GetServerTimeZones operation](getservertimezones-operation.md) request.</span></span> 
  
```XML
<GetServerTimeZonesResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <TimeZoneDefinitions/>
</GetServerTimeZonesResponseMessage>
```

 <span data-ttu-id="27891-105">**GetServerTimeZonesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="27891-105">**GetServerTimeZonesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="27891-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="27891-106">Attributes and elements</span></span>

<span data-ttu-id="27891-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="27891-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27891-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="27891-108">Attributes</span></span>

|<span data-ttu-id="27891-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="27891-109">**Attribute**</span></span>|<span data-ttu-id="27891-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="27891-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="27891-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="27891-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="27891-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="27891-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="27891-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="27891-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="27891-114">-Success</span><span class="sxs-lookup"><span data-stu-id="27891-114">-  Success</span></span>  <br/><span data-ttu-id="27891-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="27891-115">-  Warning</span></span>  <br/><span data-ttu-id="27891-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="27891-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="27891-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="27891-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="27891-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="27891-118">**Value**</span></span>|<span data-ttu-id="27891-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="27891-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="27891-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="27891-120">**Success**</span></span> <br/> |<span data-ttu-id="27891-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="27891-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="27891-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="27891-122">**Warning**</span></span> <br/> | <span data-ttu-id="27891-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="27891-123">Describes a request that was not processed.</span></span> <span data-ttu-id="27891-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="27891-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="27891-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="27891-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="27891-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="27891-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="27891-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="27891-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="27891-128">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="27891-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="27891-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="27891-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="27891-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="27891-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="27891-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="27891-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="27891-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="27891-132">**Error**</span></span> <br/> | <span data-ttu-id="27891-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="27891-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="27891-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="27891-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="27891-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="27891-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="27891-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="27891-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="27891-137">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="27891-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="27891-138">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="27891-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="27891-139">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="27891-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="27891-140">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="27891-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="27891-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="27891-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="27891-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="27891-142">Child elements</span></span>

|<span data-ttu-id="27891-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="27891-143">**Element**</span></span>|<span data-ttu-id="27891-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="27891-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27891-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="27891-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="27891-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="27891-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="27891-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="27891-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="27891-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="27891-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="27891-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="27891-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="27891-150">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="27891-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="27891-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="27891-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="27891-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="27891-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="27891-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="27891-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="27891-154">TimeZoneDefinitions</span><span class="sxs-lookup"><span data-stu-id="27891-154">TimeZoneDefinitions</span></span>](timezonedefinitions.md) <br/> |<span data-ttu-id="27891-155">Enthält ein Array von Zeitzonendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="27891-155">Contains an array of time zone definitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="27891-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="27891-156">Parent elements</span></span>

|<span data-ttu-id="27891-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="27891-157">**Element**</span></span>|<span data-ttu-id="27891-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="27891-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27891-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="27891-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="27891-160">Enthält die Antwortnachrichten für eine Exchange-Webdienste (EWS)-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="27891-160">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27891-161">Hinweise</span><span class="sxs-lookup"><span data-stu-id="27891-161">Remarks</span></span>

<span data-ttu-id="27891-162">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="27891-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27891-163">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="27891-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27891-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="27891-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="27891-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="27891-165">Schema Name</span></span>  <br/> |<span data-ttu-id="27891-166">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="27891-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="27891-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="27891-167">Validation File</span></span>  <br/> |<span data-ttu-id="27891-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="27891-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="27891-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="27891-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="27891-170">False</span><span class="sxs-lookup"><span data-stu-id="27891-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="27891-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27891-171">See also</span></span>

- [<span data-ttu-id="27891-172">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="27891-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

