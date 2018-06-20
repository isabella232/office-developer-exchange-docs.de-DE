---
title: GetClientAccessToken-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 086876cc-e22c-4e89-89f9-19e78af51217
description: Hier finden Sie Informationen über die GetClientAccessToken EWS Vorgang.
ms.openlocfilehash: afa9a315a8421f31c345c9547a5d80bed41e9fbc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758597"
---
# <a name="getclientaccesstoken-operation"></a><span data-ttu-id="a2f4e-103">GetClientAccessToken-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a2f4e-103">GetClientAccessToken operation</span></span>

<span data-ttu-id="a2f4e-104">Hier finden Sie Informationen zum **GetClientAccessToken** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="a2f4e-104">Find information about the **GetClientAccessToken** EWS operation.</span></span> 
  
<span data-ttu-id="a2f4e-105">Der Vorgang **GetClientAccessToken** Ruft ein Client Access-token für eine Mail-app für Outlook.</span><span class="sxs-lookup"><span data-stu-id="a2f4e-105">The **GetClientAccessToken** operation gets a client access token for a mail app for Outlook.</span></span> 
  
<span data-ttu-id="a2f4e-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a2f4e-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getclientaccesstoken-operation"></a><span data-ttu-id="a2f4e-107">Verwenden des GetClientAccessToken-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="a2f4e-107">Using the GetClientAccessToken operation</span></span>

<span data-ttu-id="a2f4e-108">Die Anforderung **GetClientAccessToken** Vorgang enthält zwei erforderliche Argumente: der Bezeichner der app und den Typ des Tokens.</span><span class="sxs-lookup"><span data-stu-id="a2f4e-108">The **GetClientAccessToken** operation request takes two required arguments: the identifier of the app, and the token type.</span></span> <span data-ttu-id="a2f4e-109">Die [GetAppManifests-Vorgang](getappmanifests-operation.md) können Sie die app-ID anfordern.</span><span class="sxs-lookup"><span data-stu-id="a2f4e-109">You can use the [GetAppManifests operation](getappmanifests-operation.md) to request the app identifier.</span></span> 
  
### <a name="getclientaccesstoken-operation-soap-headers"></a><span data-ttu-id="a2f4e-110">GetClientAccessToken Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="a2f4e-110">GetClientAccessToken operation SOAP headers</span></span>

<span data-ttu-id="a2f4e-111">Der Vorgang **GetClientAccessToken** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="a2f4e-111">The **GetClientAccessToken** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="a2f4e-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="a2f4e-112">**Header name**</span></span>|<span data-ttu-id="a2f4e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a2f4e-113">**Element**</span></span>|<span data-ttu-id="a2f4e-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a2f4e-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a2f4e-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="a2f4e-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="a2f4e-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="a2f4e-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="a2f4e-117">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="a2f4e-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="a2f4e-118">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a2f4e-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="a2f4e-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="a2f4e-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="a2f4e-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a2f4e-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="a2f4e-121">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="a2f4e-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="a2f4e-122">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="a2f4e-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getclientaccesstoken-operation-request-example-get-a-caller-identity-token"></a><span data-ttu-id="a2f4e-123">GetClientAccessToken Vorgang-anforderungsbeispiel: Abrufen einer anruferidentität token</span><span class="sxs-lookup"><span data-stu-id="a2f4e-123">GetClientAccessToken operation request example: Get a caller identity token</span></span>

<span data-ttu-id="a2f4e-124">Im folgenden Beispiel wird eine **GetClientAccessToken** Vorgang Anforderung veranschaulicht, wie eine anruferidentität für eine app token abrufen.</span><span class="sxs-lookup"><span data-stu-id="a2f4e-124">The following example of a **GetClientAccessToken** operation request shows how to get a caller identity token for an app.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetClientAccessToken>
         <m:TokenRequests>
            <t:TokenRequest>
               <t:Id>1C50226D-04B5-4AB2-9FCD-42E236B59E4B</t:Id>
               <t:TokenType>CallerIdentity</t:TokenType>
            </t:TokenRequest>
         </m:TokenRequests>
      </m:GetClientAccessToken>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="a2f4e-125">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="a2f4e-125">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="a2f4e-126">GetClientAccessToken</span><span class="sxs-lookup"><span data-stu-id="a2f4e-126">GetClientAccessToken</span></span>](getclientaccesstoken.md)
    
- [<span data-ttu-id="a2f4e-127">TokenRequests</span><span class="sxs-lookup"><span data-stu-id="a2f4e-127">TokenRequests</span></span>](tokenrequests.md)
    
- [<span data-ttu-id="a2f4e-128">TokenRequest</span><span class="sxs-lookup"><span data-stu-id="a2f4e-128">TokenRequest</span></span>](tokenrequest.md)
    
- [<span data-ttu-id="a2f4e-129">ID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="a2f4e-129">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="a2f4e-130">"TokenType"</span><span class="sxs-lookup"><span data-stu-id="a2f4e-130">TokenType</span></span>](tokentype.md)
    
## <a name="successful-getclientaccesstoken-operation-response"></a><span data-ttu-id="a2f4e-131">Erfolgreiche GetClientAccessToken Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="a2f4e-131">Successful GetClientAccessToken operation response</span></span>

