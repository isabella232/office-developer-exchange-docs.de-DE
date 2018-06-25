---
title: GetImItemList-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e31d14e1-0c1f-4b69-98b7-157d59c13698
description: Hier finden Sie Informationen über die GetImItemList EWS Vorgang.
ms.openlocfilehash: 3977b0ad31e819cd973ce261ba3152b3840003b3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758700"
---
# <a name="getimitemlist-operation"></a><span data-ttu-id="d6f8e-103">GetImItemList-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d6f8e-103">GetImItemList operation</span></span>

<span data-ttu-id="d6f8e-104">Hier finden Sie Informationen zum **GetImItemList** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-104">Find information about the **GetImItemList** EWS operation.</span></span> 
  
## <a name="using-the-getimitemlist-operation"></a><span data-ttu-id="d6f8e-105">Verwenden des GetImItemList-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d6f8e-105">Using the GetImItemList operation</span></span>

<span data-ttu-id="d6f8e-106">Der Vorgang **GetImItemList** Ruft die Liste der Gruppen für instant messaging (IM) und Instant Messaging wenden Sie sich an Personen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-106">The **GetImItemList** operation retrieves the list of instant messaging (IM) groups and IM contact personas in a mailbox.</span></span> <span data-ttu-id="d6f8e-107">Der Vorgang **GetImItemList** akzeptiert keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-107">The **GetImItemList** operation does not take any arguments.</span></span> 
  
<span data-ttu-id="d6f8e-108">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-108">This operation was introduced in Exchange Server 2013.</span></span>
  
### <a name="getimitemlist-operation-soap-headers"></a><span data-ttu-id="d6f8e-109">GetImItemList Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="d6f8e-109">GetImItemList operation SOAP headers</span></span>

<span data-ttu-id="d6f8e-110">Der Vorgang **GetImItemList** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-110">The **GetImItemList** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="d6f8e-111">**Headername**</span><span class="sxs-lookup"><span data-stu-id="d6f8e-111">**Header name**</span></span>|<span data-ttu-id="d6f8e-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6f8e-112">**Element**</span></span>|<span data-ttu-id="d6f8e-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6f8e-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d6f8e-114">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="d6f8e-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="d6f8e-115">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="d6f8e-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="d6f8e-116">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="d6f8e-117">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d6f8e-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="d6f8e-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="d6f8e-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="d6f8e-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="d6f8e-120">Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="d6f8e-121">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d6f8e-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="d6f8e-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="d6f8e-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="d6f8e-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="d6f8e-124">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="d6f8e-125">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d6f8e-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="d6f8e-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="d6f8e-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d6f8e-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="d6f8e-128">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="d6f8e-129">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getimitemlist-operation-request-example-request-your-im-items-list"></a><span data-ttu-id="d6f8e-130">GetImItemList Vorgang-anforderungsbeispiel: Liste der Sofortnachrichten anfordern</span><span class="sxs-lookup"><span data-stu-id="d6f8e-130">GetImItemList operation request example: Request your IM items list</span></span>

<span data-ttu-id="d6f8e-131">Im folgenden Beispiel wird eine **GetImItemList** Vorgang Anforderung veranschaulicht, wie die Liste der Gruppen Sofortnachrichten anfordern und Sofortnachrichten wenden Sie sich an Personen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-131">The following example of a **GetImItemList** operation request shows how to request the list of IM groups and IM contact personas in a mailbox.</span></span> <span data-ttu-id="d6f8e-132">Das **GetImItemList** -Element ist die Elementoption nur in der SOAP-Text.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-132">The **GetImItemList** element is the only element option in the SOAP body.</span></span> 
  
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
      <m:GetImItemList/>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d6f8e-133">Die Anforderung SOAP-Text enthält das folgende Element:</span><span class="sxs-lookup"><span data-stu-id="d6f8e-133">The request SOAP body contains the following element:</span></span>
  
- [<span data-ttu-id="d6f8e-134">GetImItemList</span><span class="sxs-lookup"><span data-stu-id="d6f8e-134">GetImItemList</span></span>](getimitemlist.md)
    
