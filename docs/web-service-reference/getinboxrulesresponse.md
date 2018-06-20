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
description: Das GetInboxRulesResponse-Element definiert eine Antwort auf eine GetInboxRules Vorgang an.
ms.openlocfilehash: d84064ab777fe13ded7727381842ddd1ee9d047d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758715"
---
# <a name="getinboxrulesresponse"></a><span data-ttu-id="fe310-103">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="fe310-103">GetInboxRulesResponse</span></span>

<span data-ttu-id="fe310-104">Das **GetInboxRulesResponse** -Element definiert eine Antwort auf eine [GetInboxRules Vorgang](getinboxrules-operation.md) an.</span><span class="sxs-lookup"><span data-stu-id="fe310-104">The **GetInboxRulesResponse** element defines a response to a [GetInboxRules operation](getinboxrules-operation.md) request.</span></span> 
  
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

 <span data-ttu-id="fe310-105">**GetInboxRulesResponseType**</span><span class="sxs-lookup"><span data-stu-id="fe310-105">**GetInboxRulesResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fe310-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fe310-106">Attributes and elements</span></span>

<span data-ttu-id="fe310-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fe310-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fe310-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fe310-108">Attributes</span></span>

|<span data-ttu-id="fe310-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fe310-109">**Attribute**</span></span>|<span data-ttu-id="fe310-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fe310-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe310-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="fe310-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="fe310-112">Beschreibt den Status einer Antwort [GetInboxRules Vorgang](getinboxrules-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="fe310-112">Describes the status of a [GetInboxRules operation](getinboxrules-operation.md) response.</span></span> <br/><br/><span data-ttu-id="fe310-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="fe310-113">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="fe310-114">-Success</span><span class="sxs-lookup"><span data-stu-id="fe310-114">-  Success</span></span>  <br/><span data-ttu-id="fe310-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="fe310-115">-  Warning</span></span>  <br/><span data-ttu-id="fe310-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="fe310-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="fe310-117">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="fe310-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="fe310-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fe310-118">**Value**</span></span>|<span data-ttu-id="fe310-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fe310-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe310-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="fe310-120">**Success**</span></span> <br/> |<span data-ttu-id="fe310-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="fe310-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="fe310-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="fe310-122">**Warning**</span></span> <br/> | <span data-ttu-id="fe310-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="fe310-123">Describes a request that was not processed.</span></span> <span data-ttu-id="fe310-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="fe310-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="fe310-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="fe310-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="fe310-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="fe310-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="fe310-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="fe310-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="fe310-128">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="fe310-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="fe310-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="fe310-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="fe310-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="fe310-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="fe310-131">-Ein Kontingent überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="fe310-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="fe310-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="fe310-132">**Error**</span></span> <br/> | <span data-ttu-id="fe310-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fe310-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="fe310-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="fe310-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="fe310-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="fe310-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="fe310-136">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="fe310-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="fe310-137">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="fe310-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="fe310-138">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="fe310-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="fe310-139">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="fe310-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="fe310-140">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="fe310-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="fe310-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="fe310-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fe310-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fe310-142">Child elements</span></span>

|<span data-ttu-id="fe310-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="fe310-143">**Element**</span></span>|<span data-ttu-id="fe310-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fe310-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe310-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="fe310-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="fe310-146">Beschreibung des Status der Antwort enthält.</span><span class="sxs-lookup"><span data-stu-id="fe310-146">Provides text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="fe310-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="fe310-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="fe310-148">Enthält Statusinformationen über die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="fe310-148">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="fe310-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="fe310-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="fe310-150">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="fe310-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="fe310-151">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="fe310-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="fe310-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="fe310-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="fe310-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="fe310-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="fe310-154">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="fe310-154">OutlookRuleBlobExists</span></span>](outlookruleblobexists.md) <br/> |<span data-ttu-id="fe310-155">Gibt an, ob ein Microsoft Outlook-Regel Blob im Postfach des Benutzers vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="fe310-155">Indicates whether a Microsoft Outlook rule blob exists in the user's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fe310-156">InboxRules</span><span class="sxs-lookup"><span data-stu-id="fe310-156">InboxRules</span></span>](inboxrules.md) <br/> |<span data-ttu-id="fe310-157">Stellt ein Array von Regeln in das Postfach des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="fe310-157">Represents an array of the rules in the user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fe310-158">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fe310-158">Parent elements</span></span>

<span data-ttu-id="fe310-159">Keine.</span><span class="sxs-lookup"><span data-stu-id="fe310-159">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="fe310-160">Textwert</span><span class="sxs-lookup"><span data-stu-id="fe310-160">Text value</span></span>

<span data-ttu-id="fe310-161">Keine.</span><span class="sxs-lookup"><span data-stu-id="fe310-161">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe310-162">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fe310-162">Remarks</span></span>

<span data-ttu-id="fe310-163">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fe310-163">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fe310-164">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="fe310-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe310-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="fe310-165">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fe310-166">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fe310-166">Schema name</span></span>  <br/> |<span data-ttu-id="fe310-167">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="fe310-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fe310-168">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fe310-168">Validation file</span></span>  <br/> |<span data-ttu-id="fe310-169">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fe310-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fe310-170">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="fe310-170">Can be empty</span></span>  <br/> |<span data-ttu-id="fe310-171">False</span><span class="sxs-lookup"><span data-stu-id="fe310-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fe310-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe310-172">See also</span></span>

- [<span data-ttu-id="fe310-173">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="fe310-173">GetInboxRules</span></span>](getinboxrules.md)
- [<span data-ttu-id="fe310-174">GetInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="fe310-174">GetInboxRules operation</span></span>](getinboxrules-operation.md)

