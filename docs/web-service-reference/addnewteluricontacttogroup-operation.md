---
title: AddNewTelUriContactToGroup-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9688ce8-2465-45bb-8bd2-94b32ed4885c
description: Hier finden Sie Informationen zur Verwendung von AddNewTelUriContactToGroup EWS-Vorgangs.
ms.openlocfilehash: 34450171776b4215d9c0a39700a309e2e2d755dd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757236"
---
# <a name="addnewteluricontacttogroup-operation"></a><span data-ttu-id="664e0-103">AddNewTelUriContactToGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="664e0-103">AddNewTelUriContactToGroup operation</span></span>

<span data-ttu-id="664e0-104">Hier finden Sie Informationen dazu, wie Sie den **AddNewTelUriContactToGroup** EWS-Vorgang verwenden.</span><span class="sxs-lookup"><span data-stu-id="664e0-104">Find information about how to use the **AddNewTelUriContactToGroup** EWS operation.</span></span> 
  
<span data-ttu-id="664e0-105">**AddNewTelUriContactToGroup** -Vorgang fügt einen neuen Kontakt zu einer Gruppe basierend auf Telefonnummer des Kontakts.</span><span class="sxs-lookup"><span data-stu-id="664e0-105">The **AddNewTelUriContactToGroup** operation adds a new contact to a group based on a contact's phone number.</span></span> 
  
<span data-ttu-id="664e0-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="664e0-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addnewteluricontacttogroup-operation"></a><span data-ttu-id="664e0-107">Verwenden des AddNewTelUriContactToGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="664e0-107">Using the AddNewTelUriContactToGroup operation</span></span>

<span data-ttu-id="664e0-108">Eine **AddNewTelUriContactToGroup** Vorgang Anforderung sendet TEL-URI eines Kontakts, SIP-URI, Telefonnummer und der Gruppe, um den Kontakt hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="664e0-108">An **AddNewTelUriContactToGroup** operation request submits a contact's TEL URI, SIP URI, phone number, and the group to add the contact to.</span></span> <span data-ttu-id="664e0-109">Eine Antwort auf einen Vorgang **AddNewTelUriContactToGroup** wird eine Rolle für den neuen Kontakt erstellt.</span><span class="sxs-lookup"><span data-stu-id="664e0-109">An **AddNewTelUriContactToGroup** operation response creates a persona for the new contact.</span></span> <span data-ttu-id="664e0-110">Dieser Vorgang ermöglicht es Clients, um einen neuen Kontakt hinzufügen, auch wenn der Kontakt nicht über einen Namen verfügt.</span><span class="sxs-lookup"><span data-stu-id="664e0-110">This operation allows clients to add a new contact even if the contact does not have a name.</span></span> 
  
### <a name="addnewteluricontacttogroup-operation-soap-headers"></a><span data-ttu-id="664e0-111">AddNewTelUriContactToGroup Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="664e0-111">AddNewTelUriContactToGroup operation SOAP headers</span></span>

<span data-ttu-id="664e0-112">Der Vorgang **AddNewTelUriContactToGroup** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="664e0-112">The **AddNewTelUriContactToGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="664e0-113">**Headername**</span><span class="sxs-lookup"><span data-stu-id="664e0-113">**Header name**</span></span>|<span data-ttu-id="664e0-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="664e0-114">**Element**</span></span>|<span data-ttu-id="664e0-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="664e0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="664e0-116">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="664e0-116">**Impersonation**</span></span> <br/> |[<span data-ttu-id="664e0-117">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="664e0-117">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="664e0-118">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="664e0-118">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="664e0-119">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="664e0-119">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="664e0-120">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="664e0-120">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="664e0-121">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="664e0-121">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="664e0-122">Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="664e0-122">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="664e0-123">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="664e0-123">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="664e0-124">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="664e0-124">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="664e0-125">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="664e0-125">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="664e0-126">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="664e0-126">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="664e0-127">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="664e0-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="664e0-128">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="664e0-128">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="664e0-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="664e0-129">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="664e0-130">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="664e0-130">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="664e0-131">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="664e0-131">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="addnewteluricontacttogroup-operation-request-example-add-a-new-contact-to-a-group"></a><span data-ttu-id="664e0-132">AddNewTelUriContactToGroup Vorgang-anforderungsbeispiel: Hinzufügen ein neues Kontakts zu einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="664e0-132">AddNewTelUriContactToGroup operation request example: Add a new contact to a group</span></span>

