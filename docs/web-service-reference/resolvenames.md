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
description: Das ResolveNames-Element definiert eine Anforderung zum Auflösen eindeutiger Namen.
ms.openlocfilehash: 9c36a5f84451f91e90a8e7148cf384b5cacd7f29
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467949"
---
# <a name="resolvenames"></a><span data-ttu-id="2f43e-103">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="2f43e-103">ResolveNames</span></span>

<span data-ttu-id="2f43e-104">Das **ResolveNames** -Element definiert eine Anforderung zum Auflösen eindeutiger Namen.</span><span class="sxs-lookup"><span data-stu-id="2f43e-104">The **ResolveNames** element defines a request to resolve ambiguous names.</span></span> 
  
```XML
<ResolveNames ReturnFullContactData="" SearchScope="" ContactDataShape="">
   <ParentFolderIds/>
   <UnresolvedEntry/>
</ResolveNames>
```

 <span data-ttu-id="2f43e-105">**ResolveNamesType**</span><span class="sxs-lookup"><span data-stu-id="2f43e-105">**ResolveNamesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2f43e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2f43e-106">Attributes and elements</span></span>

<span data-ttu-id="2f43e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2f43e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f43e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2f43e-108">Attributes</span></span>

|<span data-ttu-id="2f43e-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2f43e-109">**Attribute**</span></span>|<span data-ttu-id="2f43e-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f43e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2f43e-111">**ReturnFullContactData**</span><span class="sxs-lookup"><span data-stu-id="2f43e-111">**ReturnFullContactData**</span></span> <br/> |<span data-ttu-id="2f43e-112">Beschreibt, ob die vollständigen Kontaktdetails für öffentliche Kontakte für einen aufgelösten Namen in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2f43e-112">Describes whether the full contact details for public contacts for a resolved name are returned in the response.</span></span> <span data-ttu-id="2f43e-113">Dieses Attribut ist für öffentliche Kontakte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2f43e-113">This attribute is required for public contacts.</span></span> <span data-ttu-id="2f43e-114">Dieser Wert wirkt sich nicht auf private Kontakte und private Verteilerlisten aus, für die [ItemID](itemid.md) immer zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2f43e-114">This value does not affect private contacts and private distribution lists, for which [ItemId](itemid.md) is always returned.</span></span>  <br/> |
|<span data-ttu-id="2f43e-115">**SearchScope**</span><span class="sxs-lookup"><span data-stu-id="2f43e-115">**SearchScope**</span></span> <br/> |<span data-ttu-id="2f43e-116">Gibt die Reihenfolge und den Bereich für eine ResolveNames-Suche an.</span><span class="sxs-lookup"><span data-stu-id="2f43e-116">Identifies the order and scope for a ResolveNames search.</span></span>  <br/> |
|<span data-ttu-id="2f43e-117">ContactDataShape</span><span class="sxs-lookup"><span data-stu-id="2f43e-117">ContactDataShape</span></span>  <br/> |<span data-ttu-id="2f43e-118">Gibt den Eigenschaftensatz an, der für Kontakte zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2f43e-118">Identifies the property set returned for contacts.</span></span> <span data-ttu-id="2f43e-119">Dieses Attribut wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2f43e-119">This attribute was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>  <br/> |
   
#### <a name="returnfullcontactdata-attribute-values"></a><span data-ttu-id="2f43e-120">ReturnFullContactData-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="2f43e-120">ReturnFullContactData attribute values</span></span>

|<span data-ttu-id="2f43e-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2f43e-121">**Value**</span></span>|<span data-ttu-id="2f43e-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f43e-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2f43e-123">Wahr</span><span class="sxs-lookup"><span data-stu-id="2f43e-123">True</span></span>  <br/> |<span data-ttu-id="2f43e-124">Die vollständigen Kontaktdetails für öffentliche Kontakte werden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f43e-124">Full contact details for public contacts are returned.</span></span>  <br/> |
|<span data-ttu-id="2f43e-125">Falsch</span><span class="sxs-lookup"><span data-stu-id="2f43e-125">False</span></span>  <br/> |<span data-ttu-id="2f43e-126">Die vollständigen Kontaktdetails für öffentliche Kontakte werden nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f43e-126">Full contact details for public contacts are not returned.</span></span>  <br/> |
   
