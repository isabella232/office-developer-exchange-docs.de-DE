---
title: GetImItems-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 51186691-46d2-4d5c-b8bc-4ee2bb20fbe7
description: Hier finden Sie Informationen zum GetImItems-EWS-Vorgang.
ms.openlocfilehash: 960f4683dd478b0e5f8cf18fa8d1593b7433a249
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456045"
---
# <a name="getimitems-operation"></a><span data-ttu-id="75f3f-103">GetImItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="75f3f-103">GetImItems operation</span></span>

<span data-ttu-id="75f3f-104">Hier finden Sie Informationen zum **GetImItems** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="75f3f-104">Find information about the **GetImItems** EWS operation.</span></span> 
  
<span data-ttu-id="75f3f-105">Der **GetImItems** -Vorgang ruft Informationen zu Chatgruppen und Chat Kontaktpersonen ab.</span><span class="sxs-lookup"><span data-stu-id="75f3f-105">The **GetImItems** operation retrieves information about instant messaging (IM) groups and IM contact personas.</span></span> 
  
<span data-ttu-id="75f3f-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="75f3f-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getimitems-operation"></a><span data-ttu-id="75f3f-107">Verwenden des GetImItems-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="75f3f-107">Using the GetImItems operation</span></span>

<span data-ttu-id="75f3f-108">Der **GetImItems** -Vorgang nimmt Gruppen-und Kontaktelement-IDs an und gibt eine Reihe von Informationen zu den Gruppen und Kontakten zurück.</span><span class="sxs-lookup"><span data-stu-id="75f3f-108">The **GetImItems** operation accepts group and contact item identifiers and returns a set of information about the groups and contacts.</span></span> <span data-ttu-id="75f3f-109">Die in der Antwort zurückgegebenen Eigenschaftensätze werden durch erweiterte Eigenschaften, mehrere Kontakt Bezeichner, Gruppenbezeichner und erweiterte Eigenschaftendefinitionen als Argumente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="75f3f-109">The property sets returned in the response are identified by extended properties, multiple contact identifiers, group identifiers, and extended property definitions as arguments.</span></span> 
  
### <a name="getimitems-operation-soap-headers"></a><span data-ttu-id="75f3f-110">SOAP-Header des GetImItems-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="75f3f-110">GetImItems operation SOAP headers</span></span>

<span data-ttu-id="75f3f-111">Der **GetImItems** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="75f3f-111">The **GetImItems** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="75f3f-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="75f3f-112">**Header name**</span></span>|<span data-ttu-id="75f3f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="75f3f-113">**Element**</span></span>|<span data-ttu-id="75f3f-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="75f3f-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="75f3f-115">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="75f3f-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="75f3f-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="75f3f-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="75f3f-117">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="75f3f-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="75f3f-118">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="75f3f-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="75f3f-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="75f3f-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="75f3f-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="75f3f-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="75f3f-121">Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="75f3f-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="75f3f-122">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="75f3f-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="75f3f-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="75f3f-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="75f3f-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="75f3f-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="75f3f-125">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="75f3f-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="75f3f-126">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="75f3f-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="75f3f-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="75f3f-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="75f3f-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="75f3f-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="75f3f-129">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="75f3f-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="75f3f-130">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="75f3f-130">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getimitems-operation-request-example-get-detailed-information-about-im-contacts-and-groups"></a><span data-ttu-id="75f3f-131">GetImItems-Vorgangs Anforderungs Beispiel: Abrufen detaillierter Informationen zu Chat Kontakten und Gruppen</span><span class="sxs-lookup"><span data-stu-id="75f3f-131">GetImItems operation request example: Get detailed information about IM contacts and groups</span></span>

