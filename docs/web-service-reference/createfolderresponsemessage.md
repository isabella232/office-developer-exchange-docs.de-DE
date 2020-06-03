---
title: CreateFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateFolderResponseMessage
api_type:
- schema
ms.assetid: 1301dd15-b008-4fd9-8c89-b15a20b186e2
description: Das CreateFolderResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen CreateFolder-Vorgangsanforderung.
ms.openlocfilehash: 386dd2aa4e114d8382d5c83a3d6da70b1ccbbada
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457529"
---
# <a name="createfolderresponsemessage"></a><span data-ttu-id="88665-103">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="88665-103">CreateFolderResponseMessage</span></span>

<span data-ttu-id="88665-104">Das **CreateFolderResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [CreateFolder-Vorgangs](createfolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="88665-104">The **CreateFolderResponseMessage** element contains the status and result of a single [CreateFolder operation](createfolder-operation.md) request.</span></span> 
  
```xml
<CreateFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</CreateFolderResponseMessage>
```

<span data-ttu-id="88665-105">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="88665-105">**FolderInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="88665-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="88665-106">Attributes and elements</span></span>

<span data-ttu-id="88665-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="88665-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88665-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="88665-108">Attributes</span></span>

|<span data-ttu-id="88665-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="88665-109">**Attribute**</span></span>|<span data-ttu-id="88665-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88665-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="88665-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="88665-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="88665-112">Beschreibt den Status einer [CreateFolder-Vorgangs](createfolder-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="88665-112">Describes the status of a [CreateFolder operation](createfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="88665-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="88665-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="88665-114">-Success</span><span class="sxs-lookup"><span data-stu-id="88665-114">-  Success</span></span>  <br/><span data-ttu-id="88665-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="88665-115">-  Warning</span></span>  <br/><span data-ttu-id="88665-116">-Error</span><span class="sxs-lookup"><span data-stu-id="88665-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="88665-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="88665-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="88665-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="88665-118">**Value**</span></span>|<span data-ttu-id="88665-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88665-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="88665-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="88665-120">**Success**</span></span> <br/> |<span data-ttu-id="88665-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="88665-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="88665-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="88665-122">**Warning**</span></span> <br/> | <span data-ttu-id="88665-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="88665-123">Describes a request that was not processed.</span></span> <span data-ttu-id="88665-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="88665-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="88665-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="88665-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="88665-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="88665-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="88665-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="88665-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="88665-128">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="88665-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="88665-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="88665-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="88665-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="88665-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="88665-131">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="88665-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="88665-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="88665-132">**Error**</span></span> <br/> | <span data-ttu-id="88665-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="88665-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="88665-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="88665-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="88665-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="88665-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="88665-136">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="88665-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="88665-137">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="88665-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="88665-138">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="88665-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="88665-139">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="88665-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="88665-140">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="88665-140">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="88665-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="88665-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="88665-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="88665-142">Child elements</span></span>

|<span data-ttu-id="88665-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="88665-143">**Element**</span></span>|<span data-ttu-id="88665-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88665-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88665-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="88665-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="88665-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="88665-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="88665-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="88665-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="88665-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="88665-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="88665-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="88665-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="88665-150">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="88665-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="88665-151">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="88665-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="88665-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="88665-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="88665-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="88665-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="88665-154">Ordner</span><span class="sxs-lookup"><span data-stu-id="88665-154">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="88665-155">Enthält ein Array erstellter Ordner.</span><span class="sxs-lookup"><span data-stu-id="88665-155">Contains an array of created folders.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="88665-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="88665-156">Parent elements</span></span>

|<span data-ttu-id="88665-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="88665-157">**Element**</span></span>|<span data-ttu-id="88665-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88665-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88665-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="88665-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="88665-160">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="88665-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88665-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88665-161">Remarks</span></span>

<span data-ttu-id="88665-162">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server mit installierter Client Zugriffs-Server Rolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="88665-162">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="88665-163">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="88665-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88665-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="88665-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="88665-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="88665-165">Schema Name</span></span>  <br/> |<span data-ttu-id="88665-166">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="88665-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="88665-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="88665-167">Validation File</span></span>  <br/> |<span data-ttu-id="88665-168">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="88665-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="88665-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="88665-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="88665-170">False</span><span class="sxs-lookup"><span data-stu-id="88665-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88665-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88665-171">See also</span></span>

- [<span data-ttu-id="88665-172">CreateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="88665-172">CreateFolder operation</span></span>](createfolder-operation.md)
- [<span data-ttu-id="88665-173">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="88665-173">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="88665-174">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="88665-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

