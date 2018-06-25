---
title: ResolveNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: c85207e1-1315-443b-94ec-2b58f405076b
description: Das ResolveNames-Element definiert eine Anforderung zum Auflösen von Names nicht eindeutig.
ms.openlocfilehash: e97b6e78d99cf8ffa3d680907916882d40963f59
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831172"
---
# <a name="resolvenames"></a><span data-ttu-id="5e76f-103">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="5e76f-103">ResolveNames</span></span>

<span data-ttu-id="5e76f-104">Das **ResolveNames** -Element definiert eine Anforderung zum Auflösen von Names nicht eindeutig.</span><span class="sxs-lookup"><span data-stu-id="5e76f-104">The **ResolveNames** element defines a request to resolve ambiguous names.</span></span> 
  
```XML
<ResolveNames ReturnFullContactData="" SearchScope="" ContactDataShape="">
   <ParentFolderIds/>
   <UnresolvedEntry/>
</ResolveNames>
```

 <span data-ttu-id="5e76f-105">**ResolveNamesType**</span><span class="sxs-lookup"><span data-stu-id="5e76f-105">**ResolveNamesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5e76f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5e76f-106">Attributes and elements</span></span>

<span data-ttu-id="5e76f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5e76f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5e76f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5e76f-108">Attributes</span></span>

|<span data-ttu-id="5e76f-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5e76f-109">**Attribute**</span></span>|<span data-ttu-id="5e76f-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5e76f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5e76f-111">**ReturnFullContactData**</span><span class="sxs-lookup"><span data-stu-id="5e76f-111">**ReturnFullContactData**</span></span> <br/> |<span data-ttu-id="5e76f-112">Beschreibt, ob der vollständige Kontaktdetails für Öffentliche Kontakte für einen aufgelösten Namen in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5e76f-112">Describes whether the full contact details for public contacts for a resolved name are returned in the response.</span></span> <span data-ttu-id="5e76f-113">Dieses Attribut ist für Öffentliche Kontakte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5e76f-113">This attribute is required for public contacts.</span></span> <span data-ttu-id="5e76f-114">Dieser Wert wirkt sich nicht private Kontakte und private Verteilerlisten, für die [ItemId](itemid.md) immer zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5e76f-114">This value does not affect private contacts and private distribution lists, for which [ItemId](itemid.md) is always returned.</span></span>  <br/> |
|<span data-ttu-id="5e76f-115">**SearchScope**</span><span class="sxs-lookup"><span data-stu-id="5e76f-115">**SearchScope**</span></span> <br/> |<span data-ttu-id="5e76f-116">Gibt die Reihenfolge und ResolveNames Suchbereich.</span><span class="sxs-lookup"><span data-stu-id="5e76f-116">Identifies the order and scope for a ResolveNames search.</span></span>  <br/> |
|<span data-ttu-id="5e76f-117">ContactDataShape</span><span class="sxs-lookup"><span data-stu-id="5e76f-117">ContactDataShape</span></span>  <br/> |<span data-ttu-id="5e76f-118">Identifiziert den Eigenschaftensatz für Kontakte zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5e76f-118">Identifies the property set returned for contacts.</span></span> <span data-ttu-id="5e76f-119">Dieses Attribut wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5e76f-119">This attribute was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>  <br/> |
   
#### <a name="returnfullcontactdata-attribute-values"></a><span data-ttu-id="5e76f-120">Attributwerte ReturnFullContactData</span><span class="sxs-lookup"><span data-stu-id="5e76f-120">ReturnFullContactData attribute values</span></span>

|<span data-ttu-id="5e76f-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5e76f-121">**Value**</span></span>|<span data-ttu-id="5e76f-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5e76f-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5e76f-123">True</span><span class="sxs-lookup"><span data-stu-id="5e76f-123">True</span></span>  <br/> |<span data-ttu-id="5e76f-124">Vollständige Kontaktdetails für Öffentliche Kontakte werden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5e76f-124">Full contact details for public contacts are returned.</span></span>  <br/> |
|<span data-ttu-id="5e76f-125">False</span><span class="sxs-lookup"><span data-stu-id="5e76f-125">False</span></span>  <br/> |<span data-ttu-id="5e76f-126">Vollständige Kontaktdetails für Öffentliche Kontakte werden nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5e76f-126">Full contact details for public contacts are not returned.</span></span>  <br/> |
   