<span data-ttu-id="a2f4e-132">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetClientAccessToken** Vorgang an eine anruferidentität für eine app token abrufen.</span><span class="sxs-lookup"><span data-stu-id="a2f4e-132">The following example shows a successful response to a **GetClientAccessToken** operation request to get a caller identity token for an app.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a2f4e-133">Die token Werte in diesem Artikel wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a2f4e-133">The token values in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetClientAccessTokenResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:GetClientAccessTokenResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Token>
                  <t:Id>1C50226D-04B5-4AB2-9FCD-42E236B59E4B</t:Id>
                  <t:TokenType>CallerIdentity</t:TokenType>
                  <t:TokenValue>eyJ0eXAmv0QitaJg</t:TokenValue>
                  <t:TTL>479</t:TTL>
               </m:Token>
            </m:GetClientAccessTokenResponseMessage>
         </m:ResponseMessages>
      </m:GetClientAccessTokenResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="a2f4e-134">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="a2f4e-134">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="a2f4e-135">GetClientAccessTokenResponse</span><span class="sxs-lookup"><span data-stu-id="a2f4e-135">GetClientAccessTokenResponse</span></span>](getclientaccesstokenresponse.md)
    
- [<span data-ttu-id="a2f4e-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a2f4e-136">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a2f4e-137">GetClientAccessTokenResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a2f4e-137">GetClientAccessTokenResponseMessage</span></span>](getclientaccesstokenresponsemessage.md)
    
- [<span data-ttu-id="a2f4e-138">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a2f4e-138">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a2f4e-139">Token (ClientAccessTokenType)</span><span class="sxs-lookup"><span data-stu-id="a2f4e-139">Token (ClientAccessTokenType)</span></span>](token-clientaccesstokentype.md)
    
- [<span data-ttu-id="a2f4e-140">ID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="a2f4e-140">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="a2f4e-141">"TokenType" (ClientAccessTokenType)</span><span class="sxs-lookup"><span data-stu-id="a2f4e-141">TokenType (ClientAccessTokenType)</span></span>](tokentype-clientaccesstokentype.md)
    
- [<span data-ttu-id="a2f4e-142">TokenValue</span><span class="sxs-lookup"><span data-stu-id="a2f4e-142">TokenValue</span></span>](tokenvalue.md)
    
- [<span data-ttu-id="a2f4e-143">TTL (ClientAccessTokenTypeType)</span><span class="sxs-lookup"><span data-stu-id="a2f4e-143">TTL (ClientAccessTokenTypeType)</span></span>](ttl-clientaccesstokentypetype.md)
    
## <a name="getclientaccesstoken-operation-error-response"></a><span data-ttu-id="a2f4e-144">GetClientAccessToken Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="a2f4e-144">GetClientAccessToken operation error response</span></span>

<span data-ttu-id="a2f4e-145">Das folgende Beispiel zeigt eine Fehlerantwort an eine **GetClientAccessToken** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a2f4e-145">The following example shows an error response to a **GetClientAccessToken** operation request.</span></span> <span data-ttu-id="a2f4e-146">Dies ist eine Antwort auf eine Anforderung an einen Rückruf Erweiterung ohne die entsprechenden Berechtigungen token abrufen.</span><span class="sxs-lookup"><span data-stu-id="a2f4e-146">This is a response to a request to get an extension callback token without the appropriate permissions.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetClientAccessTokenResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:GetClientAccessTokenResponseMessage ResponseClass="Error">
               <m:MessageText>The caller does not have enough permission for this token request.</m:MessageText>
               <m:ResponseCode>ErrorInvalidClientAccessTokenRequest</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
            </m:GetClientAccessTokenResponseMessage>
         </m:ResponseMessages>
      </m:GetClientAccessTokenResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="a2f4e-147">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="a2f4e-147">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="a2f4e-148">GetClientAccessTokenResponse</span><span class="sxs-lookup"><span data-stu-id="a2f4e-148">GetClientAccessTokenResponse</span></span>](getclientaccesstokenresponse.md)
    
- [<span data-ttu-id="a2f4e-149">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a2f4e-149">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a2f4e-150">GetClientAccessTokenResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a2f4e-150">GetClientAccessTokenResponseMessage</span></span>](getclientaccesstokenresponsemessage.md)
    
- [<span data-ttu-id="a2f4e-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="a2f4e-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="a2f4e-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a2f4e-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a2f4e-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="a2f4e-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="a2f4e-154">Zusätzliche Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="a2f4e-154">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a2f4e-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2f4e-155">See also</span></span>

- [<span data-ttu-id="a2f4e-156">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="a2f4e-156">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="a2f4e-157">GetAppManifests-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a2f4e-157">GetAppManifests operation</span></span>](getappmanifests-operation.md)
    
- [<span data-ttu-id="a2f4e-158">Outlook-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="a2f4e-158">Outlook add-ins</span></span>](http://msdn.microsoft.com/library/71e64bc9-e347-4f5d-8948-0a47b5dd93e6%28Office.15%29.aspx)
    

