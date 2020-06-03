---
title: AddDistributionGroupToImList-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5aa9bec8-71cf-4a6e-8ec8-b4965b40fd4a
description: Hier finden Sie Informationen zum AddDistributionGroupToImList-EWS-Vorgang.
ms.openlocfilehash: e68e21b6994af5773f5cf991d55129e1db3367ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463692"
---
# <a name="adddistributiongrouptoimlist-operation"></a><span data-ttu-id="ecc86-103">AddDistributionGroupToImList-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ecc86-103">AddDistributionGroupToImList operation</span></span>

<span data-ttu-id="ecc86-104">Hier finden Sie Informationen zum **AddDistributionGroupToImList** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ecc86-104">Find information about the **AddDistributionGroupToImList** EWS operation.</span></span> 
  
<span data-ttu-id="ecc86-105">Mit dem **AddDistributionGroupToImList** -Exchange-Webdienste Vorgang wird der Liste der Chatnachrichten (Instant Messaging) im einheitlichen Kontaktspeicher eine Verteilergruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ecc86-105">The **AddDistributionGroupToImList** Exchange Web Services (EWS) operation adds a distribution group to the instant messaging (IM) list in the Unified Contact Store.</span></span> 
  
<span data-ttu-id="ecc86-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ecc86-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-adddistributiongrouptoimlist-operation"></a><span data-ttu-id="ecc86-107">Verwenden des AddDistributionGroupToImList-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="ecc86-107">Using the AddDistributionGroupToImList operation</span></span>

<span data-ttu-id="ecc86-108">Der **AddDistributionGroupToImList** -Vorgang verwendet ein einzelnes Argument, das eine Verteilergruppe identifiziert, die der Liste "Chat" hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ecc86-108">The **AddDistributionGroupToImList** operation takes a single argument that identifies a distribution group to add to the IM list.</span></span> <span data-ttu-id="ecc86-109">Bei diesem Vorgang wird keine Verteilergruppe erstellt; die Verteilergruppe muss bereits erstellt sein.</span><span class="sxs-lookup"><span data-stu-id="ecc86-109">This operation does not create a distribution group; the distribution group must already be created.</span></span> 
  
<span data-ttu-id="ecc86-110">Dieser Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ecc86-110">This operation can use the SOAP headers that are listed in the following table.</span></span>
  
<span data-ttu-id="ecc86-111">**Tabelle 1. SOAP-Header des AddDistributionGroupToImList-Vorgangs**</span><span class="sxs-lookup"><span data-stu-id="ecc86-111">**Table 1. AddDistributionGroupToImList operation SOAP headers**</span></span>

|<span data-ttu-id="ecc86-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="ecc86-112">**Header name**</span></span>|<span data-ttu-id="ecc86-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ecc86-113">**Element**</span></span>|<span data-ttu-id="ecc86-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ecc86-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ecc86-115">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="ecc86-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="ecc86-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="ecc86-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="ecc86-p102">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ecc86-p102">Identifies the user whom the client application is impersonating. This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ecc86-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="ecc86-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="ecc86-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="ecc86-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="ecc86-121">Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ecc86-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="ecc86-122">Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ecc86-122">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ecc86-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="ecc86-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="ecc86-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="ecc86-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="ecc86-p104">Gibt die Schemaversion für die Vorgangsanforderung an. Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ecc86-p104">Identifies the schema version for the operation request. This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ecc86-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="ecc86-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="ecc86-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ecc86-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="ecc86-p105">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dies gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="ecc86-p105">Identifies the version of the server that responded to the request. This is applicable to a response.</span></span>  <br/> |
   
## <a name="adddistributiongrouptoimlist-operation-request-example"></a><span data-ttu-id="ecc86-131">AddDistributionGroupToImList-Vorgangsanforderung (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="ecc86-131">AddDistributionGroupToImList operation request example</span></span>

<span data-ttu-id="ecc86-132">Im folgenden Beispiel einer **AddDistributionGroupToImList** -Vorgangsanforderung wird gezeigt, wie der Liste "Chat" eine Verteilergruppe hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ecc86-132">The following example of an **AddDistributionGroupToImList** operation request shows how to add a distribution group to the IM list.</span></span> 
  
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
      <m:AddDistributionGroupToImList>
         <m:SmtpAddress>distributionlist1@example.com</m:SmtpAddress>
      </m:AddDistributionGroupToImList>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="ecc86-133">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="ecc86-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ecc86-134">AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="ecc86-134">AddDistributionGroupToImList</span></span>](adddistributiongrouptoimlist.md)   