## <a name="successful-getimitemlist-operation-response"></a><span data-ttu-id="d6f8e-135">Erfolgreiche GetImItemList Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="d6f8e-135">Successful GetImItemList operation response</span></span>

<span data-ttu-id="d6f8e-136">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetImItemList** Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-136">The following example shows a successful response to a **GetImItemList** operation request.</span></span> <span data-ttu-id="d6f8e-137">Die Antwort enthält vier Gruppen von Sofortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-137">The response contains four IM groups.</span></span> <span data-ttu-id="d6f8e-138">Drei der Gruppen Sofortnachrichten – andere Kontakte, markierter und Favoriten – Standardgruppen im Exchange-Speicher sind.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-138">Three of the IM groups — Other Contacts, Tagged, and Favorites — are default groups in the Exchange store.</span></span> <span data-ttu-id="d6f8e-139">Die MyCustomGroup2-Gruppe ist eine benutzerdefinierte Gruppe von Benutzern erstellte.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-139">The MyCustomGroup2 group is a custom user-created group.</span></span> <span data-ttu-id="d6f8e-140">Die Gruppen weitere Kontakte und markierter haben keine Mitglieder.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-140">The Other Contacts and Tagged groups do not have members.</span></span> <span data-ttu-id="d6f8e-141">Gruppe Favoriten verfügt über einen einzelnen Kontakt Member.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-141">The Favorites group has a single contact member.</span></span> <span data-ttu-id="d6f8e-142">Die MyCustomGroup2 hat zwei Member Kontakte.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-142">The MyCustomGroup2 has two member contacts.</span></span> <span data-ttu-id="d6f8e-143">Element-IDs werden bereitgestellt, sodass nachfolgende **GetItem** Anforderungen ausgeführt werden können, um weitere Informationen über die Instant Messaging-Kontakte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-143">The item identifiers are provided so that subsequent **GetItem** requests can be performed to get more information about the IM contacts.</span></span> 
  
