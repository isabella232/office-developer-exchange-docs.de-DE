---
title: UpdateUserConfigurationResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateUserConfigurationResponseMessage
api_type:
- schema
ms.assetid: 27728e57-5a9b-4314-ad64-df7869098f62
description: Das UpdateUserConfigurationResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen UpdateUserConfiguration-Vorgangsanforderung.
ms.openlocfilehash: 9c885c87f4b48df16e4097b9c4eafd7e9278c7b8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468523"
---
# <a name="updateuserconfigurationresponsemessage"></a><span data-ttu-id="cf2f9-103">UpdateUserConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cf2f9-103">UpdateUserConfigurationResponseMessage</span></span>

<span data-ttu-id="cf2f9-104">Das **UpdateUserConfigurationResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen UpdateUserConfiguration-Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-104">The **UpdateUserConfigurationResponseMessage** element contains the status and result of a single UpdateUserConfiguration operation request.</span></span> 
  
```xml
<UpdateUserConfigurationResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</UpdateUserConfigurationResponseMessage>
```

 <span data-ttu-id="cf2f9-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="cf2f9-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cf2f9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cf2f9-106">Attributes and elements</span></span>

<span data-ttu-id="cf2f9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf2f9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cf2f9-108">Attributes</span></span>

|<span data-ttu-id="cf2f9-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="cf2f9-109">**Attribute**</span></span>|<span data-ttu-id="cf2f9-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cf2f9-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf2f9-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="cf2f9-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="cf2f9-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="cf2f9-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="cf2f9-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="cf2f9-114">-Success</span><span class="sxs-lookup"><span data-stu-id="cf2f9-114">-  Success</span></span>  <br/><span data-ttu-id="cf2f9-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="cf2f9-115">-  Warning</span></span>  <br/><span data-ttu-id="cf2f9-116">-Error</span><span class="sxs-lookup"><span data-stu-id="cf2f9-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="cf2f9-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="cf2f9-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="cf2f9-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="cf2f9-118">**Value**</span></span>|<span data-ttu-id="cf2f9-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cf2f9-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf2f9-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="cf2f9-120">**Success**</span></span> <br/> |<span data-ttu-id="cf2f9-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="cf2f9-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="cf2f9-122">**Warning**</span></span> <br/> | <span data-ttu-id="cf2f9-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-123">Describes a request that was not processed.</span></span> <span data-ttu-id="cf2f9-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="cf2f9-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="cf2f9-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="cf2f9-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="cf2f9-127">-Der Active Directory Verzeichnisdienst ist offline.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="cf2f9-128">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="cf2f9-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="cf2f9-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="cf2f9-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="cf2f9-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="cf2f9-132">**Error**</span></span> <br/> | <span data-ttu-id="cf2f9-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="cf2f9-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="cf2f9-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="cf2f9-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="cf2f9-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="cf2f9-136">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="cf2f9-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="cf2f9-137">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="cf2f9-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="cf2f9-138">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="cf2f9-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="cf2f9-139">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="cf2f9-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="cf2f9-140">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="cf2f9-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="cf2f9-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="cf2f9-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cf2f9-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cf2f9-142">Child elements</span></span>

|<span data-ttu-id="cf2f9-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="cf2f9-143">**Element**</span></span>|<span data-ttu-id="cf2f9-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cf2f9-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf2f9-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="cf2f9-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="cf2f9-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="cf2f9-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cf2f9-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="cf2f9-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="cf2f9-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="cf2f9-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="cf2f9-150">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="cf2f9-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="cf2f9-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="cf2f9-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="cf2f9-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cf2f9-154">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cf2f9-154">Parent elements</span></span>

|<span data-ttu-id="cf2f9-155">**Element**</span><span class="sxs-lookup"><span data-stu-id="cf2f9-155">**Element**</span></span>|<span data-ttu-id="cf2f9-156">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cf2f9-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf2f9-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cf2f9-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="cf2f9-158">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf2f9-159">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf2f9-159">Remarks</span></span>

<span data-ttu-id="cf2f9-160">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server mit installierter Client Zugriffs-Server Rolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="cf2f9-160">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf2f9-161">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="cf2f9-161">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf2f9-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="cf2f9-162">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cf2f9-163">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cf2f9-163">Schema Name</span></span>  <br/> |<span data-ttu-id="cf2f9-164">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="cf2f9-164">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cf2f9-165">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cf2f9-165">Validation File</span></span>  <br/> |<span data-ttu-id="cf2f9-166">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cf2f9-166">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cf2f9-167">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cf2f9-167">Can be Empty</span></span>  <br/> |<span data-ttu-id="cf2f9-168">False</span><span class="sxs-lookup"><span data-stu-id="cf2f9-168">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf2f9-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf2f9-169">See also</span></span>

- [<span data-ttu-id="cf2f9-170">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cf2f9-170">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