- [<span data-ttu-id="ecc86-135">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="ecc86-135">SmtpAddress</span></span>](smtpaddress.md)
    
## <a name="successful-adddistributiongrouptoimlist-operation-response"></a><span data-ttu-id="ecc86-136">Erfolgreiche Reaktion des AddDistributionGroupToImList-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="ecc86-136">Successful AddDistributionGroupToImList operation response</span></span>

<span data-ttu-id="ecc86-137">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **AddDistributionGroupToImList** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="ecc86-137">The following example shows a successful response to an **AddDistributionGroupToImList** operation request.</span></span> 
  
<span data-ttu-id="ecc86-138">Die erfolgreiche Antwort enthält den Anzeigenamen der Verteilergruppe, die Exchange-Informationsspeicher Klasse für die Verteilergruppe und die EWS-ID der neuen Verteilergruppe.</span><span class="sxs-lookup"><span data-stu-id="ecc86-138">The successful response contains the distribution group display name, the Exchange store class for the distribution group, and the EWS identifier of the new distribution group.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/"
            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
            xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="ecc86-139">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="ecc86-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ecc86-140">AddDistributionGroupToImListResponse</span><span class="sxs-lookup"><span data-stu-id="ecc86-140">AddDistributionGroupToImListResponse</span></span>](adddistributiongrouptoimlistresponse.md)
    
- [<span data-ttu-id="ecc86-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ecc86-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ecc86-142">Imgroup</span><span class="sxs-lookup"><span data-stu-id="ecc86-142">ImGroup</span></span>](imgroup.md)
    
- [<span data-ttu-id="ecc86-143">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="ecc86-143">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="ecc86-144">GroupType</span><span class="sxs-lookup"><span data-stu-id="ecc86-144">GroupType</span></span>](grouptype.md)
    
- [<span data-ttu-id="ecc86-145">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="ecc86-145">ExchangeStoreId</span></span>](exchangestoreid.md)
    
## <a name="adddistributiongrouptoimlist-operation-errorinvalidimdistributiongroupsmtpaddress-error-response"></a><span data-ttu-id="ecc86-146">AddDistributionGroupToImList-Vorgang ErrorInvalidImDistributionGroupSmtpAddress-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="ecc86-146">AddDistributionGroupToImList operation ErrorInvalidImDistributionGroupSmtpAddress error response</span></span>

<span data-ttu-id="ecc86-147">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **AddDistributionGroupToImList** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="ecc86-147">The following example shows an error response to an **AddDistributionGroupToImList** operation request.</span></span> <span data-ttu-id="ecc86-148">Die folgende Fehlermeldung tritt auf, wenn ein Versuch unternommen wird, eine Verteilergruppe hinzuzufügen, die nicht in der Exchange-Informationsspeicher vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ecc86-148">The following error response occurs when an attempt is made to add a distribution group that does not exist in the Exchange store.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddDistributionGroupToImListResponse ResponseClass="Error" 
                                            xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified IM distribution group SMTP address is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImDistributionGroupSmtpAddress</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </AddDistributionGroupToImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="ecc86-149">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="ecc86-149">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ecc86-150">AddDistributionGroupToImListResponse</span><span class="sxs-lookup"><span data-stu-id="ecc86-150">AddDistributionGroupToImListResponse</span></span>](adddistributiongrouptoimlistresponse.md)
    
- [<span data-ttu-id="ecc86-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="ecc86-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="ecc86-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ecc86-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="ecc86-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecc86-153">See also</span></span>

- [<span data-ttu-id="ecc86-154">Personen und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="ecc86-154">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)   
- [<span data-ttu-id="ecc86-155">AddImGroup</span><span class="sxs-lookup"><span data-stu-id="ecc86-155">AddImGroup</span></span>](addimgroup-operation.md)   
- [<span data-ttu-id="ecc86-156">RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="ecc86-156">RemoveImGroup</span></span>](removeimgroup-operation.md)
    

