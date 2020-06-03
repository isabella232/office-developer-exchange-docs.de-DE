---
title: GetPersona-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e2146df0-53d0-4caf-9758-b600bbc14b6a
description: Hier finden Sie Informationen zum EWS-Vorgang getpersona.
ms.openlocfilehash: 2b335c694a85f87c96432ea6d7c1c674613d2f17
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460946"
---
# <a name="getpersona-operation"></a><span data-ttu-id="f8a6e-103">GetPersona-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f8a6e-103">GetPersona operation</span></span>

<span data-ttu-id="f8a6e-104">Hier finden Sie Informationen zum EWS-Vorgang **getpersona** .</span><span class="sxs-lookup"><span data-stu-id="f8a6e-104">Find information about the **GetPersona** EWS operation.</span></span> 
  
<span data-ttu-id="f8a6e-105">Der **getpersona** -Vorgang gibt eine Gruppe von Eigenschaften zurück, die einer Rolle zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f8a6e-105">The **GetPersona** operation returns a set of properties that are associated with a persona.</span></span> 
  
<span data-ttu-id="f8a6e-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f8a6e-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getpersona-operation"></a><span data-ttu-id="f8a6e-107">Verwenden des getpersona-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f8a6e-107">Using the GetPersona operation</span></span>

<span data-ttu-id="f8a6e-108">Der **getpersona** -Vorgang ermöglicht den Zugriff auf aggregierte Kontaktinformationen in Form einer Persona.</span><span class="sxs-lookup"><span data-stu-id="f8a6e-108">The **GetPersona** operation provides access to aggregated contact information in the form of a persona.</span></span> <span data-ttu-id="f8a6e-109">Das [Persona](personaid.md) -Element in der Anforderung gibt die Rolle an, die in der Antwort zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8a6e-109">The [PersonaId](personaid.md) element in the request identifies the persona to return in the response.</span></span> <span data-ttu-id="f8a6e-110">Die Antwort kann eine Standardgruppe von Persona-Eigenschaften oder einen benutzerdefinierten Eigenschaftensatz enthalten.</span><span class="sxs-lookup"><span data-stu-id="f8a6e-110">The response can contain a default set of persona properties or a custom property set.</span></span> <span data-ttu-id="f8a6e-111">Es wird empfohlen, einen benutzerdefinierten Eigenschaften festzulegen, damit nicht verwendete Eigenschaften nicht verarbeitet und vom Server an den Client gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8a6e-111">We recommend that you specify a custom property set so that unused properties are not processed and sent from the server to the client.</span></span> 
  
### <a name="getpersona-operation-soap-headers"></a><span data-ttu-id="f8a6e-112">SOAP-Kopfzeilen des getpersona-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f8a6e-112">GetPersona operation SOAP headers</span></span>

<span data-ttu-id="f8a6e-113">Der **getpersona** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f8a6e-113">The **GetPersona** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="f8a6e-114">**Headername**</span><span class="sxs-lookup"><span data-stu-id="f8a6e-114">**Header name**</span></span>|<span data-ttu-id="f8a6e-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="f8a6e-115">**Element**</span></span>|<span data-ttu-id="f8a6e-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f8a6e-116">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f8a6e-117">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="f8a6e-117">**Impersonation**</span></span> <br/> |[<span data-ttu-id="f8a6e-118">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="f8a6e-118">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="f8a6e-119">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="f8a6e-119">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="f8a6e-120">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f8a6e-120">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f8a6e-121">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="f8a6e-121">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="f8a6e-122">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="f8a6e-122">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="f8a6e-123">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="f8a6e-123">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="f8a6e-124">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f8a6e-124">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f8a6e-125">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="f8a6e-125">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="f8a6e-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f8a6e-126">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="f8a6e-127">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="f8a6e-127">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="f8a6e-128">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="f8a6e-128">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getpersona-operation-request-example-return-a-default-set-of-properties-for-a-persona"></a><span data-ttu-id="f8a6e-129">Getpersona-Vorgangs Anforderungs Beispiel: Zurückgeben eines Standardsatzes von Eigenschaften für eine Rolle</span><span class="sxs-lookup"><span data-stu-id="f8a6e-129">GetPersona operation request example: Return a default set of properties for a persona</span></span>

<span data-ttu-id="f8a6e-130">Im folgenden Beispiel einer **getpersona** -Vorgangsanforderung wird gezeigt, wie eine Standardgruppe von Eigenschaften zurückgegeben wird, die einer Rolle zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f8a6e-130">The following example of a **GetPersona** operation request shows how to return a default set of properties that are associated with a persona.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013"/>
   </soap:Header>
   <soap:Body xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <GetPersona>
         <PersonaId Id="AAQkADEzAQAKtOtR/l4MlLqHWORfhSYKU="/>
      </GetPersona>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="f8a6e-131">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="f8a6e-131">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f8a6e-132">GetPersona</span><span class="sxs-lookup"><span data-stu-id="f8a6e-132">GetPersona</span></span>](getpersona.md)
    
