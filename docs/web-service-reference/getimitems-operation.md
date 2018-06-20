---
title: GetImItems-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 51186691-46d2-4d5c-b8bc-4ee2bb20fbe7
description: Hier finden Sie Informationen über die GetImItems EWS Vorgang.
ms.openlocfilehash: 4335cc22b22dc5f102f2221f7fdb22a506ba026f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758701"
---
# <a name="getimitems-operation"></a><span data-ttu-id="ab8cc-103">GetImItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ab8cc-103">GetImItems operation</span></span>

<span data-ttu-id="ab8cc-104">Hier finden Sie Informationen zum **GetImItems** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-104">Find information about the **GetImItems** EWS operation.</span></span> 
  
<span data-ttu-id="ab8cc-105">Der Vorgang **GetImItems** werden Informationen zu instant messaging (IM) Gruppen abgerufen und Sofortnachrichten wenden Sie sich an Rollen.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-105">The **GetImItems** operation retrieves information about instant messaging (IM) groups and IM contact personas.</span></span> 
  
<span data-ttu-id="ab8cc-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getimitems-operation"></a><span data-ttu-id="ab8cc-107">Verwenden des GetImItems-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="ab8cc-107">Using the GetImItems operation</span></span>

<span data-ttu-id="ab8cc-108">Der **GetImItems** -Vorgang akzeptiert, Gruppen- und Element-IDs und gibt einen Satz von Informationen zu den Gruppen und Kontakte.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-108">The **GetImItems** operation accepts group and contact item identifiers and returns a set of information about the groups and contacts.</span></span> <span data-ttu-id="ab8cc-109">Die in der Antwort zurückgegebenen Eigenschaftensätze werden durch erweiterte Eigenschaften, mehrere Kontakt-IDs, Gruppen-IDs identifiziert und erweiterte Eigenschaftsdefinitionen als Argumente.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-109">The property sets returned in the response are identified by extended properties, multiple contact identifiers, group identifiers, and extended property definitions as arguments.</span></span> 
  
### <a name="getimitems-operation-soap-headers"></a><span data-ttu-id="ab8cc-110">GetImItems Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="ab8cc-110">GetImItems operation SOAP headers</span></span>

<span data-ttu-id="ab8cc-111">Der Vorgang **GetImItems** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-111">The **GetImItems** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="ab8cc-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="ab8cc-112">**Header name**</span></span>|<span data-ttu-id="ab8cc-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ab8cc-113">**Element**</span></span>|<span data-ttu-id="ab8cc-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab8cc-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ab8cc-115">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="ab8cc-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="ab8cc-116">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="ab8cc-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="ab8cc-117">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="ab8cc-118">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ab8cc-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="ab8cc-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="ab8cc-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="ab8cc-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="ab8cc-121">Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="ab8cc-122">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ab8cc-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="ab8cc-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="ab8cc-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="ab8cc-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="ab8cc-125">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="ab8cc-126">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ab8cc-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="ab8cc-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="ab8cc-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ab8cc-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="ab8cc-129">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="ab8cc-130">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-130">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getimitems-operation-request-example-get-detailed-information-about-im-contacts-and-groups"></a><span data-ttu-id="ab8cc-131">GetImItems Vorgang-anforderungsbeispiel: Abrufen detaillierter Informationen zu Instant Messaging-Kontakten und Gruppen</span><span class="sxs-lookup"><span data-stu-id="ab8cc-131">GetImItems operation request example: Get detailed information about IM contacts and groups</span></span>