<span data-ttu-id="d6f8e-144">Dieses Beispiel gibt zwei Rollen.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-144">This example returns two personas.</span></span> <span data-ttu-id="d6f8e-145">Die erste Rolle stellt zwei Kontaktelementen: Anthony Smith und Tony Smith.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-145">The first persona represents two contact items: Anthony Smith and Tony Smith.</span></span> <span data-ttu-id="d6f8e-146">Die kombinierte Kontaktinformationen wird im **Persona** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-146">The combined contact information is returned in the **Persona** object.</span></span> <span data-ttu-id="d6f8e-147">Die zweite Rolle stellt einen einzelnen Kontakt mit dem Anzeigenamen des Terence Adams.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-147">The second persona represents a single contact with the display name of Terence Adams.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d6f8e-148">Der Exchange-Speicher-IDs, Element-IDs, IDs, Ordner-IDs und Persona Bezeichner wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-148">The Exchange store identifiers, item identifiers, source identifiers, folder identifiers, and persona identifiers have been shortened to preserve readability.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
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
      <GetImItemListResponse ResponseClass="Success" 
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <ImItemList>
            <Groups xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <ImGroup>
                  <DisplayName>Other Contacts</DisplayName>
                  <GroupType>IPM.DistList.MOC.OtherContacts</GroupType>
                  <ExchangeStoreId Id="AAMkAGQ1MjJjMTBkLThQoTbWAAAAAAQUAAA=" 
                                   ChangeKey="EgAAAA==" />
               </ImGroup>
               <ImGroup>
                  <DisplayName>Tagged</DisplayName>
                  <GroupType>IPM.DistList.MOC.Tagged</GroupType>
                  <ExchangeStoreId Id="AAMkAGQ1MjJAAQTAAA=" 
                                   ChangeKey="EgAAAA==" />
               </ImGroup>
               <ImGroup>
                  <DisplayName>Favorites</DisplayName>
                  <GroupType>IPM.DistList.MOC.Favorites</GroupType>
                  <ExchangeStoreId Id="AAMkAGQ1MjJjMTAAAAAQSAAA=" 
                                   ChangeKey="EgAAAA==" />
                  <MemberCorrelationKey>
                     <ItemId Id="AAMkAGQ1MjJtt/bhQoTbWAAAAAAvcAAA=" 
                             ChangeKey="EQAAAA==" />
                  </MemberCorrelationKey>
               </ImGroup>
               <ImGroup>
                  <DisplayName>MyCustomGroup2</DisplayName>
                  <GroupType>IPM.DistList.MOC.UserGroup</GroupType>
                  <ExchangeStoreId Id="AAMkAGQ1MjJjKAAA=" 
                                   ChangeKey="EgAAAA==" />
                  <MemberCorrelationKey>
                     <ItemId Id="AAMkAGQ1Matt/bhQoTbWAAAAAAvcAAA=" 
                             ChangeKey="EQAAAA==" />
                     <ItemId Id="AAMkAGQ1MjJjMTBkTbWAAAAAAveAAA=" 
                             ChangeKey="EQAAAA==" />
                  </MemberCorrelationKey>
               </ImGroup>
            </Groups>
            <Personas xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <Persona>
                  <PersonaId Id="AAQkAGQ1MjJjMTBkLTc4YkZmRkYQAQAFgxE1nBcqRGgYWWorM9/+s=" />
                  <PersonaType>Person</PersonaType>
                  <CreationTime>2012-01-12T22:14:36Z</CreationTime>
                  <DisplayName>Anthony Smith</DisplayName>
                  <DisplayNameFirstLast>Anthony Smith</DisplayNameFirstLast>
                  <DisplayNameLastFirst>Smith Anthony</DisplayNameLastFirst>
                  <FileAs>Smith, Anthony</FileAs>
                  <FileAsId>LastCommaFirst</FileAsId>
                  <GivenName>Anthony</GivenName>
                  <Surname>Smith</Surname>
                  <EmailAddress>
                     <Name>tsmith@contoso.com</Name>
                     <EmailAddress>tsmith@contoso.com</EmailAddress>
                     <RoutingType>SMTP</RoutingType>
                  </EmailAddress>
                  <EmailAddresses>
                     <EmailAddress>
                        <Name>tsmith@contoso.com</Name>
                        <EmailAddress>tsmith@contoso.com</EmailAddress>
                        <RoutingType>SMTP</RoutingType>
                     </EmailAddress>
                  </EmailAddresses>
                  <ImAddress>tsmith@contoso.com</ImAddress>
                  <RelevanceScore>2147483647</RelevanceScore>
                  <Attributions>
                     <Attribution>
                        <Id>0</Id>
                        <SourceId Id="AQMkAGQ1MjIAYzEwZC03OGNlLTQ5Bq239uFChNtYAAAIvDAAAAA==" 
                                  ChangeKey="EQAAABYAAABtF8oI7iVOQatt/bhQoTbWAAAAADB3" />
                        <DisplayName>Outlook</DisplayName>
                        <IsWritable>true</IsWritable>
                        <IsQuickContact>false</IsQuickContact>
                        <IsHidden>false</IsHidden>
                        <FolderId Id="AQMkAGQ1MjIAYzEMikE3AQBtF8oI7iVOQatt/bhQoTbWAAADEAAAAA==" 
                                  ChangeKey="AQAAAA==" />
                     </Attribution>
                     <Attribution>
                        <Id>1</Id>
                        <SourceId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04/bhQoTbWAAAAAAveAAA=" 
                                  ChangeKey="EQAAABYAAABtF8oI7iVOQatt/bhQoTbWAAAAAAym" />
                        <DisplayName>Outlook</DisplayName>
                        <IsWritable>true</IsWritable>
                        <IsQuickContact>true</IsQuickContact>
                        <IsHidden>false</IsHidden>
                        <FolderId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDA5Qatt/bhQoTbWAAAAAAvZAAA=" 
                                  ChangeKey="AQAAAA==" />
                     </Attribution>
                  </Attributions>
                  <DisplayNames>
                     <StringAttributedValue>
                        <Value>Anthony Smith</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                     <StringAttributedValue>
                        <Value>Tony Smith</Value>
                        <Attributions>
                           <Attribution>1</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </DisplayNames>
                  <FileAses>
                     <StringAttributedValue>
                        <Value>Smith, Anthony</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </FileAses>
                  <FileAsIds>
                     <StringAttributedValue>
                        <Value>LastCommaFirst</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                     <StringAttributedValue>
                        <Value>None</Value>
                        <Attributions>
                           <Attribution>1</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </FileAsIds>
                  <GivenNames>
                     <StringAttributedValue>
                        <Value>Anthony</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </GivenNames>
                  <Surnames>
                     <StringAttributedValue>
                        <Value>Smith</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </Surnames>
                  <HomePhones>
                     <PhoneNumberAttributedValue>
                        <Value>
                           <Number>4255550110</Number>
                           <Type>Home</Type>
                        </Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </PhoneNumberAttributedValue>
                  </HomePhones>
                  <MobilePhones>
                     <PhoneNumberAttributedValue>
                        <Value>
                           <Number>4255550120</Number>
                           <Type>Mobile</Type>
                        </Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </PhoneNumberAttributedValue>
                  </MobilePhones>
                  <Emails1>
                     <EmailAddressAttributedValue>
                        <Value>
                           <Name>tsmith@contoso.com</Name>
                           <EmailAddress>tsmith@contoso.com</EmailAddress>
                           <RoutingType>SMTP</RoutingType>
                        </Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                           <Attribution>1</Attribution>
                        </Attributions>
                     </EmailAddressAttributedValue>
                  </Emails1>
                  <ImAddresses>
                     <StringAttributedValue>
                        <Value>tsmith@contoso.com</Value>
                        <Attributions>
                           <Attribution>1</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </ImAddresses>
               </Persona>
               <Persona>
                  <PersonaId Id="AAQkAGQ1MjJjMTBkLkYQAQAJ3EkhEEXN5KufGbSYJanZk=" />
                  <PersonaType>Person</PersonaType>
                  <CreationTime>2012-01-05T23:06:58Z</CreationTime>
                  <DisplayName>Terence Adams</DisplayName>
                  <DisplayNameFirstLast>Terence Adams</DisplayNameFirstLast>
                  <DisplayNameLastFirst>Terence Adams</DisplayNameLastFirst>
                  <FileAsId>None</FileAsId>
                  <EmailAddress>
                     <Name>Terence Adams</Name>
                     <EmailAddress>tadams@contoso.com</EmailAddress>
                     <RoutingType>SMTP</RoutingType>
                  </EmailAddress>
                  <EmailAddresses>
                     <EmailAddress>
                        <Name>Terence Adams</Name>
                        <EmailAddress>tadams@contoso.com</EmailAddress>
                        <RoutingType>SMTP</RoutingType>
                     </EmailAddress>
                  </EmailAddresses>
                  <ImAddress>tadams@contoso.com</ImAddress>
                  <RelevanceScore>2147483647</RelevanceScore>
                  <Attributions>
                     <Attribution>
                        <Id>0</Id>
                        <SourceId Id="AAMkAGQ1MjVOQatt/bhQoTbWAAAA7iVOQatt/bhQoTbWAAAAAAvcAAA=" 
                                  ChangeKey="EQAAABYAAABtF8oI7iVOQatt/bhQoTbWAAAAAAyg" />
                        <DisplayName>Outlook</DisplayName>
                        <IsWritable>true</IsWritable>
                        <IsQuickContact>true</IsQuickContact>
                        <IsHidden>false</IsHidden>
                        <FolderId Id="AAMkAGQ1MjJjMTBkLTc4Y2rBtF8oI7iVOQatt/bhQoTbWAAAAAAvZAAA=" 
                                  ChangeKey="AQAAAA==" />
                     </Attribution>
                  </Attributions>
                  <DisplayNames>
                     <StringAttributedValue>
                        <Value>Terence Adams</Value>
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
                  <Emails1>
                     <EmailAddressAttributedValue>
                        <Value>
                           <Name>Terence Adams</Name>
                           <EmailAddress>tadams@contoso.com</EmailAddress>
                           <RoutingType>SMTP</RoutingType>
                        </Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </EmailAddressAttributedValue>
                  </Emails1>
                  <ImAddresses>
                     <StringAttributedValue>
                        <Value>tadams@contoso.com</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </ImAddresses>
               </Persona>
            </Personas>
         </ImItemList>
      </GetImItemListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="d6f8e-149">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="d6f8e-149">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d6f8e-150">GetImItemListResponse</span><span class="sxs-lookup"><span data-stu-id="d6f8e-150">GetImItemListResponse</span></span>](getimitemlistresponse.md)
    
