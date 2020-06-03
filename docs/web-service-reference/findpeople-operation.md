---
title: FindPeople-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 446106b7-ff2d-4107-90c1-29f4d38ba128
description: Hier finden Sie Informationen zum FindPeople-EWS-Vorgang.
ms.openlocfilehash: ab5edc3f140e34123ce1f009c401ddd61a0e2598
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462908"
---
# <a name="findpeople-operation"></a><span data-ttu-id="cf2ff-103">FindPeople-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cf2ff-103">FindPeople operation</span></span>

<span data-ttu-id="cf2ff-104">Hier finden Sie Informationen zum **FindPeople** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-104">Find information about the **FindPeople** EWS operation.</span></span> 
  
<span data-ttu-id="cf2ff-105">Der **FindPeople** -Vorgang gibt alle Persona-Objekte aus einem angegebenen Kontaktordner zurück oder ruft Kontakte ab, die mit einer angegebenen Abfragezeichenfolge übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-105">The **FindPeople** operation returns all persona objects from a specified Contacts folder or retrieves contacts that match a specified query string.</span></span> 
  
<span data-ttu-id="cf2ff-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-findpeople-operation"></a><span data-ttu-id="cf2ff-107">Verwenden des FindPeople-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="cf2ff-107">Using the FindPeople operation</span></span>

<span data-ttu-id="cf2ff-108">Der **FindPeople** -Vorgang gibt aggregierte Kontaktinformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-108">The **FindPeople** operation returns aggregated contact information.</span></span> 
  
<span data-ttu-id="cf2ff-109">Der **FindPeople** -Vorgang basiert auf der vorhandenen Funktionalität der komplexen Typen [Restriction](restriction.md) und [BaseShape](baseshape.md) , indem eine Aggregations Einschränkung hinzugefügt und zusätzliche Eigenschaften zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-109">The **FindPeople** operation builds on the existing functionality of the [Restriction](restriction.md) and [BaseShape](baseshape.md) complex types by adding an aggregation restriction and the ability to return additional properties.</span></span> <span data-ttu-id="cf2ff-110">Mithilfe einer Einschränkung kann ein Client Filter wie "nur Ergebnisse mit einer Chat Adresse zurückgeben" angeben.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-110">By using a restriction, a client can specify filters such as "only return results that have an IM address".</span></span> <span data-ttu-id="cf2ff-111">Das Standardsuchverhalten zielt sowohl auf das persönliche Postfach des angegebenen Benutzers als auch auf die globale Adressliste (GAL) ab.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-111">The default search behavior targets both the specified user's personal mailbox and the global address list (GAL).</span></span> <span data-ttu-id="cf2ff-112">Wenn Sie die GAL als primären Suchordner durchsuchen, müssen Sie anstelle einer Einschränkung eine Abfragezeichenfolge angeben, da diese Operation nicht das Durchsuchen der GAL zulässt.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-112">When searching the GAL as the primary search folder, you must specify a query string instead of a restriction, because this operation does not allow for browsing of the GAL.</span></span> 
  
### <a name="findpeople-operation-soap-headers"></a><span data-ttu-id="cf2ff-113">SOAP-Header des FindPeople-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="cf2ff-113">FindPeople operation SOAP headers</span></span>

