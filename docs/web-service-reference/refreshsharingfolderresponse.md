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
description: Das RefreshSharingFolderResponse-Element definiert eine Antwort auf eine RefreshSharingFolder-Vorgangsanforderung.
ms.openlocfilehash: f37dd4d31546169391305936167143ff5ebd5f91
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468929"
---
# <a name="refreshsharingfolderresponse"></a><span data-ttu-id="18554-103">RefreshSharingFolderResponse</span><span class="sxs-lookup"><span data-stu-id="18554-103">RefreshSharingFolderResponse</span></span>

<span data-ttu-id="18554-104">Das **RefreshSharingFolderResponse** -Element definiert eine Antwort auf eine [RefreshSharingFolder-Vorgangs](refreshsharingfolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="18554-104">The **RefreshSharingFolderResponse** element defines a response to a [RefreshSharingFolder operation](refreshsharingfolder-operation.md) request.</span></span> 
  
```xml
<RefreshSharingFolderResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</RefreshSharingFolderResponse>
```

 <span data-ttu-id="18554-105">**RefreshSharingFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="18554-105">**RefreshSharingFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="18554-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="18554-106">Attributes and elements</span></span>

<span data-ttu-id="18554-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="18554-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18554-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="18554-108">Attributes</span></span>

|<span data-ttu-id="18554-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="18554-109">**Attribute**</span></span>|<span data-ttu-id="18554-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18554-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18554-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="18554-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="18554-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="18554-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="18554-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="18554-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="18554-114">-Success</span><span class="sxs-lookup"><span data-stu-id="18554-114">-  Success</span></span>  <br/><span data-ttu-id="18554-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="18554-115">-  Warning</span></span>  <br/><span data-ttu-id="18554-116">-Error</span><span class="sxs-lookup"><span data-stu-id="18554-116">-  Error</span></span>  <br/>- |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="18554-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="18554-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="18554-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="18554-118">**Value**</span></span>|<span data-ttu-id="18554-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18554-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18554-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="18554-120">**Success**</span></span> <br/> |<span data-ttu-id="18554-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="18554-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="18554-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="18554-122">**Warning**</span></span> <br/> | <span data-ttu-id="18554-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="18554-123">Describes a request that was not processed.</span></span> <span data-ttu-id="18554-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="18554-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="18554-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="18554-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="18554-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="18554-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="18554-127">-Der Active Directory Verzeichnisdienst ist offline.</span><span class="sxs-lookup"><span data-stu-id="18554-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="18554-128">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="18554-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="18554-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="18554-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="18554-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="18554-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="18554-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="18554-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="18554-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="18554-132">**Error**</span></span> <br/> | <span data-ttu-id="18554-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="18554-133">Describes a request that cannot be fulfilled.</span></span><br/><br/> <span data-ttu-id="18554-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="18554-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="18554-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="18554-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="18554-136">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="18554-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="18554-137">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="18554-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="18554-138">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="18554-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="18554-139">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="18554-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="18554-140">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="18554-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/>  <br/><span data-ttu-id="18554-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="18554-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="18554-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="18554-142">Child elements</span></span>

|<span data-ttu-id="18554-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="18554-143">**Element**</span></span>|<span data-ttu-id="18554-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18554-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18554-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="18554-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="18554-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="18554-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="18554-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="18554-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="18554-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="18554-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="18554-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="18554-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="18554-150">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="18554-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="18554-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="18554-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="18554-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="18554-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="18554-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="18554-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="18554-154">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="18554-154">Parent elements</span></span>

<span data-ttu-id="18554-155">Keine.</span><span class="sxs-lookup"><span data-stu-id="18554-155">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="18554-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18554-156">Remarks</span></span>

<span data-ttu-id="18554-157">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste des Computers gehostet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="18554-157">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18554-158">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="18554-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18554-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="18554-159">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="18554-160">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="18554-160">Schema Name</span></span>  <br/> |<span data-ttu-id="18554-161">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="18554-161">Messages schema</span></span>  <br/> |
|<span data-ttu-id="18554-162">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="18554-162">Validation File</span></span>  <br/> |<span data-ttu-id="18554-163">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="18554-163">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="18554-164">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="18554-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="18554-165">False</span><span class="sxs-lookup"><span data-stu-id="18554-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18554-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18554-166">See also</span></span>

- [<span data-ttu-id="18554-167">RefreshSharingFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="18554-167">RefreshSharingFolder operation</span></span>](refreshsharingfolder-operation.md)
- [<span data-ttu-id="18554-168">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="18554-168">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