- [<span data-ttu-id="f8a6e-133">PersonaId</span><span class="sxs-lookup"><span data-stu-id="f8a6e-133">PersonaId</span></span>](personaid.md)
    
## <a name="successful-getpersona-operation-response"></a><span data-ttu-id="f8a6e-134">Erfolgreiche getpersona-Vorgangs Antwort</span><span class="sxs-lookup"><span data-stu-id="f8a6e-134">Successful GetPersona operation response</span></span>

<span data-ttu-id="f8a6e-135">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Vorgangsanforderung von **getpersona** .</span><span class="sxs-lookup"><span data-stu-id="f8a6e-135">The following example shows a successful response to a **GetPersona** operation request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f8a6e-136">Alle Element-IDs und Änderungsschlüssel in diesem Artikel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f8a6e-136">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="432" 
                           MinorBuildNumber="5" 
                           Version="Exchange2013"
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                     xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetPersonaResponseMessage ResponseClass="Success"
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <Persona>
            <PersonaId Id="AAQkADEzAQAKtOtR="
              xmlns="https://schemas.microsoft.com/exchange/services/2006/types"/>
            <PersonaType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Person</PersonaType>
            <CreationTime xmlns="https://schemas.microsoft.com/exchange/services/2006/types">2012-06-01T17:00:34Z</CreationTime>
            <DisplayName xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Brian Johnson</DisplayName>
            <DisplayNameFirstLast xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Brian Johnson</DisplayNameFirstLast>
            <DisplayNameLastFirst xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Johnson Brian</DisplayNameLastFirst>
            <FileAs xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Johnson, Brian</FileAs>
            <FileAsId xmlns="https://schemas.microsoft.com/exchange/services/2006/types">None</FileAsId>
            <GivenName xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Brian</GivenName>
            <Surname xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Johnsoon</Surname>
            <CompanyName xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Contoso</CompanyName>
            <RelevanceScore xmlns="https://schemas.microsoft.com/exchange/services/2006/types">4255550110</RelevanceScore>
            <Attributions xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Attribution>
                  <Id>0</Id>
                  <SourceId Id="AAMkA =" ChangeKey="EQAAABY+"/>
                  <DisplayName>Outlook</DisplayName>
                  <IsWritable>true</IsWritable>
                  <IsQuickContact>false</IsQuickContact>
                  <IsHidden>false</IsHidden>
                  <FolderId Id="AAMkA=" ChangeKey="AQAAAA=="/>
               </Attribution>
            </Attributions>
            <DisplayNames xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Brian Johnson</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </DisplayNames>
            <FileAses xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Johnson, Brian</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </FileAses>
            <FileAsIds xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>None</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </FileAsIds>
            <GivenNames xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Brian</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </GivenNames>
            <Surnames xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Johnson</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </Surnames>
            <MobilePhones xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <PhoneNumberAttributedValue>
                  <Value>
                     <Number>(425)555-0110</Number>
                     <Type>Mobile</Type>
                  </Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </PhoneNumberAttributedValue>
            </MobilePhones>
            <CompanyNames xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Contoso</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </CompanyNames>
         </Persona>
      </GetPersonaResponseMessage>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="f8a6e-137">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="f8a6e-137">The response SOAP body contains the following elements:</span></span>
  
- <span data-ttu-id="f8a6e-138">GetPersonaResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f8a6e-138">GetPersonaResponseMessage</span></span>
    
- [<span data-ttu-id="f8a6e-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f8a6e-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f8a6e-140">Persona</span><span class="sxs-lookup"><span data-stu-id="f8a6e-140">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="f8a6e-141">PersonaId</span><span class="sxs-lookup"><span data-stu-id="f8a6e-141">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="f8a6e-142">Personatype</span><span class="sxs-lookup"><span data-stu-id="f8a6e-142">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="f8a6e-143">CreationTime</span><span class="sxs-lookup"><span data-stu-id="f8a6e-143">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="f8a6e-144">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="f8a6e-144">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="f8a6e-145">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="f8a6e-145">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="f8a6e-146">FileAs</span><span class="sxs-lookup"><span data-stu-id="f8a6e-146">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="f8a6e-147">FileAsId</span><span class="sxs-lookup"><span data-stu-id="f8a6e-147">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="f8a6e-148">GivenName</span><span class="sxs-lookup"><span data-stu-id="f8a6e-148">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="f8a6e-149">Nachname</span><span class="sxs-lookup"><span data-stu-id="f8a6e-149">Surname</span></span>](surname.md)
    
- [<span data-ttu-id="f8a6e-150">CompanyName</span><span class="sxs-lookup"><span data-stu-id="f8a6e-150">CompanyName</span></span>](companyname.md)
    