- [<span data-ttu-id="d6f8e-151">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d6f8e-151">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d6f8e-152">ImItemList</span><span class="sxs-lookup"><span data-stu-id="d6f8e-152">ImItemList</span></span>](imitemlist.md)
    
- [<span data-ttu-id="d6f8e-153">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="d6f8e-153">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="d6f8e-154">GroupType</span><span class="sxs-lookup"><span data-stu-id="d6f8e-154">GroupType</span></span>](grouptype.md)
    
- [<span data-ttu-id="d6f8e-155">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="d6f8e-155">ExchangeStoreId</span></span>](exchangestoreid.md)
    
- [<span data-ttu-id="d6f8e-156">MemberCorrelationKey</span><span class="sxs-lookup"><span data-stu-id="d6f8e-156">MemberCorrelationKey</span></span>](membercorrelationkey.md)
    
- [<span data-ttu-id="d6f8e-157">ItemId</span><span class="sxs-lookup"><span data-stu-id="d6f8e-157">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="d6f8e-158">Rollen</span><span class="sxs-lookup"><span data-stu-id="d6f8e-158">Personas</span></span>](personas-ex15websvcsotherref.md)
    
- [<span data-ttu-id="d6f8e-159">PersonaId</span><span class="sxs-lookup"><span data-stu-id="d6f8e-159">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="d6f8e-160">PersonaType</span><span class="sxs-lookup"><span data-stu-id="d6f8e-160">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="d6f8e-161">CreationTime</span><span class="sxs-lookup"><span data-stu-id="d6f8e-161">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="d6f8e-162">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="d6f8e-162">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="d6f8e-163">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="d6f8e-163">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="d6f8e-164">FileAs</span><span class="sxs-lookup"><span data-stu-id="d6f8e-164">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="d6f8e-165">FileAsId</span><span class="sxs-lookup"><span data-stu-id="d6f8e-165">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="d6f8e-166">Vorname</span><span class="sxs-lookup"><span data-stu-id="d6f8e-166">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="d6f8e-167">Nachname</span><span class="sxs-lookup"><span data-stu-id="d6f8e-167">Surname</span></span>](surname.md)
    
