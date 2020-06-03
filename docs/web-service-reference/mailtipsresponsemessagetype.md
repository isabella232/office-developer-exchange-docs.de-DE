---
title: MailTipsResponseMessageType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsResponseMessageType
api_type:
- schema
ms.assetid: 532cb9d9-1232-4e88-80aa-4cf163eb05da
description: Das MailTipsResponseMessageType-Element stellt Einstellungen für e-Mail-Tipps dar.
ms.openlocfilehash: 5244f26ef927a817a9087c299fd1124acb828aa0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44454036"
---
# <a name="mailtipsresponsemessagetype"></a><span data-ttu-id="03f9c-103">MailTipsResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="03f9c-103">MailTipsResponseMessageType</span></span>

<span data-ttu-id="03f9c-104">Das **MailTipsResponseMessageType** -Element stellt Einstellungen für e-Mail-Tipps dar.</span><span class="sxs-lookup"><span data-stu-id="03f9c-104">The **MailTipsResponseMessageType** element represents mail tips settings.</span></span> 
  
```XML
<MailTipsResponseMessageType ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MailTips/>
</MailTipsResponseMessageType>
```

 <span data-ttu-id="03f9c-105">**MailTipsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="03f9c-105">**MailTipsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="03f9c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="03f9c-106">Attributes and elements</span></span>

<span data-ttu-id="03f9c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="03f9c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="03f9c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="03f9c-108">Attributes</span></span>

|<span data-ttu-id="03f9c-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="03f9c-109">**Attribute**</span></span>|<span data-ttu-id="03f9c-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="03f9c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="03f9c-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="03f9c-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="03f9c-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="03f9c-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="03f9c-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="03f9c-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="03f9c-114">-Success</span><span class="sxs-lookup"><span data-stu-id="03f9c-114">-  Success</span></span>  <br/><span data-ttu-id="03f9c-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="03f9c-115">-  Warning</span></span>  <br/><span data-ttu-id="03f9c-116">-Error</span><span class="sxs-lookup"><span data-stu-id="03f9c-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="03f9c-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="03f9c-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="03f9c-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="03f9c-118">**Value**</span></span>|<span data-ttu-id="03f9c-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="03f9c-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="03f9c-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="03f9c-120">**Success**</span></span> <br/> |<span data-ttu-id="03f9c-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="03f9c-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="03f9c-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="03f9c-122">**Warning**</span></span> <br/> | <span data-ttu-id="03f9c-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="03f9c-123">Describes a request that was not processed.</span></span> <span data-ttu-id="03f9c-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="03f9c-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="03f9c-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="03f9c-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="03f9c-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="03f9c-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="03f9c-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="03f9c-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="03f9c-128">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="03f9c-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="03f9c-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="03f9c-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="03f9c-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="03f9c-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="03f9c-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="03f9c-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="03f9c-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="03f9c-132">**Error**</span></span> <br/> | <span data-ttu-id="03f9c-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="03f9c-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="03f9c-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="03f9c-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="03f9c-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="03f9c-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="03f9c-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="03f9c-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="03f9c-137">-Ein unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="03f9c-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="03f9c-138">-Ein Attribut oder Element, das im Kontext ungültig ist</span><span class="sxs-lookup"><span data-stu-id="03f9c-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="03f9c-139">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client</span><span class="sxs-lookup"><span data-stu-id="03f9c-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="03f9c-140">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="03f9c-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="03f9c-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="03f9c-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="03f9c-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="03f9c-142">Child elements</span></span>

|<span data-ttu-id="03f9c-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="03f9c-143">**Element**</span></span>|<span data-ttu-id="03f9c-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="03f9c-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="03f9c-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="03f9c-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="03f9c-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="03f9c-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="03f9c-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="03f9c-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="03f9c-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="03f9c-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="03f9c-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="03f9c-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="03f9c-150">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="03f9c-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="03f9c-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="03f9c-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="03f9c-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="03f9c-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="03f9c-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="03f9c-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="03f9c-154">E-Mail-Info</span><span class="sxs-lookup"><span data-stu-id="03f9c-154">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="03f9c-155">Stellt Werte für verschiedene Arten von e-Mail-Tipps dar.</span><span class="sxs-lookup"><span data-stu-id="03f9c-155">Represents values for various types of mail tips.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="03f9c-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="03f9c-156">Parent elements</span></span>

|<span data-ttu-id="03f9c-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="03f9c-157">**Element**</span></span>|<span data-ttu-id="03f9c-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="03f9c-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="03f9c-159">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="03f9c-159">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span></span>](responsemessages-arrayofmailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="03f9c-160">Stellt eine Liste der e-Mail-Tipps Antwortnachrichten dar.</span><span class="sxs-lookup"><span data-stu-id="03f9c-160">Represents a list of mail tips response messages.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="03f9c-161">Textwert</span><span class="sxs-lookup"><span data-stu-id="03f9c-161">Text value</span></span>

<span data-ttu-id="03f9c-162">Keine.</span><span class="sxs-lookup"><span data-stu-id="03f9c-162">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="03f9c-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03f9c-163">Remarks</span></span>

<span data-ttu-id="03f9c-164">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="03f9c-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="03f9c-165">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="03f9c-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="03f9c-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="03f9c-166">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="03f9c-167">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="03f9c-167">Schema Name</span></span>  <br/> |<span data-ttu-id="03f9c-168">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="03f9c-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="03f9c-169">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="03f9c-169">Validation File</span></span>  <br/> |<span data-ttu-id="03f9c-170">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="03f9c-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="03f9c-171">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="03f9c-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="03f9c-172">False</span><span class="sxs-lookup"><span data-stu-id="03f9c-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="03f9c-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03f9c-173">See also</span></span>

- [<span data-ttu-id="03f9c-174">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="03f9c-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

