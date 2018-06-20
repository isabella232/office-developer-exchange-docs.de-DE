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
description: Das UpdateUserConfigurationResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung UpdateUserConfiguration Vorgang.
ms.openlocfilehash: db26bb4bc821ac9a09c350009ab8132466e759bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839411"
---
# <a name="updateuserconfigurationresponsemessage"></a><span data-ttu-id="cd107-103">UpdateUserConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cd107-103">UpdateUserConfigurationResponseMessage</span></span>

<span data-ttu-id="cd107-104">Das **UpdateUserConfigurationResponseMessage** -Element enthält den Status und das Ergebnis einer Anforderung UpdateUserConfiguration Vorgang.</span><span class="sxs-lookup"><span data-stu-id="cd107-104">The **UpdateUserConfigurationResponseMessage** element contains the status and result of a single UpdateUserConfiguration operation request.</span></span> 
  
```xml
<UpdateUserConfigurationResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</UpdateUserConfigurationResponseMessage>
```

 <span data-ttu-id="cd107-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="cd107-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cd107-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cd107-106">Attributes and elements</span></span>

<span data-ttu-id="cd107-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cd107-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd107-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cd107-108">Attributes</span></span>

|<span data-ttu-id="cd107-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="cd107-109">**Attribute**</span></span>|<span data-ttu-id="cd107-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cd107-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd107-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="cd107-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="cd107-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="cd107-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="cd107-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="cd107-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="cd107-114">-Success</span><span class="sxs-lookup"><span data-stu-id="cd107-114">-  Success</span></span>  <br/><span data-ttu-id="cd107-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="cd107-115">-  Warning</span></span>  <br/><span data-ttu-id="cd107-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="cd107-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="cd107-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="cd107-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="cd107-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="cd107-118">**Value**</span></span>|<span data-ttu-id="cd107-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cd107-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd107-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="cd107-120">**Success**</span></span> <br/> |<span data-ttu-id="cd107-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="cd107-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="cd107-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="cd107-122">**Warning**</span></span> <br/> | <span data-ttu-id="cd107-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="cd107-123">Describes a request that was not processed.</span></span> <span data-ttu-id="cd107-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="cd107-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="cd107-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="cd107-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="cd107-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="cd107-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="cd107-127">– Der Active Directory-Verzeichnisdienst ist offline.</span><span class="sxs-lookup"><span data-stu-id="cd107-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="cd107-128">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="cd107-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="cd107-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="cd107-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="cd107-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="cd107-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="cd107-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="cd107-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="cd107-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="cd107-132">**Error**</span></span> <br/> | <span data-ttu-id="cd107-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="cd107-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="cd107-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="cd107-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="cd107-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="cd107-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="cd107-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="cd107-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="cd107-137">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="cd107-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="cd107-138">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="cd107-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="cd107-139">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="cd107-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="cd107-140">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="cd107-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="cd107-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="cd107-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cd107-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cd107-142">Child elements</span></span>

|<span data-ttu-id="cd107-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="cd107-143">**Element**</span></span>|<span data-ttu-id="cd107-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cd107-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd107-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="cd107-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="cd107-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="cd107-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="cd107-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cd107-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="cd107-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="cd107-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="cd107-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="cd107-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="cd107-150">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="cd107-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="cd107-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="cd107-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="cd107-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="cd107-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="cd107-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="cd107-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cd107-154">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cd107-154">Parent elements</span></span>

|<span data-ttu-id="cd107-155">**Element**</span><span class="sxs-lookup"><span data-stu-id="cd107-155">**Element**</span></span>|<span data-ttu-id="cd107-156">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cd107-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd107-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cd107-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="cd107-158">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cd107-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd107-159">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cd107-159">Remarks</span></span>

<span data-ttu-id="cd107-160">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, der Exchange-Server, mit die Clientzugriffs-Serverrolle installiert ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd107-160">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd107-161">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="cd107-161">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd107-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd107-162">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cd107-163">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cd107-163">Schema Name</span></span>  <br/> |<span data-ttu-id="cd107-164">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="cd107-164">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cd107-165">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cd107-165">Validation File</span></span>  <br/> |<span data-ttu-id="cd107-166">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cd107-166">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cd107-167">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cd107-167">Can be Empty</span></span>  <br/> |<span data-ttu-id="cd107-168">False</span><span class="sxs-lookup"><span data-stu-id="cd107-168">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd107-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd107-169">See also</span></span>

- [<span data-ttu-id="cd107-170">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cd107-170">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

