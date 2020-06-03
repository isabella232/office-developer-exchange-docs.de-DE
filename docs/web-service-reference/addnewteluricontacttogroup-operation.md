---
title: AddNewTelUriContactToGroup-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9688ce8-2465-45bb-8bd2-94b32ed4885c
description: Hier finden Sie Informationen zur Verwendung des AddNewTelUriContactToGroup-EWS-Vorgangs.
ms.openlocfilehash: 91228ec627ad928d2f1837c135af24846f811b1c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464945"
---
# <a name="addnewteluricontacttogroup-operation"></a><span data-ttu-id="d5581-103">AddNewTelUriContactToGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d5581-103">AddNewTelUriContactToGroup operation</span></span>

<span data-ttu-id="d5581-104">Hier finden Sie Informationen zur Verwendung des **AddNewTelUriContactToGroup** -EWS-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="d5581-104">Find information about how to use the **AddNewTelUriContactToGroup** EWS operation.</span></span> 
  
<span data-ttu-id="d5581-105">Mit dem **AddNewTelUriContactToGroup** -Vorgang wird eine neue Kontaktgruppe basierend auf der Telefonnummer eines Kontakts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d5581-105">The **AddNewTelUriContactToGroup** operation adds a new contact to a group based on a contact's phone number.</span></span> 
  
<span data-ttu-id="d5581-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d5581-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addnewteluricontacttogroup-operation"></a><span data-ttu-id="d5581-107">Verwenden des AddNewTelUriContactToGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d5581-107">Using the AddNewTelUriContactToGroup operation</span></span>

<span data-ttu-id="d5581-108">Eine **AddNewTelUriContactToGroup** -Vorgangsanforderung sendet den Tel-URI, den SIP-URI, die Telefonnummer und die Gruppe des Kontakts, um den Kontakt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d5581-108">An **AddNewTelUriContactToGroup** operation request submits a contact's TEL URI, SIP URI, phone number, and the group to add the contact to.</span></span> <span data-ttu-id="d5581-109">Eine **AddNewTelUriContactToGroup** -Vorgangs Antwort erstellt eine Persona für den neuen Kontakt.</span><span class="sxs-lookup"><span data-stu-id="d5581-109">An **AddNewTelUriContactToGroup** operation response creates a persona for the new contact.</span></span> <span data-ttu-id="d5581-110">Dieser Vorgang ermöglicht Clients das Hinzufügen eines neuen Kontakts, auch wenn der Kontakt keinen Namen hat.</span><span class="sxs-lookup"><span data-stu-id="d5581-110">This operation allows clients to add a new contact even if the contact does not have a name.</span></span> 
  
### <a name="addnewteluricontacttogroup-operation-soap-headers"></a><span data-ttu-id="d5581-111">SOAP-Header des AddNewTelUriContactToGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d5581-111">AddNewTelUriContactToGroup operation SOAP headers</span></span>

<span data-ttu-id="d5581-112">Der **AddNewTelUriContactToGroup** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d5581-112">The **AddNewTelUriContactToGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="d5581-113">**Headername**</span><span class="sxs-lookup"><span data-stu-id="d5581-113">**Header name**</span></span>|<span data-ttu-id="d5581-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5581-114">**Element**</span></span>|<span data-ttu-id="d5581-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5581-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d5581-116">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="d5581-116">**Impersonation**</span></span> <br/> |[<span data-ttu-id="d5581-117">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="d5581-117">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="d5581-118">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="d5581-118">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="d5581-119">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d5581-119">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d5581-120">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="d5581-120">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="d5581-121">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="d5581-121">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="d5581-122">Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d5581-122">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="d5581-123">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d5581-123">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d5581-124">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="d5581-124">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="d5581-125">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="d5581-125">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="d5581-126">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="d5581-126">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="d5581-127">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d5581-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d5581-128">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="d5581-128">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="d5581-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d5581-129">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="d5581-130">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="d5581-130">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="d5581-131">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="d5581-131">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="addnewteluricontacttogroup-operation-request-example-add-a-new-contact-to-a-group"></a><span data-ttu-id="d5581-132">AddNewTelUriContactToGroup-Vorgangs Anforderungs Beispiel: Hinzufügen eines neuen Kontakts zu einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="d5581-132">AddNewTelUriContactToGroup operation request example: Add a new contact to a group</span></span>

