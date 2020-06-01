---
title: CreateManagedFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateManagedFolderResponseMessage
api_type:
- schema
ms.assetid: a72eefc3-ef0b-4b44-a74b-e6907b5b5f68
description: Das CreateManagedFolderResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen CreateManagedFolder-Vorgangsanforderung.
ms.openlocfilehash: 03ebcaeb79b2fac20882d2cea3d1e24b42dd472f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467704"
---
# <a name="createmanagedfolderresponsemessage"></a><span data-ttu-id="cdc09-103">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cdc09-103">CreateManagedFolderResponseMessage</span></span>

<span data-ttu-id="cdc09-104">Das **CreateManagedFolderResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [CreateManagedFolder-Vorgangs](createmanagedfolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cdc09-104">The **CreateManagedFolderResponseMessage** element contains the status and result of a single [CreateManagedFolder operation](createmanagedfolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="cdc09-105">CreateManagedFolderResponse</span><span class="sxs-lookup"><span data-stu-id="cdc09-105">CreateManagedFolderResponse</span></span>](createmanagedfolderresponse.md)  
- [<span data-ttu-id="cdc09-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cdc09-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="cdc09-107">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cdc09-107">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md)
  
```xml
<CreateManagedFolderResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</CreateManagedFolderResponseMessage>
```

<span data-ttu-id="cdc09-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="cdc09-108">**FolderInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="cdc09-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cdc09-109">Attributes and elements</span></span>

<span data-ttu-id="cdc09-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cdc09-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cdc09-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="cdc09-111">Attributes</span></span>

|<span data-ttu-id="cdc09-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="cdc09-112">**Attribute**</span></span>|<span data-ttu-id="cdc09-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cdc09-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cdc09-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="cdc09-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="cdc09-115">Beschreibt den Status einer [CreateManagedFolder-Vorgangs](createmanagedfolder-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="cdc09-115">Describes the status of a [CreateManagedFolder operation](createmanagedfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="cdc09-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="cdc09-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="cdc09-117">-Success</span><span class="sxs-lookup"><span data-stu-id="cdc09-117">-  Success</span></span>  <br/><span data-ttu-id="cdc09-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="cdc09-118">-  Warning</span></span>  <br/><span data-ttu-id="cdc09-119">-Error</span><span class="sxs-lookup"><span data-stu-id="cdc09-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="cdc09-120">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="cdc09-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="cdc09-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="cdc09-121">**Value**</span></span>|<span data-ttu-id="cdc09-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cdc09-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cdc09-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="cdc09-123">**Success**</span></span> <br/> |<span data-ttu-id="cdc09-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="cdc09-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="cdc09-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="cdc09-125">**Warning**</span></span> <br/> | <span data-ttu-id="cdc09-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="cdc09-126">Describes a request that was not processed.</span></span> <span data-ttu-id="cdc09-127">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="cdc09-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="cdc09-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="cdc09-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="cdc09-129">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="cdc09-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="cdc09-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="cdc09-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="cdc09-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="cdc09-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="cdc09-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="cdc09-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="cdc09-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="cdc09-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="cdc09-134">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="cdc09-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="cdc09-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="cdc09-135">**Error**</span></span> <br/> | <span data-ttu-id="cdc09-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cdc09-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="cdc09-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="cdc09-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="cdc09-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="cdc09-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="cdc09-139">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="cdc09-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="cdc09-140">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="cdc09-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="cdc09-141">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="cdc09-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="cdc09-142">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="cdc09-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="cdc09-143">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="cdc09-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="cdc09-144">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="cdc09-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cdc09-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cdc09-145">Child elements</span></span>

|<span data-ttu-id="cdc09-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="cdc09-146">**Element**</span></span>|<span data-ttu-id="cdc09-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cdc09-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cdc09-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="cdc09-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="cdc09-149">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="cdc09-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="cdc09-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cdc09-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="cdc09-151">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cdc09-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="cdc09-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="cdc09-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="cdc09-153">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="cdc09-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="cdc09-154">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="cdc09-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="cdc09-155">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="cdc09-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="cdc09-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="cdc09-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="cdc09-157">Ordner</span><span class="sxs-lookup"><span data-stu-id="cdc09-157">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="cdc09-158">Enthält ein Array erstellter verwalteter Ordner.</span><span class="sxs-lookup"><span data-stu-id="cdc09-158">Contains an array of created managed folders.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cdc09-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cdc09-159">Parent elements</span></span>

|<span data-ttu-id="cdc09-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="cdc09-160">**Element**</span></span>|<span data-ttu-id="cdc09-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cdc09-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cdc09-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cdc09-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="cdc09-163">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cdc09-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cdc09-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdc09-164">Remarks</span></span>

<span data-ttu-id="cdc09-165">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="cdc09-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cdc09-166">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="cdc09-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cdc09-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="cdc09-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cdc09-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cdc09-168">Schema Name</span></span>  <br/> |<span data-ttu-id="cdc09-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="cdc09-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cdc09-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cdc09-170">Validation File</span></span>  <br/> |<span data-ttu-id="cdc09-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cdc09-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cdc09-172">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cdc09-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="cdc09-173">False</span><span class="sxs-lookup"><span data-stu-id="cdc09-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cdc09-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdc09-174">See also</span></span>

- [<span data-ttu-id="cdc09-175">CreateManagedFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cdc09-175">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)
- [<span data-ttu-id="cdc09-176">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="cdc09-176">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="cdc09-177">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cdc09-177">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

