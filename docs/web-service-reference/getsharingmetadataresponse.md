---
title: GetSharingMetadataResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingMetadataResponse
api_type:
- schema
ms.assetid: 1acc2d8f-7104-4b36-9c04-dd4fc4f571bb
description: Das GetSharingMetadataResponse-Element definiert eine Antwort auf eine GetSharingMetadata-Vorgangsanforderung.
ms.openlocfilehash: eabeda2e6138e78858ffb044603f696ec65f3deb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530176"
---
# <a name="getsharingmetadataresponse"></a><span data-ttu-id="65402-103">GetSharingMetadataResponse</span><span class="sxs-lookup"><span data-stu-id="65402-103">GetSharingMetadataResponse</span></span>

<span data-ttu-id="65402-104">Das **GetSharingMetadataResponse** -Element definiert eine Antwort auf eine [GetSharingMetadata-Vorgangs](getsharingmetadata-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="65402-104">The **GetSharingMetadataResponse** element defines a response to a [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span> 
  
```xml
<GetSharingMetadataResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>   <EncryptedSharedFolderDataCollection/>   <InvalidRecipients/>
</GetSharingMetadataResponse>
```

 <span data-ttu-id="65402-105">**GetSharingMetadataResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="65402-105">**GetSharingMetadataResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="65402-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="65402-106">Attributes and elements</span></span>

<span data-ttu-id="65402-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="65402-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65402-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="65402-108">Attributes</span></span>

|<span data-ttu-id="65402-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="65402-109">**Attribute**</span></span>|<span data-ttu-id="65402-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="65402-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="65402-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="65402-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="65402-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="65402-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="65402-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="65402-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="65402-114">-Success</span><span class="sxs-lookup"><span data-stu-id="65402-114">-  Success</span></span>  <br/><span data-ttu-id="65402-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="65402-115">-  Warning</span></span>  <br/><span data-ttu-id="65402-116">-Error</span><span class="sxs-lookup"><span data-stu-id="65402-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="65402-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="65402-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="65402-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="65402-118">**Value**</span></span>|<span data-ttu-id="65402-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="65402-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="65402-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="65402-120">**Success**</span></span> <br/> |<span data-ttu-id="65402-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="65402-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="65402-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="65402-122">**Warning**</span></span> <br/> | <span data-ttu-id="65402-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="65402-123">Describes a request that was not processed.</span></span> <span data-ttu-id="65402-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="65402-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="65402-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="65402-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="65402-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="65402-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="65402-127">-Der Active Directory Verzeichnisdienst ist offline.</span><span class="sxs-lookup"><span data-stu-id="65402-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="65402-128">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="65402-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="65402-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="65402-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="65402-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="65402-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="65402-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="65402-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="65402-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="65402-132">**Error**</span></span> <br/> | <span data-ttu-id="65402-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="65402-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="65402-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="65402-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="65402-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="65402-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="65402-136">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="65402-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="65402-137">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="65402-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="65402-138">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="65402-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="65402-139">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="65402-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="65402-140">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="65402-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/>  <br/><span data-ttu-id="65402-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="65402-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="65402-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="65402-142">Child elements</span></span>

|<span data-ttu-id="65402-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="65402-143">**Element**</span></span>|<span data-ttu-id="65402-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="65402-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65402-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="65402-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="65402-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="65402-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="65402-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="65402-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="65402-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="65402-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="65402-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="65402-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="65402-150">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="65402-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="65402-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="65402-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="65402-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="65402-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="65402-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="65402-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="65402-154">EncryptedSharedFolderDataCollection</span><span class="sxs-lookup"><span data-stu-id="65402-154">EncryptedSharedFolderDataCollection</span></span>](encryptedsharedfolderdatacollection.md) <br/> |<span data-ttu-id="65402-155">Enthält eine Auflistung von Datenstrukturen, die ein Client verwenden kann, um die Freigabe seiner Kalender-oder Kontaktdaten für andere Clients zu autorisieren.</span><span class="sxs-lookup"><span data-stu-id="65402-155">Contains a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
|[<span data-ttu-id="65402-156">InvalidRecipients</span><span class="sxs-lookup"><span data-stu-id="65402-156">InvalidRecipients</span></span>](invalidrecipients.md) <br/> |<span data-ttu-id="65402-157">Stellt die Empfänger der Anforderung für die Ordnerfreigabe dar, die ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="65402-157">Represents recipients of the folder sharing request that are invalid.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="65402-158">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="65402-158">Parent elements</span></span>

<span data-ttu-id="65402-159">Keine.</span><span class="sxs-lookup"><span data-stu-id="65402-159">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="65402-160">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65402-160">Remarks</span></span>

<span data-ttu-id="65402-161">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste des Computers gehostet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="65402-161">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65402-162">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="65402-162">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65402-163">Namespace</span><span class="sxs-lookup"><span data-stu-id="65402-163">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="65402-164">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="65402-164">Schema Name</span></span>  <br/> |<span data-ttu-id="65402-165">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="65402-165">Messages schema</span></span>  <br/> |
|<span data-ttu-id="65402-166">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="65402-166">Validation File</span></span>  <br/> |<span data-ttu-id="65402-167">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="65402-167">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="65402-168">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="65402-168">Can be Empty</span></span>  <br/> |<span data-ttu-id="65402-169">False</span><span class="sxs-lookup"><span data-stu-id="65402-169">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65402-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65402-170">See also</span></span>

- [<span data-ttu-id="65402-171">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="65402-171">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)
- [<span data-ttu-id="65402-172">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="65402-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

