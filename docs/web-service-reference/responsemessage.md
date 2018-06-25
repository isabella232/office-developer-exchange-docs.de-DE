---
title: ResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseMessage
api_type:
- schema
ms.assetid: bf57265a-d354-4cd7-bbfc-d93e19cbede6
description: Das ResponseMessage-Element enthält beschreibende Informationen über den Antwortstatus für eine einzelne Entität innerhalb einer Anforderung.
ms.openlocfilehash: 69f1f6f12d10044045b72dd644536e742c479b9e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831191"
---
# <a name="responsemessage"></a><span data-ttu-id="2def3-103">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2def3-103">ResponseMessage</span></span>

<span data-ttu-id="2def3-104">Das **ResponseMessage** -Element enthält beschreibende Informationen über den Antwortstatus für eine einzelne Entität innerhalb einer Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2def3-104">The **ResponseMessage** element provides descriptive information about the response status for a single entity within a request.</span></span> 
  
```xml
<ResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</ResponseMessage>
```

 <span data-ttu-id="2def3-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2def3-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2def3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2def3-106">Attributes and elements</span></span>

<span data-ttu-id="2def3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2def3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2def3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2def3-108">Attributes</span></span>

|<span data-ttu-id="2def3-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2def3-109">**Attribute**</span></span>|<span data-ttu-id="2def3-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2def3-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2def3-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="2def3-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="2def3-112">Stellt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="2def3-112">Represents the status of the response.</span></span> <br/><br/><span data-ttu-id="2def3-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="2def3-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="2def3-114">-Success</span><span class="sxs-lookup"><span data-stu-id="2def3-114">-  Success</span></span>  <br/><span data-ttu-id="2def3-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="2def3-115">-  Warning</span></span>  <br/><span data-ttu-id="2def3-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="2def3-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="2def3-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="2def3-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="2def3-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2def3-118">**Value**</span></span>|<span data-ttu-id="2def3-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2def3-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2def3-120">Erfolg</span><span class="sxs-lookup"><span data-stu-id="2def3-120">Success</span></span>  <br/> |<span data-ttu-id="2def3-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="2def3-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="2def3-122">Warning</span><span class="sxs-lookup"><span data-stu-id="2def3-122">Warning</span></span>  <br/> | <span data-ttu-id="2def3-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="2def3-123">Describes a request that was not processed.</span></span> <span data-ttu-id="2def3-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="2def3-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="2def3-125">Es folgen einige möglichen Ursachen für Warnungen:</span><span class="sxs-lookup"><span data-stu-id="2def3-125">The following are some possible causes for warnings:</span></span>  <br/><br/><span data-ttu-id="2def3-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="2def3-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="2def3-127">– Der Active Directory-Verzeichnisdienst ist offline.</span><span class="sxs-lookup"><span data-stu-id="2def3-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="2def3-128">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="2def3-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="2def3-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="2def3-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="2def3-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="2def3-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="2def3-131">-Ein Kontingent überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="2def3-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="2def3-132">Fehler</span><span class="sxs-lookup"><span data-stu-id="2def3-132">Error</span></span>  <br/> | <span data-ttu-id="2def3-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2def3-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="2def3-134">Es folgen einige möglichen Ursachen für Fehler:</span><span class="sxs-lookup"><span data-stu-id="2def3-134">The following are some possible causes for errors:</span></span>  <br/><br/><span data-ttu-id="2def3-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="2def3-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="2def3-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="2def3-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="2def3-137">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="2def3-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="2def3-138">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="2def3-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="2def3-139">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="2def3-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="2def3-140">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="2def3-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="2def3-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="2def3-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2def3-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2def3-142">Child elements</span></span>

|<span data-ttu-id="2def3-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="2def3-143">**Element**</span></span>|<span data-ttu-id="2def3-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2def3-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2def3-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="2def3-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="2def3-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="2def3-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="2def3-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2def3-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="2def3-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="2def3-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="2def3-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2def3-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="2def3-150">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="2def3-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="2def3-151">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="2def3-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="2def3-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="2def3-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="2def3-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="2def3-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2def3-154">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2def3-154">Parent elements</span></span>