- [<span data-ttu-id="f8a6e-151">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="f8a6e-151">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="f8a6e-152">Zuordnungen (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="f8a6e-152">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md)
    
- [<span data-ttu-id="f8a6e-153">Attribution (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="f8a6e-153">Attribution (string)</span></span>](attribution-string.md)
    
- [<span data-ttu-id="f8a6e-154">ID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="f8a6e-154">ID (String)</span></span>](id-string.md)
    
- <span data-ttu-id="f8a6e-155">[Quell](sourceid.md) -Nr SourceID</span><span class="sxs-lookup"><span data-stu-id="f8a6e-155">[SourceId](sourceid.md) SourceId</span></span> 
    
- [<span data-ttu-id="f8a6e-156">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="f8a6e-156">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="f8a6e-157">Isschreibbar</span><span class="sxs-lookup"><span data-stu-id="f8a6e-157">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="f8a6e-158">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="f8a6e-158">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="f8a6e-159">IsHidden</span><span class="sxs-lookup"><span data-stu-id="f8a6e-159">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="f8a6e-160">FolderId</span><span class="sxs-lookup"><span data-stu-id="f8a6e-160">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="f8a6e-161">Display Names</span><span class="sxs-lookup"><span data-stu-id="f8a6e-161">DisplayNames</span></span>](displaynames.md)
    
- [<span data-ttu-id="f8a6e-162">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="f8a6e-162">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="f8a6e-163">Wert (ArrayOfStringValueType)</span><span class="sxs-lookup"><span data-stu-id="f8a6e-163">Value (ArrayOfStringValueType)</span></span>](value-arrayofstringvaluetype.md)
    
- [<span data-ttu-id="f8a6e-164">Zuordnungen (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="f8a6e-164">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="f8a6e-165">Attribution (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="f8a6e-165">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="f8a6e-166">FileAses</span><span class="sxs-lookup"><span data-stu-id="f8a6e-166">FileAses</span></span>](fileases.md)
    
- [<span data-ttu-id="f8a6e-167">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="f8a6e-167">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="f8a6e-168">GivenNames</span><span class="sxs-lookup"><span data-stu-id="f8a6e-168">GivenNames</span></span>](givennames.md)
    
- [<span data-ttu-id="f8a6e-169">Nachnamen</span><span class="sxs-lookup"><span data-stu-id="f8a6e-169">Surnames</span></span>](surnames.md)
    
- [<span data-ttu-id="f8a6e-170">Handys</span><span class="sxs-lookup"><span data-stu-id="f8a6e-170">MobilePhones</span></span>](mobilephones.md)
    
- [<span data-ttu-id="f8a6e-171">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="f8a6e-171">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md)
    
- [<span data-ttu-id="f8a6e-172">Wert (PersonaPhoneNumberType)</span><span class="sxs-lookup"><span data-stu-id="f8a6e-172">Value (PersonaPhoneNumberType)</span></span>](value-personaphonenumbertype.md)
    
- [<span data-ttu-id="f8a6e-173">Number</span><span class="sxs-lookup"><span data-stu-id="f8a6e-173">Number</span></span>](number.md)
    
- [<span data-ttu-id="f8a6e-174">Typ (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="f8a6e-174">Type (string)</span></span>](type-string.md)
    
- [<span data-ttu-id="f8a6e-175">Companynames</span><span class="sxs-lookup"><span data-stu-id="f8a6e-175">CompanyNames</span></span>](companynames.md)
    
## <a name="getpersona-operation-error-response"></a><span data-ttu-id="f8a6e-176">Getpersona-Operation-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="f8a6e-176">GetPersona operation error response</span></span>

<span data-ttu-id="f8a6e-177">Das folgende Beispiel zeigt eine Fehlerantwort auf eine Vorgangsanforderung von **getpersona** .</span><span class="sxs-lookup"><span data-stu-id="f8a6e-177">The following example shows an error response to a **GetPersona** operation request.</span></span> <span data-ttu-id="f8a6e-178">Dies ist eine Antwort auf eine Anforderung, die eine falsch angegebene Persona-ID enthält.</span><span class="sxs-lookup"><span data-stu-id="f8a6e-178">This is a response to a request that contains an incorrectly specified persona identifier.</span></span> 
  
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
      <GetPersonaResponseMessage ResponseClass="Error" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Id is malformed.</MessageText>
         <ResponseCode>ErrorInvalidIdMalformed</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetPersonaResponseMessage>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="f8a6e-179">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="f8a6e-179">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f8a6e-180">GetPersonaResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f8a6e-180">GetPersonaResponseMessage</span></span>](getpersonaresponsemessage.md)
    
- [<span data-ttu-id="f8a6e-181">MessageText</span><span class="sxs-lookup"><span data-stu-id="f8a6e-181">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="f8a6e-182">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f8a6e-182">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f8a6e-183">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f8a6e-183">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="f8a6e-184">Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="f8a6e-184">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f8a6e-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8a6e-185">See also</span></span>

- [<span data-ttu-id="f8a6e-186">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="f8a6e-186">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="f8a6e-187">Personen und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f8a6e-187">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="f8a6e-188">FindPeople-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f8a6e-188">FindPeople operation</span></span>](findpeople-operation.md)
    

