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
description: Das ResponseMessage-Element enthält beschreibende Informationen zum Antwortstatus für eine einzelne Entität innerhalb einer Anforderung.
ms.openlocfilehash: a7f4240b1e988cb69d67118c6db58db0d7babba5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467158"
---
# <a name="responsemessage"></a><span data-ttu-id="ef702-103">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ef702-103">ResponseMessage</span></span>

<span data-ttu-id="ef702-104">Das **ResponseMessage** -Element enthält beschreibende Informationen zum Antwortstatus für eine einzelne Entität innerhalb einer Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ef702-104">The **ResponseMessage** element provides descriptive information about the response status for a single entity within a request.</span></span> 
  
```xml
<ResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</ResponseMessage>
```

 <span data-ttu-id="ef702-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ef702-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef702-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ef702-106">Attributes and elements</span></span>

<span data-ttu-id="ef702-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ef702-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef702-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ef702-108">Attributes</span></span>

|<span data-ttu-id="ef702-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ef702-109">**Attribute**</span></span>|<span data-ttu-id="ef702-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef702-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef702-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="ef702-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="ef702-112">Stellt den Status der Antwort dar.</span><span class="sxs-lookup"><span data-stu-id="ef702-112">Represents the status of the response.</span></span> <br/><br/><span data-ttu-id="ef702-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="ef702-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="ef702-114">-Success</span><span class="sxs-lookup"><span data-stu-id="ef702-114">-  Success</span></span>  <br/><span data-ttu-id="ef702-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="ef702-115">-  Warning</span></span>  <br/><span data-ttu-id="ef702-116">-Error</span><span class="sxs-lookup"><span data-stu-id="ef702-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="ef702-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="ef702-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="ef702-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ef702-118">**Value**</span></span>|<span data-ttu-id="ef702-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef702-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef702-120">Erfolg</span><span class="sxs-lookup"><span data-stu-id="ef702-120">Success</span></span>  <br/> |<span data-ttu-id="ef702-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ef702-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="ef702-122">Warnung</span><span class="sxs-lookup"><span data-stu-id="ef702-122">Warning</span></span>  <br/> | <span data-ttu-id="ef702-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ef702-123">Describes a request that was not processed.</span></span> <span data-ttu-id="ef702-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ef702-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="ef702-125">Es folgen einige mögliche Ursachen für Warnungen:</span><span class="sxs-lookup"><span data-stu-id="ef702-125">The following are some possible causes for warnings:</span></span>  <br/><br/><span data-ttu-id="ef702-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="ef702-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="ef702-127">-Der Active Directory Verzeichnisdienst ist offline.</span><span class="sxs-lookup"><span data-stu-id="ef702-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="ef702-128">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="ef702-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="ef702-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="ef702-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="ef702-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="ef702-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="ef702-131">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="ef702-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="ef702-132">Fehler (ungefährer Wortlaut)</span><span class="sxs-lookup"><span data-stu-id="ef702-132">Error</span></span>  <br/> | <span data-ttu-id="ef702-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ef702-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="ef702-134">Im folgenden finden Sie einige mögliche Ursachen für Fehler:</span><span class="sxs-lookup"><span data-stu-id="ef702-134">The following are some possible causes for errors:</span></span>  <br/><br/><span data-ttu-id="ef702-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="ef702-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="ef702-136">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="ef702-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="ef702-137">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="ef702-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="ef702-138">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="ef702-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="ef702-139">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="ef702-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="ef702-140">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="ef702-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="ef702-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="ef702-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ef702-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef702-142">Child elements</span></span>

|<span data-ttu-id="ef702-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="ef702-143">**Element**</span></span>|<span data-ttu-id="ef702-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef702-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef702-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="ef702-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ef702-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="ef702-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ef702-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ef702-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ef702-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ef702-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="ef702-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ef702-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ef702-150">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="ef702-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="ef702-151">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="ef702-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="ef702-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="ef702-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ef702-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="ef702-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ef702-154">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef702-154">Parent elements</span></span>