<span data-ttu-id="d5581-133">Im folgenden Beispiel einer **AddNewTelUriContactToGroup** -Vorgangsanforderung wird gezeigt, wie ein neuer Kontakt erstellt und der neue Kontakt einer Sofortnachrichten Gruppe mithilfe der Tel-und SIP-URIs des Kontakts hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d5581-133">The following example of an **AddNewTelUriContactToGroup** operation request shows how to create a new contact and add the new contact to an instant messaging (IM) group by using the contact's TEL and SIP URIs.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d5581-134">Alle Element-IDs und Änderungsschlüssel in diesem Artikel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d5581-134">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
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
      <m:AddNewTelUriContactToGroup>
         <m:TelUriAddress>tel:5625550100</m:TelUriAddress>
         <m:ImContactSipUriAddress>sip:john@contoso.com</m:ImContactSipUriAddress>
         <m:ImTelephoneNumber>5625550100</m:ImTelephoneNumber>
         <m:GroupId Id="AAMkADEzOTm4QrAABY7+0GAAA="/>
      </m:AddNewTelUriContactToGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d5581-135">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="d5581-135">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d5581-136">AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="d5581-136">AddNewTelUriContactToGroup</span></span>](addnewteluricontacttogroup.md)
    
- [<span data-ttu-id="d5581-137">TelUriAddress</span><span class="sxs-lookup"><span data-stu-id="d5581-137">TelUriAddress</span></span>](teluriaddress.md)
    
- [<span data-ttu-id="d5581-138">ImContactSipUriAddress</span><span class="sxs-lookup"><span data-stu-id="d5581-138">ImContactSipUriAddress</span></span>](imcontactsipuriaddress.md)
    
- [<span data-ttu-id="d5581-139">ImTelephoneNumber</span><span class="sxs-lookup"><span data-stu-id="d5581-139">ImTelephoneNumber</span></span>](imtelephonenumber.md)
    
- [<span data-ttu-id="d5581-140">GroupId</span><span class="sxs-lookup"><span data-stu-id="d5581-140">GroupId</span></span>](groupid.md)
    
## <a name="successful-addnewteluricontacttogroup-operation-response"></a><span data-ttu-id="d5581-141">Erfolgreiche Reaktion des AddNewTelUriContactToGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d5581-141">Successful AddNewTelUriContactToGroup operation response</span></span>

<span data-ttu-id="d5581-142">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **AddNewTelUriContactToGroup** -Vorgangsanforderung zum Erstellen eines Kontakts.</span><span class="sxs-lookup"><span data-stu-id="d5581-142">The following example shows a successful response to an **AddNewTelUriContactToGroup** operation request to create a contact.</span></span> <span data-ttu-id="d5581-143">Die Antwort enthält den zugeordneten Rollenbezeichner für den Kontakt, den Anzeigenamen der Rolle, die in diesem Fall auf der Telefonnummer des Kontakts basiert, und die Element-ID des Kontakts, die als Teil der Quellbezeichner-Attribution angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d5581-143">The response contains the associated persona identifier for the contact, the display name of the persona, which in this case is based on the contact's phone number, and the contact's item identifier, which is displayed as part of the source identifier attribution.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/"                           
            xmlns:xsd="http://www.w3.org/2001/XMLSchema"
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" />
   </s:Header>
   <s:Body>
      <AddNewTelUriContactToGroupResponse ResponseClass="Success" 
                                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="d5581-144">Der SOAP-Antworttext Körper enthält folgende Elemente:</span><span class="sxs-lookup"><span data-stu-id="d5581-144">The response SOAP body contains following elements:</span></span>
  
- [<span data-ttu-id="d5581-145">AddNewTelUriContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="d5581-145">AddNewTelUriContactToGroupResponse</span></span>](addnewteluricontacttogroupresponse.md)
    
