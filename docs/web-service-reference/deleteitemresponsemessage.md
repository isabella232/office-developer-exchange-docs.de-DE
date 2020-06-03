---
title: DeleteItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItemResponseMessage
api_type:
- schema
ms.assetid: c3d34c4d-8d83-4612-aa9e-66f9cc7314df
description: Das DeleteItemResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen DeleteItem-Vorgangsanforderung.
ms.openlocfilehash: 78e3efc6a9e9e6629d7efe7f2dc294e0a731005a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526928"
---
# <a name="deleteitemresponsemessage"></a><span data-ttu-id="8af8e-103">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8af8e-103">DeleteItemResponseMessage</span></span>

<span data-ttu-id="8af8e-104">Das **DeleteItemResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [DeleteItem-Vorgangs](deleteitem-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8af8e-104">The **DeleteItemResponseMessage** element contains the status and result of a single [DeleteItem operation](deleteitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="8af8e-105">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="8af8e-105">DeleteItemResponse</span></span>](deleteitemresponse.md) 
- [<span data-ttu-id="8af8e-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8af8e-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="8af8e-107">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8af8e-107">DeleteItemResponseMessage</span></span>](deleteitemresponsemessage.md)
  
```xml
<DeleteItemResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DeleteItemResponseMessage>
```

 <span data-ttu-id="8af8e-108">**DeleteItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="8af8e-108">**DeleteItemResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8af8e-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8af8e-109">Attributes and elements</span></span>

<span data-ttu-id="8af8e-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8af8e-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8af8e-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="8af8e-111">Attributes</span></span>

|<span data-ttu-id="8af8e-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8af8e-112">**Attribute**</span></span>|<span data-ttu-id="8af8e-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8af8e-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8af8e-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="8af8e-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="8af8e-115">Beschreibt den Status einer [DeleteItem-Vorgangs](deleteitem-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="8af8e-115">Describes the status of a [DeleteItem operation](deleteitem-operation.md) response.</span></span><br/><br/><span data-ttu-id="8af8e-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="8af8e-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="8af8e-117">-Success</span><span class="sxs-lookup"><span data-stu-id="8af8e-117">- Success</span></span>  <br/><span data-ttu-id="8af8e-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="8af8e-118">-  Warning</span></span>  <br/><span data-ttu-id="8af8e-119">-Error</span><span class="sxs-lookup"><span data-stu-id="8af8e-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="8af8e-120">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="8af8e-120">ResponseClass attribute</span></span>

|<span data-ttu-id="8af8e-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8af8e-121">**Value**</span></span>|<span data-ttu-id="8af8e-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8af8e-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8af8e-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="8af8e-123">**Success**</span></span> <br/> |<span data-ttu-id="8af8e-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="8af8e-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="8af8e-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="8af8e-125">**Warning**</span></span> <br/> | <span data-ttu-id="8af8e-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="8af8e-126">Describes a request that was not processed.</span></span> <span data-ttu-id="8af8e-127">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="8af8e-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="8af8e-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="8af8e-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="8af8e-129">– Der Exchange-Informationsspeicher wird während des Batches offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="8af8e-129">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="8af8e-130">-Active Directory-Domänendienste (AD DS) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="8af8e-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="8af8e-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="8af8e-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="8af8e-132">-Die Nachrichtendatenbank (MDB) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="8af8e-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="8af8e-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="8af8e-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="8af8e-134">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="8af8e-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="8af8e-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="8af8e-135">**Error**</span></span> <br/> | <span data-ttu-id="8af8e-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8af8e-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="8af8e-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="8af8e-137">The following are examples of sources of errors:</span></span><br/><br/><span data-ttu-id="8af8e-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="8af8e-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="8af8e-139">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="8af8e-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="8af8e-140">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="8af8e-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="8af8e-141">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="8af8e-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="8af8e-142">-Ein Client versucht, die Fehler Protokollierungsstufe oberhalb der vom Administrator zulässigen Maximalstufe festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8af8e-142">-  A client attempt to set the error logging level above the maximum level that is permitted by the administrator</span></span>  <br/><span data-ttu-id="8af8e-143">-Ein Client versucht, die Schweregrad Fehlerstufe unter der vom Administrator angegebenen Standardstufe festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8af8e-143">-  A client attempt to set the severity failure level below the default level that is specified by the administrator</span></span>  <br/><span data-ttu-id="8af8e-144">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="8af8e-144">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="8af8e-145">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="8af8e-145">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="8af8e-146">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="8af8e-146">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8af8e-147">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8af8e-147">Child elements</span></span>

|<span data-ttu-id="8af8e-148">**Element**</span><span class="sxs-lookup"><span data-stu-id="8af8e-148">**Element**</span></span>|<span data-ttu-id="8af8e-149">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8af8e-149">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8af8e-150">MessageText</span><span class="sxs-lookup"><span data-stu-id="8af8e-150">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="8af8e-151">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="8af8e-151">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="8af8e-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8af8e-152">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="8af8e-153">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="8af8e-153">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="8af8e-154">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8af8e-154">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="8af8e-155">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="8af8e-155">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="8af8e-156">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="8af8e-156">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="8af8e-157">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="8af8e-157">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="8af8e-158">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="8af8e-158">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8af8e-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8af8e-159">Parent elements</span></span>

|<span data-ttu-id="8af8e-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="8af8e-160">**Element**</span></span>|<span data-ttu-id="8af8e-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8af8e-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8af8e-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8af8e-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="8af8e-163">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8af8e-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8af8e-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8af8e-164">Remarks</span></span>

<span data-ttu-id="8af8e-165">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8af8e-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="8af8e-166">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="8af8e-166">Version differences</span></span>

<span data-ttu-id="8af8e-167">In Versionen von Exchange, beginnend mit Build 15.00.0986.00, ist das **DeleteItemResponseMessage** -Element vom Typ **DeleteItemResponseMessageType**.</span><span class="sxs-lookup"><span data-stu-id="8af8e-167">In versions of Exchange starting with build 15.00.0986.00, the **DeleteItemResponseMessage** element is of type **DeleteItemResponseMessageType**.</span></span> <span data-ttu-id="8af8e-168">In früheren Versionen ist das-Element vom Typ **ResponseMessageType**.</span><span class="sxs-lookup"><span data-stu-id="8af8e-168">In previous versions, the element is of type **ResponseMessageType**.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8af8e-169">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8af8e-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8af8e-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="8af8e-170">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8af8e-171">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8af8e-171">Schema Name</span></span>  <br/> |<span data-ttu-id="8af8e-172">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8af8e-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8af8e-173">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8af8e-173">Validation File</span></span>  <br/> |<span data-ttu-id="8af8e-174">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="8af8e-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8af8e-175">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8af8e-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="8af8e-176">False</span><span class="sxs-lookup"><span data-stu-id="8af8e-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8af8e-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8af8e-177">See also</span></span>

- [<span data-ttu-id="8af8e-178">DeleteItem-Operation</span><span class="sxs-lookup"><span data-stu-id="8af8e-178">DeleteItem operation</span></span>](deleteitem-operation.md)
- [<span data-ttu-id="8af8e-179">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="8af8e-179">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="8af8e-180">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8af8e-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="8af8e-181">Löschen von Elementen (Exchange Webdienste)</span><span class="sxs-lookup"><span data-stu-id="8af8e-181">Deleting Items (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/9bfc39e6-d944-4eb6-8aee-cbaf1e37c67d%28Office.15%29.aspx)