<span data-ttu-id="ab8cc-132">Im folgenden Beispiel wird eine **GetImItems** Vorgang Anforderung veranschaulicht, wie zur Anforderung detaillierte Informationen zu Instant Messaging-Kontakte und Gruppen.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-132">The following example of a **GetImItems** operation request shows how to request detailed information about IM contacts and groups.</span></span> <span data-ttu-id="ab8cc-133">Ein Vorgang **GetImItems** kann anfordern mindestens einen Kontakt oder eine Gruppe von Details.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-133">A **GetImItems** operation can request one or more contact or group details.</span></span> <span data-ttu-id="ab8cc-134">Sie können auch erweiterte Eigenschaften verwenden, benutzerdefinierte Eigenschaften auf Gruppen und Kontakte abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-134">You can also use extended properties to get custom properties on groups and contacts.</span></span> <span data-ttu-id="ab8cc-135">Wenn eine angeforderte erweiterte Eigenschaft nicht für ein Element vorhanden ist, wird die Antwort ignorieren angeforderte Eigenschaft und die Antwort für die standardmäßigen-Eigenschaft zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-135">If a requested extended property does not exist on an item, the response will ignore the requested property and return the response for the default property set.</span></span> <span data-ttu-id="ab8cc-136">Dieses Beispiel zeigt, wie den Anzeigenamen mithilfe von erweiterten Eigenschaften abrufen.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-136">This example shows you how to get the display name by using extended properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ab8cc-137">Bezeichner für alle Elemente aus, und Ändern von Schlüsseln in diesem Artikel wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-137">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> <span data-ttu-id="ab8cc-138">Notiz, die Tasten ändern, werden vom Dienst für diesen Vorgang ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-138">Note that change keys are ignored by the service for this operation.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="ab8cc-139">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="ab8cc-139">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ab8cc-140">GetImItems</span><span class="sxs-lookup"><span data-stu-id="ab8cc-140">GetImItems</span></span>](getimitems.md)
    
- [<span data-ttu-id="ab8cc-141">ContactIds</span><span class="sxs-lookup"><span data-stu-id="ab8cc-141">ContactIds</span></span>](contactids.md)
    
- [<span data-ttu-id="ab8cc-142">ItemId</span><span class="sxs-lookup"><span data-stu-id="ab8cc-142">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="ab8cc-143">GroupIds</span><span class="sxs-lookup"><span data-stu-id="ab8cc-143">GroupIds</span></span>](groupids.md)
    
- [<span data-ttu-id="ab8cc-144">ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)</span><span class="sxs-lookup"><span data-stu-id="ab8cc-144">ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)</span></span>](extendedproperties-nonemptyarrayofextendedfielduris.md)
    
- [<span data-ttu-id="ab8cc-145">ExtendedProperty (PathToExtendedFieldType)</span><span class="sxs-lookup"><span data-stu-id="ab8cc-145">ExtendedProperty (PathToExtendedFieldType)</span></span>](extendedproperty-pathtoextendedfieldtype.md)
    
## <a name="successful-getimitems-operation-response"></a><span data-ttu-id="ab8cc-146">Erfolgreiche GetImItems Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="ab8cc-146">Successful GetImItems operation response</span></span>

<span data-ttu-id="ab8cc-147">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **GetImItems** , um eine im-Kontakt und Gruppe zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-147">The following example shows a successful response to a **GetImItems** request to get an IM contact and group.</span></span> <span data-ttu-id="ab8cc-148">Der Anzeigename wird in einer erweiterten Eigenschaft angefordert.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-148">The display name is requested in an extended property.</span></span> <span data-ttu-id="ab8cc-149">Im-Kontakte werden in Form einer Rolle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-149">IM contacts are returned in the form of a persona.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetImItemsResponse ResponseClass="Success" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <ImItemList>
            <Groups xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
            <Personas xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="ab8cc-150">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="ab8cc-150">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ab8cc-151">GetImItemsResponse</span><span class="sxs-lookup"><span data-stu-id="ab8cc-151">GetImItemsResponse</span></span>](getimitemsresponse.md)
    
- [<span data-ttu-id="ab8cc-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ab8cc-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ab8cc-153">ImItemList</span><span class="sxs-lookup"><span data-stu-id="ab8cc-153">ImItemList</span></span>](imitemlist.md)
    
- [<span data-ttu-id="ab8cc-154">Gruppen (ArrayOfImGroupType)</span><span class="sxs-lookup"><span data-stu-id="ab8cc-154">Groups (ArrayOfImGroupType)</span></span>](groups-arrayofimgrouptype.md)
    
- [<span data-ttu-id="ab8cc-155">ImGroup</span><span class="sxs-lookup"><span data-stu-id="ab8cc-155">ImGroup</span></span>](imgroup.md)
    
- [<span data-ttu-id="ab8cc-156">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="ab8cc-156">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="ab8cc-157">GroupType</span><span class="sxs-lookup"><span data-stu-id="ab8cc-157">GroupType</span></span>](grouptype.md)
    
- [<span data-ttu-id="ab8cc-158">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="ab8cc-158">ExchangeStoreId</span></span>](exchangestoreid.md)
    