|<span data-ttu-id="ef702-155">**Element**</span><span class="sxs-lookup"><span data-stu-id="ef702-155">**Element**</span></span>|<span data-ttu-id="ef702-156">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef702-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef702-157">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="ef702-157">FreeBusyResponse</span></span>](freebusyresponse.md) <br/> |<span data-ttu-id="ef702-158">Enthält die Frei/Gebucht-Informationen für einen einzelnen Postfachbenutzer.</span><span class="sxs-lookup"><span data-stu-id="ef702-158">Contains the free/busy information for a single mailbox user.</span></span> <br/> <br/> <span data-ttu-id="ef702-159">Im folgenden finden Sie den XPath 2,0-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="ef702-159">The following is the XPath 2.0 expression to this element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray[i]/FreeBusyResponse` <br/> |
|[<span data-ttu-id="ef702-160">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="ef702-160">SuggestionsResponse</span></span>](suggestionsresponse.md) <br/> |<span data-ttu-id="ef702-161">Enthält Antwortinformationen und Vorschlagsdaten für angeforderte Besprechungsvorschläge.</span><span class="sxs-lookup"><span data-stu-id="ef702-161">Contains response information and suggestion data for requested meeting suggestions.</span></span>  <br/><br/> <span data-ttu-id="ef702-162">Im folgenden finden Sie den XPath 2,0-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="ef702-162">The following is the XPath 2.0 expression to this element:</span></span><br/>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse` <br/> |
|[<span data-ttu-id="ef702-163">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="ef702-163">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md) <br/> |<span data-ttu-id="ef702-164">Enthält die Antwortergebnisse und die Abwesenheitseinstellungen für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="ef702-164">Contains the response results and the OOF settings for a user.</span></span>  <br/><br/> <span data-ttu-id="ef702-165">Im folgenden finden Sie den XPath 2,0-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="ef702-165">The following is the XPath 2.0 expression to this element:</span></span>  <br/><br/>  `/GetUserOofSettingsResponse` <br/> |
|[<span data-ttu-id="ef702-166">SetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="ef702-166">SetUserOofSettingsResponse</span></span>](setuseroofsettingsresponse.md) <br/> |<span data-ttu-id="ef702-167">Enthält das Ergebnis einer versuchten [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ef702-167">Contains the result of an attempted [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) message.</span></span> <br/> <br/> <span data-ttu-id="ef702-168">Im folgenden finden Sie den XPath 2,0-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="ef702-168">The following is the XPath 2.0 expression to this element:</span></span>  <br/><br/>  `/SetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef702-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef702-169">Remarks</span></span>

<span data-ttu-id="ef702-170">Der **ResponseMessageType** -Typ ist für alle Exchange Webdienste-Antworten üblich.</span><span class="sxs-lookup"><span data-stu-id="ef702-170">The **ResponseMessageType** type is common to all Exchange Web Services responses.</span></span> <span data-ttu-id="ef702-171">Der **ResponseMessageType** -Typ wird um die folgenden komplexen Typen erweitert:</span><span class="sxs-lookup"><span data-stu-id="ef702-171">The **ResponseMessageType** type is extended by the following complex types:</span></span> 
  
- <span data-ttu-id="ef702-172">**ApplyConversationActionResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ef702-172">**ApplyConversationActionResponseMessageType**</span></span>
    
- <span data-ttu-id="ef702-173">**AttachmentInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ef702-173">**AttachmentInfoResponseMessageType**</span></span>
    
- <span data-ttu-id="ef702-174">**DeleteAttachmentResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ef702-174">**DeleteAttachmentResponseMessageType**</span></span>
    
- <span data-ttu-id="ef702-175">**DeleteItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ef702-175">**DeleteItemResponseMessageType**</span></span>
    
- <span data-ttu-id="ef702-176">**ExpandDLResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ef702-176">**ExpandDLResponseMessageType**</span></span>
    
- <span data-ttu-id="ef702-177">**FindFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ef702-177">**FindFolderResponseMessageType**</span></span>
    
- <span data-ttu-id="ef702-178">**FindItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ef702-178">**FindItemResponseMessageType**</span></span>
    
- <span data-ttu-id="ef702-179">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ef702-179">**FolderInfoResponseMessageType**</span></span>
    
- <span data-ttu-id="ef702-180">**GetEventsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ef702-180">**GetEventsResponseMessageType**</span></span>
    
- <span data-ttu-id="ef702-181">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ef702-181">**ItemInfoResponseMessageType**</span></span>
    
- <span data-ttu-id="ef702-182">**ResolveNamesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ef702-182">**ResolveNamesResponseMessageType**</span></span>
    
- <span data-ttu-id="ef702-183">**SubscribeResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ef702-183">**SubscribeResponseMessageType**</span></span>
    
- <span data-ttu-id="ef702-184">**SendNotificationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ef702-184">**SendNotificationResponseMessageType**</span></span>
    
- <span data-ttu-id="ef702-185">**SyncFolderHierarchyResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ef702-185">**SyncFolderHierarchyResponseMessageType**</span></span>
    
- <span data-ttu-id="ef702-186">**SyncFolderItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ef702-186">**SyncFolderItemsResponseMessageType**</span></span>
    
<span data-ttu-id="ef702-187">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ef702-187">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="ef702-188">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="ef702-188">Version differences</span></span>

<span data-ttu-id="ef702-189">Die **ApplyConversationActionResponseMessage** -und **DeleteItemResponseMessageType** -Typen wurden in Exchange Build 15.00.0986.00 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ef702-189">The **ApplyConversationActionResponseMessage** and **DeleteItemResponseMessageType** types were introduced in Exchange build 15.00.0986.00.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ef702-190">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ef702-190">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef702-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef702-191">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ef702-192">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ef702-192">Schema Name</span></span>  <br/> |<span data-ttu-id="ef702-193">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ef702-193">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ef702-194">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ef702-194">Validation File</span></span>  <br/> |<span data-ttu-id="ef702-195">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ef702-195">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ef702-196">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ef702-196">Can be Empty</span></span>  <br/> |<span data-ttu-id="ef702-197">False</span><span class="sxs-lookup"><span data-stu-id="ef702-197">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef702-198">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef702-198">See also</span></span>

- [<span data-ttu-id="ef702-199">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ef702-199">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="ef702-200">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ef702-200">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)
- [<span data-ttu-id="ef702-201">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ef702-201">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
- [<span data-ttu-id="ef702-202">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="ef702-202">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

