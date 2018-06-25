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
description: Das CreateManagedFolderResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung CreateManagedFolder Vorgang.
ms.openlocfilehash: e561cac949ebebc647b16578c6acbcd6132eeef7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757798"
---
# <a name="createmanagedfolderresponsemessage"></a><span data-ttu-id="f78fc-103">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f78fc-103">CreateManagedFolderResponseMessage</span></span>

<span data-ttu-id="f78fc-104">Das **CreateManagedFolderResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [CreateManagedFolder Vorgang](createmanagedfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="f78fc-104">The **CreateManagedFolderResponseMessage** element contains the status and result of a single [CreateManagedFolder operation](createmanagedfolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="f78fc-105">CreateManagedFolderResponse</span><span class="sxs-lookup"><span data-stu-id="f78fc-105">CreateManagedFolderResponse</span></span>](createmanagedfolderresponse.md)  
- [<span data-ttu-id="f78fc-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f78fc-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="f78fc-107">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f78fc-107">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md)
  
```xml
<CreateManagedFolderResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</CreateManagedFolderResponseMessage>
```

<span data-ttu-id="f78fc-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f78fc-108">**FolderInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f78fc-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f78fc-109">Attributes and elements</span></span>

<span data-ttu-id="f78fc-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f78fc-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f78fc-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="f78fc-111">Attributes</span></span>

|<span data-ttu-id="f78fc-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f78fc-112">**Attribute**</span></span>|<span data-ttu-id="f78fc-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f78fc-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f78fc-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="f78fc-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="f78fc-115">Beschreibt den Status einer Antwort [CreateManagedFolder Vorgang](createmanagedfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="f78fc-115">Describes the status of a [CreateManagedFolder operation](createmanagedfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="f78fc-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="f78fc-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="f78fc-117">-Success</span><span class="sxs-lookup"><span data-stu-id="f78fc-117">-  Success</span></span>  <br/><span data-ttu-id="f78fc-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="f78fc-118">-  Warning</span></span>  <br/><span data-ttu-id="f78fc-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="f78fc-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="f78fc-120">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="f78fc-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="f78fc-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f78fc-121">**Value**</span></span>|<span data-ttu-id="f78fc-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f78fc-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f78fc-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="f78fc-123">**Success**</span></span> <br/> |<span data-ttu-id="f78fc-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="f78fc-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="f78fc-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="f78fc-125">**Warning**</span></span> <br/> | <span data-ttu-id="f78fc-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="f78fc-126">Describes a request that was not processed.</span></span> <span data-ttu-id="f78fc-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="f78fc-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="f78fc-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="f78fc-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="f78fc-129">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="f78fc-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="f78fc-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="f78fc-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="f78fc-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="f78fc-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="f78fc-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="f78fc-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="f78fc-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="f78fc-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="f78fc-134">-Ein Kontingent überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="f78fc-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="f78fc-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="f78fc-135">**Error**</span></span> <br/> | <span data-ttu-id="f78fc-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f78fc-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="f78fc-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="f78fc-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="f78fc-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="f78fc-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="f78fc-139">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="f78fc-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="f78fc-140">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="f78fc-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="f78fc-141">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f78fc-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="f78fc-142">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="f78fc-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="f78fc-143">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="f78fc-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="f78fc-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="f78fc-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f78fc-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f78fc-145">Child elements</span></span>

|<span data-ttu-id="f78fc-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="f78fc-146">**Element**</span></span>|<span data-ttu-id="f78fc-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f78fc-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f78fc-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="f78fc-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="f78fc-149">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="f78fc-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="f78fc-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f78fc-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="f78fc-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="f78fc-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="f78fc-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f78fc-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="f78fc-153">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f78fc-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="f78fc-154">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="f78fc-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="f78fc-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="f78fc-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="f78fc-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="f78fc-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="f78fc-157">Ordner</span><span class="sxs-lookup"><span data-stu-id="f78fc-157">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f78fc-158">Enthält ein Array von erstellte verwaltete Ordner.</span><span class="sxs-lookup"><span data-stu-id="f78fc-158">Contains an array of created managed folders.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f78fc-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f78fc-159">Parent elements</span></span>

|<span data-ttu-id="f78fc-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="f78fc-160">**Element**</span></span>|<span data-ttu-id="f78fc-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f78fc-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f78fc-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f78fc-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="f78fc-163">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f78fc-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f78fc-164">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f78fc-164">Remarks</span></span>

<span data-ttu-id="f78fc-165">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f78fc-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f78fc-166">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f78fc-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f78fc-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="f78fc-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f78fc-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f78fc-168">Schema Name</span></span>  <br/> |<span data-ttu-id="f78fc-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f78fc-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f78fc-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f78fc-170">Validation File</span></span>  <br/> |<span data-ttu-id="f78fc-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f78fc-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f78fc-172">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f78fc-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="f78fc-173">False</span><span class="sxs-lookup"><span data-stu-id="f78fc-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f78fc-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f78fc-174">See also</span></span>

- [<span data-ttu-id="f78fc-175">CreateManagedFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f78fc-175">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)
- [<span data-ttu-id="f78fc-176">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="f78fc-176">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="f78fc-177">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f78fc-177">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

