---
title: AddDistributionGroupToImList-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5aa9bec8-71cf-4a6e-8ec8-b4965b40fd4a
description: Hier finden Sie Informationen über die AddDistributionGroupToImList EWS Vorgang.
ms.openlocfilehash: 7c562c317890a4cffb9e5844ea41c1096a8595b4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757219"
---
# <a name="adddistributiongrouptoimlist-operation"></a><span data-ttu-id="22da2-103">AddDistributionGroupToImList-Vorgang</span><span class="sxs-lookup"><span data-stu-id="22da2-103">AddDistributionGroupToImList operation</span></span>

<span data-ttu-id="22da2-104">Hier finden Sie Informationen zum **AddDistributionGroupToImList** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="22da2-104">Find information about the **AddDistributionGroupToImList** EWS operation.</span></span> 
  
<span data-ttu-id="22da2-105">Der Vorgang des **AddDistributionGroupToImList** Exchange-Webdienste (EWS) hinzugefügt Instant messaging (IM)-Liste in der einheitliche Kontaktspeicher eine Verteilergruppe.</span><span class="sxs-lookup"><span data-stu-id="22da2-105">The **AddDistributionGroupToImList** Exchange Web Services (EWS) operation adds a distribution group to the instant messaging (IM) list in the Unified Contact Store.</span></span> 
  
<span data-ttu-id="22da2-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="22da2-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-adddistributiongrouptoimlist-operation"></a><span data-ttu-id="22da2-107">Verwenden des AddDistributionGroupToImList-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="22da2-107">Using the AddDistributionGroupToImList operation</span></span>

<span data-ttu-id="22da2-108">Der Vorgang **AddDistributionGroupToImList** erhält ein einzelnes Argument, das identifiziert eine Verteilergruppe, um die Instant Messaging-Liste hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="22da2-108">The **AddDistributionGroupToImList** operation takes a single argument that identifies a distribution group to add to the IM list.</span></span> <span data-ttu-id="22da2-109">Dieser Vorgang wird eine Verteilergruppe nicht erstellt; die Verteilergruppe muss bereits erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="22da2-109">This operation does not create a distribution group; the distribution group must already be created.</span></span> 
  
<span data-ttu-id="22da2-110">Dieser Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="22da2-110">This operation can use the SOAP headers that are listed in the following table.</span></span>
  
<span data-ttu-id="22da2-111">**In Tabelle 1. AddDistributionGroupToImList Vorgang SOAP-Header**</span><span class="sxs-lookup"><span data-stu-id="22da2-111">**Table 1. AddDistributionGroupToImList operation SOAP headers**</span></span>

|<span data-ttu-id="22da2-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="22da2-112">**Header name**</span></span>|<span data-ttu-id="22da2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="22da2-113">**Element**</span></span>|<span data-ttu-id="22da2-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="22da2-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="22da2-115">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="22da2-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="22da2-116">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="22da2-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="22da2-p102">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="22da2-p102">Identifies the user whom the client application is impersonating. This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="22da2-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="22da2-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="22da2-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="22da2-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="22da2-121">Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22da2-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="22da2-122">Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="22da2-122">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="22da2-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="22da2-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="22da2-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="22da2-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="22da2-p104">Gibt die Schemaversion für die Vorgangsanforderung an. Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="22da2-p104">Identifies the schema version for the operation request. This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="22da2-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="22da2-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="22da2-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="22da2-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="22da2-p105">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dies gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="22da2-p105">Identifies the version of the server that responded to the request. This is applicable to a response.</span></span>  <br/> |
   
## <a name="adddistributiongrouptoimlist-operation-request-example"></a><span data-ttu-id="22da2-131">AddDistributionGroupToImList Vorgang anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="22da2-131">AddDistributionGroupToImList operation request example</span></span>

<span data-ttu-id="22da2-132">Im folgenden Beispiel wird ein **AddDistributionGroupToImList** Vorgang Anforderung veranschaulicht das Hinzufügen eine Verteilergruppe der Instant Messaging-Liste.</span><span class="sxs-lookup"><span data-stu-id="22da2-132">The following example of an **AddDistributionGroupToImList** operation request shows how to add a distribution group to the IM list.</span></span> 
  
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
      <m:AddDistributionGroupToImList>
         <m:SmtpAddress>distributionlist1@example.com</m:SmtpAddress>
      </m:AddDistributionGroupToImList>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="22da2-133">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="22da2-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="22da2-134">AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="22da2-134">AddDistributionGroupToImList</span></span>](adddistributiongrouptoimlist.md)   
