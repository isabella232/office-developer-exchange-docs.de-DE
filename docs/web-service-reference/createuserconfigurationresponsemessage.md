---
title: CreateUserConfigurationResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateUserConfigurationResponseMessage
api_type:
- schema
ms.assetid: 9c11427c-74c9-4c6a-a0e7-7d5556670c1e
description: Das CreateUserConfigurationResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen CreateUserConfiguration-Anforderung.
ms.openlocfilehash: 3217734f7451ad397c531cd9ff9ce7d44b13f6ba
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463734"
---
# <a name="createuserconfigurationresponsemessage"></a><span data-ttu-id="b4e27-103">CreateUserConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b4e27-103">CreateUserConfigurationResponseMessage</span></span>

<span data-ttu-id="b4e27-104">Das **CreateUserConfigurationResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen **CreateUserConfiguration** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b4e27-104">The **CreateUserConfigurationResponseMessage** element contains the status and result of a single **CreateUserConfiguration** request.</span></span> 
  
```xml
<CreateUserConfigurationResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</CreateUserConfigurationResponseMessage>
```

<span data-ttu-id="b4e27-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="b4e27-105">**ResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b4e27-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b4e27-106">Attributes and elements</span></span>

<span data-ttu-id="b4e27-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b4e27-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b4e27-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b4e27-108">Attributes</span></span>

|<span data-ttu-id="b4e27-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b4e27-109">**Attribute**</span></span>|<span data-ttu-id="b4e27-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b4e27-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b4e27-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="b4e27-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="b4e27-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="b4e27-112">Describes the status of the response.</span></span><br/><br/><span data-ttu-id="b4e27-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="b4e27-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="b4e27-114">-Success</span><span class="sxs-lookup"><span data-stu-id="b4e27-114">-  Success</span></span>  <br/><span data-ttu-id="b4e27-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="b4e27-115">-  Warning</span></span>  <br/><span data-ttu-id="b4e27-116">-Error</span><span class="sxs-lookup"><span data-stu-id="b4e27-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="b4e27-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="b4e27-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="b4e27-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b4e27-118">**Value**</span></span>|<span data-ttu-id="b4e27-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b4e27-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b4e27-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="b4e27-120">**Success**</span></span> <br/> |<span data-ttu-id="b4e27-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="b4e27-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="b4e27-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="b4e27-122">**Warning**</span></span> <br/> | <span data-ttu-id="b4e27-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="b4e27-123">Describes a request that was not processed.</span></span> <span data-ttu-id="b4e27-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="b4e27-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="b4e27-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="b4e27-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="b4e27-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="b4e27-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="b4e27-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="b4e27-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="b4e27-128">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="b4e27-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="b4e27-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="b4e27-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="b4e27-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="b4e27-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="b4e27-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="b4e27-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="b4e27-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="b4e27-132">**Error**</span></span> <br/> | <span data-ttu-id="b4e27-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b4e27-133">Describes a request that cannot be fulfilled.</span></span><br/><br/> <span data-ttu-id="b4e27-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="b4e27-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="b4e27-135">-Ungültige Attribute oder Elemente.</span><span class="sxs-lookup"><span data-stu-id="b4e27-135">-  Invalid attributes or elements.</span></span>  <br/><span data-ttu-id="b4e27-136">-Attribute oder Elemente außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="b4e27-136">-  Attributes or elements that are out of range.</span></span>  <br/><span data-ttu-id="b4e27-137">-Ein unbekanntes Tag.</span><span class="sxs-lookup"><span data-stu-id="b4e27-137">-  An unknown tag.</span></span>  <br/><span data-ttu-id="b4e27-138">-Das Attribut oder Element ist im Kontext ungültig.</span><span class="sxs-lookup"><span data-stu-id="b4e27-138">-  The attribute or element is not valid in the context.</span></span>  <br/><span data-ttu-id="b4e27-139">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client.</span><span class="sxs-lookup"><span data-stu-id="b4e27-139">-  An unauthorized access attempt by any client.</span></span>  <br/><span data-ttu-id="b4e27-140">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf.</span><span class="sxs-lookup"><span data-stu-id="b4e27-140">-  A server-side failure in response to a valid client-side call.</span></span><br/><br/>  <span data-ttu-id="b4e27-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="b4e27-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b4e27-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b4e27-142">Child elements</span></span>

|<span data-ttu-id="b4e27-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="b4e27-143">**Element**</span></span>|<span data-ttu-id="b4e27-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b4e27-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b4e27-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="b4e27-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="b4e27-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="b4e27-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="b4e27-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b4e27-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="b4e27-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b4e27-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="b4e27-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b4e27-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="b4e27-150">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="b4e27-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="b4e27-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="b4e27-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="b4e27-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="b4e27-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="b4e27-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="b4e27-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b4e27-154">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b4e27-154">Parent elements</span></span>

|<span data-ttu-id="b4e27-155">**Element**</span><span class="sxs-lookup"><span data-stu-id="b4e27-155">**Element**</span></span>|<span data-ttu-id="b4e27-156">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b4e27-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b4e27-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b4e27-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="b4e27-158">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b4e27-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b4e27-159">Textwert</span><span class="sxs-lookup"><span data-stu-id="b4e27-159">Text value</span></span>

<span data-ttu-id="b4e27-160">Keine.</span><span class="sxs-lookup"><span data-stu-id="b4e27-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b4e27-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4e27-161">Remarks</span></span>

<span data-ttu-id="b4e27-162">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b4e27-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b4e27-163">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b4e27-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4e27-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="b4e27-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b4e27-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b4e27-165">Schema Name</span></span>  <br/> |<span data-ttu-id="b4e27-166">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b4e27-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b4e27-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b4e27-167">Validation File</span></span>  <br/> |<span data-ttu-id="b4e27-168">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b4e27-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b4e27-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b4e27-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="b4e27-170">False</span><span class="sxs-lookup"><span data-stu-id="b4e27-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b4e27-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4e27-171">See also</span></span>

- [<span data-ttu-id="b4e27-172">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b4e27-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

