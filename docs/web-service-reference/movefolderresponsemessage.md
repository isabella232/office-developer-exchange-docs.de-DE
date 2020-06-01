---
title: MoveFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveFolderResponseMessage
api_type:
- schema
ms.assetid: 54917251-96af-44c2-ae90-d545f0a16e2e
description: Das MoveFolderResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen MoveFolder-Vorgangsanforderung.
ms.openlocfilehash: 634fec89445b49d1c8c42541f2fc50d07b5a1acd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467473"
---
# <a name="movefolderresponsemessage"></a><span data-ttu-id="85658-103">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="85658-103">MoveFolderResponseMessage</span></span>

<span data-ttu-id="85658-104">Das **MoveFolderResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [MoveFolder-Vorgangs](movefolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="85658-104">The **MoveFolderResponseMessage** element contains the status and result of a single [MoveFolder operation](movefolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="85658-105">MoveFolderResponse</span><span class="sxs-lookup"><span data-stu-id="85658-105">MoveFolderResponse</span></span>](movefolderresponse.md)
- [<span data-ttu-id="85658-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="85658-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="85658-107">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="85658-107">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md)
  
```xml
<MoveFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</MoveFolderResponseMessage>
```

 <span data-ttu-id="85658-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="85658-108">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85658-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="85658-109">Attributes and elements</span></span>

<span data-ttu-id="85658-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="85658-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85658-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="85658-111">Attributes</span></span>

|<span data-ttu-id="85658-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="85658-112">**Attribute**</span></span>|<span data-ttu-id="85658-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85658-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85658-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="85658-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="85658-115">Beschreibt den Status einer [MoveFolder-Vorgangs](movefolder-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="85658-115">Describes the status of a [MoveFolder operation](movefolder-operation.md) response.</span></span> <br/><br/><span data-ttu-id="85658-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="85658-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="85658-117">-Success</span><span class="sxs-lookup"><span data-stu-id="85658-117">-  Success</span></span>  <br/><span data-ttu-id="85658-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="85658-118">-  Warning</span></span>  <br/><span data-ttu-id="85658-119">-Error</span><span class="sxs-lookup"><span data-stu-id="85658-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="85658-120">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="85658-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="85658-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="85658-121">**Value**</span></span>|<span data-ttu-id="85658-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85658-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85658-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="85658-123">**Success**</span></span> <br/> |<span data-ttu-id="85658-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="85658-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="85658-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="85658-125">**Warning**</span></span> <br/> | <span data-ttu-id="85658-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="85658-126">Describes a request that was not processed.</span></span> <span data-ttu-id="85658-127">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="85658-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="85658-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="85658-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="85658-129">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="85658-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="85658-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="85658-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="85658-131">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="85658-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="85658-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="85658-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="85658-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="85658-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="85658-134">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="85658-134">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="85658-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="85658-135">**Error**</span></span> <br/> | <span data-ttu-id="85658-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="85658-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="85658-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="85658-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="85658-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="85658-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="85658-139">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="85658-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="85658-140">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="85658-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="85658-141">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="85658-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="85658-142">-Alle nicht autorisierten Zugriffsversuche durch einen Client</span><span class="sxs-lookup"><span data-stu-id="85658-142">-  Any unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="85658-143">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="85658-143">-  Any server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="85658-144">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="85658-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="85658-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="85658-145">Child elements</span></span>

|<span data-ttu-id="85658-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="85658-146">**Element**</span></span>|<span data-ttu-id="85658-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85658-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85658-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="85658-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="85658-149">Eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="85658-149">A text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="85658-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="85658-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="85658-151">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="85658-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="85658-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="85658-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="85658-153">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="85658-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="85658-154">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="85658-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="85658-155">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="85658-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="85658-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="85658-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="85658-157">Ordner</span><span class="sxs-lookup"><span data-stu-id="85658-157">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="85658-158">Enthält ein Array verschobener Ordner.</span><span class="sxs-lookup"><span data-stu-id="85658-158">Contains an array of moved folders.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="85658-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="85658-159">Parent elements</span></span>

|<span data-ttu-id="85658-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="85658-160">**Element**</span></span>|<span data-ttu-id="85658-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85658-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85658-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="85658-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="85658-163">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="85658-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85658-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85658-164">Remarks</span></span>

<span data-ttu-id="85658-165">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="85658-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85658-166">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="85658-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85658-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="85658-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="85658-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="85658-168">Schema Name</span></span>  <br/> |<span data-ttu-id="85658-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="85658-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="85658-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="85658-170">Validation File</span></span>  <br/> |<span data-ttu-id="85658-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="85658-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="85658-172">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="85658-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="85658-173">False</span><span class="sxs-lookup"><span data-stu-id="85658-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="85658-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85658-174">See also</span></span>

- [<span data-ttu-id="85658-175">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="85658-175">MoveFolder</span></span>](movefolder.md)
- [<span data-ttu-id="85658-176">MoveFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="85658-176">MoveFolder operation</span></span>](movefolder-operation.md)

