---
title: GetFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetFolderResponseMessage
api_type:
- schema
ms.assetid: 51359863-d110-4c12-b89f-aba5e3e40c1d
description: Das GetFolderResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen GetFolder-Vorgangsanforderung.
ms.openlocfilehash: ddf23790e804c3f0562f65ebaa3cb591433eab69
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456458"
---
# <a name="getfolderresponsemessage"></a><span data-ttu-id="55f0a-103">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="55f0a-103">GetFolderResponseMessage</span></span>

<span data-ttu-id="55f0a-104">Das **GetFolderResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [GetFolder-Vorgangs](getfolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="55f0a-104">The **GetFolderResponseMessage** element contains the status and result of a single [GetFolder operation](getfolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="55f0a-105">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="55f0a-105">GetFolderResponse</span></span>](getfolderresponse.md) 
- [<span data-ttu-id="55f0a-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="55f0a-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="55f0a-107">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="55f0a-107">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
  
```xml
<GetFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</GetFolderResponseMessage>
```

 <span data-ttu-id="55f0a-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="55f0a-108">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="55f0a-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="55f0a-109">Attributes and elements</span></span>

<span data-ttu-id="55f0a-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="55f0a-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="55f0a-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="55f0a-111">Attributes</span></span>

|<span data-ttu-id="55f0a-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="55f0a-112">**Attribute**</span></span>|<span data-ttu-id="55f0a-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55f0a-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="55f0a-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="55f0a-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="55f0a-115">Beschreibt den Status einer [GetFolder-Vorgangs](getfolder-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="55f0a-115">Describes the status of a [GetFolder operation](getfolder-operation.md) response.</span></span> <br/><br/><span data-ttu-id="55f0a-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="55f0a-116">The following values are valid for this attribute:</span></span><br/>  <br/><span data-ttu-id="55f0a-117">-Success</span><span class="sxs-lookup"><span data-stu-id="55f0a-117">-  Success</span></span>  <br/><span data-ttu-id="55f0a-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="55f0a-118">-  Warning</span></span>  <br/><span data-ttu-id="55f0a-119">-Error</span><span class="sxs-lookup"><span data-stu-id="55f0a-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="55f0a-120">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="55f0a-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="55f0a-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="55f0a-121">**Value**</span></span>|<span data-ttu-id="55f0a-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55f0a-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="55f0a-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="55f0a-123">**Success**</span></span> <br/> |<span data-ttu-id="55f0a-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="55f0a-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="55f0a-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="55f0a-125">**Warning**</span></span> <br/> | <span data-ttu-id="55f0a-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="55f0a-126">Describes a request that was not processed.</span></span> <span data-ttu-id="55f0a-127">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="55f0a-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="55f0a-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="55f0a-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="55f0a-129">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="55f0a-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="55f0a-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="55f0a-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="55f0a-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="55f0a-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="55f0a-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="55f0a-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="55f0a-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="55f0a-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="55f0a-134">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="55f0a-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="55f0a-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="55f0a-135">**Error**</span></span> <br/> | <span data-ttu-id="55f0a-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="55f0a-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="55f0a-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="55f0a-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="55f0a-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="55f0a-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="55f0a-139">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="55f0a-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="55f0a-140">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="55f0a-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="55f0a-141">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="55f0a-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="55f0a-142">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="55f0a-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="55f0a-143">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="55f0a-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="55f0a-144">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="55f0a-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="55f0a-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55f0a-145">Child elements</span></span>

|<span data-ttu-id="55f0a-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="55f0a-146">**Element**</span></span>|<span data-ttu-id="55f0a-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55f0a-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55f0a-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="55f0a-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="55f0a-149">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="55f0a-149">Provides text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="55f0a-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="55f0a-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="55f0a-151">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="55f0a-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="55f0a-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="55f0a-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="55f0a-153">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="55f0a-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="55f0a-154">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="55f0a-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="55f0a-155">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="55f0a-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="55f0a-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="55f0a-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="55f0a-157">Ordner</span><span class="sxs-lookup"><span data-stu-id="55f0a-157">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="55f0a-158">Enthält ein Array von Ordnern, die in Ordnervorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55f0a-158">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="55f0a-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55f0a-159">Parent elements</span></span>

|<span data-ttu-id="55f0a-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="55f0a-160">**Element**</span></span>|<span data-ttu-id="55f0a-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55f0a-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55f0a-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="55f0a-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="55f0a-163">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="55f0a-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55f0a-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55f0a-164">Remarks</span></span>

<span data-ttu-id="55f0a-165">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="55f0a-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="55f0a-166">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="55f0a-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55f0a-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="55f0a-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="55f0a-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="55f0a-168">Schema Name</span></span>  <br/> |<span data-ttu-id="55f0a-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="55f0a-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="55f0a-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="55f0a-170">Validation File</span></span>  <br/> |<span data-ttu-id="55f0a-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="55f0a-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="55f0a-172">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="55f0a-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="55f0a-173">False</span><span class="sxs-lookup"><span data-stu-id="55f0a-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55f0a-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55f0a-174">See also</span></span>

- [<span data-ttu-id="55f0a-175">GetFolder</span><span class="sxs-lookup"><span data-stu-id="55f0a-175">GetFolder</span></span>](getfolder.md)
- [<span data-ttu-id="55f0a-176">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="55f0a-176">GetFolderResponse</span></span>](getfolderresponse.md) 
- [<span data-ttu-id="55f0a-177">GetFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="55f0a-177">GetFolder operation</span></span>](getfolder-operation.md)

