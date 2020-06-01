---
title: GetInboxRulesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetInboxRulesResponse
api_type:
- schema
ms.assetid: 6d6c1950-c328-489a-94bf-a250fdbd5cd9
description: Das GetInboxRulesResponse-Element definiert eine Antwort auf eine GetInboxRules-Vorgangsanforderung.
ms.openlocfilehash: 0d67d7eaf6ffbeeb790249190a98f252dbdb9c87
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458285"
---
# <a name="getinboxrulesresponse"></a><span data-ttu-id="c61d8-103">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="c61d8-103">GetInboxRulesResponse</span></span>

<span data-ttu-id="c61d8-104">Das **GetInboxRulesResponse** -Element definiert eine Antwort auf eine [GetInboxRules-Vorgangs](getinboxrules-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c61d8-104">The **GetInboxRulesResponse** element defines a response to a [GetInboxRules operation](getinboxrules-operation.md) request.</span></span> 
  
```XML
<GetInboxRulesResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <OutlookRuleBlobExists/>
   <InboxRules/>
</GetInboxRulesResponse>
```

 <span data-ttu-id="c61d8-105">**GetInboxRulesResponseType**</span><span class="sxs-lookup"><span data-stu-id="c61d8-105">**GetInboxRulesResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c61d8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c61d8-106">Attributes and elements</span></span>

<span data-ttu-id="c61d8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c61d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c61d8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c61d8-108">Attributes</span></span>

|<span data-ttu-id="c61d8-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c61d8-109">**Attribute**</span></span>|<span data-ttu-id="c61d8-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c61d8-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c61d8-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="c61d8-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="c61d8-112">Beschreibt den Status einer [GetInboxRules-Vorgangs](getinboxrules-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="c61d8-112">Describes the status of a [GetInboxRules operation](getinboxrules-operation.md) response.</span></span> <br/><br/><span data-ttu-id="c61d8-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="c61d8-113">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="c61d8-114">-Success</span><span class="sxs-lookup"><span data-stu-id="c61d8-114">-  Success</span></span>  <br/><span data-ttu-id="c61d8-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="c61d8-115">-  Warning</span></span>  <br/><span data-ttu-id="c61d8-116">-Error</span><span class="sxs-lookup"><span data-stu-id="c61d8-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="c61d8-117">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="c61d8-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="c61d8-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c61d8-118">**Value**</span></span>|<span data-ttu-id="c61d8-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c61d8-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c61d8-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="c61d8-120">**Success**</span></span> <br/> |<span data-ttu-id="c61d8-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="c61d8-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="c61d8-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="c61d8-122">**Warning**</span></span> <br/> | <span data-ttu-id="c61d8-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="c61d8-123">Describes a request that was not processed.</span></span> <span data-ttu-id="c61d8-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="c61d8-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="c61d8-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="c61d8-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="c61d8-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="c61d8-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="c61d8-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="c61d8-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="c61d8-128">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="c61d8-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="c61d8-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="c61d8-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="c61d8-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="c61d8-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="c61d8-131">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="c61d8-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="c61d8-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="c61d8-132">**Error**</span></span> <br/> | <span data-ttu-id="c61d8-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c61d8-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="c61d8-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="c61d8-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="c61d8-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="c61d8-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="c61d8-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="c61d8-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="c61d8-137">-Ein unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="c61d8-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="c61d8-138">-Ein Attribut oder Element, das im Kontext ungültig ist</span><span class="sxs-lookup"><span data-stu-id="c61d8-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="c61d8-139">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client</span><span class="sxs-lookup"><span data-stu-id="c61d8-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="c61d8-140">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="c61d8-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="c61d8-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="c61d8-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c61d8-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c61d8-142">Child elements</span></span>

|<span data-ttu-id="c61d8-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="c61d8-143">**Element**</span></span>|<span data-ttu-id="c61d8-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c61d8-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c61d8-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="c61d8-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="c61d8-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="c61d8-146">Provides text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="c61d8-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c61d8-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="c61d8-148">Stellt Statusinformationen zur Anforderung bereit.</span><span class="sxs-lookup"><span data-stu-id="c61d8-148">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="c61d8-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c61d8-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="c61d8-150">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="c61d8-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="c61d8-151">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="c61d8-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="c61d8-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="c61d8-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="c61d8-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="c61d8-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="c61d8-154">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="c61d8-154">OutlookRuleBlobExists</span></span>](outlookruleblobexists.md) <br/> |<span data-ttu-id="c61d8-155">Gibt an, ob ein Microsoft Outlook-Regel-BLOB im Postfach des Benutzers vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c61d8-155">Indicates whether a Microsoft Outlook rule blob exists in the user's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c61d8-156">InboxRules</span><span class="sxs-lookup"><span data-stu-id="c61d8-156">InboxRules</span></span>](inboxrules.md) <br/> |<span data-ttu-id="c61d8-157">Stellt ein Array der Regeln im Postfach des Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="c61d8-157">Represents an array of the rules in the user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c61d8-158">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c61d8-158">Parent elements</span></span>

<span data-ttu-id="c61d8-159">Keine.</span><span class="sxs-lookup"><span data-stu-id="c61d8-159">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="c61d8-160">Textwert</span><span class="sxs-lookup"><span data-stu-id="c61d8-160">Text value</span></span>

<span data-ttu-id="c61d8-161">Keine.</span><span class="sxs-lookup"><span data-stu-id="c61d8-161">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c61d8-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c61d8-162">Remarks</span></span>

<span data-ttu-id="c61d8-163">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c61d8-163">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c61d8-164">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c61d8-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c61d8-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="c61d8-165">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c61d8-166">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c61d8-166">Schema name</span></span>  <br/> |<span data-ttu-id="c61d8-167">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c61d8-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c61d8-168">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c61d8-168">Validation file</span></span>  <br/> |<span data-ttu-id="c61d8-169">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c61d8-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c61d8-170">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c61d8-170">Can be empty</span></span>  <br/> |<span data-ttu-id="c61d8-171">False</span><span class="sxs-lookup"><span data-stu-id="c61d8-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c61d8-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c61d8-172">See also</span></span>

- [<span data-ttu-id="c61d8-173">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="c61d8-173">GetInboxRules</span></span>](getinboxrules.md)
- [<span data-ttu-id="c61d8-174">GetInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c61d8-174">GetInboxRules operation</span></span>](getinboxrules-operation.md)

