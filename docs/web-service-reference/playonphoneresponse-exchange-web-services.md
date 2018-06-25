---
title: PlayOnPhoneResponse (Exchange Web Services)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PlayOnPhoneResponse
api_type:
- schema
ms.assetid: 578b70d1-dc9d-4bce-b859-0109b2d2bcec
description: Das PlayOnPhoneResponse-Element gibt die Antwort auf eine Anforderung an eine Voicemail über das Telefon abgespielt werden soll.
ms.openlocfilehash: 203309bdd6d17b1c78054e673f8a340c2f069b38
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830831"
---
# <a name="playonphoneresponse-exchange-web-services"></a><span data-ttu-id="86e3b-103">PlayOnPhoneResponse (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="86e3b-103">PlayOnPhoneResponse (Exchange Web Services)</span></span>

<span data-ttu-id="86e3b-104">Das **PlayOnPhoneResponse** -Element gibt die Antwort auf eine Anforderung an eine Voicemail über das Telefon abgespielt werden soll.</span><span class="sxs-lookup"><span data-stu-id="86e3b-104">The **PlayOnPhoneResponse** element specifies the response to a request to play a voice mail over the telephone.</span></span> 
  
```xml
<PlayOnPhoneResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <PhoneCallId/>
</PlayOnPhoneResponse>
```

 <span data-ttu-id="86e3b-105">**PlayOnPhoneResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="86e3b-105">**PlayOnPhoneResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="86e3b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="86e3b-106">Attributes and elements</span></span>

<span data-ttu-id="86e3b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="86e3b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="86e3b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="86e3b-108">Attributes</span></span>

|<span data-ttu-id="86e3b-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="86e3b-109">**Attribute**</span></span>|<span data-ttu-id="86e3b-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="86e3b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="86e3b-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="86e3b-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="86e3b-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="86e3b-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="86e3b-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="86e3b-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="86e3b-114">-Success</span><span class="sxs-lookup"><span data-stu-id="86e3b-114">-  Success</span></span>  <br/><span data-ttu-id="86e3b-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="86e3b-115">-  Warning</span></span>  <br/><span data-ttu-id="86e3b-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="86e3b-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="86e3b-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="86e3b-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="86e3b-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="86e3b-118">**Value**</span></span>|<span data-ttu-id="86e3b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="86e3b-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="86e3b-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="86e3b-120">**Success**</span></span> <br/> |<span data-ttu-id="86e3b-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="86e3b-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="86e3b-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="86e3b-122">**Warning**</span></span> <br/> | <span data-ttu-id="86e3b-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="86e3b-123">Describes a request that was not processed.</span></span> <span data-ttu-id="86e3b-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="86e3b-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="86e3b-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="86e3b-125">The following are examples of sources of warnings:</span></span> <br/><br/><span data-ttu-id="86e3b-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="86e3b-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="86e3b-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="86e3b-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="86e3b-128">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="86e3b-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="86e3b-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="86e3b-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="86e3b-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="86e3b-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="86e3b-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="86e3b-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="86e3b-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="86e3b-132">**Error**</span></span> <br/> | <span data-ttu-id="86e3b-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="86e3b-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="86e3b-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="86e3b-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="86e3b-135">-Ungültige Attribute oder Elemente.</span><span class="sxs-lookup"><span data-stu-id="86e3b-135">-  Invalid attributes or elements.</span></span>  <br/><span data-ttu-id="86e3b-136">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="86e3b-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="86e3b-137">-Eine unbekannte Marke.</span><span class="sxs-lookup"><span data-stu-id="86e3b-137">-  An unknown tag.</span></span>  <br/><span data-ttu-id="86e3b-138">-Ein Attribut oder ein Element, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="86e3b-138">-  An attribute or element that is not valid in the context.</span></span>  <br/><span data-ttu-id="86e3b-139">-Eine Versuch nicht autorisierten Zugriff von jedem Client.</span><span class="sxs-lookup"><span data-stu-id="86e3b-139">-  An unauthorized access attempt by any client.</span></span>  <br/><span data-ttu-id="86e3b-140">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf.</span><span class="sxs-lookup"><span data-stu-id="86e3b-140">-  A server-side failure in response to a valid client-side call.</span></span>  <br/><br/>  <span data-ttu-id="86e3b-141">Informationen zu dem Fehler kann in den [ResponseCode](responsecode.md) und [MessageText](messagetext.md) Elementthemen gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="86e3b-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) element topics.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="86e3b-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="86e3b-142">Child elements</span></span>

|<span data-ttu-id="86e3b-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="86e3b-143">**Element**</span></span>|<span data-ttu-id="86e3b-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="86e3b-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86e3b-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="86e3b-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="86e3b-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="86e3b-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="86e3b-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="86e3b-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="86e3b-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="86e3b-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="86e3b-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="86e3b-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="86e3b-150">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="86e3b-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="86e3b-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="86e3b-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="86e3b-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="86e3b-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="86e3b-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="86e3b-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="86e3b-154">PhoneCallId</span><span class="sxs-lookup"><span data-stu-id="86e3b-154">PhoneCallId</span></span>](phonecallid.md) <br/> |<span data-ttu-id="86e3b-155">Gibt den Bezeichner entgegengenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="86e3b-155">Specifies the telephone call identifier.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="86e3b-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="86e3b-156">Parent elements</span></span>

<span data-ttu-id="86e3b-157">Keine.</span><span class="sxs-lookup"><span data-stu-id="86e3b-157">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="86e3b-158">Hinweise</span><span class="sxs-lookup"><span data-stu-id="86e3b-158">Remarks</span></span>

<span data-ttu-id="86e3b-159">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="86e3b-159">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="86e3b-160">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="86e3b-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86e3b-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="86e3b-161">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="86e3b-162">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="86e3b-162">Schema Name</span></span>  <br/> |<span data-ttu-id="86e3b-163">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="86e3b-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="86e3b-164">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="86e3b-164">Validation File</span></span>  <br/> |<span data-ttu-id="86e3b-165">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="86e3b-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="86e3b-166">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="86e3b-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="86e3b-167">False</span><span class="sxs-lookup"><span data-stu-id="86e3b-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="86e3b-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86e3b-168">See also</span></span>

- [<span data-ttu-id="86e3b-169">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="86e3b-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

