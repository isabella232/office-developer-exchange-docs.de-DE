---
title: UnsubscribeResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnsubscribeResponseMessage
api_type:
- schema
ms.assetid: 92c53b13-0ca1-4b44-b925-b23682e9417c
description: Das UnsubscribeResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen unsubscribe-Vorgangsanforderung.
ms.openlocfilehash: e5b42404d09e6367c134934409ec2a45351e135e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467165"
---
# <a name="unsubscriberesponsemessage"></a><span data-ttu-id="ffeae-103">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ffeae-103">UnsubscribeResponseMessage</span></span>

<span data-ttu-id="ffeae-104">Das **UnsubscribeResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [unsubscribe-Vorgangs](unsubscribe-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ffeae-104">The **UnsubscribeResponseMessage** element contains the status and result of a single [Unsubscribe operation](unsubscribe-operation.md) request.</span></span> 
  
- [<span data-ttu-id="ffeae-105">UnsubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="ffeae-105">UnsubscribeResponse</span></span>](unsubscriberesponse.md)
- [<span data-ttu-id="ffeae-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ffeae-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="ffeae-107">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ffeae-107">UnsubscribeResponseMessage</span></span>](unsubscriberesponsemessage.md)
  
```xml
<UnsubscribeResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</UnsubscribeResponseMessage>
```

 <span data-ttu-id="ffeae-108">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ffeae-108">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ffeae-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ffeae-109">Attributes and elements</span></span>

<span data-ttu-id="ffeae-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ffeae-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ffeae-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="ffeae-111">Attributes</span></span>

|<span data-ttu-id="ffeae-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ffeae-112">**Attribute**</span></span>|<span data-ttu-id="ffeae-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffeae-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ffeae-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="ffeae-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="ffeae-115">Beschreibt den Status einer [Kündigungs Vorgangs](unsubscribe-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="ffeae-115">Describes the status of an [Unsubscribe operation](unsubscribe-operation.md) response.</span></span> <br/><br/><span data-ttu-id="ffeae-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="ffeae-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="ffeae-117">-Success</span><span class="sxs-lookup"><span data-stu-id="ffeae-117">-  Success</span></span>  <br/><span data-ttu-id="ffeae-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="ffeae-118">-  Warning</span></span>  <br/><span data-ttu-id="ffeae-119">-Error</span><span class="sxs-lookup"><span data-stu-id="ffeae-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="ffeae-120">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="ffeae-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="ffeae-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ffeae-121">**Value**</span></span>|<span data-ttu-id="ffeae-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffeae-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ffeae-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="ffeae-123">**Success**</span></span> <br/> |<span data-ttu-id="ffeae-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ffeae-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="ffeae-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="ffeae-125">**Warning**</span></span> <br/> | <span data-ttu-id="ffeae-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ffeae-126">Describes a request that was not processed.</span></span> <span data-ttu-id="ffeae-127">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ffeae-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="ffeae-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="ffeae-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="ffeae-129">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="ffeae-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="ffeae-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="ffeae-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="ffeae-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="ffeae-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="ffeae-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="ffeae-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="ffeae-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="ffeae-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="ffeae-134">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="ffeae-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="ffeae-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="ffeae-135">**Error**</span></span> <br/> | <span data-ttu-id="ffeae-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ffeae-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="ffeae-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="ffeae-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="ffeae-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="ffeae-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="ffeae-139">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="ffeae-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="ffeae-140">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="ffeae-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="ffeae-141">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="ffeae-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="ffeae-142">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="ffeae-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="ffeae-143">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="ffeae-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="ffeae-144">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="ffeae-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ffeae-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ffeae-145">Child elements</span></span>

|<span data-ttu-id="ffeae-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="ffeae-146">**Element**</span></span>|<span data-ttu-id="ffeae-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffeae-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ffeae-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="ffeae-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ffeae-149">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="ffeae-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ffeae-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ffeae-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ffeae-151">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ffeae-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="ffeae-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ffeae-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ffeae-153">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="ffeae-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="ffeae-154">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="ffeae-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="ffeae-155">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="ffeae-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ffeae-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="ffeae-156">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ffeae-157">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ffeae-157">Parent elements</span></span>

|<span data-ttu-id="ffeae-158">**Element**</span><span class="sxs-lookup"><span data-stu-id="ffeae-158">**Element**</span></span>|<span data-ttu-id="ffeae-159">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffeae-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ffeae-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ffeae-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="ffeae-161">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ffeae-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffeae-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffeae-162">Remarks</span></span>

<span data-ttu-id="ffeae-163">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ffeae-163">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ffeae-164">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ffeae-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ffeae-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="ffeae-165">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ffeae-166">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ffeae-166">Schema Name</span></span>  <br/> |<span data-ttu-id="ffeae-167">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ffeae-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ffeae-168">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ffeae-168">Validation File</span></span>  <br/> |<span data-ttu-id="ffeae-169">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ffeae-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ffeae-170">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ffeae-170">Can be Empty</span></span>  <br/> |<span data-ttu-id="ffeae-171">False</span><span class="sxs-lookup"><span data-stu-id="ffeae-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ffeae-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffeae-172">See also</span></span>

- [<span data-ttu-id="ffeae-173">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="ffeae-173">Unsubscribe operation</span></span>](unsubscribe-operation.md)
- [<span data-ttu-id="ffeae-174">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ffeae-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

