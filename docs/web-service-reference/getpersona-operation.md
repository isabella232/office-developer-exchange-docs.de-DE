---
title: GetPersona-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e2146df0-53d0-4caf-9758-b600bbc14b6a
description: Hier finden Sie Informationen über die GetPersona EWS Vorgang.
ms.openlocfilehash: c6ac357eaa34e9bae2fe0a79a4a2d02449100e78
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758770"
---
# <a name="getpersona-operation"></a><span data-ttu-id="e2d5f-103">GetPersona-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e2d5f-103">GetPersona operation</span></span>

<span data-ttu-id="e2d5f-104">Hier finden Sie Informationen zum **GetPersona** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-104">Find information about the **GetPersona** EWS operation.</span></span> 
  
<span data-ttu-id="e2d5f-105">Der Vorgang **GetPersona** gibt einen Satz von Eigenschaften, die einer Rolle zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-105">The **GetPersona** operation returns a set of properties that are associated with a persona.</span></span> 
  
<span data-ttu-id="e2d5f-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getpersona-operation"></a><span data-ttu-id="e2d5f-107">Verwenden des GetPersona-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="e2d5f-107">Using the GetPersona operation</span></span>

<span data-ttu-id="e2d5f-108">Der Vorgang **GetPersona** bietet Zugriff auf aggregierten Kontaktinformationen in Form einer Rolle.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-108">The **GetPersona** operation provides access to aggregated contact information in the form of a persona.</span></span> <span data-ttu-id="e2d5f-109">Das [PersonaId](personaid.md) -Element in der Anforderung identifiziert die Rolle in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-109">The [PersonaId](personaid.md) element in the request identifies the persona to return in the response.</span></span> <span data-ttu-id="e2d5f-110">Die Antwort kann einen Standardsatz Eigenschaften Rolle oder einen benutzerdefinierten Eigenschaftensatz enthalten.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-110">The response can contain a default set of persona properties or a custom property set.</span></span> <span data-ttu-id="e2d5f-111">Es wird empfohlen, dass Sie angeben, dass eine benutzerdefinierte Eigenschaft festlegen, sodass Sie nicht verwendete Eigenschaften nicht verarbeitet und vom Server an den Client gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-111">We recommend that you specify a custom property set so that unused properties are not processed and sent from the server to the client.</span></span> 
  
### <a name="getpersona-operation-soap-headers"></a><span data-ttu-id="e2d5f-112">GetPersona Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="e2d5f-112">GetPersona operation SOAP headers</span></span>

<span data-ttu-id="e2d5f-113">Der Vorgang **GetPersona** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-113">The **GetPersona** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="e2d5f-114">**Headername**</span><span class="sxs-lookup"><span data-stu-id="e2d5f-114">**Header name**</span></span>|<span data-ttu-id="e2d5f-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="e2d5f-115">**Element**</span></span>|<span data-ttu-id="e2d5f-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2d5f-116">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e2d5f-117">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="e2d5f-117">**Impersonation**</span></span> <br/> |[<span data-ttu-id="e2d5f-118">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="e2d5f-118">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="e2d5f-119">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-119">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="e2d5f-120">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-120">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e2d5f-121">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="e2d5f-121">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="e2d5f-122">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="e2d5f-122">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="e2d5f-123">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-123">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="e2d5f-124">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-124">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e2d5f-125">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="e2d5f-125">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="e2d5f-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e2d5f-126">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="e2d5f-127">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-127">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="e2d5f-128">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-128">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getpersona-operation-request-example-return-a-default-set-of-properties-for-a-persona"></a><span data-ttu-id="e2d5f-129">GetPersona Vorgang-anforderungsbeispiel: Zurückgeben von einen Standardsatz Eigenschaften für eine Rolle</span><span class="sxs-lookup"><span data-stu-id="e2d5f-129">GetPersona operation request example: Return a default set of properties for a persona</span></span>

<span data-ttu-id="e2d5f-130">Im folgenden Beispiel wird eine **GetPersona** Vorgang Anforderung zeigt, wie einen Standardsatz Eigenschaften zurückgegeben, die einer Rolle zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-130">The following example of a **GetPersona** operation request shows how to return a default set of properties that are associated with a persona.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013"/>
   </soap:Header>
   <soap:Body xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <GetPersona>
         <PersonaId Id="AAQkADEzAQAKtOtR/l4MlLqHWORfhSYKU="/>
      </GetPersona>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="e2d5f-131">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="e2d5f-131">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e2d5f-132">GetPersona</span><span class="sxs-lookup"><span data-stu-id="e2d5f-132">GetPersona</span></span>](getpersona.md)
    