#### <a name="searchscope-attribute-values"></a><span data-ttu-id="2f43e-127">SearchScope-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="2f43e-127">SearchScope attribute values</span></span>

|<span data-ttu-id="2f43e-128">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2f43e-128">**Value**</span></span>|<span data-ttu-id="2f43e-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f43e-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2f43e-130">ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="2f43e-130">ActiveDirectory</span></span>  <br/> |<span data-ttu-id="2f43e-131">Es wird nur der Active Directory-Verzeichnisdienst durchsucht.</span><span class="sxs-lookup"><span data-stu-id="2f43e-131">Only the Active Directory directory service is searched.</span></span>  <br/> |
|<span data-ttu-id="2f43e-132">ActiveDirectoryContacts</span><span class="sxs-lookup"><span data-stu-id="2f43e-132">ActiveDirectoryContacts</span></span>  <br/> |<span data-ttu-id="2f43e-133">Active Directory wird zuerst durchsucht, und dann werden die in der [ParentFolderIds](parentfolderids.md) -Eigenschaft angegebenen Kontaktordner durchsucht.</span><span class="sxs-lookup"><span data-stu-id="2f43e-133">Active Directory is searched first, and then the contact folders that are specified in the [ParentFolderIds](parentfolderids.md) property are searched.</span></span>  <br/> |
|<span data-ttu-id="2f43e-134">Kontakte</span><span class="sxs-lookup"><span data-stu-id="2f43e-134">Contacts</span></span>  <br/> |<span data-ttu-id="2f43e-135">Nur die Kontaktordner, die von der [ParentFolderIds](parentfolderids.md) -Eigenschaft identifiziert werden, werden durchsucht.</span><span class="sxs-lookup"><span data-stu-id="2f43e-135">Only the contact folders that are identified by the [ParentFolderIds](parentfolderids.md) property are searched.</span></span>  <br/> |
|<span data-ttu-id="2f43e-136">ContactsActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="2f43e-136">ContactsActiveDirectory</span></span>  <br/> |<span data-ttu-id="2f43e-137">Kontaktordner, die von der [ParentFolderIds](parentfolderids.md) -Eigenschaft identifiziert werden, werden zuerst durchsucht, und dann wird Active Directory durchsucht.</span><span class="sxs-lookup"><span data-stu-id="2f43e-137">Contact folders that are identified by the [ParentFolderIds](parentfolderids.md) property are searched first and then Active Directory is searched.</span></span>  <br/> |
   
#### <a name="contactdatashape-attribute-values"></a><span data-ttu-id="2f43e-138">ContactDataShape-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="2f43e-138">ContactDataShape attribute values</span></span>