<span data-ttu-id="cf2ff-114">Der **FindPeople** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-114">The **FindPeople** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="cf2ff-115">**Headername**</span><span class="sxs-lookup"><span data-stu-id="cf2ff-115">**Header name**</span></span>|<span data-ttu-id="cf2ff-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="cf2ff-116">**Element**</span></span>|<span data-ttu-id="cf2ff-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cf2ff-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cf2ff-118">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="cf2ff-118">**Impersonation**</span></span> <br/> |[<span data-ttu-id="cf2ff-119">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="cf2ff-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="cf2ff-120">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-120">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="cf2ff-121">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="cf2ff-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="cf2ff-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="cf2ff-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="cf2ff-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="cf2ff-124">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="cf2ff-125">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="cf2ff-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="cf2ff-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="cf2ff-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="cf2ff-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="cf2ff-128">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="cf2ff-129">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="findpeople-operation-request-example"></a><span data-ttu-id="cf2ff-130">FindPeople-Vorgangsanforderung (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="cf2ff-130">FindPeople operation request example</span></span>

<span data-ttu-id="cf2ff-131">Im folgenden Beispiel einer **FindPeople** -Vorgangsanforderung wird gezeigt, wie die ersten 100-Kontakte aus dem Ordner Kontakte zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-131">The following example of a **FindPeople** operation request shows how to return the first 100 contacts from the Contacts folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:FindPeople>
         <m:IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="100" Offset="0"/>
         <m:ParentFolderId>
            <t:DistinguishedFolderId Id="contacts"/>
         </m:ParentFolderId>
      </m:FindPeople>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="cf2ff-132">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="cf2ff-132">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="cf2ff-133">FindPeople</span><span class="sxs-lookup"><span data-stu-id="cf2ff-133">FindPeople</span></span>](findpeople.md)
    
- [<span data-ttu-id="cf2ff-134">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="cf2ff-134">IndexedPageItemView</span></span>](indexedpageitemview.md)
    
- [<span data-ttu-id="cf2ff-135">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="cf2ff-135">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)
    
- [<span data-ttu-id="cf2ff-136">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="cf2ff-136">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
<span data-ttu-id="cf2ff-137">Im folgenden Beispiel einer **FindPeople** -Vorgangsanforderung wird gezeigt, wie die ersten 100-Kontakte aus der GAL mithilfe einer Abfragezeichenfolge zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-137">The following example of a **FindPeople** operation request shows how to return the first 100 contacts from the GAL by using a query string.</span></span> <span data-ttu-id="cf2ff-138">Durch Festlegen von **DistinguishedFolderId** auf "Directory" wird die GAL als primäre Quelle für Personas durchsucht.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-138">Setting the **DistinguishedFolderId** to "directory" will search the GAL as the primary source of personas.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
    <m:FindPeople>
      <m:PersonaShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="persona:DisplayName"/>
          <t:FieldURI FieldURI="persona:Title"/>
        </t:AdditionalProperties>
      </m:PersonaShape>
      <m:IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="100" Offset="0"/>
      <m:ParentFolderId>
        <t:DistinguishedFolderId Id="directory"/>
      </m:ParentFolderId>
      <m:QueryString>adams</m:QueryString>
    </m:FindPeople>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-findpeople-operation-response"></a><span data-ttu-id="cf2ff-139">Erfolgreiche Reaktion des FindPeople-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="cf2ff-139">Successful FindPeople operation response</span></span>

<span data-ttu-id="cf2ff-140">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **FindPeople** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="cf2ff-140">The following example shows a successful response to a **FindPeople** operation request.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?><s:Envelope 
   xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
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
    <FindPeopleResponse ResponseClass="Success" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <People>
        <Persona xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <PersonaId Id="AAQkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04ZjU5LWI3MTYzNGNkZmRkYQAQAOjFqObcLmtOlzlRnHdXQjo=" />
          <CreationTime>2012-01-11T22:25:37Z</CreationTime>
          <DisplayName>Terry Adams</DisplayName>
          <DisplayNameFirstLast>Terry Adams</DisplayNameFirstLast>
          <DisplayNameLastFirst>Adams Terry</DisplayNameLastFirst>
          <FileAs>Adams, Terry</FileAs>
          <GivenName>Terry</GivenName>
          <Surname>Adams</Surname>
          <EmailAddress>
            <Name>terry@litwareinc.com</Name>
            <EmailAddress>terry@litwareinc.com</EmailAddress>
            <RoutingType>SMTP</RoutingType>
          </EmailAddress>
          <EmailAddresses>
            <EmailAddress>
              <Name>terry@litwareinc.com</Name>
              <EmailAddress>terry@litwareinc.com</EmailAddress>
              <RoutingType>SMTP</RoutingType>
            </EmailAddress>
            <EmailAddress>
              <Name>tadams@contoso.com</Name>
              <EmailAddress>tadams@contoso.com</EmailAddress>
              <RoutingType>SMTP</RoutingType>
            </EmailAddress>
          </EmailAddresses>
          <RelevanceScore>2147483647</RelevanceScore>
        </Persona>
      </People>
      <TotalNumberOfPeopleInView>1</TotalNumberOfPeopleInView>
    </FindPeopleResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="cf2ff-141">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="cf2ff-141">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="cf2ff-142">FindPeopleResponse</span><span class="sxs-lookup"><span data-stu-id="cf2ff-142">FindPeopleResponse</span></span>](findpeopleresponse.md)
    
- [<span data-ttu-id="cf2ff-143">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cf2ff-143">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="cf2ff-144">Personen</span><span class="sxs-lookup"><span data-stu-id="cf2ff-144">People</span></span>](people.md)
    
- [<span data-ttu-id="cf2ff-145">Persona</span><span class="sxs-lookup"><span data-stu-id="cf2ff-145">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="cf2ff-146">PersonaId</span><span class="sxs-lookup"><span data-stu-id="cf2ff-146">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="cf2ff-147">CreationTime</span><span class="sxs-lookup"><span data-stu-id="cf2ff-147">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="cf2ff-148">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="cf2ff-148">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="cf2ff-149">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="cf2ff-149">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="cf2ff-150">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="cf2ff-150">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="cf2ff-151">FileAs</span><span class="sxs-lookup"><span data-stu-id="cf2ff-151">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="cf2ff-152">GivenName</span><span class="sxs-lookup"><span data-stu-id="cf2ff-152">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="cf2ff-153">Nachname</span><span class="sxs-lookup"><span data-stu-id="cf2ff-153">Surname</span></span>](surname.md)
    
- [<span data-ttu-id="cf2ff-154">Emails (ArrayOfEmailAddressesType)</span><span class="sxs-lookup"><span data-stu-id="cf2ff-154">EmailAddresses (ArrayOfEmailAddressesType)</span></span>](emailaddresses-arrayofemailaddressestype.md)
    
- [<span data-ttu-id="cf2ff-155">E-mailemail (e-)</span><span class="sxs-lookup"><span data-stu-id="cf2ff-155">EmailAddress (EmailAddressType)</span></span>](emailaddress-emailaddresstype.md)
    
- [<span data-ttu-id="cf2ff-156">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="cf2ff-156">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="cf2ff-157">E-mailemail (e-)</span><span class="sxs-lookup"><span data-stu-id="cf2ff-157">EmailAddress (EmailAddressType)</span></span>](emailaddress-emailaddresstype.md)
    
- [<span data-ttu-id="cf2ff-158">Routingtype (e-mailemailtype)</span><span class="sxs-lookup"><span data-stu-id="cf2ff-158">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="cf2ff-159">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="cf2ff-159">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="cf2ff-160">TotalNumberOfPeopleInView</span><span class="sxs-lookup"><span data-stu-id="cf2ff-160">TotalNumberOfPeopleInView</span></span>](totalnumberofpeopleinview.md)
    
## <a name="findpeople-operation-error-response"></a><span data-ttu-id="cf2ff-161">Fehlerantwort des FindPeople-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="cf2ff-161">FindPeople operation error response</span></span>

<span data-ttu-id="cf2ff-162">Informationen zu Fehlercodes, die für EWS allgemein sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="cf2ff-162">For error codes that are generic to EWS, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf2ff-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf2ff-163">See also</span></span>

- [<span data-ttu-id="cf2ff-164">Personen und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="cf2ff-164">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="cf2ff-165">GetPersona-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cf2ff-165">GetPersona operation</span></span>](getpersona-operation.md)
    