- [<span data-ttu-id="22da2-135">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="22da2-135">SmtpAddress</span></span>](smtpaddress.md)
    
## <a name="successful-adddistributiongrouptoimlist-operation-response"></a><span data-ttu-id="22da2-136">Erfolgreiche AddDistributionGroupToImList Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="22da2-136">Successful AddDistributionGroupToImList operation response</span></span>

<span data-ttu-id="22da2-137">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung des **AddDistributionGroupToImList** -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="22da2-137">The following example shows a successful response to an **AddDistributionGroupToImList** operation request.</span></span> 
  
<span data-ttu-id="22da2-138">Die erfolgreiche Antwort enthält den Namen der Verteilergruppe anzeigen, die Exchange-Speicher-Klasse für die Verteilergruppe, und die EWS-Bezeichner des neuen Verteilergruppe.</span><span class="sxs-lookup"><span data-stu-id="22da2-138">The successful response contains the distribution group display name, the Exchange store class for the distribution group, and the EWS identifier of the new distribution group.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/"
            xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
            xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <s:Header>
      <t:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013"/>
   </s:Header>
   <s:Body>
      <m:AddDistributionGroupToImListResponse ResponseClass="Success">
         <m:ResponseCode>NoError</m:ResponseCode>
         <m:ImGroup>
            <t:DisplayName>distributionlist1@example.com</t:DisplayName>
            <t:GroupType>IPM.DistList.MOC.DG</t:GroupType>
            <t:ExchangeStoreId Id="AAMkAGQ1MjJjAA=" 
                             ChangeKey="EgAAAA=="/>
      </m:ImGroup>
      </m:AddDistributionGroupToImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="22da2-139">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="22da2-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="22da2-140">AddDistributionGroupToImListResponse</span><span class="sxs-lookup"><span data-stu-id="22da2-140">AddDistributionGroupToImListResponse</span></span>](adddistributiongrouptoimlistresponse.md)
    
- [<span data-ttu-id="22da2-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="22da2-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="22da2-142">ImGroup</span><span class="sxs-lookup"><span data-stu-id="22da2-142">ImGroup</span></span>](imgroup.md)
    
- [<span data-ttu-id="22da2-143">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="22da2-143">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="22da2-144">GroupType</span><span class="sxs-lookup"><span data-stu-id="22da2-144">GroupType</span></span>](grouptype.md)
    
- [<span data-ttu-id="22da2-145">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="22da2-145">ExchangeStoreId</span></span>](exchangestoreid.md)
    
## <a name="adddistributiongrouptoimlist-operation-errorinvalidimdistributiongroupsmtpaddress-error-response"></a><span data-ttu-id="22da2-146">AddDistributionGroupToImList Vorgang ErrorInvalidImDistributionGroupSmtpAddress Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="22da2-146">AddDistributionGroupToImList operation ErrorInvalidImDistributionGroupSmtpAddress error response</span></span>

<span data-ttu-id="22da2-147">Das folgende Beispiel zeigt eine Fehlerantwort an eine **AddDistributionGroupToImList** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="22da2-147">The following example shows an error response to an **AddDistributionGroupToImList** operation request.</span></span> <span data-ttu-id="22da2-148">Die folgende Fehlerantwort tritt auf, wenn versucht wird, eine Verteilergruppe hinzuzufügen, die nicht im Exchange-Speicher vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="22da2-148">The following error response occurs when an attempt is made to add a distribution group that does not exist in the Exchange store.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddDistributionGroupToImListResponse ResponseClass="Error" 
                                            xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified IM distribution group SMTP address is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImDistributionGroupSmtpAddress</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </AddDistributionGroupToImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="22da2-149">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="22da2-149">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="22da2-150">AddDistributionGroupToImListResponse</span><span class="sxs-lookup"><span data-stu-id="22da2-150">AddDistributionGroupToImListResponse</span></span>](adddistributiongrouptoimlistresponse.md)
    
- [<span data-ttu-id="22da2-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="22da2-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="22da2-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="22da2-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="22da2-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22da2-153">See also</span></span>

- [<span data-ttu-id="22da2-154">Benutzer und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="22da2-154">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)   
- [<span data-ttu-id="22da2-155">AddImGroup</span><span class="sxs-lookup"><span data-stu-id="22da2-155">AddImGroup</span></span>](addimgroup-operation.md)   
- [<span data-ttu-id="22da2-156">RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="22da2-156">RemoveImGroup</span></span>](removeimgroup-operation.md)
    