|<span data-ttu-id="2f43e-139">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2f43e-139">**Value**</span></span>|<span data-ttu-id="2f43e-140">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f43e-140">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2f43e-141">IdOnly</span><span class="sxs-lookup"><span data-stu-id="2f43e-141">IdOnly</span></span>  <br/> |<span data-ttu-id="2f43e-142">Die Eigenschaft Contact Item Identifier wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f43e-142">The contact item identifier property is returned.</span></span>  <br/> |
|<span data-ttu-id="2f43e-143">Standard</span><span class="sxs-lookup"><span data-stu-id="2f43e-143">Default</span></span>  <br/> |<span data-ttu-id="2f43e-144">Die Standardeinstellungen für Kontaktelemente werden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f43e-144">The Default set of contact item properties is returned.</span></span> <span data-ttu-id="2f43e-145">Weitere Informationen finden Sie unter [Response Shapes in EWS](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2f43e-145">For more information, see [Response shapes in EWS](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).</span></span>  <br/> |
|<span data-ttu-id="2f43e-146">AllProperties</span><span class="sxs-lookup"><span data-stu-id="2f43e-146">AllProperties</span></span>  <br/> |<span data-ttu-id="2f43e-147">Die allproperties-Gruppe der Kontaktelement Eigenschaften wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f43e-147">The AllProperties set of contact item properties are returned.</span></span> <span data-ttu-id="2f43e-148">Weitere Informationen finden Sie unter [Response Shapes in EWS](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2f43e-148">For more information, see [Response shapes in EWS](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2f43e-149">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2f43e-149">Child elements</span></span>

|<span data-ttu-id="2f43e-150">**Element**</span><span class="sxs-lookup"><span data-stu-id="2f43e-150">**Element**</span></span>|<span data-ttu-id="2f43e-151">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f43e-151">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f43e-152">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="2f43e-152">ParentFolderIds</span></span>](parentfolderids.md) <br/> |<span data-ttu-id="2f43e-153">Enthält ein Array von Kontaktordner Bezeichnern, die durchsucht werden, wenn das **SearchScope** -Attribut auf ActiveDirectoryContacts, Contacts oder ContactsActiveDirectory festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2f43e-153">Contains an array of contact folder identifiers that would be searched if the **SearchScope** attribute is set to ActiveDirectoryContacts, Contacts, or ContactsActiveDirectory.</span></span> <span data-ttu-id="2f43e-154">Das ParentFolderIds-Array kann nur einen einzelnen Kontaktordner Bezeichner enthalten.</span><span class="sxs-lookup"><span data-stu-id="2f43e-154">The ParentFolderIds array can only contain a single contact folder identifier.</span></span> <span data-ttu-id="2f43e-155">Wenn das **ParentFolderIds** -Element nicht vorhanden ist, wird der Standardordner Kontakte durchsucht.</span><span class="sxs-lookup"><span data-stu-id="2f43e-155">If the **ParentFolderIds** element is not present, the default Contacts folder is searched.</span></span>  <br/> <span data-ttu-id="2f43e-156">Die Ordner-ID kann für den Stellvertretungszugriff verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f43e-156">The folder identifier can be used for delegate access.</span></span>  <br/> <span data-ttu-id="2f43e-157">Active Directory suchen werden mithilfe von Zugriffssteuerungslisten (Access Control Lists, ACLs) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f43e-157">Active Directory searches are performed by using access control lists (ACLs).</span></span> <span data-ttu-id="2f43e-158">Einige Benutzer verfügen möglicherweise nicht über die Rechte zum Anzeigen einiger Active Directory-Objekte.</span><span class="sxs-lookup"><span data-stu-id="2f43e-158">Some users might not have the rights to see some Active Directory objects.</span></span>  <br/> <span data-ttu-id="2f43e-159">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="2f43e-159">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="2f43e-160">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="2f43e-160">UnresolvedEntry</span></span>](unresolvedentry.md) <br/> |<span data-ttu-id="2f43e-161">Enthält den Namen eines Kontakts oder einer Verteilerliste, die aufgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f43e-161">Contains the name of a contact or distribution list to resolve.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2f43e-162">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2f43e-162">Parent elements</span></span>

<span data-ttu-id="2f43e-163">Keine.</span><span class="sxs-lookup"><span data-stu-id="2f43e-163">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2f43e-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f43e-164">Remarks</span></span>

<span data-ttu-id="2f43e-165">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2f43e-165">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f43e-166">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2f43e-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f43e-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f43e-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2f43e-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2f43e-168">Schema name</span></span>  <br/> |<span data-ttu-id="2f43e-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2f43e-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2f43e-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2f43e-170">Validation file</span></span>  <br/> |<span data-ttu-id="2f43e-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2f43e-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2f43e-172">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2f43e-172">Can be empty</span></span>  <br/> |<span data-ttu-id="2f43e-173">False</span><span class="sxs-lookup"><span data-stu-id="2f43e-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f43e-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f43e-174">See also</span></span>



[<span data-ttu-id="2f43e-175">ResolveNames-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2f43e-175">ResolveNames operation</span></span>](resolvenames-operation.md)
  
[<span data-ttu-id="2f43e-176">ResolveNamesType</span><span class="sxs-lookup"><span data-stu-id="2f43e-176">ResolveNamesType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesType.aspx)
  
[<span data-ttu-id="2f43e-177">ResolveNamesSearchScopeType</span><span class="sxs-lookup"><span data-stu-id="2f43e-177">ResolveNamesSearchScopeType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesSearchScopeType.aspx)


- [<span data-ttu-id="2f43e-178">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2f43e-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="2f43e-179">Verwenden der Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="2f43e-179">Using Name Resolution</span></span>](https://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

