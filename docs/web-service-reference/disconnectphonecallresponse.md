---
title: DisconnectPhoneCallResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DisconnectPhoneCallResponse
api_type:
- schema
ms.assetid: 05041799-5b81-4b87-ada8-ce6c506ffe01
description: Das DisconnectPhoneCallResponse-Element enthält den Status und das Ergebnis einer einzelnen DisconnectPhoneCall-Anforderung.
ms.openlocfilehash: 6c0696a1d9ab3242920d051b409105644a6b03aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458446"
---
# <a name="disconnectphonecallresponse"></a><span data-ttu-id="9694a-103">DisconnectPhoneCallResponse</span><span class="sxs-lookup"><span data-stu-id="9694a-103">DisconnectPhoneCallResponse</span></span>

<span data-ttu-id="9694a-104">Das **DisconnectPhoneCallResponse** -Element enthält den Status und das Ergebnis einer einzelnen **DisconnectPhoneCall** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9694a-104">The **DisconnectPhoneCallResponse** element contains the status and result of a single **DisconnectPhoneCall** request.</span></span> 
  
```xml
<DisconnectPhoneCallResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DisconnectPhoneCallResponse>
```

 <span data-ttu-id="9694a-105">**DisconnectPhoneCallResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="9694a-105">**DisconnectPhoneCallResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9694a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9694a-106">Attributes and elements</span></span>

<span data-ttu-id="9694a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9694a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9694a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9694a-108">Attributes</span></span>

|<span data-ttu-id="9694a-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9694a-109">**Attribute**</span></span>|<span data-ttu-id="9694a-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9694a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9694a-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="9694a-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="9694a-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="9694a-112">Describes the status of the response.</span></span><br/><br/><span data-ttu-id="9694a-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="9694a-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="9694a-114">-Success</span><span class="sxs-lookup"><span data-stu-id="9694a-114">-  Success</span></span>  <br/><span data-ttu-id="9694a-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="9694a-115">-  Warning</span></span>  <br/><span data-ttu-id="9694a-116">-Error</span><span class="sxs-lookup"><span data-stu-id="9694a-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="9694a-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="9694a-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="9694a-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9694a-118">**Value**</span></span>|<span data-ttu-id="9694a-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9694a-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9694a-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="9694a-120">**Success**</span></span> <br/> |<span data-ttu-id="9694a-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="9694a-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="9694a-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="9694a-122">**Warning**</span></span> <br/> | <span data-ttu-id="9694a-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="9694a-123">Describes a request that was not processed.</span></span> <span data-ttu-id="9694a-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="9694a-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="9694a-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="9694a-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="9694a-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="9694a-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="9694a-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="9694a-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="9694a-128">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="9694a-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="9694a-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="9694a-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="9694a-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="9694a-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="9694a-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="9694a-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="9694a-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="9694a-132">**Error**</span></span> <br/> | <span data-ttu-id="9694a-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9694a-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="9694a-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="9694a-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="9694a-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="9694a-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="9694a-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="9694a-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="9694a-137">-Ein unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="9694a-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="9694a-138">-Ein Attribut oder Element, das im Kontext ungültig ist</span><span class="sxs-lookup"><span data-stu-id="9694a-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="9694a-139">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client</span><span class="sxs-lookup"><span data-stu-id="9694a-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="9694a-140">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="9694a-140">-  A server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="9694a-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="9694a-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9694a-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9694a-142">Child elements</span></span>

|<span data-ttu-id="9694a-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="9694a-143">**Element**</span></span>|<span data-ttu-id="9694a-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9694a-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9694a-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="9694a-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="9694a-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="9694a-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="9694a-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9694a-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="9694a-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="9694a-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="9694a-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9694a-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="9694a-150">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="9694a-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="9694a-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="9694a-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="9694a-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="9694a-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="9694a-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="9694a-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9694a-154">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9694a-154">Parent elements</span></span>

<span data-ttu-id="9694a-155">Keine.</span><span class="sxs-lookup"><span data-stu-id="9694a-155">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="9694a-156">Textwert</span><span class="sxs-lookup"><span data-stu-id="9694a-156">Text value</span></span>

<span data-ttu-id="9694a-157">Keine.</span><span class="sxs-lookup"><span data-stu-id="9694a-157">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9694a-158">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9694a-158">Remarks</span></span>

<span data-ttu-id="9694a-159">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9694a-159">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9694a-160">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9694a-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9694a-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="9694a-161">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9694a-162">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9694a-162">Schema Name</span></span>  <br/> |<span data-ttu-id="9694a-163">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="9694a-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9694a-164">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9694a-164">Validation File</span></span>  <br/> |<span data-ttu-id="9694a-165">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9694a-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9694a-166">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9694a-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="9694a-167">False</span><span class="sxs-lookup"><span data-stu-id="9694a-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9694a-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9694a-168">See also</span></span>

- [<span data-ttu-id="9694a-169">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9694a-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

