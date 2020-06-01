---
title: DeleteUserConfigurationResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteUserConfigurationResponseMessage
api_type:
- schema
ms.assetid: 543b1743-7e1c-4acb-93bd-34532e7fe79b
description: Das DeleteUserConfigurationResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen DeleteUserConfiguration-Anforderung.
ms.openlocfilehash: d8d15d0fb57b5f7fc16454fb6b03713faee22a03
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458754"
---
# <a name="deleteuserconfigurationresponsemessage"></a><span data-ttu-id="fb09d-103">DeleteUserConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fb09d-103">DeleteUserConfigurationResponseMessage</span></span>

<span data-ttu-id="fb09d-104">Das **DeleteUserConfigurationResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen **DeleteUserConfiguration** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="fb09d-104">The **DeleteUserConfigurationResponseMessage** element contains the status and result of a single **DeleteUserConfiguration** request.</span></span> 
  
```xml
<DeleteUserConfigurationResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DeleteUserConfigurationResponseMessage>
```

 <span data-ttu-id="fb09d-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="fb09d-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fb09d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fb09d-106">Attributes and elements</span></span>

<span data-ttu-id="fb09d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fb09d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fb09d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fb09d-108">Attributes</span></span>

|<span data-ttu-id="fb09d-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fb09d-109">**Attribute**</span></span>|<span data-ttu-id="fb09d-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fb09d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fb09d-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="fb09d-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="fb09d-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="fb09d-112">Describes the status of the response.</span></span><br/><br/><span data-ttu-id="fb09d-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="fb09d-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="fb09d-114">-Success</span><span class="sxs-lookup"><span data-stu-id="fb09d-114">-  Success</span></span>  <br/><span data-ttu-id="fb09d-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="fb09d-115">-  Warning</span></span>  <br/><span data-ttu-id="fb09d-116">-Error</span><span class="sxs-lookup"><span data-stu-id="fb09d-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="fb09d-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="fb09d-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="fb09d-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fb09d-118">**Value**</span></span>|<span data-ttu-id="fb09d-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fb09d-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fb09d-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="fb09d-120">**Success**</span></span> <br/> |<span data-ttu-id="fb09d-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="fb09d-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="fb09d-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="fb09d-122">**Warning**</span></span> <br/> | <span data-ttu-id="fb09d-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="fb09d-123">Describes a request that was not processed.</span></span> <span data-ttu-id="fb09d-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="fb09d-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="fb09d-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="fb09d-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="fb09d-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="fb09d-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="fb09d-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="fb09d-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="fb09d-128">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="fb09d-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="fb09d-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="fb09d-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="fb09d-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="fb09d-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="fb09d-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="fb09d-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="fb09d-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="fb09d-132">**Error**</span></span> <br/> | <span data-ttu-id="fb09d-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="fb09d-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="fb09d-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="fb09d-134">The following are examples of sources of errors:</span></span><br/><br/><span data-ttu-id="fb09d-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="fb09d-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="fb09d-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="fb09d-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="fb09d-137">-Ein unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="fb09d-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="fb09d-138">-Ein Attribut oder Element, das im Kontext ungültig ist</span><span class="sxs-lookup"><span data-stu-id="fb09d-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="fb09d-139">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client</span><span class="sxs-lookup"><span data-stu-id="fb09d-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="fb09d-140">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="fb09d-140">-  A server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="fb09d-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="fb09d-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fb09d-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fb09d-142">Child elements</span></span>

|<span data-ttu-id="fb09d-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="fb09d-143">**Element**</span></span>|<span data-ttu-id="fb09d-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fb09d-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fb09d-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="fb09d-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="fb09d-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="fb09d-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="fb09d-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="fb09d-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="fb09d-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="fb09d-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="fb09d-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="fb09d-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="fb09d-150">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="fb09d-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="fb09d-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="fb09d-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="fb09d-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="fb09d-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="fb09d-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="fb09d-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fb09d-154">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fb09d-154">Parent elements</span></span>

|<span data-ttu-id="fb09d-155">**Element**</span><span class="sxs-lookup"><span data-stu-id="fb09d-155">**Element**</span></span>|<span data-ttu-id="fb09d-156">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fb09d-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fb09d-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="fb09d-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="fb09d-158">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="fb09d-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fb09d-159">Textwert</span><span class="sxs-lookup"><span data-stu-id="fb09d-159">Text value</span></span>

<span data-ttu-id="fb09d-160">Keine.</span><span class="sxs-lookup"><span data-stu-id="fb09d-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb09d-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb09d-161">Remarks</span></span>

<span data-ttu-id="fb09d-162">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fb09d-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fb09d-163">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fb09d-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb09d-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb09d-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fb09d-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fb09d-165">Schema Name</span></span>  <br/> |<span data-ttu-id="fb09d-166">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="fb09d-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fb09d-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fb09d-167">Validation File</span></span>  <br/> |<span data-ttu-id="fb09d-168">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="fb09d-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fb09d-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fb09d-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="fb09d-170">False</span><span class="sxs-lookup"><span data-stu-id="fb09d-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fb09d-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb09d-171">See also</span></span>

- [<span data-ttu-id="fb09d-172">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fb09d-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

