---
title: EmptyFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 678dd5ce-8d9e-4939-bf1b-a8e148f4f449
description: Das EmptyFolderResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen EmptyFolder-Anforderung.
ms.openlocfilehash: fd69df45d7e1d6538a977b79711baa769413ea66
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526214"
---
# <a name="emptyfolderresponsemessage"></a><span data-ttu-id="8a830-103">EmptyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8a830-103">EmptyFolderResponseMessage</span></span>

<span data-ttu-id="8a830-104">Das **EmptyFolderResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [EmptyFolder](emptyfolder.md) -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8a830-104">The **EmptyFolderResponseMessage** element contains the status and result of a single [EmptyFolder](emptyfolder.md) request.</span></span> 
  
```XML
<EmptyFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</EmptyFolderResponseMessage>
```

 <span data-ttu-id="8a830-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="8a830-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8a830-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8a830-106">Attributes and elements</span></span>

<span data-ttu-id="8a830-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8a830-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a830-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8a830-108">Attributes</span></span>

|<span data-ttu-id="8a830-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8a830-109">**Attribute**</span></span>|<span data-ttu-id="8a830-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8a830-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a830-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="8a830-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="8a830-112">Beschreibt den Status einer [EmptyFolder-Vorgangs](emptyfolder-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="8a830-112">Describes the status of an [EmptyFolder operation](emptyfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="8a830-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="8a830-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="8a830-114">-Success</span><span class="sxs-lookup"><span data-stu-id="8a830-114">-  Success</span></span>  <br/><span data-ttu-id="8a830-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="8a830-115">-  Warning</span></span>  <br/><span data-ttu-id="8a830-116">-Error</span><span class="sxs-lookup"><span data-stu-id="8a830-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="8a830-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="8a830-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="8a830-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8a830-118">**Value**</span></span>|<span data-ttu-id="8a830-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8a830-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a830-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="8a830-120">**Success**</span></span> <br/> |<span data-ttu-id="8a830-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="8a830-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="8a830-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="8a830-122">**Warning**</span></span> <br/> | <span data-ttu-id="8a830-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="8a830-123">Describes a request that was not processed.</span></span> <span data-ttu-id="8a830-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="8a830-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="8a830-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="8a830-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="8a830-126">– Der Exchange-Informationsspeicher wird während des Batches offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="8a830-126">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="8a830-127">-Active Directory-Domänendienste (AD DS) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="8a830-127">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="8a830-128">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="8a830-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="8a830-129">-Die Nachrichtendatenbank (MDB) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="8a830-129">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="8a830-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="8a830-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="8a830-131">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="8a830-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="8a830-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="8a830-132">**Error**</span></span> <br/> | <span data-ttu-id="8a830-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8a830-133">Describes a request that cannot be fulfilled.</span></span><br/><br/> <span data-ttu-id="8a830-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="8a830-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="8a830-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="8a830-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="8a830-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="8a830-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="8a830-137">-Ein unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="8a830-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="8a830-138">-Ein Attribut oder Element, das im Kontext ungültig ist</span><span class="sxs-lookup"><span data-stu-id="8a830-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="8a830-139">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client</span><span class="sxs-lookup"><span data-stu-id="8a830-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="8a830-140">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="8a830-140">-  A server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="8a830-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="8a830-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8a830-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8a830-142">Child elements</span></span>

|<span data-ttu-id="8a830-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="8a830-143">**Element**</span></span>|<span data-ttu-id="8a830-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8a830-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8a830-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="8a830-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="8a830-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="8a830-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="8a830-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8a830-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="8a830-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="8a830-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="8a830-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8a830-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="8a830-150">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="8a830-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="8a830-151">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="8a830-151">It contains the value of 0.</span></span>  <br/> |
|[<span data-ttu-id="8a830-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="8a830-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="8a830-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="8a830-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8a830-154">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8a830-154">Parent elements</span></span>

|<span data-ttu-id="8a830-155">**Element**</span><span class="sxs-lookup"><span data-stu-id="8a830-155">**Element**</span></span>|<span data-ttu-id="8a830-156">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8a830-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8a830-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8a830-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="8a830-158">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8a830-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8a830-159">Textwert</span><span class="sxs-lookup"><span data-stu-id="8a830-159">Text value</span></span>

<span data-ttu-id="8a830-160">Keine.</span><span class="sxs-lookup"><span data-stu-id="8a830-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8a830-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a830-161">Remarks</span></span>

<span data-ttu-id="8a830-162">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8a830-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a830-163">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8a830-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a830-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="8a830-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8a830-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8a830-165">Schema Name</span></span>  <br/> |<span data-ttu-id="8a830-166">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8a830-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8a830-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8a830-167">Validation File</span></span>  <br/> |<span data-ttu-id="8a830-168">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="8a830-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8a830-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8a830-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="8a830-170">False</span><span class="sxs-lookup"><span data-stu-id="8a830-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a830-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a830-171">See also</span></span>

- [<span data-ttu-id="8a830-172">EmptyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8a830-172">EmptyFolder operation</span></span>](emptyfolder-operation.md)
- [<span data-ttu-id="8a830-173">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="8a830-173">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="8a830-174">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8a830-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

