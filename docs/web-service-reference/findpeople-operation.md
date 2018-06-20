---
title: FindPeople-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 446106b7-ff2d-4107-90c1-29f4d38ba128
description: Hier finden Sie Informationen über die FindPeople EWS Vorgang.
ms.openlocfilehash: 97c34d7df590d20513e8f1ad476d62f16815a42b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758474"
---
# <a name="findpeople-operation"></a><span data-ttu-id="c3802-103">FindPeople-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c3802-103">FindPeople operation</span></span>

<span data-ttu-id="c3802-104">Hier finden Sie Informationen zum **FindPeople** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c3802-104">Find information about the **FindPeople** EWS operation.</span></span> 
  
<span data-ttu-id="c3802-105">Der Vorgang **FindPeople** alle Persona-Objekte aus einem angegebenen Kontakteordner zurückgegeben oder abgerufen Kontakte, die mit eine Zeichenfolge der angegebenen Abfrage übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="c3802-105">The **FindPeople** operation returns all persona objects from a specified Contacts folder or retrieves contacts that match a specified query string.</span></span> 
  
<span data-ttu-id="c3802-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c3802-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-findpeople-operation"></a><span data-ttu-id="c3802-107">Verwenden des FindPeople-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="c3802-107">Using the FindPeople operation</span></span>

<span data-ttu-id="c3802-108">Der Vorgang **FindPeople** gibt aggregierten Kontaktinformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="c3802-108">The **FindPeople** operation returns aggregated contact information.</span></span> 
  
<span data-ttu-id="c3802-109">Der Vorgang **FindPeople** basiert auf der vorhandenen Funktionalität der [Einschränkung](restriction.md) und [BaseShape](baseshape.md) komplexen Typen durch Hinzufügen einer Einschränkung Aggregation und die Möglichkeit, zusätzliche Eigenschaften zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c3802-109">The **FindPeople** operation builds on the existing functionality of the [Restriction](restriction.md) and [BaseShape](baseshape.md) complex types by adding an aggregation restriction and the ability to return additional properties.</span></span> <span data-ttu-id="c3802-110">Mithilfe einer Einschränkung kann einen Client wie beispielsweise "nur Ergebnisse zurück, die eine IM-Adresse haben" Filter angeben.</span><span class="sxs-lookup"><span data-stu-id="c3802-110">By using a restriction, a client can specify filters such as "only return results that have an IM address".</span></span> <span data-ttu-id="c3802-111">Das Standardverhalten für die Suche beruht auf das angegebene Postfach des Benutzers persönliche und der globalen Adressliste (GAL).</span><span class="sxs-lookup"><span data-stu-id="c3802-111">The default search behavior targets both the specified user's personal mailbox and the global address list (GAL).</span></span> <span data-ttu-id="c3802-112">Bei der Suche der globalen Adressliste als primäre Suchordner müssen Sie eine Abfragezeichenfolge anstelle einer Einschränkung angeben, da dieser Vorgang nicht, zum Durchsuchen der globalen Adressliste zulässt.</span><span class="sxs-lookup"><span data-stu-id="c3802-112">When searching the GAL as the primary search folder, you must specify a query string instead of a restriction, because this operation does not allow for browsing of the GAL.</span></span> 
  
### <a name="findpeople-operation-soap-headers"></a><span data-ttu-id="c3802-113">FindPeople Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="c3802-113">FindPeople operation SOAP headers</span></span>

<span data-ttu-id="c3802-114">Der Vorgang **FindPeople** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="c3802-114">The **FindPeople** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="c3802-115">**Headername**</span><span class="sxs-lookup"><span data-stu-id="c3802-115">**Header name**</span></span>|<span data-ttu-id="c3802-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c3802-116">**Element**</span></span>|<span data-ttu-id="c3802-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c3802-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c3802-118">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="c3802-118">**Impersonation**</span></span> <br/> |[<span data-ttu-id="c3802-119">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="c3802-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="c3802-120">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="c3802-120">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="c3802-121">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c3802-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c3802-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="c3802-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="c3802-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="c3802-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="c3802-124">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="c3802-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="c3802-125">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c3802-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c3802-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="c3802-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="c3802-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c3802-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="c3802-128">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="c3802-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="c3802-129">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="c3802-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="findpeople-operation-request-example"></a><span data-ttu-id="c3802-130">FindPeople Vorgang anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="c3802-130">FindPeople operation request example</span></span>

<span data-ttu-id="c3802-131">Im folgenden Beispiel wird eine **FindPeople** Vorgang Anforderung zeigt, wie die ersten 100 Kontakte aus dem Ordner Kontakte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c3802-131">The following example of a **FindPeople** operation request shows how to return the first 100 contacts from the Contacts folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="c3802-132">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="c3802-132">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c3802-133">FindPeople</span><span class="sxs-lookup"><span data-stu-id="c3802-133">FindPeople</span></span>](findpeople.md)
    