<span data-ttu-id="75f3f-132">Im folgenden Beispiel einer **GetImItems** -Vorgangsanforderung wird gezeigt, wie detaillierte Informationen zu Chat Kontakten und Gruppen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="75f3f-132">The following example of a **GetImItems** operation request shows how to request detailed information about IM contacts and groups.</span></span> <span data-ttu-id="75f3f-133">Ein **GetImItems** -Vorgang kann einen oder mehrere Kontakt-oder Gruppendetails anfordern.</span><span class="sxs-lookup"><span data-stu-id="75f3f-133">A **GetImItems** operation can request one or more contact or group details.</span></span> <span data-ttu-id="75f3f-134">Sie können auch erweiterte Eigenschaften verwenden, um benutzerdefinierte Eigenschaften für Gruppen und Kontakte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="75f3f-134">You can also use extended properties to get custom properties on groups and contacts.</span></span> <span data-ttu-id="75f3f-135">Wenn eine angeforderte erweiterte Eigenschaft für ein Element nicht vorhanden ist, wird die angeforderte Eigenschaft von der Antwort ignoriert, und die Antwort für den standardmäßigen Eigenschaftensatz wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="75f3f-135">If a requested extended property does not exist on an item, the response will ignore the requested property and return the response for the default property set.</span></span> <span data-ttu-id="75f3f-136">In diesem Beispiel wird gezeigt, wie der Anzeigename mithilfe erweiterter Eigenschaften abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="75f3f-136">This example shows you how to get the display name by using extended properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="75f3f-137">Alle Element-IDs und Änderungsschlüssel in diesem Artikel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="75f3f-137">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> <span data-ttu-id="75f3f-138">Beachten Sie, dass Änderungsschlüssel vom Dienst für diesen Vorgang ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="75f3f-138">Note that change keys are ignored by the service for this operation.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:GetImItems>
         <m:ContactIds>
            <t:ItemId Id="AAMkADEzOTExYACABmEhpSAAA=" ChangeKey="EQAAABBmNDjF"/>
         </m:ContactIds>
         <m:GroupIds>
            <t:ItemId Id="AAMkADEzOTExYjJkBY7+0EAAA=" ChangeKey="EgAAAA=="/>
         </m:GroupIds>         
         <m:ExtendedProperties>
            <t:ExtendedProperty PropertyTag="0x3001" PropertyType="String"/>
         </m:ExtendedProperties>
      </m:GetImItems>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="75f3f-139">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="75f3f-139">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="75f3f-140">GetImItems</span><span class="sxs-lookup"><span data-stu-id="75f3f-140">GetImItems</span></span>](getimitems.md)
    
- [<span data-ttu-id="75f3f-141">Die</span><span class="sxs-lookup"><span data-stu-id="75f3f-141">ContactIds</span></span>](contactids.md)
    
- [<span data-ttu-id="75f3f-142">ItemId</span><span class="sxs-lookup"><span data-stu-id="75f3f-142">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="75f3f-143">GroupIds</span><span class="sxs-lookup"><span data-stu-id="75f3f-143">GroupIds</span></span>](groupids.md)
    
- [<span data-ttu-id="75f3f-144">ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)</span><span class="sxs-lookup"><span data-stu-id="75f3f-144">ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)</span></span>](extendedproperties-nonemptyarrayofextendedfielduris.md)
    
- [<span data-ttu-id="75f3f-145">Extended (pathtoextendedfieldtype Schematyp)</span><span class="sxs-lookup"><span data-stu-id="75f3f-145">ExtendedProperty (PathToExtendedFieldType)</span></span>](extendedproperty-pathtoextendedfieldtype.md)
    
## <a name="successful-getimitems-operation-response"></a><span data-ttu-id="75f3f-146">Erfolgreiche Reaktion des GetImItems-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="75f3f-146">Successful GetImItems operation response</span></span>

