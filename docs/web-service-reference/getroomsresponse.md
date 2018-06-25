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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758791"
---
# <a name="getroomsresponse"></a><span data-ttu-id="8ff4f-103">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="8ff4f-103">GetRoomsResponse</span></span>

<span data-ttu-id="8ff4f-104">Das **GetRoomsResponse** -Element definiert eine Antwort auf eine [GetRooms Vorgang](getrooms-operation.md) an.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-104">The **GetRoomsResponse** element defines a response to a [GetRooms operation](getrooms-operation.md) request.</span></span> 
  
- [<span data-ttu-id="8ff4f-105">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8ff4f-105">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="8ff4f-106">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="8ff4f-106">GetRoomsResponse</span></span>](getroomsresponse.md)
  
```XML
<GetRoomsResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Rooms/>
</GetRoomsResponse>
```

 <span data-ttu-id="8ff4f-107">**GetRoomsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="8ff4f-107">**GetRoomsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8ff4f-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8ff4f-108">Attributes and elements</span></span>

<span data-ttu-id="8ff4f-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8ff4f-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="8ff4f-110">Attributes</span></span>

|<span data-ttu-id="8ff4f-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8ff4f-111">**Attribute**</span></span>|<span data-ttu-id="8ff4f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8ff4f-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8ff4f-113">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="8ff4f-113">**ResponseClass**</span></span> <br/> | <span data-ttu-id="8ff4f-114">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-114">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="8ff4f-115">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="8ff4f-115">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="8ff4f-116">-Success</span><span class="sxs-lookup"><span data-stu-id="8ff4f-116">-  Success</span></span>  <br/><span data-ttu-id="8ff4f-117">-Warnung</span><span class="sxs-lookup"><span data-stu-id="8ff4f-117">-  Warning</span></span>  <br/><span data-ttu-id="8ff4f-118">-Fehler</span><span class="sxs-lookup"><span data-stu-id="8ff4f-118">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="8ff4f-119">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="8ff4f-119">ResponseClass attribute values</span></span>

|<span data-ttu-id="8ff4f-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8ff4f-120">**Value**</span></span>|<span data-ttu-id="8ff4f-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8ff4f-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8ff4f-122">**Success**</span><span class="sxs-lookup"><span data-stu-id="8ff4f-122">**Success**</span></span> <br/> |<span data-ttu-id="8ff4f-123">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-123">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="8ff4f-124">**Warning**</span><span class="sxs-lookup"><span data-stu-id="8ff4f-124">**Warning**</span></span> <br/> | <span data-ttu-id="8ff4f-125">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-125">Describes a request that was not processed.</span></span> <span data-ttu-id="8ff4f-126">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-126">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="8ff4f-127">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="8ff4f-127">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="8ff4f-128">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-128">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="8ff4f-129">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-129">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="8ff4f-130">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-130">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="8ff4f-131">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-131">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="8ff4f-132">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="8ff4f-133">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-133">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="8ff4f-134">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="8ff4f-134">**Error**</span></span> <br/> | <span data-ttu-id="8ff4f-135">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="8ff4f-136">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="8ff4f-136">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="8ff4f-137">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="8ff4f-137">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="8ff4f-138">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="8ff4f-138">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="8ff4f-139">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="8ff4f-139">-  An unknown tag</span></span>  <br/><span data-ttu-id="8ff4f-140">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-140">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="8ff4f-141">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="8ff4f-141">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="8ff4f-142">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="8ff4f-142">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="8ff4f-143">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8ff4f-144">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8ff4f-144">Child elements</span></span>

|<span data-ttu-id="8ff4f-145">**Element**</span><span class="sxs-lookup"><span data-stu-id="8ff4f-145">**Element**</span></span>|<span data-ttu-id="8ff4f-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8ff4f-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8ff4f-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="8ff4f-147">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="8ff4f-148">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-148">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="8ff4f-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8ff4f-149">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="8ff4f-150">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-150">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="8ff4f-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8ff4f-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="8ff4f-152">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-152">Currently unused and reserved for future use.</span></span> <span data-ttu-id="8ff4f-153">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-153">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="8ff4f-154">MessageXml</span><span class="sxs-lookup"><span data-stu-id="8ff4f-154">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="8ff4f-155">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-155">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="8ff4f-156">Chatrooms</span><span class="sxs-lookup"><span data-stu-id="8ff4f-156">Rooms</span></span>](rooms.md) <br/> |<span data-ttu-id="8ff4f-157">Enthält eine Liste der e-Mail-Adressen und Anzeigenamen, die Besprechungsräumen darstellen.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-157">Provides a list of email addresses and display names that represent meeting rooms.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8ff4f-158">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8ff4f-158">Parent elements</span></span>

|<span data-ttu-id="8ff4f-159">**Element**</span><span class="sxs-lookup"><span data-stu-id="8ff4f-159">**Element**</span></span>|<span data-ttu-id="8ff4f-160">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8ff4f-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8ff4f-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8ff4f-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="8ff4f-162">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ff4f-163">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8ff4f-163">Remarks</span></span>

<span data-ttu-id="8ff4f-164">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8ff4f-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8ff4f-165">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8ff4f-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ff4f-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="8ff4f-166">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8ff4f-167">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8ff4f-167">Schema Name</span></span>  <br/> |<span data-ttu-id="8ff4f-168">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8ff4f-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8ff4f-169">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8ff4f-169">Validation File</span></span>  <br/> |<span data-ttu-id="8ff4f-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8ff4f-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8ff4f-171">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8ff4f-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="8ff4f-172">False</span><span class="sxs-lookup"><span data-stu-id="8ff4f-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8ff4f-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ff4f-173">See also</span></span>

- [<span data-ttu-id="8ff4f-174">GetRooms-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8ff4f-174">GetRooms operation</span></span>](getrooms-operation.md)
- [<span data-ttu-id="8ff4f-175">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8ff4f-175">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