<span data-ttu-id="664e0-133">Im folgenden Beispiel wird ein **AddNewTelUriContactToGroup** Vorgang Anforderung zeigt zum Erstellen eines neuen Kontakts und Hinzufügen von neuen Kontakt zu einer instant messaging (IM) Gruppe mithilfe des Kontakts TEL und SIP-URIs.</span><span class="sxs-lookup"><span data-stu-id="664e0-133">The following example of an **AddNewTelUriContactToGroup** operation request shows how to create a new contact and add the new contact to an instant messaging (IM) group by using the contact's TEL and SIP URIs.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="664e0-134">Bezeichner für alle Elemente aus, und Ändern von Schlüsseln in diesem Artikel wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="664e0-134">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
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
      <m:AddNewTelUriContactToGroup>
         <m:TelUriAddress>tel:5625550100</m:TelUriAddress>
         <m:ImContactSipUriAddress>sip:john@contoso.com</m:ImContactSipUriAddress>
         <m:ImTelephoneNumber>5625550100</m:ImTelephoneNumber>
         <m:GroupId Id="AAMkADEzOTm4QrAABY7+0GAAA="/>
      </m:AddNewTelUriContactToGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="664e0-135">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="664e0-135">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="664e0-136">AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="664e0-136">AddNewTelUriContactToGroup</span></span>](addnewteluricontacttogroup.md)
    
- [<span data-ttu-id="664e0-137">TelUriAddress</span><span class="sxs-lookup"><span data-stu-id="664e0-137">TelUriAddress</span></span>](teluriaddress.md)
    
- [<span data-ttu-id="664e0-138">ImContactSipUriAddress</span><span class="sxs-lookup"><span data-stu-id="664e0-138">ImContactSipUriAddress</span></span>](imcontactsipuriaddress.md)
    
- [<span data-ttu-id="664e0-139">ImTelephoneNumber</span><span class="sxs-lookup"><span data-stu-id="664e0-139">ImTelephoneNumber</span></span>](imtelephonenumber.md)
    
- [<span data-ttu-id="664e0-140">GroupId</span><span class="sxs-lookup"><span data-stu-id="664e0-140">GroupId</span></span>](groupid.md)
    
## <a name="successful-addnewteluricontacttogroup-operation-response"></a><span data-ttu-id="664e0-141">Erfolgreiche AddNewTelUriContactToGroup Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="664e0-141">Successful AddNewTelUriContactToGroup operation response</span></span>

<span data-ttu-id="664e0-142">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **AddNewTelUriContactToGroup** Vorgang, um einen Kontakt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="664e0-142">The following example shows a successful response to an **AddNewTelUriContactToGroup** operation request to create a contact.</span></span> <span data-ttu-id="664e0-143">Die Antwort enthält den zugeordneten Rolle Bezeichner für den Kontakt, den Anzeigenamen der Rolle, die in diesem Fall auf die Telefonnummer des Kontakts basiert, und Elementbezeichner des Kontakts, die als Teil der Abschreibung Bezeichner Quelle angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="664e0-143">The response contains the associated persona identifier for the contact, the display name of the persona, which in this case is based on the contact's phone number, and the contact's item identifier, which is displayed as part of the source identifier attribution.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/"                           
            xmlns:xsd="http://www.w3.org/2001/XMLSchema"
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
            xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" />
   </s:Header>
   <s:Body>
      <AddNewTelUriContactToGroupResponse ResponseClass="Success" 
                                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <Persona>
            <t:PersonaId Id="AAQkADE686dX3s="/>
            <t:PersonaType>Person</t:PersonaType>
            <t:CreationTime>2012-10-29T23:10:13Z</t:CreationTime>
            <t:DisplayName/>
            <t:DisplayNameFirstLast>5625550100</t:DisplayNameFirstLast>
            <t:DisplayNameLastFirst>5625550100</t:DisplayNameLastFirst>
            <t:FileAs/>
            <t:FileAsId >None</t:FileAsId>
            <t:RelevanceScore >2147483647</t:RelevanceScore>
            <t:Attributions>
               <t:Attribution>
                  <t:Id>0</t:Id>
                  <t:SourceId Id="ABhHuhCAAA=" ChangeKey="EQAAABxFU"/>
                  <t:DisplayName>Lync Contacts</t:DisplayName>
                  <t:IsWritable>false</t:IsWritable>
                  <t:IsQuickContact>true</t:IsQuickContact>
                  <t:IsHidden>false</t:IsHidden>
               </t:Attribution>
            </t:Attributions>
            <t:FileAsIds>
               <t:StringAttributedValue>
                  <t:Value>None</t:Value>
                  <t:Attributions>
                     <t:Attribution>0</t:Attribution>
                  </t:Attributions>
               </t:StringAttributedValue>
            </t:FileAsIds>
            <t:OtherTelephones>
               <t:PhoneNumberAttributedValue>
                  <t:Value>
                     <t:Number>5625550100</t:Number>
                     <t:Type>Other</t:Type>
                  </t:Value>
                  <t:Attributions>
                     <t:Attribution>0</t:Attribution>
                  </t:Attributions>
               </t:PhoneNumberAttributedValue>
            </t:OtherTelephones>
         </Persona>
      </AddNewTelUriContactToGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="664e0-144">Die Antwort SOAP-Text enthält den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="664e0-144">The response SOAP body contains following elements:</span></span>
  
