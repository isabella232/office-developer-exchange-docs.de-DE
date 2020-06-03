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
description: Das GetSharingFolderResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen GetSharingFolder-Vorgangsanforderung.
ms.openlocfilehash: 85a78a23bac72942c6278b5d97e2bb4c2992ab46
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463958"
---
# <a name="getsharingfolderresponsemessage"></a><span data-ttu-id="1149f-103">GetSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1149f-103">GetSharingFolderResponseMessage</span></span>

<span data-ttu-id="1149f-104">Das **GetSharingFolderResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [GetSharingFolder-Vorgangs](getsharingfolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="1149f-104">The **GetSharingFolderResponseMessage** element contains the status and result of a single [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span> 
  
```xml
<GetSharingFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>   <SharingFolderId/>
</GetSharingFolderResponseMessage>
```

 <span data-ttu-id="1149f-105">**GetSharingFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="1149f-105">**GetSharingFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1149f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1149f-106">Attributes and elements</span></span>

<span data-ttu-id="1149f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1149f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1149f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1149f-108">Attributes</span></span>

|<span data-ttu-id="1149f-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1149f-109">**Attribute**</span></span>|<span data-ttu-id="1149f-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1149f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1149f-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="1149f-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="1149f-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="1149f-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="1149f-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="1149f-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="1149f-114">-Success</span><span class="sxs-lookup"><span data-stu-id="1149f-114">-  Success</span></span>  <br/><span data-ttu-id="1149f-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="1149f-115">-  Warning</span></span>  <br/><span data-ttu-id="1149f-116">-Error</span><span class="sxs-lookup"><span data-stu-id="1149f-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="1149f-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="1149f-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="1149f-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1149f-118">**Value**</span></span>|<span data-ttu-id="1149f-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1149f-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1149f-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="1149f-120">**Success**</span></span> <br/> |<span data-ttu-id="1149f-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="1149f-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="1149f-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="1149f-122">**Warning**</span></span> <br/> | <span data-ttu-id="1149f-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="1149f-123">Describes a request that was not processed.</span></span> <span data-ttu-id="1149f-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1149f-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="1149f-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="1149f-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="1149f-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="1149f-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="1149f-127">-Der Active Directory Verzeichnisdienst ist offline.</span><span class="sxs-lookup"><span data-stu-id="1149f-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="1149f-128">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="1149f-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="1149f-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="1149f-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="1149f-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="1149f-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="1149f-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="1149f-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="1149f-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="1149f-132">**Error**</span></span> <br/> | <span data-ttu-id="1149f-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1149f-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="1149f-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="1149f-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="1149f-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="1149f-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="1149f-136">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="1149f-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="1149f-137">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="1149f-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="1149f-138">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="1149f-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="1149f-139">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="1149f-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="1149f-140">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="1149f-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="1149f-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="1149f-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1149f-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1149f-142">Child elements</span></span>

|<span data-ttu-id="1149f-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="1149f-143">**Element**</span></span>|<span data-ttu-id="1149f-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1149f-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1149f-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="1149f-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="1149f-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="1149f-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="1149f-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1149f-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="1149f-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="1149f-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="1149f-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="1149f-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="1149f-150">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="1149f-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="1149f-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="1149f-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="1149f-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="1149f-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="1149f-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="1149f-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="1149f-154">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="1149f-154">SharingFolderId</span></span>](sharingfolderid.md) <br/> |<span data-ttu-id="1149f-155">Stellt den Bezeichner des lokalen Ordners in einer Freigabebeziehung dar.</span><span class="sxs-lookup"><span data-stu-id="1149f-155">Represents the identifier of the local folder in a sharing relationship.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1149f-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1149f-156">Parent elements</span></span>

|<span data-ttu-id="1149f-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="1149f-157">**Element**</span></span>|<span data-ttu-id="1149f-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1149f-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1149f-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1149f-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="1149f-160">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="1149f-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1149f-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1149f-161">Remarks</span></span>

<span data-ttu-id="1149f-162">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste des Computers gehostet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1149f-162">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1149f-163">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1149f-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1149f-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="1149f-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1149f-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1149f-165">Schema Name</span></span>  <br/> |<span data-ttu-id="1149f-166">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="1149f-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1149f-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1149f-167">Validation File</span></span>  <br/> |<span data-ttu-id="1149f-168">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="1149f-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1149f-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1149f-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="1149f-170">False</span><span class="sxs-lookup"><span data-stu-id="1149f-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1149f-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1149f-171">See also</span></span>

- [<span data-ttu-id="1149f-172">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1149f-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