<span data-ttu-id="75f3f-147">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetImItems** -Anforderung zum Abrufen eines Chat Kontakts und einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="75f3f-147">The following example shows a successful response to a **GetImItems** request to get an IM contact and group.</span></span> <span data-ttu-id="75f3f-148">Der Anzeigename wird in einer erweiterten Eigenschaft angefordert.</span><span class="sxs-lookup"><span data-stu-id="75f3f-148">The display name is requested in an extended property.</span></span> <span data-ttu-id="75f3f-149">Chat-Kontakte werden in Form einer Persona zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="75f3f-149">IM contacts are returned in the form of a persona.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetImItemsResponse ResponseClass="Success" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <ImItemList>
            <Groups xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <ImGroup>
                  <DisplayName>Exchange SDK Team</DisplayName>
                  <GroupType>IPM.DistList.MOC.UserGroup</GroupType>
                  <ExchangeStoreId Id="AAMkADEzQrAABY7+0EAAA=" ChangeKey="EgAAAA=="/>
                  <MemberCorrelationKey>
                     <ItemId Id="AAMkADEzOTExYjeGgGqm4QrAABmEhpSAAA=" ChangeKey="EQAAAA=="/>
                  </MemberCorrelationKey>
                  <ExtendedProperties>
                     <ExtendedProperty>
                        <ExtendedFieldURI PropertyTag="0x3001" PropertyType="String"/>
                        <Value>Exchange SDK Team</Value>
                     </ExtendedProperty>
                  </ExtendedProperties>
               </ImGroup>
            </Groups>
            <Personas xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Persona>
                  <PersonaId Id="AAQkADEzOTBZImBzN5J/uHXc="/>
                  <PersonaType>Person</PersonaType>
                  <CreationTime>2012-11-07T00:10:35Z</CreationTime>
                  <DisplayName>Tony Smith</DisplayName>
                  <DisplayNameFirstLast>Tony Smith</DisplayNameFirstLast>
                  <DisplayNameLastFirst>Tony Smith</DisplayNameLastFirst>
                  <FileAs/>
                  <FileAsId>None</FileAsId>
                  <ImAddress>tsmith@contoso.com</ImAddress>
                  <RelevanceScore>2147483647</RelevanceScore>
                  <Attributions>
                     <Attribution>
                        <Id>0</Id>
                        <SourceId Id="AAMkADEzhQaoeGgGqm4QrAABmEhpSAAA=" ChangeKey="EQArAABmNDjF"/>
                        <DisplayName>Lync Contacts</DisplayName>
                        <IsWritable>false</IsWritable>
                        <IsQuickContact>true</IsQuickContact>
                        <IsHidden>false</IsHidden>
                     </Attribution>
                  </Attributions>
                  <DisplayNames>
                     <StringAttributedValue>
                        <Value>Tony Smith</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </DisplayNames>
                  <FileAsIds>
                     <StringAttributedValue>
                        <Value>None</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </FileAsIds>
                  <ImAddresses>
                     <StringAttributedValue>
                        <Value>tsmith@contoso.com</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </ImAddresses>
                  <ExtendedProperties>
                     <ExtendedPropertyAttributedValue>
                        <Value>
                           <ExtendedFieldURI PropertyTag="0x3001" PropertyType="String"/>
                           <Value>Tony Smith</Value>
                        </Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </ExtendedPropertyAttributedValue>
                  </ExtendedProperties>
               </Persona>
            </Personas>
         </ImItemList>
      </GetImItemsResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="75f3f-150">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="75f3f-150">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="75f3f-151">GetImItemsResponse</span><span class="sxs-lookup"><span data-stu-id="75f3f-151">GetImItemsResponse</span></span>](getimitemsresponse.md)
    
- [<span data-ttu-id="75f3f-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="75f3f-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="75f3f-153">Imitemlist</span><span class="sxs-lookup"><span data-stu-id="75f3f-153">ImItemList</span></span>](imitemlist.md)
    
- [<span data-ttu-id="75f3f-154">Gruppen (ArrayOfImGroupType)</span><span class="sxs-lookup"><span data-stu-id="75f3f-154">Groups (ArrayOfImGroupType)</span></span>](groups-arrayofimgrouptype.md)
    
- [<span data-ttu-id="75f3f-155">Imgroup</span><span class="sxs-lookup"><span data-stu-id="75f3f-155">ImGroup</span></span>](imgroup.md)
    
- [<span data-ttu-id="75f3f-156">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="75f3f-156">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="75f3f-157">GroupType</span><span class="sxs-lookup"><span data-stu-id="75f3f-157">GroupType</span></span>](grouptype.md)
    
- [<span data-ttu-id="75f3f-158">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="75f3f-158">ExchangeStoreId</span></span>](exchangestoreid.md)
    
- [<span data-ttu-id="75f3f-159">MemberCorrelationKey</span><span class="sxs-lookup"><span data-stu-id="75f3f-159">MemberCorrelationKey</span></span>](membercorrelationkey.md)
    
