---
title: RefreshSharingFolderResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RefreshSharingFolderResponse
api_type:
- schema
ms.assetid: 951ab681-f2d5-4f10-933e-ff199685ff8e
description: Das RefreshSharingFolderResponse-Element definiert eine Antwort auf eine RefreshSharingFolder Vorgang an.
ms.openlocfilehash: 4ef7a63b2153c6106dae988439f499046689c2b4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831048"
---
# <a name="refreshsharingfolderresponse"></a><span data-ttu-id="dc674-103">RefreshSharingFolderResponse</span><span class="sxs-lookup"><span data-stu-id="dc674-103">RefreshSharingFolderResponse</span></span>

<span data-ttu-id="dc674-104">Das **RefreshSharingFolderResponse** -Element definiert eine Antwort auf eine [RefreshSharingFolder Vorgang](refreshsharingfolder-operation.md) an.</span><span class="sxs-lookup"><span data-stu-id="dc674-104">The **RefreshSharingFolderResponse** element defines a response to a [RefreshSharingFolder operation](refreshsharingfolder-operation.md) request.</span></span> 
  
```xml
<RefreshSharingFolderResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</RefreshSharingFolderResponse>
```

 <span data-ttu-id="dc674-105">**RefreshSharingFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="dc674-105">**RefreshSharingFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc674-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dc674-106">Attributes and elements</span></span>

<span data-ttu-id="dc674-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dc674-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc674-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dc674-108">Attributes</span></span>

|<span data-ttu-id="dc674-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="dc674-109">**Attribute**</span></span>|<span data-ttu-id="dc674-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dc674-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dc674-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="dc674-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="dc674-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="dc674-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="dc674-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="dc674-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="dc674-114">-Success</span><span class="sxs-lookup"><span data-stu-id="dc674-114">-  Success</span></span>  <br/><span data-ttu-id="dc674-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="dc674-115">-  Warning</span></span>  <br/><span data-ttu-id="dc674-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="dc674-116">-  Error</span></span>  <br/>- |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="dc674-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="dc674-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="dc674-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="dc674-118">**Value**</span></span>|<span data-ttu-id="dc674-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dc674-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dc674-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="dc674-120">**Success**</span></span> <br/> |<span data-ttu-id="dc674-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="dc674-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="dc674-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="dc674-122">**Warning**</span></span> <br/> | <span data-ttu-id="dc674-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="dc674-123">Describes a request that was not processed.</span></span> <span data-ttu-id="dc674-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="dc674-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="dc674-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="dc674-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="dc674-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="dc674-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="dc674-127">– Der Active Directory-Verzeichnisdienst ist offline.</span><span class="sxs-lookup"><span data-stu-id="dc674-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="dc674-128">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="dc674-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="dc674-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="dc674-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="dc674-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="dc674-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="dc674-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="dc674-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="dc674-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="dc674-132">**Error**</span></span> <br/> | <span data-ttu-id="dc674-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="dc674-133">Describes a request that cannot be fulfilled.</span></span><br/><br/> <span data-ttu-id="dc674-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="dc674-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="dc674-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="dc674-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="dc674-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="dc674-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="dc674-137">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="dc674-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="dc674-138">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="dc674-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="dc674-139">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="dc674-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="dc674-140">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="dc674-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/>  <br/><span data-ttu-id="dc674-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="dc674-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dc674-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dc674-142">Child elements</span></span>

|<span data-ttu-id="dc674-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="dc674-143">**Element**</span></span>|<span data-ttu-id="dc674-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dc674-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc674-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="dc674-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="dc674-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="dc674-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="dc674-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="dc674-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="dc674-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="dc674-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="dc674-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="dc674-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="dc674-150">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="dc674-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="dc674-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="dc674-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="dc674-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="dc674-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="dc674-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="dc674-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dc674-154">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dc674-154">Parent elements</span></span>

<span data-ttu-id="dc674-155">Keine.</span><span class="sxs-lookup"><span data-stu-id="dc674-155">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc674-156">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dc674-156">Remarks</span></span>

<span data-ttu-id="dc674-157">Das Schema, das dieses Element beschreibt befindet sich das virtuelle IIS-Verzeichnis, dass Hosts Exchange-Webdienste des Computers, auf dem Microsoft Exchange Server ausgeführt wird die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="dc674-157">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc674-158">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="dc674-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc674-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc674-159">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dc674-160">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dc674-160">Schema Name</span></span>  <br/> |<span data-ttu-id="dc674-161">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="dc674-161">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dc674-162">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dc674-162">Validation File</span></span>  <br/> |<span data-ttu-id="dc674-163">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dc674-163">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dc674-164">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="dc674-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="dc674-165">False</span><span class="sxs-lookup"><span data-stu-id="dc674-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc674-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc674-166">See also</span></span>

- [<span data-ttu-id="dc674-167">RefreshSharingFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="dc674-167">RefreshSharingFolder operation</span></span>](refreshsharingfolder-operation.md)
- [<span data-ttu-id="dc674-168">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="dc674-168">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

