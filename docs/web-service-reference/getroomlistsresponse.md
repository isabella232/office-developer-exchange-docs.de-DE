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
description: Das GetRoomListsResponse-Element definiert die Antwort von einer GetRoomLists-Vorgangsanforderung.
ms.openlocfilehash: b6d7c2baa2861309d72bcbf880eaed2ad0989175
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462943"
---
# <a name="getroomlistsresponse"></a><span data-ttu-id="39baf-103">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="39baf-103">GetRoomListsResponse</span></span>

<span data-ttu-id="39baf-104">Das **GetRoomListsResponse** -Element definiert die Antwort von einer [GetRoomLists-Vorgangs](getroomlists-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="39baf-104">The **GetRoomListsResponse** element defines the response from a [GetRoomLists operation](getroomlists-operation.md) request.</span></span> 
  
- [<span data-ttu-id="39baf-105">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="39baf-105">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="39baf-106">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="39baf-106">GetRoomListsResponse</span></span>](getroomlistsresponse.md)
  
```XML
<GetRoomListsResponse ResponseClass="">   
<MessageText/>   
<ResponseCode/>   
<DescriptiveLinkKey/>   
<MessageXml/>   
<RoomLists/>
</GetRoomListsResponse>
```

 <span data-ttu-id="39baf-107">**GetRoomListsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="39baf-107">**GetRoomListsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="39baf-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="39baf-108">Attributes and elements</span></span>

<span data-ttu-id="39baf-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="39baf-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39baf-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="39baf-110">Attributes</span></span>

|<span data-ttu-id="39baf-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="39baf-111">**Attribute**</span></span>|<span data-ttu-id="39baf-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="39baf-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="39baf-113">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="39baf-113">**ResponseClass**</span></span> <br/> | <span data-ttu-id="39baf-114">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="39baf-114">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="39baf-115">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="39baf-115">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="39baf-116">-Success</span><span class="sxs-lookup"><span data-stu-id="39baf-116">-  Success</span></span>  <br/><span data-ttu-id="39baf-117">-Warnung</span><span class="sxs-lookup"><span data-stu-id="39baf-117">-  Warning</span></span>  <br/><span data-ttu-id="39baf-118">-Error</span><span class="sxs-lookup"><span data-stu-id="39baf-118">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="39baf-119">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="39baf-119">ResponseClass attribute values</span></span>

|<span data-ttu-id="39baf-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="39baf-120">**Value**</span></span>|<span data-ttu-id="39baf-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="39baf-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="39baf-122">**Success**</span><span class="sxs-lookup"><span data-stu-id="39baf-122">**Success**</span></span> <br/> |<span data-ttu-id="39baf-123">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="39baf-123">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="39baf-124">**Warning**</span><span class="sxs-lookup"><span data-stu-id="39baf-124">**Warning**</span></span> <br/> | <span data-ttu-id="39baf-125">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="39baf-125">Describes a request that was not processed.</span></span> <span data-ttu-id="39baf-126">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="39baf-126">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="39baf-127">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="39baf-127">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="39baf-128">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="39baf-128">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="39baf-129">-Der Active Directory Verzeichnisdienst ist offline.</span><span class="sxs-lookup"><span data-stu-id="39baf-129">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="39baf-130">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="39baf-130">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="39baf-131">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="39baf-131">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="39baf-132">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="39baf-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="39baf-133">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="39baf-133">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="39baf-134">**Error**</span><span class="sxs-lookup"><span data-stu-id="39baf-134">**Error**</span></span> <br/> | <span data-ttu-id="39baf-135">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="39baf-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="39baf-136">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="39baf-136">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="39baf-137">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="39baf-137">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="39baf-138">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="39baf-138">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="39baf-139">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="39baf-139">-  Unknown tag</span></span>  <br/><span data-ttu-id="39baf-140">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="39baf-140">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="39baf-141">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="39baf-141">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="39baf-142">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="39baf-142">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="39baf-143">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="39baf-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/>- |
   
### <a name="child-elements"></a><span data-ttu-id="39baf-144">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="39baf-144">Child elements</span></span>

|<span data-ttu-id="39baf-145">**Element**</span><span class="sxs-lookup"><span data-stu-id="39baf-145">**Element**</span></span>|<span data-ttu-id="39baf-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="39baf-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39baf-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="39baf-147">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="39baf-148">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="39baf-148">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="39baf-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="39baf-149">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="39baf-150">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="39baf-150">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="39baf-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="39baf-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="39baf-152">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="39baf-152">Currently unused and reserved for future use.</span></span> <span data-ttu-id="39baf-153">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="39baf-153">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="39baf-154">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="39baf-154">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="39baf-155">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="39baf-155">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="39baf-156">RoomLists</span><span class="sxs-lookup"><span data-stu-id="39baf-156">RoomLists</span></span>](roomlists.md) <br/> |<span data-ttu-id="39baf-157">Enthält eine Liste von e-Mail-Adressen und Anzeigenamen, die Listen von Besprechungsräumen darstellen.</span><span class="sxs-lookup"><span data-stu-id="39baf-157">Provides a list of e-mail addresses and display names that represent lists of meeting rooms.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="39baf-158">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="39baf-158">Parent elements</span></span>

|<span data-ttu-id="39baf-159">**Element**</span><span class="sxs-lookup"><span data-stu-id="39baf-159">**Element**</span></span>|<span data-ttu-id="39baf-160">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="39baf-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39baf-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="39baf-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="39baf-162">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="39baf-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="39baf-163">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="39baf-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39baf-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="39baf-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="39baf-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="39baf-165">Schema Name</span></span>  <br/> |<span data-ttu-id="39baf-166">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="39baf-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="39baf-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="39baf-167">Validation File</span></span>  <br/> |<span data-ttu-id="39baf-168">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="39baf-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="39baf-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="39baf-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="39baf-170">False</span><span class="sxs-lookup"><span data-stu-id="39baf-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39baf-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39baf-171">See also</span></span>

- [<span data-ttu-id="39baf-172">GetRoomLists-Vorgang</span><span class="sxs-lookup"><span data-stu-id="39baf-172">GetRoomLists operation</span></span>](getroomlists-operation.md)
- [<span data-ttu-id="39baf-173">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="39baf-173">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

