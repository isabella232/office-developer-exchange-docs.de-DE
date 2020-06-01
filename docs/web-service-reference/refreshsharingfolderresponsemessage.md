---
title: RefreshSharingFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RefreshSharingFolderResponseMessage
api_type:
- schema
ms.assetid: 53ee65bd-cf75-4e04-9b27-eff1b040ae82
description: Das RefreshSharingFolderResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen RefreshSharingFolder-Vorgangsanforderung.
ms.openlocfilehash: f2cc357298d523b418d2c45598639627c5a63252
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468670"
---
# <a name="refreshsharingfolderresponsemessage"></a><span data-ttu-id="ac226-103">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ac226-103">RefreshSharingFolderResponseMessage</span></span>

<span data-ttu-id="ac226-104">Das **RefreshSharingFolderResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [RefreshSharingFolder-Vorgangs](refreshsharingfolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ac226-104">The **RefreshSharingFolderResponseMessage** element contains the status and result of a single [RefreshSharingFolder operation](refreshsharingfolder-operation.md) request.</span></span> 
  
```xml
<RefreshSharingFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</RefreshSharingFolderResponseMessage>
```

 <span data-ttu-id="ac226-105">**RefreshSharingFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ac226-105">**RefreshSharingFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ac226-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ac226-106">Attributes and elements</span></span>

<span data-ttu-id="ac226-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ac226-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac226-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ac226-108">Attributes</span></span>

|<span data-ttu-id="ac226-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ac226-109">**Attribute**</span></span>|<span data-ttu-id="ac226-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac226-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ac226-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="ac226-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="ac226-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="ac226-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="ac226-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="ac226-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="ac226-114">-Success</span><span class="sxs-lookup"><span data-stu-id="ac226-114">-  Success</span></span>  <br/><span data-ttu-id="ac226-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="ac226-115">-  Warning</span></span>  <br/><span data-ttu-id="ac226-116">-Error</span><span class="sxs-lookup"><span data-stu-id="ac226-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="ac226-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="ac226-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="ac226-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ac226-118">**Value**</span></span>|<span data-ttu-id="ac226-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac226-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ac226-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="ac226-120">**Success**</span></span> <br/> |<span data-ttu-id="ac226-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ac226-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="ac226-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="ac226-122">**Warning**</span></span> <br/> | <span data-ttu-id="ac226-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ac226-123">Describes a request that was not processed.</span></span> <span data-ttu-id="ac226-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ac226-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="ac226-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="ac226-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="ac226-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="ac226-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="ac226-127">-Der Active Directory Verzeichnisdienst ist offline.</span><span class="sxs-lookup"><span data-stu-id="ac226-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="ac226-128">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="ac226-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="ac226-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="ac226-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="ac226-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="ac226-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="ac226-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="ac226-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="ac226-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="ac226-132">**Error**</span></span> <br/> | <span data-ttu-id="ac226-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ac226-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="ac226-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="ac226-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="ac226-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="ac226-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="ac226-136">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="ac226-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="ac226-137">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="ac226-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="ac226-138">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="ac226-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="ac226-139">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="ac226-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="ac226-140">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="ac226-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="ac226-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="ac226-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ac226-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac226-142">Child elements</span></span>

|<span data-ttu-id="ac226-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="ac226-143">**Element**</span></span>|<span data-ttu-id="ac226-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac226-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac226-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="ac226-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ac226-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="ac226-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ac226-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ac226-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ac226-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ac226-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="ac226-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ac226-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ac226-150">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="ac226-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="ac226-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="ac226-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="ac226-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="ac226-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ac226-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="ac226-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ac226-154">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac226-154">Parent elements</span></span>

|<span data-ttu-id="ac226-155">**Element**</span><span class="sxs-lookup"><span data-stu-id="ac226-155">**Element**</span></span>|<span data-ttu-id="ac226-156">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac226-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac226-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ac226-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="ac226-158">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ac226-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac226-159">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac226-159">Remarks</span></span>

<span data-ttu-id="ac226-160">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste des Computers gehostet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ac226-160">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac226-161">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ac226-161">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac226-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac226-162">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ac226-163">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ac226-163">Schema Name</span></span>  <br/> |<span data-ttu-id="ac226-164">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ac226-164">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ac226-165">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ac226-165">Validation File</span></span>  <br/> |<span data-ttu-id="ac226-166">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ac226-166">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ac226-167">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ac226-167">Can be Empty</span></span>  <br/> |<span data-ttu-id="ac226-168">False</span><span class="sxs-lookup"><span data-stu-id="ac226-168">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac226-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac226-169">See also</span></span>

- [<span data-ttu-id="ac226-170">RefreshSharingFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ac226-170">RefreshSharingFolder operation</span></span>](refreshsharingfolder-operation.md)
- [<span data-ttu-id="ac226-171">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ac226-171">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

