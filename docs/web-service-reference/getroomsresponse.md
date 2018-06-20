---
title: GetRoomsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetRoomsResponse
api_type:
- schema
ms.assetid: a8c85f65-bb63-4e7a-b0ca-7c9a04560a58
description: Das GetRoomsResponse-Element definiert eine Antwort auf eine GetRooms Vorgang an.
ms.openlocfilehash: 7399ab910a99b39757eb752b11a4771ba81be46a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758791"
---
# <a name="getroomsresponse"></a><span data-ttu-id="e9174-103">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="e9174-103">GetRoomsResponse</span></span>

<span data-ttu-id="e9174-104">Das **GetRoomsResponse** -Element definiert eine Antwort auf eine [GetRooms Vorgang](getrooms-operation.md) an.</span><span class="sxs-lookup"><span data-stu-id="e9174-104">The **GetRoomsResponse** element defines a response to a [GetRooms operation](getrooms-operation.md) request.</span></span> 
  
- [<span data-ttu-id="e9174-105">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e9174-105">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="e9174-106">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="e9174-106">GetRoomsResponse</span></span>](getroomsresponse.md)
  
```XML
<GetRoomsResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Rooms/>
</GetRoomsResponse>
```

 <span data-ttu-id="e9174-107">**GetRoomsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e9174-107">**GetRoomsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e9174-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e9174-108">Attributes and elements</span></span>

<span data-ttu-id="e9174-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e9174-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e9174-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="e9174-110">Attributes</span></span>

|<span data-ttu-id="e9174-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e9174-111">**Attribute**</span></span>|<span data-ttu-id="e9174-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e9174-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e9174-113">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="e9174-113">**ResponseClass**</span></span> <br/> | <span data-ttu-id="e9174-114">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="e9174-114">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="e9174-115">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="e9174-115">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="e9174-116">-Success</span><span class="sxs-lookup"><span data-stu-id="e9174-116">-  Success</span></span>  <br/><span data-ttu-id="e9174-117">-Warnung</span><span class="sxs-lookup"><span data-stu-id="e9174-117">-  Warning</span></span>  <br/><span data-ttu-id="e9174-118">-Fehler</span><span class="sxs-lookup"><span data-stu-id="e9174-118">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="e9174-119">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="e9174-119">ResponseClass attribute values</span></span>

|<span data-ttu-id="e9174-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e9174-120">**Value**</span></span>|<span data-ttu-id="e9174-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e9174-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e9174-122">**Success**</span><span class="sxs-lookup"><span data-stu-id="e9174-122">**Success**</span></span> <br/> |<span data-ttu-id="e9174-123">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="e9174-123">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="e9174-124">**Warning**</span><span class="sxs-lookup"><span data-stu-id="e9174-124">**Warning**</span></span> <br/> | <span data-ttu-id="e9174-125">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="e9174-125">Describes a request that was not processed.</span></span> <span data-ttu-id="e9174-126">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="e9174-126">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="e9174-127">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="e9174-127">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="e9174-128">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="e9174-128">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="e9174-129">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="e9174-129">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="e9174-130">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="e9174-130">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="e9174-131">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="e9174-131">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="e9174-132">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="e9174-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="e9174-133">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="e9174-133">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="e9174-134">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="e9174-134">**Error**</span></span> <br/> | <span data-ttu-id="e9174-135">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e9174-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="e9174-136">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="e9174-136">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="e9174-137">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="e9174-137">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="e9174-138">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="e9174-138">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="e9174-139">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="e9174-139">-  An unknown tag</span></span>  <br/><span data-ttu-id="e9174-140">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="e9174-140">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="e9174-141">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="e9174-141">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="e9174-142">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="e9174-142">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="e9174-143">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="e9174-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e9174-144">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e9174-144">Child elements</span></span>

|<span data-ttu-id="e9174-145">**Element**</span><span class="sxs-lookup"><span data-stu-id="e9174-145">**Element**</span></span>|<span data-ttu-id="e9174-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e9174-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e9174-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="e9174-147">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="e9174-148">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="e9174-148">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="e9174-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e9174-149">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="e9174-150">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="e9174-150">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="e9174-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e9174-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="e9174-152">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="e9174-152">Currently unused and reserved for future use.</span></span> <span data-ttu-id="e9174-153">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="e9174-153">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="e9174-154">MessageXml</span><span class="sxs-lookup"><span data-stu-id="e9174-154">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="e9174-155">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="e9174-155">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="e9174-156">Chatrooms</span><span class="sxs-lookup"><span data-stu-id="e9174-156">Rooms</span></span>](rooms.md) <br/> |<span data-ttu-id="e9174-157">Enthält eine Liste der e-Mail-Adressen und Anzeigenamen, die Besprechungsräumen darstellen.</span><span class="sxs-lookup"><span data-stu-id="e9174-157">Provides a list of email addresses and display names that represent meeting rooms.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e9174-158">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e9174-158">Parent elements</span></span>

|<span data-ttu-id="e9174-159">**Element**</span><span class="sxs-lookup"><span data-stu-id="e9174-159">**Element**</span></span>|<span data-ttu-id="e9174-160">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e9174-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e9174-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e9174-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="e9174-162">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e9174-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9174-163">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e9174-163">Remarks</span></span>

<span data-ttu-id="e9174-164">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e9174-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e9174-165">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e9174-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e9174-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="e9174-166">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e9174-167">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e9174-167">Schema Name</span></span>  <br/> |<span data-ttu-id="e9174-168">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="e9174-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e9174-169">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e9174-169">Validation File</span></span>  <br/> |<span data-ttu-id="e9174-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e9174-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e9174-171">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e9174-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="e9174-172">False</span><span class="sxs-lookup"><span data-stu-id="e9174-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e9174-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9174-173">See also</span></span>

- [<span data-ttu-id="e9174-174">GetRooms-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e9174-174">GetRooms operation</span></span>](getrooms-operation.md)
- [<span data-ttu-id="e9174-175">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e9174-175">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

