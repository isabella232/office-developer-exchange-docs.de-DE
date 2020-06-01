---
title: PlayOnPhoneResponse (Exchange Webdienste)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PlayOnPhoneResponse
api_type:
- schema
ms.assetid: 578b70d1-dc9d-4bce-b859-0109b2d2bcec
description: Das PlayOnPhoneResponse-Element gibt die Antwort auf eine Anforderung an, eine Voicemail über das Telefon wiederzugeben.
ms.openlocfilehash: 907864d7fe669aac99b2ff6d1c5eba71b9ddf79f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459623"
---
# <a name="playonphoneresponse-exchange-web-services"></a><span data-ttu-id="ff73c-103">PlayOnPhoneResponse (Exchange Webdienste)</span><span class="sxs-lookup"><span data-stu-id="ff73c-103">PlayOnPhoneResponse (Exchange Web Services)</span></span>

<span data-ttu-id="ff73c-104">Das **PlayOnPhoneResponse** -Element gibt die Antwort auf eine Anforderung an, eine Voicemail über das Telefon wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="ff73c-104">The **PlayOnPhoneResponse** element specifies the response to a request to play a voice mail over the telephone.</span></span> 
  
```xml
<PlayOnPhoneResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <PhoneCallId/>
</PlayOnPhoneResponse>
```

 <span data-ttu-id="ff73c-105">**PlayOnPhoneResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ff73c-105">**PlayOnPhoneResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ff73c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ff73c-106">Attributes and elements</span></span>

<span data-ttu-id="ff73c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ff73c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff73c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ff73c-108">Attributes</span></span>

|<span data-ttu-id="ff73c-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ff73c-109">**Attribute**</span></span>|<span data-ttu-id="ff73c-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff73c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ff73c-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="ff73c-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="ff73c-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="ff73c-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="ff73c-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="ff73c-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="ff73c-114">-Success</span><span class="sxs-lookup"><span data-stu-id="ff73c-114">-  Success</span></span>  <br/><span data-ttu-id="ff73c-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="ff73c-115">-  Warning</span></span>  <br/><span data-ttu-id="ff73c-116">-Error</span><span class="sxs-lookup"><span data-stu-id="ff73c-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="ff73c-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="ff73c-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="ff73c-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ff73c-118">**Value**</span></span>|<span data-ttu-id="ff73c-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff73c-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ff73c-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="ff73c-120">**Success**</span></span> <br/> |<span data-ttu-id="ff73c-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ff73c-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="ff73c-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="ff73c-122">**Warning**</span></span> <br/> | <span data-ttu-id="ff73c-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ff73c-123">Describes a request that was not processed.</span></span> <span data-ttu-id="ff73c-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ff73c-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="ff73c-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="ff73c-125">The following are examples of sources of warnings:</span></span> <br/><br/><span data-ttu-id="ff73c-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="ff73c-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="ff73c-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="ff73c-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="ff73c-128">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="ff73c-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="ff73c-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="ff73c-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="ff73c-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="ff73c-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="ff73c-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="ff73c-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="ff73c-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="ff73c-132">**Error**</span></span> <br/> | <span data-ttu-id="ff73c-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ff73c-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="ff73c-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="ff73c-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="ff73c-135">-Ungültige Attribute oder Elemente.</span><span class="sxs-lookup"><span data-stu-id="ff73c-135">-  Invalid attributes or elements.</span></span>  <br/><span data-ttu-id="ff73c-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="ff73c-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="ff73c-137">-Ein unbekanntes Tag.</span><span class="sxs-lookup"><span data-stu-id="ff73c-137">-  An unknown tag.</span></span>  <br/><span data-ttu-id="ff73c-138">-Ein Attribut oder Element, das im Kontext nicht gültig ist.</span><span class="sxs-lookup"><span data-stu-id="ff73c-138">-  An attribute or element that is not valid in the context.</span></span>  <br/><span data-ttu-id="ff73c-139">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client.</span><span class="sxs-lookup"><span data-stu-id="ff73c-139">-  An unauthorized access attempt by any client.</span></span>  <br/><span data-ttu-id="ff73c-140">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf.</span><span class="sxs-lookup"><span data-stu-id="ff73c-140">-  A server-side failure in response to a valid client-side call.</span></span>  <br/><br/>  <span data-ttu-id="ff73c-141">Informationen zum Fehler finden Sie in den Themen [Response Code](responsecode.md) und [MessageText](messagetext.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="ff73c-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) element topics.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ff73c-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ff73c-142">Child elements</span></span>

|<span data-ttu-id="ff73c-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="ff73c-143">**Element**</span></span>|<span data-ttu-id="ff73c-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff73c-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff73c-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="ff73c-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ff73c-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="ff73c-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ff73c-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ff73c-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ff73c-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ff73c-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="ff73c-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ff73c-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ff73c-150">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="ff73c-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="ff73c-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="ff73c-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="ff73c-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="ff73c-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ff73c-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="ff73c-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="ff73c-154">Anrufer</span><span class="sxs-lookup"><span data-stu-id="ff73c-154">PhoneCallId</span></span>](phonecallid.md) <br/> |<span data-ttu-id="ff73c-155">Gibt die Telefonanruf-ID an.</span><span class="sxs-lookup"><span data-stu-id="ff73c-155">Specifies the telephone call identifier.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ff73c-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ff73c-156">Parent elements</span></span>

<span data-ttu-id="ff73c-157">Keine.</span><span class="sxs-lookup"><span data-stu-id="ff73c-157">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ff73c-158">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff73c-158">Remarks</span></span>

<span data-ttu-id="ff73c-159">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ff73c-159">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ff73c-160">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ff73c-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff73c-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="ff73c-161">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ff73c-162">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ff73c-162">Schema Name</span></span>  <br/> |<span data-ttu-id="ff73c-163">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ff73c-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ff73c-164">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ff73c-164">Validation File</span></span>  <br/> |<span data-ttu-id="ff73c-165">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ff73c-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ff73c-166">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ff73c-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="ff73c-167">False</span><span class="sxs-lookup"><span data-stu-id="ff73c-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff73c-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff73c-168">See also</span></span>

- [<span data-ttu-id="ff73c-169">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ff73c-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

