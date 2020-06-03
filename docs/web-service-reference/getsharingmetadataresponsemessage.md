---
title: GetSharingMetadataResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingMetadataResponseMessage
api_type:
- schema
ms.assetid: d81b8708-ebb2-45c2-861f-b9a814eee6ba
description: Das GetSharingMetadataResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen GetSharingMetadata-Vorgangsanforderung.
ms.openlocfilehash: cca06cb12ce48ba182c4ebfe475b2acfcc861d63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457340"
---
# <a name="getsharingmetadataresponsemessage"></a><span data-ttu-id="6c73b-103">GetSharingMetadataResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6c73b-103">GetSharingMetadataResponseMessage</span></span>

<span data-ttu-id="6c73b-104">Das **GetSharingMetadataResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [GetSharingMetadata-Vorgangs](getsharingmetadata-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6c73b-104">The **GetSharingMetadataResponseMessage** element contains the status and result of a single [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span> 
  
```xml
<GetSharingMetadataResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>   <EncryptedSharedFolderDataCollection/>   <InvalidRecipients/>
</GetSharingMetadataResponseMessage>
```

 <span data-ttu-id="6c73b-105">**GetSharingMetadataResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="6c73b-105">**GetSharingMetadataResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6c73b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6c73b-106">Attributes and elements</span></span>

<span data-ttu-id="6c73b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6c73b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6c73b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6c73b-108">Attributes</span></span>

|<span data-ttu-id="6c73b-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6c73b-109">**Attribute**</span></span>|<span data-ttu-id="6c73b-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6c73b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6c73b-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="6c73b-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="6c73b-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="6c73b-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="6c73b-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="6c73b-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="6c73b-114">-Success</span><span class="sxs-lookup"><span data-stu-id="6c73b-114">-  Success</span></span>  <br/><span data-ttu-id="6c73b-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="6c73b-115">-  Warning</span></span>  <br/><span data-ttu-id="6c73b-116">-Error</span><span class="sxs-lookup"><span data-stu-id="6c73b-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="6c73b-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="6c73b-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="6c73b-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6c73b-118">**Value**</span></span>|<span data-ttu-id="6c73b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6c73b-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6c73b-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="6c73b-120">**Success**</span></span> <br/> |<span data-ttu-id="6c73b-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="6c73b-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="6c73b-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="6c73b-122">**Warning**</span></span> <br/> | <span data-ttu-id="6c73b-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="6c73b-123">Describes a request that was not processed.</span></span> <span data-ttu-id="6c73b-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="6c73b-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="6c73b-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="6c73b-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="6c73b-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="6c73b-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="6c73b-127">-Der Active Directory Verzeichnisdienst ist offline.</span><span class="sxs-lookup"><span data-stu-id="6c73b-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="6c73b-128">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="6c73b-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="6c73b-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="6c73b-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="6c73b-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="6c73b-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="6c73b-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="6c73b-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="6c73b-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="6c73b-132">**Error**</span></span> <br/> | <span data-ttu-id="6c73b-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6c73b-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="6c73b-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="6c73b-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="6c73b-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="6c73b-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="6c73b-136">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="6c73b-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="6c73b-137">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="6c73b-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="6c73b-138">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="6c73b-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="6c73b-139">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="6c73b-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="6c73b-140">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="6c73b-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="6c73b-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="6c73b-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6c73b-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6c73b-142">Child elements</span></span>

|<span data-ttu-id="6c73b-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="6c73b-143">**Element**</span></span>|<span data-ttu-id="6c73b-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6c73b-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6c73b-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="6c73b-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="6c73b-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="6c73b-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="6c73b-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6c73b-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="6c73b-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="6c73b-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="6c73b-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="6c73b-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="6c73b-150">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="6c73b-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="6c73b-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="6c73b-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="6c73b-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="6c73b-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="6c73b-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="6c73b-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="6c73b-154">EncryptedSharedFolderDataCollection</span><span class="sxs-lookup"><span data-stu-id="6c73b-154">EncryptedSharedFolderDataCollection</span></span>](encryptedsharedfolderdatacollection.md) <br/> |<span data-ttu-id="6c73b-155">Enthält eine Auflistung von Datenstrukturen, die ein Client verwenden kann, um die Freigabe seiner Kalender-oder Kontaktdaten für andere Clients zu autorisieren.</span><span class="sxs-lookup"><span data-stu-id="6c73b-155">Contains a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
|[<span data-ttu-id="6c73b-156">InvalidRecipients</span><span class="sxs-lookup"><span data-stu-id="6c73b-156">InvalidRecipients</span></span>](invalidrecipients.md) <br/> |<span data-ttu-id="6c73b-157">Stellt die Empfänger der Anforderung für die Ordnerfreigabe dar, die ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="6c73b-157">Represents recipients of the folder sharing request that are invalid.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6c73b-158">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6c73b-158">Parent elements</span></span>

|<span data-ttu-id="6c73b-159">**Element**</span><span class="sxs-lookup"><span data-stu-id="6c73b-159">**Element**</span></span>|<span data-ttu-id="6c73b-160">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6c73b-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6c73b-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6c73b-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="6c73b-162">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6c73b-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c73b-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c73b-163">Remarks</span></span>

<span data-ttu-id="6c73b-164">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste des Computers gehostet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6c73b-164">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6c73b-165">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6c73b-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c73b-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c73b-166">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6c73b-167">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6c73b-167">Schema Name</span></span>  <br/> |<span data-ttu-id="6c73b-168">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="6c73b-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6c73b-169">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6c73b-169">Validation File</span></span>  <br/> |<span data-ttu-id="6c73b-170">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6c73b-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6c73b-171">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6c73b-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="6c73b-172">False</span><span class="sxs-lookup"><span data-stu-id="6c73b-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c73b-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c73b-173">See also</span></span>

- [<span data-ttu-id="6c73b-174">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6c73b-174">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)
- [<span data-ttu-id="6c73b-175">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6c73b-175">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