- [<span data-ttu-id="e2d5f-133">PersonaId</span><span class="sxs-lookup"><span data-stu-id="e2d5f-133">PersonaId</span></span>](personaid.md)
    
## <a name="successful-getpersona-operation-response"></a><span data-ttu-id="e2d5f-134">Erfolgreiche GetPersona Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="e2d5f-134">Successful GetPersona operation response</span></span>

<span data-ttu-id="e2d5f-135">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetPersona** Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-135">The following example shows a successful response to a **GetPersona** operation request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e2d5f-136">Bezeichner für alle Elemente aus, und Ändern von Schlüsseln in diesem Artikel wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-136">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="432" 
                           MinorBuildNumber="5" 
                           Version="Exchange2013"
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                     xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetPersonaResponseMessage ResponseClass="Success"
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <Persona>
            <PersonaId Id="AAQkADEzAQAKtOtR="
              xmlns="http://schemas.microsoft.com/exchange/services/2006/types"/>
            <PersonaType xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Person</PersonaType>
            <CreationTime xmlns="http://schemas.microsoft.com/exchange/services/2006/types">2012-06-01T17:00:34Z</CreationTime>
            <DisplayName xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Brian Johnson</DisplayName>
            <DisplayNameFirstLast xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Brian Johnson</DisplayNameFirstLast>
            <DisplayNameLastFirst xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Johnson Brian</DisplayNameLastFirst>
            <FileAs xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Johnson, Brian</FileAs>
            <FileAsId xmlns="http://schemas.microsoft.com/exchange/services/2006/types">None</FileAsId>
            <GivenName xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Brian</GivenName>
            <Surname xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Johnsoon</Surname>
            <CompanyName xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Contoso</CompanyName>
            <RelevanceScore xmlns="http://schemas.microsoft.com/exchange/services/2006/types">4255550110</RelevanceScore>
            <Attributions xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
            <DisplayNames xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Brian Johnson</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </DisplayNames>
            <FileAses xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Johnson, Brian</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </FileAses>
            <FileAsIds xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>None</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </FileAsIds>
            <GivenNames xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Brian</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </GivenNames>
            <Surnames xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Johnson</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </Surnames>
            <MobilePhones xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
            <CompanyNames xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="e2d5f-137">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="e2d5f-137">The response SOAP body contains the following elements:</span></span>
  
- <span data-ttu-id="e2d5f-138">GetPersonaResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e2d5f-138">GetPersonaResponseMessage</span></span>
    
- [<span data-ttu-id="e2d5f-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e2d5f-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e2d5f-140">Rolle</span><span class="sxs-lookup"><span data-stu-id="e2d5f-140">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="e2d5f-141">PersonaId</span><span class="sxs-lookup"><span data-stu-id="e2d5f-141">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="e2d5f-142">PersonaType</span><span class="sxs-lookup"><span data-stu-id="e2d5f-142">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="e2d5f-143">CreationTime</span><span class="sxs-lookup"><span data-stu-id="e2d5f-143">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="e2d5f-144">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="e2d5f-144">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="e2d5f-145">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="e2d5f-145">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="e2d5f-146">FileAs</span><span class="sxs-lookup"><span data-stu-id="e2d5f-146">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="e2d5f-147">FileAsId</span><span class="sxs-lookup"><span data-stu-id="e2d5f-147">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="e2d5f-148">Vorname</span><span class="sxs-lookup"><span data-stu-id="e2d5f-148">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="e2d5f-149">Nachname</span><span class="sxs-lookup"><span data-stu-id="e2d5f-149">Surname</span></span>](surname.md)
    
- [<span data-ttu-id="e2d5f-150">Firma</span><span class="sxs-lookup"><span data-stu-id="e2d5f-150">CompanyName</span></span>](companyname.md)
    
