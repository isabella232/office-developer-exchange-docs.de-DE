---
title: GetSharingFolderResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingFolderResponse
api_type:
- schema
ms.assetid: fee90e84-3ad4-4c4b-831f-bbc95070aebf
description: Das GetSharingFolderResponse-Element definiert eine Antwort auf eine GetSharingFolder Vorgang an.
ms.openlocfilehash: 6d847f1bd80105d52d564770c65b342c89385dad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829675"
---
# <a name="getsharingfolderresponse"></a><span data-ttu-id="ae2a0-103">GetSharingFolderResponse</span><span class="sxs-lookup"><span data-stu-id="ae2a0-103">GetSharingFolderResponse</span></span>

<span data-ttu-id="ae2a0-104">Das **GetSharingFolderResponse** -Element definiert eine Antwort auf eine [GetSharingFolder Vorgang](getsharingfolder-operation.md) an.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-104">The **GetSharingFolderResponse** element defines a response to a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span> 
  
```XML
<GetSharingFolderResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>   <SharingFolderId/>
</GetSharingFolderResponse>
```

 <span data-ttu-id="ae2a0-105">**GetSharingFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ae2a0-105">**GetSharingFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ae2a0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ae2a0-106">Attributes and elements</span></span>

<span data-ttu-id="ae2a0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae2a0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ae2a0-108">Attributes</span></span>

|<span data-ttu-id="ae2a0-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ae2a0-109">**Attribute**</span></span>|<span data-ttu-id="ae2a0-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ae2a0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae2a0-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="ae2a0-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="ae2a0-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-112">Describes the status of the response.</span></span><br/><br/> <span data-ttu-id="ae2a0-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="ae2a0-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="ae2a0-114">-Success</span><span class="sxs-lookup"><span data-stu-id="ae2a0-114">-  Success</span></span>  <br/><span data-ttu-id="ae2a0-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="ae2a0-115">-  Warning</span></span>  <br/><span data-ttu-id="ae2a0-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="ae2a0-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="ae2a0-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="ae2a0-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="ae2a0-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ae2a0-118">**Value**</span></span>|<span data-ttu-id="ae2a0-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ae2a0-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae2a0-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="ae2a0-120">**Success**</span></span> <br/> |<span data-ttu-id="ae2a0-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="ae2a0-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="ae2a0-122">**Warning**</span></span> <br/> | <span data-ttu-id="ae2a0-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-123">Describes a request that was not processed.</span></span> <span data-ttu-id="ae2a0-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="ae2a0-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="ae2a0-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="ae2a0-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="ae2a0-127">– Der Active Directory-Verzeichnisdienst oder Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-127">-  The Active Directory directory service or Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="ae2a0-128">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="ae2a0-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="ae2a0-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="ae2a0-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="ae2a0-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="ae2a0-132">**Error**</span></span> <br/> | <span data-ttu-id="ae2a0-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="ae2a0-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="ae2a0-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="ae2a0-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="ae2a0-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="ae2a0-136">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="ae2a0-137">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="ae2a0-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="ae2a0-138">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="ae2a0-139">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="ae2a0-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="ae2a0-140">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="ae2a0-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="ae2a0-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ae2a0-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ae2a0-142">Child elements</span></span>

|<span data-ttu-id="ae2a0-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="ae2a0-143">**Element**</span></span>|<span data-ttu-id="ae2a0-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ae2a0-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae2a0-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="ae2a0-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ae2a0-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ae2a0-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ae2a0-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ae2a0-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="ae2a0-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ae2a0-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ae2a0-150">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="ae2a0-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="ae2a0-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="ae2a0-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ae2a0-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="ae2a0-154">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="ae2a0-154">SharingFolderId</span></span>](sharingfolderid.md) <br/> |<span data-ttu-id="ae2a0-155">Stellt den Bezeichner des lokalen Ordners in einer Dateifreigabe Beziehung dar.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-155">Represents the identifier of the local folder in a sharing relationship.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ae2a0-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ae2a0-156">Parent elements</span></span>

<span data-ttu-id="ae2a0-157">Keine.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-157">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ae2a0-158">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ae2a0-158">Remarks</span></span>

<span data-ttu-id="ae2a0-159">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-159">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae2a0-160">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ae2a0-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae2a0-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae2a0-161">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ae2a0-162">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ae2a0-162">Schema Name</span></span>  <br/> |<span data-ttu-id="ae2a0-163">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ae2a0-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ae2a0-164">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ae2a0-164">Validation File</span></span>  <br/> |<span data-ttu-id="ae2a0-165">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ae2a0-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ae2a0-166">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ae2a0-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="ae2a0-167">False</span><span class="sxs-lookup"><span data-stu-id="ae2a0-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae2a0-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae2a0-168">See also</span></span>

- [<span data-ttu-id="ae2a0-169">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ae2a0-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