#### <a name="searchscope-attribute-values"></a><span data-ttu-id="5e76f-127">SearchScope-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="5e76f-127">SearchScope attribute values</span></span>

|<span data-ttu-id="5e76f-128">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5e76f-128">**Value**</span></span>|<span data-ttu-id="5e76f-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5e76f-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5e76f-130">ActiveDirectory-Umgebung</span><span class="sxs-lookup"><span data-stu-id="5e76f-130">ActiveDirectory</span></span>  <br/> |<span data-ttu-id="5e76f-131">Nur der Active Directory-Verzeichnisdienst wird durchsucht.</span><span class="sxs-lookup"><span data-stu-id="5e76f-131">Only the Active Directory directory service is searched.</span></span>  <br/> |
|<span data-ttu-id="5e76f-132">ActiveDirectoryContacts</span><span class="sxs-lookup"><span data-stu-id="5e76f-132">ActiveDirectoryContacts</span></span>  <br/> |<span data-ttu-id="5e76f-133">Active Directory wird zuerst durchsucht, und klicken Sie dann die Kontakten in der [ParentFolderIds](parentfolderids.md) -Eigenschaft angegebenen Ordnern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="5e76f-133">Active Directory is searched first, and then the contact folders that are specified in the [ParentFolderIds](parentfolderids.md) property are searched.</span></span>  <br/> |
|<span data-ttu-id="5e76f-134">Kontakte</span><span class="sxs-lookup"><span data-stu-id="5e76f-134">Contacts</span></span>  <br/> |<span data-ttu-id="5e76f-135">Es werden nur der Ordner für Kontakte, die von der [ParentFolderIds](parentfolderids.md) -Eigenschaft identifiziert werden durchsucht.</span><span class="sxs-lookup"><span data-stu-id="5e76f-135">Only the contact folders that are identified by the [ParentFolderIds](parentfolderids.md) property are searched.</span></span>  <br/> |
|<span data-ttu-id="5e76f-136">ContactsActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="5e76f-136">ContactsActiveDirectory</span></span>  <br/> |<span data-ttu-id="5e76f-137">Ordner, die von der [ParentFolderIds](parentfolderids.md) -Eigenschaft identifiziert werden für Kontakte werden zuerst durchsucht, und klicken Sie dann auf Active Directory durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="5e76f-137">Contact folders that are identified by the [ParentFolderIds](parentfolderids.md) property are searched first and then Active Directory is searched.</span></span>  <br/> |
   
#### <a name="contactdatashape-attribute-values"></a><span data-ttu-id="5e76f-138">Attributwerte ContactDataShape</span><span class="sxs-lookup"><span data-stu-id="5e76f-138">ContactDataShape attribute values</span></span>

