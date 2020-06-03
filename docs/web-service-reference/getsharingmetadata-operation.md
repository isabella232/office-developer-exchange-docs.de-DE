---
title: GetSharingMetadata-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingMetadata
api_type:
- schema
ms.assetid: eaf29427-ecf8-4a5e-9a54-db2e6414b35e
description: Der GetSharingMetadata-Vorgang ruft ein nicht transparentes Authentifizierungstoken ab, das eine Freigabeeinladung identifiziert.
ms.openlocfilehash: 0390b9caa7b2e9847b1e8dcdc1b911a35e3c5864
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530183"
---
# <a name="getsharingmetadata-operation"></a><span data-ttu-id="a9ef7-103">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a9ef7-103">GetSharingMetadata operation</span></span>

<span data-ttu-id="a9ef7-104">Der **GetSharingMetadata** -Vorgang ruft ein nicht transparentes Authentifizierungstoken ab, das eine Freigabeeinladung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a9ef7-104">The **GetSharingMetadata** operation gets an opaque authentication token that identifies a sharing invitation.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="a9ef7-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="a9ef7-105">SOAP Headers</span></span>

<span data-ttu-id="a9ef7-106">Der **GetSharingMetadata** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt und beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a9ef7-106">The **GetSharingMetadata** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="a9ef7-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="a9ef7-107">**Header**</span></span>|<span data-ttu-id="a9ef7-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9ef7-108">**Element**</span></span>|<span data-ttu-id="a9ef7-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9ef7-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a9ef7-110">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="a9ef7-110">RequestVersion</span></span>  <br/> |[<span data-ttu-id="a9ef7-111">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="a9ef7-111">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="a9ef7-112">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="a9ef7-112">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="a9ef7-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="a9ef7-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="a9ef7-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a9ef7-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="a9ef7-115">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="a9ef7-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getsharingmetadata-request-example"></a><span data-ttu-id="a9ef7-116">GetSharingMetadata-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="a9ef7-116">GetSharingMetadata request example</span></span>

### <a name="description"></a><span data-ttu-id="a9ef7-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9ef7-117">Description</span></span>

<span data-ttu-id="a9ef7-118">Das folgende Beispiel zeigt, wie Sie eine Anforderung zum Abrufen eines nicht transparenten Authentifizierungstokens erstellen, das eine Freigabeeinladung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a9ef7-118">The following example shows how to form a request to get an opaque authentication token that identifies a sharing invitation.</span></span> <span data-ttu-id="a9ef7-119">In diesem Beispiel möchte user1@contoso.com den Ordner freigeben, der durch das [IdOfFolderToShare](idoffoldertoshare.md) -Element mit user1@fabikam.com und User2@Test.com angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a9ef7-119">In this example, user1@contoso.com wants to share the folder that is specified by the [IdOfFolderToShare](idoffoldertoshare.md) element with user1@fabikam.com and user2@test.com.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a9ef7-120">Code</span><span class="sxs-lookup"><span data-stu-id="a9ef7-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <m:GetSharingMetadata>
      <m:IdOfFolderToShare Id="AAMkAD=" ChangeKey="AwAAA=" />
      <m:SenderSmtpAddress>user1@contoso.com</m:SenderSmtpAddress>
      <m:Recipients>
        <t:SmtpAddress>user1@fabrikam.com</t:SmtpAddress>
        <t:SmtpAddress>user2@test.com</t:SmtpAddress>
      </m:Recipients>
    </m:GetSharingMetadata>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="a9ef7-121">Comments</span><span class="sxs-lookup"><span data-stu-id="a9ef7-121">Comments</span></span>

<span data-ttu-id="a9ef7-122">Das [Recipients (ArrayOfSmtpAddressType)-](recipients-arrayofsmtpaddresstype.md) Element enthält ein [SmtpAddress](smtpaddress.md) -Element für jeden beabsichtigten Empfänger der Freigabeeinladung.</span><span class="sxs-lookup"><span data-stu-id="a9ef7-122">The [Recipients (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) element contains one [SmtpAddress](smtpaddress.md) element for each intended recipient of the sharing invitation.</span></span> 
  
## <a name="successful-getsharingmetadata-response"></a><span data-ttu-id="a9ef7-123">Erfolgreiche GetSharingMetadata-Antwort</span><span class="sxs-lookup"><span data-stu-id="a9ef7-123">Successful GetSharingMetadata Response</span></span>

### <a name="description"></a><span data-ttu-id="a9ef7-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9ef7-124">Description</span></span>

<span data-ttu-id="a9ef7-125">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetSharingMetadata** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a9ef7-125">The following example shows a successful response to a **GetSharingMetadata** request.</span></span> <span data-ttu-id="a9ef7-126">In diesem Beispiel wurden in der entsprechenden **GetSharingMetadata** -Anforderung zwei Empfänger angegeben: user1@fabrikam.com und User2@Test.com.</span><span class="sxs-lookup"><span data-stu-id="a9ef7-126">In this example, two recipients were specified in the corresponding **GetSharingMetadata** request: user1@fabrikam.com and user2@test.com.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a9ef7-127">Code</span><span class="sxs-lookup"><span data-stu-id="a9ef7-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingMetadataResponseMessage ResponseClass="Success" 
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</ResponseCode>
      <m:EncryptedSharedFolderDataCollection>
        <t:EncryptedSharedFolderData>
          <t:Token>
            <EncryptedData Id="Assertion0" Type="http://www.w3.org/2001/04/xmlenc#Element" xmlns="http://www.w3.org/2001/04/xmlenc#">
              <EncryptionMethod Algorithm="http://www.w3.org/2001/04/xmlenc#tripledes-cbc"></EncryptionMethod>
              <ds:KeyInfo xmlns:ds="http://www.w3.org/2000/09/xmldsig#">
                <EncryptedKey>
                  <EncryptionMethod Algorithm="http://www.w3.org/2001/04/xmlenc#rsa-oaep-mgf1p"></EncryptionMethod>
                  <ds:KeyInfo Id="keyinfo">
                    <wsse:SecurityTokenReference xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd">
                      <wsse:KeyIdentifier 
                                  EncodingType="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-soap-message-security-1.0#Base64Binary" 
                                  ValueType="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-x509-token-profile-1.0#X509SubjectKeyIdentifier">
                        B4VEEAf=
                      </wsse:KeyIdentifier>
                    </wsse:SecurityTokenReference>
                  </ds:KeyInfo>
                  <CipherData>
                    <CipherValue>GI/Dxqvw2na==</CipherValue>
                  </CipherData>
                </EncryptedKey>
              </ds:KeyInfo>
              <CipherData>
                <CipherValue>L77I7Hr06z</CipherValue>
              </CipherData>
            </EncryptedData>
          </t:Token>
          <t:Data>
            <EncryptedData Type="http://www.w3.org/2001/04/xmlenc#Element" xmlns="http://www.w3.org/2001/04/xmlenc#">
              <EncryptionMethod Algorithm="http://www.w3.org/2001/04/xmlenc#aes256-cbc" />
              <KeyInfo xmlns="http://www.w3.org/2000/09/xmldsig#">
                <EncryptedKey xmlns="http://www.w3.org/2001/04/xmlenc#">
                  <EncryptionMethod Algorithm="http://www.w3.org/2001/04/xmlenc#kw-tripledes" />
                  <KeyInfo xmlns="http://www.w3.org/2000/09/xmldsig#">
                    <KeyName>key</KeyName>
                  </KeyInfo>
                  <CipherData>
                    <CipherValue>9UgtjrHiU</CipherValue>
                  </CipherData>
                </EncryptedKey>
              </KeyInfo>
              <CipherData>
                <CipherValue>NCNsJoGtQ==</CipherValue>
              </CipherData>
            </EncryptedData>
          </t:Data>
        </t:EncryptedSharedFolderData>
      </m:EncryptedSharedFolderDataCollection>
      <m:InvalidRecipients>
        <t:InvalidRecipient>
          <t:SmtpAddress>user2@test.com</t:SmtpAddress>
          <t:ResponseCode>RecipientOrganizationNotFederated</t:ResponseCode>
          <m:MessageText>The organization of these recipients is not federated for external sharing.</m:MessageText>
        </t:InvalidRecipient>
      </m:InvalidRecipients>
    </GetSharingMetadataResponseMessage>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="a9ef7-128">Comments</span><span class="sxs-lookup"><span data-stu-id="a9ef7-128">Comments</span></span>

<span data-ttu-id="a9ef7-129">Die Antwort enthält ein [EncryptedSharedFolderData](encryptedsharedfolderdata.md) -Element für jede Organisation, die durch gültige Empfänger dargestellt wird, die in der **GetSharingMetadata** -Anforderung angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a9ef7-129">The response contains one [EncryptedSharedFolderData](encryptedsharedfolderdata.md) element for each organization that is represented by valid recipients that are specified in the **GetSharingMetadata** request.</span></span> 
  
<span data-ttu-id="a9ef7-130">Die **GetSharingMetadata** -Anforderung ist erfolgreich, auch wenn in der Anforderung ungültige Empfänger angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a9ef7-130">The **GetSharingMetadata** request will succeed even if invalid recipients are specified in the request.</span></span> <span data-ttu-id="a9ef7-131">Das [InvalidRecipients](invalidrecipients.md) -Element enthält Informationen zu ungültigen Empfängern.</span><span class="sxs-lookup"><span data-stu-id="a9ef7-131">The [InvalidRecipients](invalidrecipients.md) element contains information about invalid recipients.</span></span> <span data-ttu-id="a9ef7-132">Informationen zu den Gründen, warum ein Empfänger möglicherweise ungültig ist, finden Sie unter [Response Code (InvalidRecipientResponseCodeType)](responsecode-invalidrecipientresponsecodetype.md).</span><span class="sxs-lookup"><span data-stu-id="a9ef7-132">For information about the reasons why a recipient might be invalid, see [ResponseCode (InvalidRecipientResponseCodeType)](responsecode-invalidrecipientresponsecodetype.md).</span></span>
  
<span data-ttu-id="a9ef7-133">Wenn alle vorgesehenen Empfänger ungültig sind, ist das [EncryptedSharedFolderDataCollection](encryptedsharedfolderdatacollection.md) -Element leer.</span><span class="sxs-lookup"><span data-stu-id="a9ef7-133">If all intended recipients are invalid, the [EncryptedSharedFolderDataCollection](encryptedsharedfolderdatacollection.md) element will be empty.</span></span> 
  
## <a name="getsharingmetadata-error-response"></a><span data-ttu-id="a9ef7-134">GetSharingMetadata-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="a9ef7-134">GetSharingMetadata error response</span></span>

### <a name="description"></a><span data-ttu-id="a9ef7-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9ef7-135">Description</span></span>

<span data-ttu-id="a9ef7-136">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **GetSharingMetadata** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a9ef7-136">The following example shows an error response to a **GetSharingMetadata** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a9ef7-137">Code</span><span class="sxs-lookup"><span data-stu-id="a9ef7-137">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingMetadataResponseMessage ResponseClass="Error" 
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:MessageText>The SMTP address format is invalid.</MessageText>
      <m:ResponseCode>ErrorInvalidSmtpAddress</ResponseCode>
      <m:DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetSharingMetadataResponseMessage>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="a9ef7-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9ef7-138">See also</span></span>



[<span data-ttu-id="a9ef7-139">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="a9ef7-139">GetSharingMetadata</span></span>](getsharingmetadata.md)
  
[<span data-ttu-id="a9ef7-140">GetSharingMetadataType</span><span class="sxs-lookup"><span data-stu-id="a9ef7-140">GetSharingMetadataType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingMetadataType.aspx)
  
[<span data-ttu-id="a9ef7-141">GetSharingMetadataResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a9ef7-141">GetSharingMetadataResponseMessage</span></span>](getsharingmetadataresponsemessage.md)
  
[<span data-ttu-id="a9ef7-142">GetSharingMetadataResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="a9ef7-142">GetSharingMetadataResponseMessageType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingMetadataResponseMessageType.aspx)


[<span data-ttu-id="a9ef7-143">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="a9ef7-143">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="a9ef7-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a9ef7-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