- [<span data-ttu-id="d6f8e-168">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="d6f8e-168">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="d6f8e-169">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="d6f8e-169">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="d6f8e-170">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="d6f8e-170">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="d6f8e-171">EmailAddresses (ArrayOfEmailAddressesType)</span><span class="sxs-lookup"><span data-stu-id="d6f8e-171">EmailAddresses (ArrayOfEmailAddressesType)</span></span>](emailaddresses-arrayofemailaddressestype.md)
    
- [<span data-ttu-id="d6f8e-172">ImAddress (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="d6f8e-172">ImAddress (String)</span></span>](imaddress-string.md)
    
- [<span data-ttu-id="d6f8e-173">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="d6f8e-173">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="d6f8e-174">Hinweise (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="d6f8e-174">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="d6f8e-175">Zuweisung (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="d6f8e-175">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="d6f8e-176">ID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="d6f8e-176">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="d6f8e-177">SourceId</span><span class="sxs-lookup"><span data-stu-id="d6f8e-177">SourceId</span></span>](sourceid.md)
    
- [<span data-ttu-id="d6f8e-178">IsWritable</span><span class="sxs-lookup"><span data-stu-id="d6f8e-178">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="d6f8e-179">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="d6f8e-179">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="d6f8e-180">IsHidden</span><span class="sxs-lookup"><span data-stu-id="d6f8e-180">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="d6f8e-181">FolderId</span><span class="sxs-lookup"><span data-stu-id="d6f8e-181">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="d6f8e-182">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="d6f8e-182">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="d6f8e-183">FileAses</span><span class="sxs-lookup"><span data-stu-id="d6f8e-183">FileAses</span></span>](fileases.md)
    
- [<span data-ttu-id="d6f8e-184">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="d6f8e-184">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="d6f8e-185">GivenNames</span><span class="sxs-lookup"><span data-stu-id="d6f8e-185">GivenNames</span></span>](givennames.md)
    
- [<span data-ttu-id="d6f8e-186">Nachnamen</span><span class="sxs-lookup"><span data-stu-id="d6f8e-186">Surnames</span></span>](surnames.md)
    
- [<span data-ttu-id="d6f8e-187">HomePhones</span><span class="sxs-lookup"><span data-stu-id="d6f8e-187">HomePhones</span></span>](homephones.md)
    
- [<span data-ttu-id="d6f8e-188">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="d6f8e-188">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md)
    
- [<span data-ttu-id="d6f8e-189">MobilePhones</span><span class="sxs-lookup"><span data-stu-id="d6f8e-189">MobilePhones</span></span>](mobilephones.md)
    
- [<span data-ttu-id="d6f8e-190">Emails1</span><span class="sxs-lookup"><span data-stu-id="d6f8e-190">Emails1</span></span>](emails1.md)
    
- [<span data-ttu-id="d6f8e-191">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="d6f8e-191">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md)
    
- [<span data-ttu-id="d6f8e-192">ImAddresses</span><span class="sxs-lookup"><span data-stu-id="d6f8e-192">ImAddresses</span></span>](imaddresses.md)
    
- [<span data-ttu-id="d6f8e-193">Wert (ExtendedPropertyType)</span><span class="sxs-lookup"><span data-stu-id="d6f8e-193">Value (ExtendedPropertyType)</span></span>](value-extendedpropertytype.md)
    
## <a name="getimitemlist-operation-error-response"></a><span data-ttu-id="d6f8e-194">GetImItemList Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="d6f8e-194">GetImItemList operation error response</span></span>

<span data-ttu-id="d6f8e-195">Das folgende Beispiel zeigt eine Fehlerantwort an eine **GetImItemList** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-195">The following example shows an error response to a **GetImItemList** operation request.</span></span> <span data-ttu-id="d6f8e-196">Dies ist eine Antwort auf eine Anforderung, die eine falsche angeforderte Serverversion im SOAP-Header enthält.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-196">This is a response to a request that contains an incorrect requested server version in the SOAP header.</span></span> <span data-ttu-id="d6f8e-197">Dieser Fehlerantwort ist ein SOAP-Fehler und nicht im EWS-Schema dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d6f8e-197">This error response is a SOAP fault and is not represented in the EWS schema.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Body>
      <s:Fault>
         <faultcode xmlns:a="http://schemas.microsoft.com/exchange/services/2006/types">a:ErrorIncorrectSchemaVersion</faultcode>
         <faultstring xml:lang="en-US">The request is valid but does not specify the correct server version in the RequestServerVersion SOAP header.  Ensure that the RequestServerVersion SOAP header is set with the correct RequestServerVersionValue.</faultstring>
         <detail>
            <e:ResponseCode xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">ErrorIncorrectSchemaVersion</e:ResponseCode>
            <e:Message xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">The request is valid but does not specify the correct server version in the RequestServerVersion SOAP header.  Ensure that the RequestServerVersion SOAP header is set with the correct RequestServerVersionValue.</e:Message>
         </detail>
      </s:Fault>
   </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="d6f8e-198">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6f8e-198">See also</span></span>

- [<span data-ttu-id="d6f8e-199">AddImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d6f8e-199">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="d6f8e-200">Benutzer und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="d6f8e-200">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="d6f8e-201">GetImItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d6f8e-201">GetImItems operation</span></span>](getimitems-operation.md)
    