- [<span data-ttu-id="ab8cc-159">MemberCorrelationKey</span><span class="sxs-lookup"><span data-stu-id="ab8cc-159">MemberCorrelationKey</span></span>](membercorrelationkey.md)
    
- [<span data-ttu-id="ab8cc-160">ItemId</span><span class="sxs-lookup"><span data-stu-id="ab8cc-160">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="ab8cc-161">ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)</span><span class="sxs-lookup"><span data-stu-id="ab8cc-161">ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)</span></span>](extendedproperties-nonemptyarrayofextendedfielduris.md)
    
- [<span data-ttu-id="ab8cc-162">ExtendedProperty (PathToExtendedFieldType)</span><span class="sxs-lookup"><span data-stu-id="ab8cc-162">ExtendedProperty (PathToExtendedFieldType)</span></span>](extendedproperty-pathtoextendedfieldtype.md)
    
- [<span data-ttu-id="ab8cc-163">Rollen</span><span class="sxs-lookup"><span data-stu-id="ab8cc-163">Personas</span></span>](personas-ex15websvcsotherref.md)
    
- [<span data-ttu-id="ab8cc-164">PersonaId</span><span class="sxs-lookup"><span data-stu-id="ab8cc-164">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="ab8cc-165">PersonaType</span><span class="sxs-lookup"><span data-stu-id="ab8cc-165">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="ab8cc-166">CreationTime</span><span class="sxs-lookup"><span data-stu-id="ab8cc-166">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="ab8cc-167">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="ab8cc-167">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="ab8cc-168">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="ab8cc-168">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="ab8cc-169">FileAs</span><span class="sxs-lookup"><span data-stu-id="ab8cc-169">FileAs</span></span>](fileas.md)
    
- <span data-ttu-id="ab8cc-170">[FileAsId](fileasid.md) FileAsId</span><span class="sxs-lookup"><span data-stu-id="ab8cc-170">[FileAsId](fileasid.md) FileAsId</span></span> 
    
- [<span data-ttu-id="ab8cc-171">ImAddress (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="ab8cc-171">ImAddress (String)</span></span>](imaddress-string.md)
    
- [<span data-ttu-id="ab8cc-172">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="ab8cc-172">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="ab8cc-173">Hinweise (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="ab8cc-173">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="ab8cc-174">Zuweisung (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="ab8cc-174">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="ab8cc-175">ID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="ab8cc-175">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="ab8cc-176">SourceId</span><span class="sxs-lookup"><span data-stu-id="ab8cc-176">SourceId</span></span>](sourceid.md)
    
- [<span data-ttu-id="ab8cc-177">IsWritable</span><span class="sxs-lookup"><span data-stu-id="ab8cc-177">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="ab8cc-178">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="ab8cc-178">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="ab8cc-179">IsHidden</span><span class="sxs-lookup"><span data-stu-id="ab8cc-179">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="ab8cc-180">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="ab8cc-180">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="ab8cc-181">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="ab8cc-181">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="ab8cc-182">ImAddresses</span><span class="sxs-lookup"><span data-stu-id="ab8cc-182">ImAddresses</span></span>](imaddresses.md)
    
- [<span data-ttu-id="ab8cc-183">Wert (ExtendedPropertyType)</span><span class="sxs-lookup"><span data-stu-id="ab8cc-183">Value (ExtendedPropertyType)</span></span>](value-extendedpropertytype.md)
    
## <a name="getimitems-operation-error-response"></a><span data-ttu-id="ab8cc-184">GetImItems Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="ab8cc-184">GetImItems operation error response</span></span>

<span data-ttu-id="ab8cc-185">Der Vorgang **GetImItems** Bezeichner wird nicht validiert und wird nicht die erwarteten Fehlerantwort **ErrorInvalidImContactId** oder **ErrorInvalidImGroupId** zurück, wenn Sie einen ungültigen Kontakt oder eine Gruppen-ID mit dem Dienst bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ab8cc-185">The **GetImItems** operation does not validate identifiers and will not return the expected **ErrorInvalidImContactId** or **ErrorInvalidImGroupId** error response if an invalid contact or group identifier is provided to the service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ab8cc-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab8cc-186">See also</span></span>

- [<span data-ttu-id="ab8cc-187">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="ab8cc-187">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="ab8cc-188">GetImItemList-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ab8cc-188">GetImItemList operation</span></span>](getimitemlist-operation.md)
    

