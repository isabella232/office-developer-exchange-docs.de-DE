---
title: UpdateInboxRulesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateInboxRulesResponse
api_type:
- schema
ms.assetid: 0947b6aa-0d95-421b-aebb-d03021ecc110
description: Das UpdateInboxRulesResponse-Element definiert eine Antwort auf eine UpdateInboxRules-Anforderung.
ms.openlocfilehash: 1216a32bdaf2dd5211021add0728844eb62089ed
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455905"
---
# <a name="updateinboxrulesresponse"></a><span data-ttu-id="cdb3e-103">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="cdb3e-103">UpdateInboxRulesResponse</span></span>

<span data-ttu-id="cdb3e-104">Das **UpdateInboxRulesResponse** -Element definiert eine Antwort auf eine UpdateInboxRules-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-104">The **UpdateInboxRulesResponse** element defines a response to an UpdateInboxRules request.</span></span> 
  
```XML
<UpdateInboxRulesResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RuleOperationErrors/>
</UpdateInboxRulesResponse>
```

 <span data-ttu-id="cdb3e-105">**UpdateInboxRulesResponseType**</span><span class="sxs-lookup"><span data-stu-id="cdb3e-105">**UpdateInboxRulesResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cdb3e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cdb3e-106">Attributes and elements</span></span>

<span data-ttu-id="cdb3e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cdb3e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cdb3e-108">Attributes</span></span>

|<span data-ttu-id="cdb3e-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="cdb3e-109">**Attribute**</span></span>|<span data-ttu-id="cdb3e-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cdb3e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cdb3e-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="cdb3e-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="cdb3e-112">Beschreibt den Status einer [Kündigungs Vorgangs](unsubscribe-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-112">Describes the status of an [Unsubscribe operation](unsubscribe-operation.md) response.</span></span><br/><br/> <span data-ttu-id="cdb3e-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="cdb3e-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="cdb3e-114">-Success</span><span class="sxs-lookup"><span data-stu-id="cdb3e-114">-  Success</span></span>  <br/><span data-ttu-id="cdb3e-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="cdb3e-115">-  Warning</span></span>  <br/><span data-ttu-id="cdb3e-116">-Error</span><span class="sxs-lookup"><span data-stu-id="cdb3e-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="cdb3e-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="cdb3e-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="cdb3e-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="cdb3e-118">**Value**</span></span>|<span data-ttu-id="cdb3e-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cdb3e-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cdb3e-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="cdb3e-120">**Success**</span></span> <br/> |<span data-ttu-id="cdb3e-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="cdb3e-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="cdb3e-122">**Warning**</span></span> <br/> | <span data-ttu-id="cdb3e-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-123">Describes a request that was not processed.</span></span> <span data-ttu-id="cdb3e-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="cdb3e-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="cdb3e-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="cdb3e-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="cdb3e-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="cdb3e-128">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="cdb3e-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="cdb3e-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="cdb3e-131">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="cdb3e-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="cdb3e-132">**Error**</span></span> <br/> | <span data-ttu-id="cdb3e-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="cdb3e-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="cdb3e-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="cdb3e-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="cdb3e-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="cdb3e-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="cdb3e-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="cdb3e-137">-Ein unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="cdb3e-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="cdb3e-138">-Ein Attribut oder Element, das im Kontext ungültig ist</span><span class="sxs-lookup"><span data-stu-id="cdb3e-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="cdb3e-139">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client</span><span class="sxs-lookup"><span data-stu-id="cdb3e-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="cdb3e-140">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="cdb3e-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="cdb3e-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="cdb3e-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cdb3e-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cdb3e-142">Child elements</span></span>

|<span data-ttu-id="cdb3e-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="cdb3e-143">**Element**</span></span>|<span data-ttu-id="cdb3e-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cdb3e-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cdb3e-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="cdb3e-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="cdb3e-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="cdb3e-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cdb3e-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="cdb3e-148">Stellt Statusinformationen zur Anforderung bereit.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-148">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="cdb3e-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="cdb3e-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="cdb3e-150">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="cdb3e-151">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="cdb3e-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="cdb3e-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="cdb3e-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="cdb3e-154">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="cdb3e-154">RuleOperationErrors</span></span>](ruleoperationerrors.md) <br/> |<span data-ttu-id="cdb3e-155">Stellt ein Array von Regel Validierungsfehlern für jedes Regel Feld dar, das einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-155">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cdb3e-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cdb3e-156">Parent elements</span></span>

<span data-ttu-id="cdb3e-157">Keine.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-157">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="cdb3e-158">Textwert</span><span class="sxs-lookup"><span data-stu-id="cdb3e-158">Text value</span></span>

<span data-ttu-id="cdb3e-159">Keine.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-159">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cdb3e-160">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdb3e-160">Remarks</span></span>

<span data-ttu-id="cdb3e-161">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-161">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cdb3e-162">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="cdb3e-162">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cdb3e-163">Namespace</span><span class="sxs-lookup"><span data-stu-id="cdb3e-163">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cdb3e-164">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cdb3e-164">Schema name</span></span>  <br/> |<span data-ttu-id="cdb3e-165">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="cdb3e-165">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cdb3e-166">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cdb3e-166">Validation file</span></span>  <br/> |<span data-ttu-id="cdb3e-167">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cdb3e-167">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cdb3e-168">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="cdb3e-168">Can be empty</span></span>  <br/> |<span data-ttu-id="cdb3e-169">False</span><span class="sxs-lookup"><span data-stu-id="cdb3e-169">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cdb3e-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdb3e-170">See also</span></span>

- [<span data-ttu-id="cdb3e-171">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="cdb3e-171">UpdateInboxRules</span></span>](updateinboxrules.md)
- [<span data-ttu-id="cdb3e-172">UpdateInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cdb3e-172">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)
- [<span data-ttu-id="cdb3e-173">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cdb3e-173">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