- [<span data-ttu-id="664e0-145">AddNewTelUriContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="664e0-145">AddNewTelUriContactToGroupResponse</span></span>](addnewteluricontacttogroupresponse.md)
    
- [<span data-ttu-id="664e0-146">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="664e0-146">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="664e0-147">Rolle</span><span class="sxs-lookup"><span data-stu-id="664e0-147">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="664e0-148">PersonaId</span><span class="sxs-lookup"><span data-stu-id="664e0-148">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="664e0-149">PersonaType</span><span class="sxs-lookup"><span data-stu-id="664e0-149">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="664e0-150">CreationTime</span><span class="sxs-lookup"><span data-stu-id="664e0-150">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="664e0-151">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="664e0-151">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="664e0-152">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="664e0-152">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="664e0-153">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="664e0-153">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="664e0-154">FileAs</span><span class="sxs-lookup"><span data-stu-id="664e0-154">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="664e0-155">FileAsId</span><span class="sxs-lookup"><span data-stu-id="664e0-155">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="664e0-156">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="664e0-156">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="664e0-157">Hinweise (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="664e0-157">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="664e0-158">Zuweisung (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="664e0-158">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="664e0-159">ID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="664e0-159">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="664e0-160">SourceId</span><span class="sxs-lookup"><span data-stu-id="664e0-160">SourceId</span></span>](sourceid.md)
    
- [<span data-ttu-id="664e0-161">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="664e0-161">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="664e0-162">IsWritable</span><span class="sxs-lookup"><span data-stu-id="664e0-162">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="664e0-163">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="664e0-163">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="664e0-164">IsHidden</span><span class="sxs-lookup"><span data-stu-id="664e0-164">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="664e0-165">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="664e0-165">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="664e0-166">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="664e0-166">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="664e0-167">Wert</span><span class="sxs-lookup"><span data-stu-id="664e0-167">Value</span></span>](value.md)
    
- [<span data-ttu-id="664e0-168">Hinweise (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="664e0-168">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md)
    
- [<span data-ttu-id="664e0-169">Zuweisung (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="664e0-169">Attribution (string)</span></span>](attribution-string.md)
    
- [<span data-ttu-id="664e0-170">OtherTelephones</span><span class="sxs-lookup"><span data-stu-id="664e0-170">OtherTelephones</span></span>](othertelephones.md)
    
- [<span data-ttu-id="664e0-171">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="664e0-171">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md)
    
- [<span data-ttu-id="664e0-172">Wert</span><span class="sxs-lookup"><span data-stu-id="664e0-172">Value</span></span>](value.md)
    
- [<span data-ttu-id="664e0-173">Nummer</span><span class="sxs-lookup"><span data-stu-id="664e0-173">Number</span></span>](number.md)
    
- [<span data-ttu-id="664e0-174">Typ (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="664e0-174">Type (string)</span></span>](type-string.md)
    
- [<span data-ttu-id="664e0-175">Hinweise (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="664e0-175">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md)
    
- [<span data-ttu-id="664e0-176">Zuweisung (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="664e0-176">Attribution (string)</span></span>](attribution-string.md)
    
## <a name="addnewteluricontacttogroup-operation-error-response-example"></a><span data-ttu-id="664e0-177">AddNewTelUriContactToGroup Vorgang Fehler antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="664e0-177">AddNewTelUriContactToGroup operation error response example</span></span>

<span data-ttu-id="664e0-178">Das folgende Beispiel zeigt eine Fehlerantwort an eine **AddNewTelUriContactToGroup** Vorgang Anforderung, wenn die Gruppen-ID einen wohlgeformten Wert enthält, der keinen, eine Gruppe im Postfach identifiziert.</span><span class="sxs-lookup"><span data-stu-id="664e0-178">The following example shows an error response to an **AddNewTelUriContactToGroup** operation request when the group identifier contains a well-formed value that does not identify a group in the mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddNewTelUriContactToGroupResponse ResponseClass="Error" 
                                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </AddNewTelUriContactToGroupResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="664e0-179">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="664e0-179">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="664e0-180">AddNewTelUriContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="664e0-180">AddNewTelUriContactToGroupResponse</span></span>](addnewteluricontacttogroupresponse.md)
    
- [<span data-ttu-id="664e0-181">MessageText</span><span class="sxs-lookup"><span data-stu-id="664e0-181">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="664e0-182">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="664e0-182">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="664e0-183">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="664e0-183">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="664e0-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="664e0-184">See also</span></span>

- [<span data-ttu-id="664e0-185">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="664e0-185">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="664e0-186">Benutzer und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="664e0-186">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    

