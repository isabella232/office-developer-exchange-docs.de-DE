---
title: GetRoomListsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetRoomListsResponse
api_type:
- schema
ms.assetid: 8c736f68-1026-496a-b12f-c169c078abd0
description: Das GetRoomListsResponse-Element definiert die Antwort aus einer GetRoomLists Vorgang Anforderung.
ms.openlocfilehash: 8231435f7dc348a070852f57d6152550326b5df6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758797"
---
# <a name="getroomlistsresponse"></a><span data-ttu-id="4278a-103">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="4278a-103">GetRoomListsResponse</span></span>

<span data-ttu-id="4278a-104">Das **GetRoomListsResponse** -Element definiert die Antwort von einer Anforderung [GetRoomLists Vorgang](getroomlists-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="4278a-104">The **GetRoomListsResponse** element defines the response from a [GetRoomLists operation](getroomlists-operation.md) request.</span></span> 
  
- [<span data-ttu-id="4278a-105">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4278a-105">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="4278a-106">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="4278a-106">GetRoomListsResponse</span></span>](getroomlistsresponse.md)
  
```XML
<GetRoomListsResponse ResponseClass="">   
<MessageText/>   
<ResponseCode/>   
<DescriptiveLinkKey/>   
<MessageXml/>   
<RoomLists/>
</GetRoomListsResponse>
```

 <span data-ttu-id="4278a-107">**GetRoomListsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="4278a-107">**GetRoomListsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4278a-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4278a-108">Attributes and elements</span></span>

<span data-ttu-id="4278a-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4278a-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4278a-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="4278a-110">Attributes</span></span>

|<span data-ttu-id="4278a-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4278a-111">**Attribute**</span></span>|<span data-ttu-id="4278a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4278a-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4278a-113">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="4278a-113">**ResponseClass**</span></span> <br/> | <span data-ttu-id="4278a-114">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="4278a-114">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="4278a-115">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="4278a-115">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="4278a-116">-Success</span><span class="sxs-lookup"><span data-stu-id="4278a-116">-  Success</span></span>  <br/><span data-ttu-id="4278a-117">-Warnung</span><span class="sxs-lookup"><span data-stu-id="4278a-117">-  Warning</span></span>  <br/><span data-ttu-id="4278a-118">-Fehler</span><span class="sxs-lookup"><span data-stu-id="4278a-118">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="4278a-119">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="4278a-119">ResponseClass attribute values</span></span>

|<span data-ttu-id="4278a-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4278a-120">**Value**</span></span>|<span data-ttu-id="4278a-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4278a-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4278a-122">**Success**</span><span class="sxs-lookup"><span data-stu-id="4278a-122">**Success**</span></span> <br/> |<span data-ttu-id="4278a-123">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="4278a-123">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="4278a-124">**Warning**</span><span class="sxs-lookup"><span data-stu-id="4278a-124">**Warning**</span></span> <br/> | <span data-ttu-id="4278a-125">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="4278a-125">Describes a request that was not processed.</span></span> <span data-ttu-id="4278a-126">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="4278a-126">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="4278a-127">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="4278a-127">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="4278a-128">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="4278a-128">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="4278a-129">– Der Active Directory-Verzeichnisdienst ist offline.</span><span class="sxs-lookup"><span data-stu-id="4278a-129">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="4278a-130">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="4278a-130">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="4278a-131">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="4278a-131">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="4278a-132">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="4278a-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="4278a-133">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="4278a-133">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="4278a-134">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="4278a-134">**Error**</span></span> <br/> | <span data-ttu-id="4278a-135">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4278a-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="4278a-136">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="4278a-136">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="4278a-137">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="4278a-137">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="4278a-138">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="4278a-138">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="4278a-139">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="4278a-139">-  Unknown tag</span></span>  <br/><span data-ttu-id="4278a-140">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="4278a-140">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="4278a-141">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="4278a-141">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="4278a-142">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="4278a-142">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="4278a-143">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="4278a-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/>- |
   
### <a name="child-elements"></a><span data-ttu-id="4278a-144">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4278a-144">Child elements</span></span>

|<span data-ttu-id="4278a-145">**Element**</span><span class="sxs-lookup"><span data-stu-id="4278a-145">**Element**</span></span>|<span data-ttu-id="4278a-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4278a-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4278a-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="4278a-147">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="4278a-148">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="4278a-148">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="4278a-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4278a-149">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="4278a-150">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="4278a-150">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="4278a-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="4278a-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="4278a-152">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="4278a-152">Currently unused and reserved for future use.</span></span> <span data-ttu-id="4278a-153">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="4278a-153">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="4278a-154">MessageXml</span><span class="sxs-lookup"><span data-stu-id="4278a-154">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="4278a-155">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="4278a-155">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="4278a-156">RoomLists</span><span class="sxs-lookup"><span data-stu-id="4278a-156">RoomLists</span></span>](roomlists.md) <br/> |<span data-ttu-id="4278a-157">Enthält eine Liste der e-Mail-Adressen und Anzeigenamen, die Listen von Besprechungsräumen darstellen.</span><span class="sxs-lookup"><span data-stu-id="4278a-157">Provides a list of e-mail addresses and display names that represent lists of meeting rooms.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4278a-158">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4278a-158">Parent elements</span></span>

|<span data-ttu-id="4278a-159">**Element**</span><span class="sxs-lookup"><span data-stu-id="4278a-159">**Element**</span></span>|<span data-ttu-id="4278a-160">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4278a-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4278a-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4278a-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="4278a-162">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4278a-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="4278a-163">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4278a-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4278a-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="4278a-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4278a-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4278a-165">Schema Name</span></span>  <br/> |<span data-ttu-id="4278a-166">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4278a-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4278a-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4278a-167">Validation File</span></span>  <br/> |<span data-ttu-id="4278a-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4278a-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4278a-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4278a-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="4278a-170">False</span><span class="sxs-lookup"><span data-stu-id="4278a-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4278a-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4278a-171">See also</span></span>

- [<span data-ttu-id="4278a-172">GetRoomLists-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4278a-172">GetRoomLists operation</span></span>](getroomlists-operation.md)
- [<span data-ttu-id="4278a-173">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4278a-173">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