|<span data-ttu-id="5e76f-139">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5e76f-139">**Value**</span></span>|<span data-ttu-id="5e76f-140">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5e76f-140">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5e76f-141">IdOnly</span><span class="sxs-lookup"><span data-stu-id="5e76f-141">IdOnly</span></span>  <br/> |<span data-ttu-id="5e76f-142">Die Kontaktelement Identifier-Eigenschaft wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5e76f-142">The contact item identifier property is returned.</span></span>  <br/> |
|<span data-ttu-id="5e76f-143">Standard</span><span class="sxs-lookup"><span data-stu-id="5e76f-143">Default</span></span>  <br/> |<span data-ttu-id="5e76f-144">Die Standardgruppe von Eigenschaften für Kontaktelemente wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5e76f-144">The Default set of contact item properties is returned.</span></span> <span data-ttu-id="5e76f-145">Weitere Informationen finden Sie unter [Antwort Shapes in der Exchange-Webdienste](http://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5e76f-145">For more information, see [Response shapes in EWS](http://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).</span></span>  <br/> |
|<span data-ttu-id="5e76f-146">AllProperties</span><span class="sxs-lookup"><span data-stu-id="5e76f-146">AllProperties</span></span>  <br/> |<span data-ttu-id="5e76f-147">Der AllProperties Satz von Eigenschaften für Kontaktelemente werden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5e76f-147">The AllProperties set of contact item properties are returned.</span></span> <span data-ttu-id="5e76f-148">Weitere Informationen finden Sie unter [Antwort Shapes in der Exchange-Webdienste](http://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5e76f-148">For more information, see [Response shapes in EWS](http://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5e76f-149">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5e76f-149">Child elements</span></span>

|<span data-ttu-id="5e76f-150">**Element**</span><span class="sxs-lookup"><span data-stu-id="5e76f-150">**Element**</span></span>|<span data-ttu-id="5e76f-151">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5e76f-151">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5e76f-152">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="5e76f-152">ParentFolderIds</span></span>](parentfolderids.md) <br/> |<span data-ttu-id="5e76f-153">Enthält ein Array mit den Kontaktordner-IDs, die durchsucht werden würde, wenn das **SearchScope** -Attribut auf ActiveDirectoryContacts, Kontakte oder ContactsActiveDirectory festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5e76f-153">Contains an array of contact folder identifiers that would be searched if the **SearchScope** attribute is set to ActiveDirectoryContacts, Contacts, or ContactsActiveDirectory.</span></span> <span data-ttu-id="5e76f-154">Das Array ParentFolderIds kann nur einen einzigen Kontaktordner Bezeichner enthalten.</span><span class="sxs-lookup"><span data-stu-id="5e76f-154">The ParentFolderIds array can only contain a single contact folder identifier.</span></span> <span data-ttu-id="5e76f-155">Wenn das **ParentFolderIds** -Element nicht vorhanden ist, wird der Standardordner Kontakte durchsucht.</span><span class="sxs-lookup"><span data-stu-id="5e76f-155">If the **ParentFolderIds** element is not present, the default Contacts folder is searched.</span></span>  <br/> <span data-ttu-id="5e76f-156">Die Ordner-ID kann für Stellvertretungszugriff verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e76f-156">The folder identifier can be used for delegate access.</span></span>  <br/> <span data-ttu-id="5e76f-157">Active Directory durchsucht werden mithilfe von Zugriffssteuerungslisten (ACLs) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e76f-157">Active Directory searches are performed by using access control lists (ACLs).</span></span> <span data-ttu-id="5e76f-158">Einige Benutzer haben möglicherweise nicht die Rechte für einige Active Directory-Objekte finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="5e76f-158">Some users might not have the rights to see some Active Directory objects.</span></span>  <br/> <span data-ttu-id="5e76f-159">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="5e76f-159">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="5e76f-160">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="5e76f-160">UnresolvedEntry</span></span>](unresolvedentry.md) <br/> |<span data-ttu-id="5e76f-161">Enthält den Namen des einen Kontakt oder Verteilerliste aus, zu beheben.</span><span class="sxs-lookup"><span data-stu-id="5e76f-161">Contains the name of a contact or distribution list to resolve.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5e76f-162">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5e76f-162">Parent elements</span></span>

<span data-ttu-id="5e76f-163">Keine.</span><span class="sxs-lookup"><span data-stu-id="5e76f-163">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5e76f-164">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5e76f-164">Remarks</span></span>

<span data-ttu-id="5e76f-165">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="5e76f-165">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5e76f-166">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5e76f-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5e76f-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="5e76f-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5e76f-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5e76f-168">Schema name</span></span>  <br/> |<span data-ttu-id="5e76f-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="5e76f-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5e76f-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5e76f-170">Validation file</span></span>  <br/> |<span data-ttu-id="5e76f-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5e76f-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5e76f-172">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="5e76f-172">Can be empty</span></span>  <br/> |<span data-ttu-id="5e76f-173">False</span><span class="sxs-lookup"><span data-stu-id="5e76f-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5e76f-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e76f-174">See also</span></span>



[<span data-ttu-id="5e76f-175">ResolveNames-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5e76f-175">ResolveNames operation</span></span>](resolvenames-operation.md)
  
[<span data-ttu-id="5e76f-176">ResolveNamesType</span><span class="sxs-lookup"><span data-stu-id="5e76f-176">ResolveNamesType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesType.aspx)
  
[<span data-ttu-id="5e76f-177">ResolveNamesSearchScopeType</span><span class="sxs-lookup"><span data-stu-id="5e76f-177">ResolveNamesSearchScopeType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesSearchScopeType.aspx)


- [<span data-ttu-id="5e76f-178">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5e76f-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="5e76f-179">Verwenden von namensauflösung</span><span class="sxs-lookup"><span data-stu-id="5e76f-179">Using Name Resolution</span></span>](http://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

