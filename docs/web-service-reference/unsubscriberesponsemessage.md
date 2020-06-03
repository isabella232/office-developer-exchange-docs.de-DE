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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467165"
---
# <a name="unsubscriberesponsemessage"></a><span data-ttu-id="ac16d-103">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ac16d-103">UnsubscribeResponseMessage</span></span>

<span data-ttu-id="ac16d-104">Das **UnsubscribeResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [unsubscribe-Vorgangs](unsubscribe-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ac16d-104">The **UnsubscribeResponseMessage** element contains the status and result of a single [Unsubscribe operation](unsubscribe-operation.md) request.</span></span> 
  
- [<span data-ttu-id="ac16d-105">UnsubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="ac16d-105">UnsubscribeResponse</span></span>](unsubscriberesponse.md)
- [<span data-ttu-id="ac16d-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ac16d-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="ac16d-107">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ac16d-107">UnsubscribeResponseMessage</span></span>](unsubscriberesponsemessage.md)
  
```xml
<UnsubscribeResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</UnsubscribeResponseMessage>
```

 <span data-ttu-id="ac16d-108">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ac16d-108">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ac16d-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ac16d-109">Attributes and elements</span></span>

<span data-ttu-id="ac16d-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ac16d-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac16d-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="ac16d-111">Attributes</span></span>

|<span data-ttu-id="ac16d-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ac16d-112">**Attribute**</span></span>|<span data-ttu-id="ac16d-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac16d-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ac16d-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="ac16d-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="ac16d-115">Beschreibt den Status einer [Kündigungs Vorgangs](unsubscribe-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="ac16d-115">Describes the status of an [Unsubscribe operation](unsubscribe-operation.md) response.</span></span> <br/><br/><span data-ttu-id="ac16d-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="ac16d-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="ac16d-117">-Success</span><span class="sxs-lookup"><span data-stu-id="ac16d-117">-  Success</span></span>  <br/><span data-ttu-id="ac16d-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="ac16d-118">-  Warning</span></span>  <br/><span data-ttu-id="ac16d-119">-Error</span><span class="sxs-lookup"><span data-stu-id="ac16d-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="ac16d-120">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="ac16d-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="ac16d-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ac16d-121">**Value**</span></span>|<span data-ttu-id="ac16d-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac16d-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ac16d-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="ac16d-123">**Success**</span></span> <br/> |<span data-ttu-id="ac16d-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ac16d-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="ac16d-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="ac16d-125">**Warning**</span></span> <br/> | <span data-ttu-id="ac16d-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ac16d-126">Describes a request that was not processed.</span></span> <span data-ttu-id="ac16d-127">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ac16d-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="ac16d-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="ac16d-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="ac16d-129">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="ac16d-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="ac16d-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="ac16d-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="ac16d-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="ac16d-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="ac16d-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="ac16d-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="ac16d-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="ac16d-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="ac16d-134">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="ac16d-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="ac16d-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="ac16d-135">**Error**</span></span> <br/> | <span data-ttu-id="ac16d-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ac16d-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="ac16d-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="ac16d-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="ac16d-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="ac16d-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="ac16d-139">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="ac16d-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="ac16d-140">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="ac16d-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="ac16d-141">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="ac16d-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="ac16d-142">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="ac16d-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="ac16d-143">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="ac16d-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="ac16d-144">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="ac16d-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ac16d-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac16d-145">Child elements</span></span>

|<span data-ttu-id="ac16d-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="ac16d-146">**Element**</span></span>|<span data-ttu-id="ac16d-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac16d-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac16d-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="ac16d-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ac16d-149">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="ac16d-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ac16d-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ac16d-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ac16d-151">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ac16d-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="ac16d-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ac16d-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ac16d-153">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="ac16d-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="ac16d-154">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="ac16d-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="ac16d-155">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="ac16d-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ac16d-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="ac16d-156">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ac16d-157">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac16d-157">Parent elements</span></span>

|<span data-ttu-id="ac16d-158">**Element**</span><span class="sxs-lookup"><span data-stu-id="ac16d-158">**Element**</span></span>|<span data-ttu-id="ac16d-159">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac16d-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac16d-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ac16d-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="ac16d-161">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ac16d-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac16d-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac16d-162">Remarks</span></span>

<span data-ttu-id="ac16d-163">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ac16d-163">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac16d-164">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ac16d-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac16d-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac16d-165">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ac16d-166">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ac16d-166">Schema Name</span></span>  <br/> |<span data-ttu-id="ac16d-167">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ac16d-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ac16d-168">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ac16d-168">Validation File</span></span>  <br/> |<span data-ttu-id="ac16d-169">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ac16d-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ac16d-170">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ac16d-170">Can be Empty</span></span>  <br/> |<span data-ttu-id="ac16d-171">False</span><span class="sxs-lookup"><span data-stu-id="ac16d-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac16d-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac16d-172">See also</span></span>

- [<span data-ttu-id="ac16d-173">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="ac16d-173">Unsubscribe operation</span></span>](unsubscribe-operation.md)
- [<span data-ttu-id="ac16d-174">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ac16d-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

