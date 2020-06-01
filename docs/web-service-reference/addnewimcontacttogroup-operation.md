---
title: AddNewImContactToGroup-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cb5525f-faa3-48f1-9551-df55ffc26f46
description: Hier finden Sie Informationen zum AddNewImContactToGroup-EWS-Vorgang.
ms.openlocfilehash: e91cc067b4161b366e6713a9adc16873e63b1562
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465029"
---
# <a name="addnewimcontacttogroup-operation"></a><span data-ttu-id="8dc18-103">AddNewImContactToGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8dc18-103">AddNewImContactToGroup operation</span></span>

<span data-ttu-id="8dc18-104">Hier finden Sie Informationen zum **AddNewImContactToGroup** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="8dc18-104">Find information about the **AddNewImContactToGroup** EWS operation.</span></span> 
  
<span data-ttu-id="8dc18-105">Mit dem **AddNewImContactToGroup** -Vorgang wird einer Chatgruppe (Instant Messaging) ein neuer Kontakt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8dc18-105">The **AddNewImContactToGroup** operation adds a new contact to an instant messaging (IM) group.</span></span> 
  
<span data-ttu-id="8dc18-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8dc18-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addnewimcontacttogroup-operation"></a><span data-ttu-id="8dc18-107">Verwenden des AddNewImContactToGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="8dc18-107">Using the AddNewImContactToGroup operation</span></span>

<span data-ttu-id="8dc18-108">Der **AddNewImContactToGroup** -Vorgang verwendet die folgenden drei Argumente, um einer Chatgruppe einen neuen Kontakt hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="8dc18-108">The **AddNewImContactToGroup** operation takes the following three arguments to add a new contact to an IM group:</span></span> 
  
- <span data-ttu-id="8dc18-109">**IMAddress** -Eigenschaft – gibt die Chat Adresse des Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="8dc18-109">**ImAddress** property - Identifies the contact's IM address.</span></span> <span data-ttu-id="8dc18-110">Diese Eigenschaft ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8dc18-110">This property is required.</span></span> 
    
- <span data-ttu-id="8dc18-111">**Display** Name-Eigenschaft – gibt den Anzeigenamen des Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="8dc18-111">**DisplayName** property - Identifies the contact's display name.</span></span> 
    
- <span data-ttu-id="8dc18-112">**Gruppen** -Eigenschaft-gibt die Gruppe an, der der Kontakt hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8dc18-112">**GroupId** property - Identifies the group that the contact is added to.</span></span> 
    
<span data-ttu-id="8dc18-113">Dieser Vorgang gibt die Rolle des Kontakts zurück, der der Gruppe hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="8dc18-113">This operation returns the persona of the contact that was added to the group.</span></span>
  
### <a name="addnewimcontacttogroup-operation-soap-headers"></a><span data-ttu-id="8dc18-114">SOAP-Header des AddNewImContactToGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="8dc18-114">AddNewImContactToGroup operation SOAP headers</span></span>