- [<span data-ttu-id="d5581-146">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d5581-146">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d5581-147">Persona</span><span class="sxs-lookup"><span data-stu-id="d5581-147">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="d5581-148">PersonaId</span><span class="sxs-lookup"><span data-stu-id="d5581-148">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="d5581-149">Personatype</span><span class="sxs-lookup"><span data-stu-id="d5581-149">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="d5581-150">CreationTime</span><span class="sxs-lookup"><span data-stu-id="d5581-150">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="d5581-151">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="d5581-151">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="d5581-152">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="d5581-152">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="d5581-153">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="d5581-153">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="d5581-154">FileAs</span><span class="sxs-lookup"><span data-stu-id="d5581-154">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="d5581-155">FileAsId</span><span class="sxs-lookup"><span data-stu-id="d5581-155">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="d5581-156">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="d5581-156">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="d5581-157">Zuordnungen (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="d5581-157">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="d5581-158">Attribution (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="d5581-158">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="d5581-159">ID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="d5581-159">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="d5581-160">SourceId</span><span class="sxs-lookup"><span data-stu-id="d5581-160">SourceId</span></span>](sourceid.md)
    
- [<span data-ttu-id="d5581-161">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="d5581-161">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="d5581-162">Isschreibbar</span><span class="sxs-lookup"><span data-stu-id="d5581-162">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="d5581-163">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="d5581-163">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="d5581-164">IsHidden</span><span class="sxs-lookup"><span data-stu-id="d5581-164">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="d5581-165">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="d5581-165">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="d5581-166">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="d5581-166">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="d5581-167">Wert</span><span class="sxs-lookup"><span data-stu-id="d5581-167">Value</span></span>](value.md)
    
- [<span data-ttu-id="d5581-168">Zuordnungen (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="d5581-168">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md)
    
- [<span data-ttu-id="d5581-169">Attribution (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="d5581-169">Attribution (string)</span></span>](attribution-string.md)
    
- [<span data-ttu-id="d5581-170">OtherTelephones</span><span class="sxs-lookup"><span data-stu-id="d5581-170">OtherTelephones</span></span>](othertelephones.md)
    
- [<span data-ttu-id="d5581-171">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="d5581-171">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md)
    
- [<span data-ttu-id="d5581-172">Wert</span><span class="sxs-lookup"><span data-stu-id="d5581-172">Value</span></span>](value.md)
    
- [<span data-ttu-id="d5581-173">Number</span><span class="sxs-lookup"><span data-stu-id="d5581-173">Number</span></span>](number.md)
    
- [<span data-ttu-id="d5581-174">Typ (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="d5581-174">Type (string)</span></span>](type-string.md)
    
- [<span data-ttu-id="d5581-175">Zuordnungen (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="d5581-175">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md)
    
- [<span data-ttu-id="d5581-176">Attribution (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="d5581-176">Attribution (string)</span></span>](attribution-string.md)
    
## <a name="addnewteluricontacttogroup-operation-error-response-example"></a><span data-ttu-id="d5581-177">AddNewTelUriContactToGroup-Operation-Fehlerantwort (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="d5581-177">AddNewTelUriContactToGroup operation error response example</span></span>

<span data-ttu-id="d5581-178">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **AddNewTelUriContactToGroup** -Vorgangsanforderung, wenn der Gruppenbezeichner einen wohlgeformten Wert enthält, der keine Gruppe im Postfach identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d5581-178">The following example shows an error response to an **AddNewTelUriContactToGroup** operation request when the group identifier contains a well-formed value that does not identify a group in the mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddNewTelUriContactToGroupResponse ResponseClass="Error" 
                                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </AddNewTelUriContactToGroupResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="d5581-179">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="d5581-179">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d5581-180">AddNewTelUriContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="d5581-180">AddNewTelUriContactToGroupResponse</span></span>](addnewteluricontacttogroupresponse.md)
    
- [<span data-ttu-id="d5581-181">MessageText</span><span class="sxs-lookup"><span data-stu-id="d5581-181">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="d5581-182">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d5581-182">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d5581-183">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d5581-183">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="d5581-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5581-184">See also</span></span>

- [<span data-ttu-id="d5581-185">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="d5581-185">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="d5581-186">Personen und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="d5581-186">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    