|<span data-ttu-id="2def3-155">**Element**</span><span class="sxs-lookup"><span data-stu-id="2def3-155">**Element**</span></span>|<span data-ttu-id="2def3-156">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2def3-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2def3-157">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="2def3-157">FreeBusyResponse</span></span>](freebusyresponse.md) <br/> |<span data-ttu-id="2def3-158">Die Frei/Gebucht-Informationen für ein einzelnes Postfachbenutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="2def3-158">Contains the free/busy information for a single mailbox user.</span></span> <br/> <br/> <span data-ttu-id="2def3-159">Es folgt der 2.0 XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="2def3-159">The following is the XPath 2.0 expression to this element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray[i]/FreeBusyResponse` <br/> |
|[<span data-ttu-id="2def3-160">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="2def3-160">SuggestionsResponse</span></span>](suggestionsresponse.md) <br/> |<span data-ttu-id="2def3-161">Enthält Informationen und Vorschlag Daten für Besprechungsvorschläge angefordert.</span><span class="sxs-lookup"><span data-stu-id="2def3-161">Contains response information and suggestion data for requested meeting suggestions.</span></span>  <br/><br/> <span data-ttu-id="2def3-162">Es folgt der 2.0 XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="2def3-162">The following is the XPath 2.0 expression to this element:</span></span><br/>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse` <br/> |
|[<span data-ttu-id="2def3-163">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="2def3-163">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md) <br/> |<span data-ttu-id="2def3-164">Enthält die Antwort Ergebnisse und OOF-Einstellungen für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="2def3-164">Contains the response results and the OOF settings for a user.</span></span>  <br/><br/> <span data-ttu-id="2def3-165">Es folgt der 2.0 XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="2def3-165">The following is the XPath 2.0 expression to this element:</span></span>  <br/><br/>  `/GetUserOofSettingsResponse` <br/> |
|[<span data-ttu-id="2def3-166">SetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="2def3-166">SetUserOofSettingsResponse</span></span>](setuseroofsettingsresponse.md) <br/> |<span data-ttu-id="2def3-167">Das Ergebnis einer versuchte [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) -Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="2def3-167">Contains the result of an attempted [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) message.</span></span> <br/> <br/> <span data-ttu-id="2def3-168">Es folgt der 2.0 XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="2def3-168">The following is the XPath 2.0 expression to this element:</span></span>  <br/><br/>  `/SetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2def3-169">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2def3-169">Remarks</span></span>

<span data-ttu-id="2def3-170">Der Typ **ResponseMessageType** ist für alle Exchange-Webdienste-Antworten.</span><span class="sxs-lookup"><span data-stu-id="2def3-170">The **ResponseMessageType** type is common to all Exchange Web Services responses.</span></span> <span data-ttu-id="2def3-171">Der Typ **ResponseMessageType** wird durch den folgenden komplexen Typen erweitert:</span><span class="sxs-lookup"><span data-stu-id="2def3-171">The **ResponseMessageType** type is extended by the following complex types:</span></span> 
  
- <span data-ttu-id="2def3-172">**ApplyConversationActionResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2def3-172">**ApplyConversationActionResponseMessageType**</span></span>
    
- <span data-ttu-id="2def3-173">**AttachmentInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2def3-173">**AttachmentInfoResponseMessageType**</span></span>
    
- <span data-ttu-id="2def3-174">**DeleteAttachmentResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2def3-174">**DeleteAttachmentResponseMessageType**</span></span>
    
- <span data-ttu-id="2def3-175">**DeleteItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2def3-175">**DeleteItemResponseMessageType**</span></span>
    
- <span data-ttu-id="2def3-176">**ExpandDLResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2def3-176">**ExpandDLResponseMessageType**</span></span>
    
- <span data-ttu-id="2def3-177">**FindFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2def3-177">**FindFolderResponseMessageType**</span></span>
    
- <span data-ttu-id="2def3-178">**FindItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2def3-178">**FindItemResponseMessageType**</span></span>
    
- <span data-ttu-id="2def3-179">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2def3-179">**FolderInfoResponseMessageType**</span></span>
    
- <span data-ttu-id="2def3-180">**GetEventsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2def3-180">**GetEventsResponseMessageType**</span></span>
    
- <span data-ttu-id="2def3-181">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2def3-181">**ItemInfoResponseMessageType**</span></span>
    
- <span data-ttu-id="2def3-182">**ResolveNamesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2def3-182">**ResolveNamesResponseMessageType**</span></span>
    
- <span data-ttu-id="2def3-183">**SubscribeResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2def3-183">**SubscribeResponseMessageType**</span></span>
    
- <span data-ttu-id="2def3-184">**SendNotificationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2def3-184">**SendNotificationResponseMessageType**</span></span>
    
- <span data-ttu-id="2def3-185">**SyncFolderHierarchyResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2def3-185">**SyncFolderHierarchyResponseMessageType**</span></span>
    
- <span data-ttu-id="2def3-186">**SyncFolderItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2def3-186">**SyncFolderItemsResponseMessageType**</span></span>
    
<span data-ttu-id="2def3-187">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="2def3-187">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="2def3-188">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="2def3-188">Version differences</span></span>

<span data-ttu-id="2def3-189">Die Typen **ApplyConversationActionResponseMessage** und **DeleteItemResponseMessageType** wurden in Exchange Build 15.00.0986.00 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2def3-189">The **ApplyConversationActionResponseMessage** and **DeleteItemResponseMessageType** types were introduced in Exchange build 15.00.0986.00.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="2def3-190">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2def3-190">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2def3-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="2def3-191">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2def3-192">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2def3-192">Schema Name</span></span>  <br/> |<span data-ttu-id="2def3-193">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2def3-193">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2def3-194">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2def3-194">Validation File</span></span>  <br/> |<span data-ttu-id="2def3-195">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2def3-195">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2def3-196">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2def3-196">Can be Empty</span></span>  <br/> |<span data-ttu-id="2def3-197">False</span><span class="sxs-lookup"><span data-stu-id="2def3-197">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2def3-198">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2def3-198">See also</span></span>

- [<span data-ttu-id="2def3-199">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2def3-199">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="2def3-200">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2def3-200">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)
- [<span data-ttu-id="2def3-201">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2def3-201">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
- [<span data-ttu-id="2def3-202">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="2def3-202">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