- [<span data-ttu-id="e2d5f-151">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="e2d5f-151">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="e2d5f-152">Hinweise (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="e2d5f-152">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md)
    
- [<span data-ttu-id="e2d5f-153">Zuweisung (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="e2d5f-153">Attribution (string)</span></span>](attribution-string.md)
    
- [<span data-ttu-id="e2d5f-154">ID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="e2d5f-154">ID (String)</span></span>](id-string.md)
    
- <span data-ttu-id="e2d5f-155">[SourceId](sourceid.md) SourceId</span><span class="sxs-lookup"><span data-stu-id="e2d5f-155">[SourceId](sourceid.md) SourceId</span></span> 
    
- [<span data-ttu-id="e2d5f-156">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="e2d5f-156">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="e2d5f-157">IsWritable</span><span class="sxs-lookup"><span data-stu-id="e2d5f-157">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="e2d5f-158">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="e2d5f-158">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="e2d5f-159">IsHidden</span><span class="sxs-lookup"><span data-stu-id="e2d5f-159">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="e2d5f-160">FolderId</span><span class="sxs-lookup"><span data-stu-id="e2d5f-160">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="e2d5f-161">DisplayNames</span><span class="sxs-lookup"><span data-stu-id="e2d5f-161">DisplayNames</span></span>](displaynames.md)
    
- [<span data-ttu-id="e2d5f-162">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="e2d5f-162">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="e2d5f-163">Wert (ArrayOfStringValueType)</span><span class="sxs-lookup"><span data-stu-id="e2d5f-163">Value (ArrayOfStringValueType)</span></span>](value-arrayofstringvaluetype.md)
    
- [<span data-ttu-id="e2d5f-164">Hinweise (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="e2d5f-164">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="e2d5f-165">Zuweisung (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="e2d5f-165">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="e2d5f-166">FileAses</span><span class="sxs-lookup"><span data-stu-id="e2d5f-166">FileAses</span></span>](fileases.md)
    
- [<span data-ttu-id="e2d5f-167">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="e2d5f-167">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="e2d5f-168">GivenNames</span><span class="sxs-lookup"><span data-stu-id="e2d5f-168">GivenNames</span></span>](givennames.md)
    
- [<span data-ttu-id="e2d5f-169">Nachnamen</span><span class="sxs-lookup"><span data-stu-id="e2d5f-169">Surnames</span></span>](surnames.md)
    
- [<span data-ttu-id="e2d5f-170">MobilePhones</span><span class="sxs-lookup"><span data-stu-id="e2d5f-170">MobilePhones</span></span>](mobilephones.md)
    
- [<span data-ttu-id="e2d5f-171">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="e2d5f-171">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md)
    
- [<span data-ttu-id="e2d5f-172">Wert (PersonaPhoneNumberType)</span><span class="sxs-lookup"><span data-stu-id="e2d5f-172">Value (PersonaPhoneNumberType)</span></span>](value-personaphonenumbertype.md)
    
- [<span data-ttu-id="e2d5f-173">Nummer</span><span class="sxs-lookup"><span data-stu-id="e2d5f-173">Number</span></span>](number.md)
    
- [<span data-ttu-id="e2d5f-174">Typ (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="e2d5f-174">Type (string)</span></span>](type-string.md)
    
- [<span data-ttu-id="e2d5f-175">CompanyNames</span><span class="sxs-lookup"><span data-stu-id="e2d5f-175">CompanyNames</span></span>](companynames.md)
    
## <a name="getpersona-operation-error-response"></a><span data-ttu-id="e2d5f-176">GetPersona Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="e2d5f-176">GetPersona operation error response</span></span>

<span data-ttu-id="e2d5f-177">Das folgende Beispiel zeigt eine Fehlerantwort an eine **GetPersona** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-177">The following example shows an error response to a **GetPersona** operation request.</span></span> <span data-ttu-id="e2d5f-178">Dies ist eine Antwort auf eine Anforderung, die ein Bezeichner falsch angegebenen Rolle enthält.</span><span class="sxs-lookup"><span data-stu-id="e2d5f-178">This is a response to a request that contains an incorrectly specified persona identifier.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="578" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetPersonaResponseMessage ResponseClass="Error" 
                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Id is malformed.</MessageText>
         <ResponseCode>ErrorInvalidIdMalformed</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetPersonaResponseMessage>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="e2d5f-179">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="e2d5f-179">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e2d5f-180">GetPersonaResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e2d5f-180">GetPersonaResponseMessage</span></span>](getpersonaresponsemessage.md)
    
- [<span data-ttu-id="e2d5f-181">MessageText</span><span class="sxs-lookup"><span data-stu-id="e2d5f-181">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="e2d5f-182">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e2d5f-182">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e2d5f-183">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e2d5f-183">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="e2d5f-184">Zusätzliche Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="e2d5f-184">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e2d5f-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2d5f-185">See also</span></span>

- [<span data-ttu-id="e2d5f-186">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="e2d5f-186">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="e2d5f-187">Benutzer und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e2d5f-187">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="e2d5f-188">FindPeople-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e2d5f-188">FindPeople operation</span></span>](findpeople-operation.md)
    

