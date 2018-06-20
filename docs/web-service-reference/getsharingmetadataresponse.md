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
description: Das GetSharingMetadataResponse-Element definiert eine Antwort auf eine GetSharingMetadata Vorgang an.
ms.openlocfilehash: 820b5bf7aa5528b61aa6649e5b1886885b5f022e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829676"
---
# <a name="getsharingmetadataresponse"></a><span data-ttu-id="920b8-103">GetSharingMetadataResponse</span><span class="sxs-lookup"><span data-stu-id="920b8-103">GetSharingMetadataResponse</span></span>

<span data-ttu-id="920b8-104">Das **GetSharingMetadataResponse** -Element definiert eine Antwort auf eine [GetSharingMetadata Vorgang](getsharingmetadata-operation.md) an.</span><span class="sxs-lookup"><span data-stu-id="920b8-104">The **GetSharingMetadataResponse** element defines a response to a [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span> 
  
```xml
<GetSharingMetadataResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>   <EncryptedSharedFolderDataCollection/>   <InvalidRecipients/>
</GetSharingMetadataResponse>
```

 <span data-ttu-id="920b8-105">**GetSharingMetadataResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="920b8-105">**GetSharingMetadataResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="920b8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="920b8-106">Attributes and elements</span></span>

<span data-ttu-id="920b8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="920b8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="920b8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="920b8-108">Attributes</span></span>

|<span data-ttu-id="920b8-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="920b8-109">**Attribute**</span></span>|<span data-ttu-id="920b8-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="920b8-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="920b8-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="920b8-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="920b8-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="920b8-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="920b8-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="920b8-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="920b8-114">-Success</span><span class="sxs-lookup"><span data-stu-id="920b8-114">-  Success</span></span>  <br/><span data-ttu-id="920b8-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="920b8-115">-  Warning</span></span>  <br/><span data-ttu-id="920b8-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="920b8-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="920b8-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="920b8-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="920b8-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="920b8-118">**Value**</span></span>|<span data-ttu-id="920b8-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="920b8-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="920b8-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="920b8-120">**Success**</span></span> <br/> |<span data-ttu-id="920b8-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="920b8-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="920b8-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="920b8-122">**Warning**</span></span> <br/> | <span data-ttu-id="920b8-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="920b8-123">Describes a request that was not processed.</span></span> <span data-ttu-id="920b8-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="920b8-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="920b8-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="920b8-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="920b8-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="920b8-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="920b8-127">– Der Active Directory-Verzeichnisdienst ist offline.</span><span class="sxs-lookup"><span data-stu-id="920b8-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="920b8-128">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="920b8-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="920b8-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="920b8-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="920b8-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="920b8-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="920b8-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="920b8-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="920b8-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="920b8-132">**Error**</span></span> <br/> | <span data-ttu-id="920b8-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="920b8-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="920b8-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="920b8-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="920b8-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="920b8-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="920b8-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="920b8-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="920b8-137">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="920b8-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="920b8-138">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="920b8-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="920b8-139">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="920b8-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="920b8-140">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="920b8-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/>  <br/><span data-ttu-id="920b8-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="920b8-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="920b8-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="920b8-142">Child elements</span></span>

|<span data-ttu-id="920b8-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="920b8-143">**Element**</span></span>|<span data-ttu-id="920b8-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="920b8-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="920b8-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="920b8-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="920b8-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="920b8-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="920b8-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="920b8-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="920b8-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="920b8-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="920b8-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="920b8-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="920b8-150">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="920b8-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="920b8-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="920b8-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="920b8-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="920b8-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="920b8-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="920b8-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="920b8-154">EncryptedSharedFolderDataCollection</span><span class="sxs-lookup"><span data-stu-id="920b8-154">EncryptedSharedFolderDataCollection</span></span>](encryptedsharedfolderdatacollection.md) <br/> |<span data-ttu-id="920b8-155">Enthält eine Auflistung von Datenstrukturen, die ein Client zum Autorisieren die Freigabe von dessen Kalender oder Kontaktdaten mit anderen Clients verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="920b8-155">Contains a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
|[<span data-ttu-id="920b8-156">InvalidRecipients</span><span class="sxs-lookup"><span data-stu-id="920b8-156">InvalidRecipients</span></span>](invalidrecipients.md) <br/> |<span data-ttu-id="920b8-157">Stellt den Ordner Freigabeanfrage-Empfänger, die ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="920b8-157">Represents recipients of the folder sharing request that are invalid.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="920b8-158">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="920b8-158">Parent elements</span></span>

<span data-ttu-id="920b8-159">Keine.</span><span class="sxs-lookup"><span data-stu-id="920b8-159">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="920b8-160">Hinweise</span><span class="sxs-lookup"><span data-stu-id="920b8-160">Remarks</span></span>

<span data-ttu-id="920b8-161">Das Schema, das dieses Element beschreibt befindet sich das virtuelle IIS-Verzeichnis, dass Hosts Exchange-Webdienste des Computers, auf dem Microsoft Exchange Server ausgeführt wird die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="920b8-161">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="920b8-162">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="920b8-162">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="920b8-163">Namespace</span><span class="sxs-lookup"><span data-stu-id="920b8-163">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="920b8-164">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="920b8-164">Schema Name</span></span>  <br/> |<span data-ttu-id="920b8-165">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="920b8-165">Messages schema</span></span>  <br/> |
|<span data-ttu-id="920b8-166">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="920b8-166">Validation File</span></span>  <br/> |<span data-ttu-id="920b8-167">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="920b8-167">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="920b8-168">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="920b8-168">Can be Empty</span></span>  <br/> |<span data-ttu-id="920b8-169">False</span><span class="sxs-lookup"><span data-stu-id="920b8-169">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="920b8-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="920b8-170">See also</span></span>

- [<span data-ttu-id="920b8-171">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="920b8-171">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)
- [<span data-ttu-id="920b8-172">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="920b8-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