- [<span data-ttu-id="c3802-134">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="c3802-134">IndexedPageItemView</span></span>](indexedpageitemview.md)
    
- [<span data-ttu-id="c3802-135">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="c3802-135">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)
    
- [<span data-ttu-id="c3802-136">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="c3802-136">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
<span data-ttu-id="c3802-137">Im folgenden Beispiel wird eine **FindPeople** Vorgang Anforderung veranschaulicht die ersten 100 Kontakte aus der globalen Adressliste zurückgeben, indem Sie eine Abfragezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c3802-137">The following example of a **FindPeople** operation request shows how to return the first 100 contacts from the GAL by using a query string.</span></span> <span data-ttu-id="c3802-138">Festlegen der **DistinguishedFolderId** "Verzeichnis" wird die globalen Adressliste als primäre Datenquelle Rollen gesucht.</span><span class="sxs-lookup"><span data-stu-id="c3802-138">Setting the **DistinguishedFolderId** to "directory" will search the GAL as the primary source of personas.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="successful-findpeople-operation-response"></a><span data-ttu-id="c3802-139">Erfolgreiche FindPeople Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="c3802-139">Successful FindPeople operation response</span></span>

<span data-ttu-id="c3802-140">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **FindPeople** Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="c3802-140">The following example shows a successful response to a **FindPeople** operation request.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?><s:Envelope 
   xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="349" 
                         MinorBuildNumber="0" 
                         Version="Exchange2013" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <FindPeopleResponse ResponseClass="Success" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <People>
        <Persona xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="c3802-141">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="c3802-141">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c3802-142">FindPeopleResponse</span><span class="sxs-lookup"><span data-stu-id="c3802-142">FindPeopleResponse</span></span>](findpeopleresponse.md)
    
- [<span data-ttu-id="c3802-143">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c3802-143">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c3802-144">Personen</span><span class="sxs-lookup"><span data-stu-id="c3802-144">People</span></span>](people.md)
    
- [<span data-ttu-id="c3802-145">Rolle</span><span class="sxs-lookup"><span data-stu-id="c3802-145">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="c3802-146">PersonaId</span><span class="sxs-lookup"><span data-stu-id="c3802-146">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="c3802-147">CreationTime</span><span class="sxs-lookup"><span data-stu-id="c3802-147">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="c3802-148">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="c3802-148">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="c3802-149">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="c3802-149">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="c3802-150">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="c3802-150">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="c3802-151">FileAs</span><span class="sxs-lookup"><span data-stu-id="c3802-151">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="c3802-152">Vorname</span><span class="sxs-lookup"><span data-stu-id="c3802-152">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="c3802-153">Nachname</span><span class="sxs-lookup"><span data-stu-id="c3802-153">Surname</span></span>](surname.md)
    
- [<span data-ttu-id="c3802-154">EmailAddresses (ArrayOfEmailAddressesType)</span><span class="sxs-lookup"><span data-stu-id="c3802-154">EmailAddresses (ArrayOfEmailAddressesType)</span></span>](emailaddresses-arrayofemailaddressestype.md)
    
- [<span data-ttu-id="c3802-155">EmailAddress (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="c3802-155">EmailAddress (EmailAddressType)</span></span>](emailaddress-emailaddresstype.md)
    
- [<span data-ttu-id="c3802-156">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="c3802-156">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="c3802-157">EmailAddress (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="c3802-157">EmailAddress (EmailAddressType)</span></span>](emailaddress-emailaddresstype.md)
    
- [<span data-ttu-id="c3802-158">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="c3802-158">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="c3802-159">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="c3802-159">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="c3802-160">TotalNumberOfPeopleInView</span><span class="sxs-lookup"><span data-stu-id="c3802-160">TotalNumberOfPeopleInView</span></span>](totalnumberofpeopleinview.md)
    
## <a name="findpeople-operation-error-response"></a><span data-ttu-id="c3802-161">FindPeople Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="c3802-161">FindPeople operation error response</span></span>

<span data-ttu-id="c3802-162">Fehlercodes, die für EWS generisch sind, finden Sie unter [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="c3802-162">For error codes that are generic to EWS, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c3802-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3802-163">See also</span></span>

- [<span data-ttu-id="c3802-164">Benutzer und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="c3802-164">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="c3802-165">GetPersona-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c3802-165">GetPersona operation</span></span>](getpersona-operation.md)
    

