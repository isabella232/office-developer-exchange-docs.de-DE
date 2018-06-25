---
title: GetSharingFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingFolderResponseMessage
api_type:
- schema
ms.assetid: b6f5fd09-09f3-4e34-84b4-2f6c1f10f28f
description: Das GetSharingFolderResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung GetSharingFolder Vorgang.
ms.openlocfilehash: 13ce3f628ff125140fc7459df5d567a67ddf7bc2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829672"
---
# <a name="getsharingfolderresponsemessage"></a><span data-ttu-id="a1c03-103">GetSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a1c03-103">GetSharingFolderResponseMessage</span></span>

<span data-ttu-id="a1c03-104">Das **GetSharingFolderResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [GetSharingFolder Vorgang](getsharingfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="a1c03-104">The **GetSharingFolderResponseMessage** element contains the status and result of a single [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span> 
  
```xml
<GetSharingFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>   <SharingFolderId/>
</GetSharingFolderResponseMessage>
```

 <span data-ttu-id="a1c03-105">**GetSharingFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="a1c03-105">**GetSharingFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a1c03-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a1c03-106">Attributes and elements</span></span>

<span data-ttu-id="a1c03-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a1c03-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a1c03-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a1c03-108">Attributes</span></span>

|<span data-ttu-id="a1c03-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a1c03-109">**Attribute**</span></span>|<span data-ttu-id="a1c03-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1c03-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a1c03-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="a1c03-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="a1c03-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="a1c03-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="a1c03-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="a1c03-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="a1c03-114">-Success</span><span class="sxs-lookup"><span data-stu-id="a1c03-114">-  Success</span></span>  <br/><span data-ttu-id="a1c03-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="a1c03-115">-  Warning</span></span>  <br/><span data-ttu-id="a1c03-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="a1c03-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="a1c03-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="a1c03-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="a1c03-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a1c03-118">**Value**</span></span>|<span data-ttu-id="a1c03-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1c03-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a1c03-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="a1c03-120">**Success**</span></span> <br/> |<span data-ttu-id="a1c03-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="a1c03-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="a1c03-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="a1c03-122">**Warning**</span></span> <br/> | <span data-ttu-id="a1c03-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="a1c03-123">Describes a request that was not processed.</span></span> <span data-ttu-id="a1c03-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="a1c03-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="a1c03-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="a1c03-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="a1c03-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="a1c03-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="a1c03-127">– Der Active Directory-Verzeichnisdienst ist offline.</span><span class="sxs-lookup"><span data-stu-id="a1c03-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="a1c03-128">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="a1c03-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="a1c03-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="a1c03-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="a1c03-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="a1c03-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="a1c03-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="a1c03-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="a1c03-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="a1c03-132">**Error**</span></span> <br/> | <span data-ttu-id="a1c03-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a1c03-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="a1c03-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="a1c03-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="a1c03-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="a1c03-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="a1c03-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="a1c03-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="a1c03-137">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="a1c03-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="a1c03-138">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a1c03-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="a1c03-139">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="a1c03-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="a1c03-140">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="a1c03-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="a1c03-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="a1c03-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a1c03-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a1c03-142">Child elements</span></span>

|<span data-ttu-id="a1c03-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="a1c03-143">**Element**</span></span>|<span data-ttu-id="a1c03-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1c03-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a1c03-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="a1c03-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="a1c03-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="a1c03-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="a1c03-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a1c03-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="a1c03-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="a1c03-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="a1c03-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="a1c03-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="a1c03-150">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="a1c03-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="a1c03-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="a1c03-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="a1c03-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="a1c03-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="a1c03-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="a1c03-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="a1c03-154">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="a1c03-154">SharingFolderId</span></span>](sharingfolderid.md) <br/> |<span data-ttu-id="a1c03-155">Stellt den Bezeichner des lokalen Ordners in einer Dateifreigabe Beziehung dar.</span><span class="sxs-lookup"><span data-stu-id="a1c03-155">Represents the identifier of the local folder in a sharing relationship.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a1c03-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a1c03-156">Parent elements</span></span>

|<span data-ttu-id="a1c03-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="a1c03-157">**Element**</span></span>|<span data-ttu-id="a1c03-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1c03-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a1c03-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a1c03-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="a1c03-160">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a1c03-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1c03-161">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a1c03-161">Remarks</span></span>

<span data-ttu-id="a1c03-162">Das Schema, das dieses Element beschreibt befindet sich das virtuelle IIS-Verzeichnis, dass Hosts Exchange-Webdienste des Computers, auf dem Microsoft Exchange Server ausgeführt wird die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a1c03-162">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a1c03-163">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a1c03-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1c03-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="a1c03-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a1c03-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a1c03-165">Schema Name</span></span>  <br/> |<span data-ttu-id="a1c03-166">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a1c03-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a1c03-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a1c03-167">Validation File</span></span>  <br/> |<span data-ttu-id="a1c03-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a1c03-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a1c03-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a1c03-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="a1c03-170">False</span><span class="sxs-lookup"><span data-stu-id="a1c03-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a1c03-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1c03-171">See also</span></span>

- [<span data-ttu-id="a1c03-172">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a1c03-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