- [<span data-ttu-id="75f3f-160">ItemId</span><span class="sxs-lookup"><span data-stu-id="75f3f-160">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="75f3f-161">ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)</span><span class="sxs-lookup"><span data-stu-id="75f3f-161">ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)</span></span>](extendedproperties-nonemptyarrayofextendedfielduris.md)
    
- [<span data-ttu-id="75f3f-162">Extended (pathtoextendedfieldtype Schematyp)</span><span class="sxs-lookup"><span data-stu-id="75f3f-162">ExtendedProperty (PathToExtendedFieldType)</span></span>](extendedproperty-pathtoextendedfieldtype.md)
    
- [<span data-ttu-id="75f3f-163">Personas</span><span class="sxs-lookup"><span data-stu-id="75f3f-163">Personas</span></span>](personas-ex15websvcsotherref.md)
    
- [<span data-ttu-id="75f3f-164">PersonaId</span><span class="sxs-lookup"><span data-stu-id="75f3f-164">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="75f3f-165">Personatype</span><span class="sxs-lookup"><span data-stu-id="75f3f-165">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="75f3f-166">CreationTime</span><span class="sxs-lookup"><span data-stu-id="75f3f-166">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="75f3f-167">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="75f3f-167">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="75f3f-168">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="75f3f-168">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="75f3f-169">FileAs</span><span class="sxs-lookup"><span data-stu-id="75f3f-169">FileAs</span></span>](fileas.md)
    
- <span data-ttu-id="75f3f-170">[FileAsId](fileasid.md) FileAsId</span><span class="sxs-lookup"><span data-stu-id="75f3f-170">[FileAsId](fileasid.md) FileAsId</span></span> 
    
- [<span data-ttu-id="75f3f-171">IMAddress (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="75f3f-171">ImAddress (String)</span></span>](imaddress-string.md)
    
- [<span data-ttu-id="75f3f-172">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="75f3f-172">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="75f3f-173">Zuordnungen (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="75f3f-173">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="75f3f-174">Attribution (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="75f3f-174">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="75f3f-175">ID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="75f3f-175">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="75f3f-176">SourceId</span><span class="sxs-lookup"><span data-stu-id="75f3f-176">SourceId</span></span>](sourceid.md)
    
- [<span data-ttu-id="75f3f-177">Isschreibbar</span><span class="sxs-lookup"><span data-stu-id="75f3f-177">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="75f3f-178">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="75f3f-178">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="75f3f-179">IsHidden</span><span class="sxs-lookup"><span data-stu-id="75f3f-179">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="75f3f-180">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="75f3f-180">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="75f3f-181">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="75f3f-181">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="75f3f-182">Imaddresses</span><span class="sxs-lookup"><span data-stu-id="75f3f-182">ImAddresses</span></span>](imaddresses.md)
    
- [<span data-ttu-id="75f3f-183">Wert (extendedpropertytype Schematyp)</span><span class="sxs-lookup"><span data-stu-id="75f3f-183">Value (ExtendedPropertyType)</span></span>](value-extendedpropertytype.md)
    
## <a name="getimitems-operation-error-response"></a><span data-ttu-id="75f3f-184">Fehlerantwort des GetImItems-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="75f3f-184">GetImItems operation error response</span></span>

<span data-ttu-id="75f3f-185">Der **GetImItems** -Vorgang überprüft keine Bezeichner und gibt nicht die erwartete **ErrorInvalidImContactId** -oder **ErrorInvalidImGroupId** -Fehlerantwort zurück, wenn dem Dienst ein ungültiger Kontakt oder Gruppenbezeichner zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="75f3f-185">The **GetImItems** operation does not validate identifiers and will not return the expected **ErrorInvalidImContactId** or **ErrorInvalidImGroupId** error response if an invalid contact or group identifier is provided to the service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="75f3f-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75f3f-186">See also</span></span>

- [<span data-ttu-id="75f3f-187">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="75f3f-187">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="75f3f-188">GetImItemList-Vorgang</span><span class="sxs-lookup"><span data-stu-id="75f3f-188">GetImItemList operation</span></span>](getimitemlist-operation.md)
    

