---
title: CopyItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyItemResponseMessage
api_type:
- schema
ms.assetid: a43fe442-12c8-44ab-912c-8a226c9bb3e7
description: Das CopyItemResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen CopyItem-Vorgangsanforderung.
ms.openlocfilehash: 99449a4c05d0b2ea13dfca4235aa5f40d54d1214
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466444"
---
# <a name="copyitemresponsemessage"></a><span data-ttu-id="cf2d0-103">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cf2d0-103">CopyItemResponseMessage</span></span>

<span data-ttu-id="cf2d0-104">Das **CopyItemResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [CopyItem-Vorgangs](copyitem-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-104">The **CopyItemResponseMessage** element contains the status and result of a single [CopyItem operation](copyitem-operation.md) request.</span></span> 
  
```xml
<CopyItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</CopyItemResponseMessage>
```

 <span data-ttu-id="cf2d0-105">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="cf2d0-105">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cf2d0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cf2d0-106">Attributes and elements</span></span>

<span data-ttu-id="cf2d0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf2d0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cf2d0-108">Attributes</span></span>

|<span data-ttu-id="cf2d0-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="cf2d0-109">**Attribute**</span></span>|<span data-ttu-id="cf2d0-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cf2d0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf2d0-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="cf2d0-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="cf2d0-112">Beschreibt den Status einer [CopyItem-Vorgangs](copyitem-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-112">Describes the status of a [CopyItem operation](copyitem-operation.md) response.</span></span><br/><br/><span data-ttu-id="cf2d0-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="cf2d0-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="cf2d0-114">-Success</span><span class="sxs-lookup"><span data-stu-id="cf2d0-114">- Success</span></span>  <br/><span data-ttu-id="cf2d0-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="cf2d0-115">-  Warning</span></span>  <br/><span data-ttu-id="cf2d0-116">-Error</span><span class="sxs-lookup"><span data-stu-id="cf2d0-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="cf2d0-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="cf2d0-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="cf2d0-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="cf2d0-118">**Value**</span></span>|<span data-ttu-id="cf2d0-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cf2d0-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf2d0-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="cf2d0-120">**Success**</span></span> <br/> |<span data-ttu-id="cf2d0-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="cf2d0-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="cf2d0-122">**Warning**</span></span> <br/> | <span data-ttu-id="cf2d0-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-123">Describes a request that was not processed.</span></span> <span data-ttu-id="cf2d0-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="cf2d0-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="cf2d0-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="cf2d0-126">– Der Exchange-Informationsspeicher wird während des Batches offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-126">- The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="cf2d0-127">-Active Directory-Domänendienste (AD DS) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-127">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="cf2d0-128">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="cf2d0-129">-Die Postfachdatenbank (MDB) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-129">-  The mailbox database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="cf2d0-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="cf2d0-131">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="cf2d0-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="cf2d0-132">**Error**</span></span> <br/> | <span data-ttu-id="cf2d0-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="cf2d0-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="cf2d0-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="cf2d0-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="cf2d0-135">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="cf2d0-136">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="cf2d0-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="cf2d0-137">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="cf2d0-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="cf2d0-138">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="cf2d0-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="cf2d0-139">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="cf2d0-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="cf2d0-140">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="cf2d0-140">-  Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="cf2d0-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="cf2d0-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cf2d0-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cf2d0-142">Child elements</span></span>

|<span data-ttu-id="cf2d0-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="cf2d0-143">**Element**</span></span>|<span data-ttu-id="cf2d0-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cf2d0-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf2d0-145">- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)</span><span class="sxs-lookup"><span data-stu-id="cf2d0-145">- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)</span></span> <br/> [<span data-ttu-id="cf2d0-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="cf2d0-146">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="cf2d0-147">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-147">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="cf2d0-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cf2d0-148">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="cf2d0-149">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-149">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="cf2d0-150">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="cf2d0-150">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="cf2d0-151">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-151">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="cf2d0-152">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-152">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="cf2d0-153">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="cf2d0-153">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="cf2d0-154">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-154">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="cf2d0-155">Items</span><span class="sxs-lookup"><span data-stu-id="cf2d0-155">Items</span></span>](items.md) <br/> |<span data-ttu-id="cf2d0-156">Enthält ein Array kopierter Elemente.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-156">Contains an array of copied items</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cf2d0-157">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cf2d0-157">Parent elements</span></span>

|<span data-ttu-id="cf2d0-158">**Element**</span><span class="sxs-lookup"><span data-stu-id="cf2d0-158">**Element**</span></span>|<span data-ttu-id="cf2d0-159">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cf2d0-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf2d0-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cf2d0-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="cf2d0-161">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf2d0-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf2d0-162">Remarks</span></span>

<span data-ttu-id="cf2d0-163">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="cf2d0-163">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf2d0-164">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="cf2d0-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf2d0-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="cf2d0-165">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cf2d0-166">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cf2d0-166">Schema name</span></span>  <br/> |<span data-ttu-id="cf2d0-167">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="cf2d0-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cf2d0-168">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cf2d0-168">Validation file</span></span>  <br/> |<span data-ttu-id="cf2d0-169">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cf2d0-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cf2d0-170">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="cf2d0-170">Can be empty</span></span>  <br/> |<span data-ttu-id="cf2d0-171">False</span><span class="sxs-lookup"><span data-stu-id="cf2d0-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf2d0-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf2d0-172">See also</span></span>

- [<span data-ttu-id="cf2d0-173">CopyItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cf2d0-173">CopyItem operation</span></span>](copyitem-operation.md)
- [<span data-ttu-id="cf2d0-174">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="cf2d0-174">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