<span data-ttu-id="8dc18-115">Der **AddNewImContactToGroup** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8dc18-115">The **AddNewImContactToGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="8dc18-116">**Headername**</span><span class="sxs-lookup"><span data-stu-id="8dc18-116">**Header name**</span></span>|<span data-ttu-id="8dc18-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="8dc18-117">**Element**</span></span>|<span data-ttu-id="8dc18-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8dc18-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8dc18-119">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="8dc18-119">**Impersonation**</span></span> <br/> |[<span data-ttu-id="8dc18-120">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="8dc18-120">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="8dc18-121">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="8dc18-121">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="8dc18-122">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8dc18-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="8dc18-123">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="8dc18-123">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="8dc18-124">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="8dc18-124">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="8dc18-125">Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8dc18-125">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="8dc18-126">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8dc18-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="8dc18-127">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="8dc18-127">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="8dc18-128">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="8dc18-128">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="8dc18-129">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="8dc18-129">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="8dc18-130">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8dc18-130">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="8dc18-131">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="8dc18-131">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="8dc18-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8dc18-132">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="8dc18-133">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="8dc18-133">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="8dc18-134">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="8dc18-134">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="addnewimcontacttogroup-operation-request-example-add-a-new-im-contact-to-a-group"></a><span data-ttu-id="8dc18-135">AddNewImContactToGroup-Vorgangs Anforderungs Beispiel: Hinzufügen eines neuen Chat Kontakts zu einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="8dc18-135">AddNewImContactToGroup operation request example: Add a new IM contact to a group</span></span>

<span data-ttu-id="8dc18-136">Im folgenden Beispiel einer **AddNewImContactToGroup** -Vorgangsanforderung wird gezeigt, wie einer vorhandenen Chatgruppe ein neuer Kontakt hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8dc18-136">The following example of an **AddNewImContactToGroup** operation request shows how to add a new contact to an existing IM group.</span></span> <span data-ttu-id="8dc18-137">Der Wert der **Group** -Eigenschaft für dieses Beispiel wurde von den Ergebnissen des [AddImGroup-Vorgangs](addimgroup-operation.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8dc18-137">The **GroupId** property value for this example was returned from results of the [AddImGroup operation](addimgroup-operation.md).</span></span> <span data-ttu-id="8dc18-138">Die **ExchangeStoreId** -Eigenschaft enthält den Wert der **Group** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8dc18-138">The **ExchangeStoreId** property contains the **GroupId** property value.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
      <t:TimeZoneContext>
         <t:TimeZoneDefinition Id="GMT Standard Time"/>
      </t:TimeZoneContext>
   </soap:Header>
   <soap:Body >
      <m:AddNewImContactToGroup>
         <m:ImAddress>tsmith@contoso.com</m:ImAddress>
         <m:DisplayName>Tony Smith</m:DisplayName>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDAAAQKAAA="
                    ChangeKey="EgAAAA=="/>
      </m:AddNewImContactToGroup>
   </soap:Body>
</soap:Envelope>
```

> [!NOTE]
> <span data-ttu-id="8dc18-139">Der **Gruppen** -Wert wurde verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8dc18-139">The **GroupId** value has been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="8dc18-140">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="8dc18-140">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="8dc18-141">AddNewImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="8dc18-141">AddNewImContactToGroup</span></span>](addnewimcontacttogroup.md)
    
- [<span data-ttu-id="8dc18-142">IMAddress (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="8dc18-142">ImAddress (String)</span></span>](imaddress-string.md)
    
- [<span data-ttu-id="8dc18-143">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="8dc18-143">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="8dc18-144">GroupId</span><span class="sxs-lookup"><span data-stu-id="8dc18-144">GroupId</span></span>](groupid.md)
    
## <a name="successful-addnewimcontacttogroup-operation-response"></a><span data-ttu-id="8dc18-145">Erfolgreiche Reaktion des AddNewImContactToGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="8dc18-145">Successful AddNewImContactToGroup operation response</span></span>

<span data-ttu-id="8dc18-146">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **AddNewImContactToGroup** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="8dc18-146">The following example shows a successful response to an **AddNewImContactToGroup** operation request.</span></span> <span data-ttu-id="8dc18-147">Die Antwort enthält die Person des neu erstellten Kontakts.</span><span class="sxs-lookup"><span data-stu-id="8dc18-147">The response contains the persona of the newly created contact.</span></span> <span data-ttu-id="8dc18-148">Der Kontakt wird dem Ordner Quick Contacts in Exchange hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8dc18-148">The contact is added to the Quick Contacts folder in Exchange.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8dc18-149">Die Bezeichner wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8dc18-149">Identifiers have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="349" 
                         MinorBuildNumber="0" 
                         Version="Exchange2013" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <AddNewImContactToGroupResponse ResponseClass="Success" 
                                    xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Persona>
        <PersonaId Id="AAQkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04ZjU5LWI3MTYzNGNkZmRkYQAQAJ3EkhEEXN5KufGbSYJanZk=" 
                   xmlns="https://schemas.microsoft.com/exchange/services/2006/types" />
        <PersonaType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Person</PersonaType>
        <CreationTime xmlns="https://schemas.microsoft.com/exchange/services/2006/types">2012-01-05T23:06:58Z</CreationTime>
        <DisplayName xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Tony Smith</DisplayName>
        <DisplayNameFirstLast xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Tony Smith</DisplayNameFirstLast>
        <DisplayNameLastFirst xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Tony Smith</DisplayNameLastFirst>
        <FileAsId xmlns="https://schemas.microsoft.com/exchange/services/2006/types">None</FileAsId>
        <EmailAddress xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Tony Smith</Name>
          <Address>tsmith@contoso.com</Address>
          <RoutingType>SMTP</RoutingType>
        </EmailAddress>
        <EmailAddresses xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <EmailAddress>
            <Name>Tony Smith</Name>
            <Address>tsmith@contoso.com</Address>
            <RoutingType>SMTP</RoutingType>
          </EmailAddress>
        </EmailAddresses>
        <ImAddress xmlns="https://schemas.microsoft.com/exchange/services/2006/types">tsmith@contoso.com</ImAddress>
        <RelevanceScore xmlns="https://schemas.microsoft.com/exchange/services/2006/types">2147483647</RelevanceScore>
        <Attributions xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Attribution>
            <Id>0</Id>
            <SourceId Id="BtF8oI7iVOQatt/bhQoTbWAAAAAAvcAAA=" 
                      ChangeKey="EQAAABYAAABtF8oIQoTbWAAAAAAyg" />
            <DisplayName>Outlook</DisplayName>
            <IsWritable>true</IsWritable>
            <IsQuickContact>true</IsQuickContact>
            <IsHidden>false</IsHidden>
            <FolderId Id="AAMkAGQ1MjJjMTBkLTc4YhQoTbWAAAAAAvZAAA=" 
                      ChangeKey="AQAAAA==" />
          </Attribution>
        </Attributions>
        <DisplayNames xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <StringAttributedValue>
            <Value>Tony Smith</Value>
            <Attributions>
              <Attribution>0</Attribution>
            </Attributions>
          </StringAttributedValue>
        </DisplayNames>
        <FileAsIds xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <StringAttributedValue>
            <Value>None</Value>
            <Attributions>
              <Attribution>0</Attribution>
            </Attributions>
          </StringAttributedValue>
        </FileAsIds>
        <Emails1 xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <EmailAddressAttributedValue>
            <Value>
              <Name>Tony Smith</Name>
              <Address>tsmith@contoso.com</Address>
              <RoutingType>SMTP</RoutingType>
            </Value>
            <Attributions>
              <Attribution>0</Attribution>
            </Attributions>
          </EmailAddressAttributedValue>
        </Emails1>
        <ImAddresses xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <StringAttributedValue>
            <Value>tsmith@contoso.com</Value>
            <Attributions>
              <Attribution>0</Attribution>
            </Attributions>
          </StringAttributedValue>
        </ImAddresses>
      </Persona>
    </AddNewImContactToGroupResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="8dc18-150">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="8dc18-150">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="8dc18-151">AddNewImContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="8dc18-151">AddNewImContactToGroupResponse</span></span>](addnewimcontacttogroupresponse.md)
    
- [<span data-ttu-id="8dc18-152">Persona</span><span class="sxs-lookup"><span data-stu-id="8dc18-152">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="8dc18-153">PersonaId</span><span class="sxs-lookup"><span data-stu-id="8dc18-153">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="8dc18-154">Personatype</span><span class="sxs-lookup"><span data-stu-id="8dc18-154">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="8dc18-155">CreationTime</span><span class="sxs-lookup"><span data-stu-id="8dc18-155">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="8dc18-156">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="8dc18-156">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="8dc18-157">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="8dc18-157">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="8dc18-158">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="8dc18-158">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="8dc18-159">FileAsId</span><span class="sxs-lookup"><span data-stu-id="8dc18-159">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="8dc18-160">E-mailemail (e-)</span><span class="sxs-lookup"><span data-stu-id="8dc18-160">EmailAddress (EmailAddressType)</span></span>](emailaddress-emailaddresstype.md)
    
- [<span data-ttu-id="8dc18-161">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="8dc18-161">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="8dc18-162">Address (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="8dc18-162">Address (string)</span></span>](address-string.md)
    
- [<span data-ttu-id="8dc18-163">Routingtype (e-mailemailtype)</span><span class="sxs-lookup"><span data-stu-id="8dc18-163">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="8dc18-164">IMAddress (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="8dc18-164">ImAddress (String)</span></span>](imaddress-string.md)
    
- [<span data-ttu-id="8dc18-165">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="8dc18-165">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="8dc18-166">Zuordnungen (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="8dc18-166">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="8dc18-167">Attribution (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="8dc18-167">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="8dc18-168">ID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="8dc18-168">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="8dc18-169">SourceId</span><span class="sxs-lookup"><span data-stu-id="8dc18-169">SourceId</span></span>](sourceid.md)
    
- [<span data-ttu-id="8dc18-170">Isschreibbar</span><span class="sxs-lookup"><span data-stu-id="8dc18-170">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="8dc18-171">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="8dc18-171">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="8dc18-172">IsHidden</span><span class="sxs-lookup"><span data-stu-id="8dc18-172">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="8dc18-173">FolderId</span><span class="sxs-lookup"><span data-stu-id="8dc18-173">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="8dc18-174">Display Names</span><span class="sxs-lookup"><span data-stu-id="8dc18-174">DisplayNames</span></span>](displaynames.md)
    
- [<span data-ttu-id="8dc18-175">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="8dc18-175">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="8dc18-176">Wert (ArrayOfStringValueType)</span><span class="sxs-lookup"><span data-stu-id="8dc18-176">Value (ArrayOfStringValueType)</span></span>](value-arrayofstringvaluetype.md)
    
- [<span data-ttu-id="8dc18-177">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="8dc18-177">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="8dc18-178">Emails1</span><span class="sxs-lookup"><span data-stu-id="8dc18-178">Emails1</span></span>](emails1.md)
    
- [<span data-ttu-id="8dc18-179">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="8dc18-179">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md)
    
- [<span data-ttu-id="8dc18-180">Imaddresses</span><span class="sxs-lookup"><span data-stu-id="8dc18-180">ImAddresses</span></span>](imaddresses.md)
    
## <a name="addnewimcontacttogroup-operation-error-response"></a><span data-ttu-id="8dc18-181">Fehlerantwort des AddNewImContactToGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="8dc18-181">AddNewImContactToGroup operation error response</span></span>

<span data-ttu-id="8dc18-182">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **AddNewImContactToGroup** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="8dc18-182">The following example shows an error response to a **AddNewImContactToGroup** operation request.</span></span> <span data-ttu-id="8dc18-183">Dies ist eine Antwort auf eine Anforderung zum Hinzufügen eines Kontakts zu einer Gruppe, die sich nicht im Postfach des anfordernden befindet.</span><span class="sxs-lookup"><span data-stu-id="8dc18-183">This is a response to a request to add a contact to a group that is not in the requester's mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="578" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddNewImContactToGroupResponse ResponseClass="Error" 
                                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>No mailbox with such guid.</MessageText>
         <ResponseCode>ErrorNonExistentMailbox</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <MessageXml>
            <t:Value Name="MailboxGuid" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">d5fasdadcw3d-23de-2341-8f59-b71523fsddda</t:Value>
         </MessageXml>
      </AddNewImContactToGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="8dc18-184">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="8dc18-184">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="8dc18-185">AddNewImContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="8dc18-185">AddNewImContactToGroupResponse</span></span>](addnewimcontacttogroupresponse.md)
    
- [<span data-ttu-id="8dc18-186">MessageText</span><span class="sxs-lookup"><span data-stu-id="8dc18-186">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="8dc18-187">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8dc18-187">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8dc18-188">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8dc18-188">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="8dc18-189">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="8dc18-189">MessageXml</span></span>](messagexml.md)
    
<span data-ttu-id="8dc18-190">Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="8dc18-190">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8dc18-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8dc18-191">See also</span></span>



[<span data-ttu-id="8dc18-192">AddImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8dc18-192">AddImGroup operation</span></span>](addimgroup-operation.md)
  
[<span data-ttu-id="8dc18-193">AddImContactToGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8dc18-193">AddImContactToGroup operation</span></span>](addimcontacttogroup-operation.md)
  
[<span data-ttu-id="8dc18-194">AddImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8dc18-194">AddImGroup operation</span></span>](addimgroup-operation.md)
  
[<span data-ttu-id="8dc18-195">RemoveImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8dc18-195">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
  
[<span data-ttu-id="8dc18-196">SetImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8dc18-196">SetImGroup operation</span></span>](setimgroup-operation.md)


[<span data-ttu-id="8dc18-197">Benutzer und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="8dc18-197">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)

