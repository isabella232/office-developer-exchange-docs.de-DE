---
title: GetItem-Vorgang (e-Mail-Nachricht)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: e8492e3b-1c8d-4b14-8070-9530f8306edd
description: GetItem-Vorgang ermöglicht dem Benutzer Zugriff auf Informationen über E-mail-Nachrichten.
ms.openlocfilehash: 133a893ec7cd0c206d9db573f8b952eb3c2286df
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758717"
---
# <a name="getitem-operation-email-message"></a><span data-ttu-id="d671a-103">GetItem-Vorgang (e-Mail-Nachricht)</span><span class="sxs-lookup"><span data-stu-id="d671a-103">GetItem operation (email message)</span></span>

<span data-ttu-id="d671a-104">GetItem-Vorgang ermöglicht dem Benutzer Zugriff auf Informationen über E-mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="d671a-104">The GetItem operation allows the user to access information about e-mail messages.</span></span>
  
## <a name="using-the-getitem-operation-for-messages"></a><span data-ttu-id="d671a-105">Mithilfe der GetItem Operation für Nachrichten</span><span class="sxs-lookup"><span data-stu-id="d671a-105">Using the GetItem Operation for Messages</span></span>

<span data-ttu-id="d671a-106">Die Anforderung GetItem benötigen die folgende Informationen:</span><span class="sxs-lookup"><span data-stu-id="d671a-106">The GetItem request must have the following information:</span></span>
  
- <span data-ttu-id="d671a-107">Das [ItemId](itemid.md) -Element zum Identifizieren der Elementinformationen, die zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="d671a-107">The [ItemId](itemid.md) element to identify the item information to return.</span></span> 
    
- <span data-ttu-id="d671a-108">Das [ItemShape](itemshape.md) -Element zum Identifizieren der Elementeigenschaften zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d671a-108">The [ItemShape](itemshape.md) element to identify the item properties to return.</span></span> 
    
## <a name="getitem-request-example"></a><span data-ttu-id="d671a-109">GetItem-anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="d671a-109">GetItem request example</span></span>

### <a name="description"></a><span data-ttu-id="d671a-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d671a-110">Description</span></span>

<span data-ttu-id="d671a-111">Im folgenden Beispiel wird eine Anforderung GetItem veranschaulicht, wie auf Informationen über E-mail-Nachrichten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d671a-111">The following example of a GetItem request shows how to access information about e-mail messages.</span></span>
  
### <a name="code"></a><span data-ttu-id="d671a-112">Code</span><span class="sxs-lookup"><span data-stu-id="d671a-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xmlns:xsd="http://www.w3.org/2001/XMLSchema"
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem
      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <ItemShape>
        <t:BaseShape>Default</t:BaseShape>
        <t:IncludeMimeContent>true</t:IncludeMimeContent>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="AAAlAF" ChangeKey="CQAAAB" />
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="d671a-113">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="d671a-113">Request elements</span></span>

<span data-ttu-id="d671a-114">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="d671a-114">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="d671a-115">GetItem</span><span class="sxs-lookup"><span data-stu-id="d671a-115">GetItem</span></span>](getitem.md)
    
- [<span data-ttu-id="d671a-116">ItemShape</span><span class="sxs-lookup"><span data-stu-id="d671a-116">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="d671a-117">BaseShape</span><span class="sxs-lookup"><span data-stu-id="d671a-117">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="d671a-118">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="d671a-118">IncludeMimeContent</span></span>](includemimecontent.md)
    
- [<span data-ttu-id="d671a-119">Artikelnummern ein.</span><span class="sxs-lookup"><span data-stu-id="d671a-119">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="d671a-120">ItemId</span><span class="sxs-lookup"><span data-stu-id="d671a-120">ItemId</span></span>](itemid.md)
    
## <a name="successful-getitem-e-mail-message-response-example"></a><span data-ttu-id="d671a-121">Erfolgreiche GetItem (e-Mail-Nachricht) antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="d671a-121">Successful GetItem (E-mail Message) response example</span></span>

### <a name="description"></a><span data-ttu-id="d671a-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d671a-122">Description</span></span>

<span data-ttu-id="d671a-123">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung GetItem.</span><span class="sxs-lookup"><span data-stu-id="d671a-123">The following example shows a successful response to the GetItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="d671a-124">Code</span><span class="sxs-lookup"><span data-stu-id="d671a-124">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:MimeContent CharacterSet="UTF-8">UmVjZWl</t:MimeContent>
              <t:ItemId Id="AAAlAFVz" ChangeKey="CQAAAB" />
              <t:Subject />
              <t:Sensitivity>Normal</t:Sensitivity>
              <t:Body BodyType="HTML">
                <html dir="ltr">
                  <head>
                    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
                      <meta content="MSHTML 6.00.3790.2759" name="GENERATOR">
                        <style title="owaParaStyle">P { MARGIN-TOP: 0px; MARGIN-BOTTOM: 0px } </style>
                      </head>
                  <body ocsi="x">
                    <div dir="ltr">
                      <font face="Tahoma" color="#000000" size="2"></font>&amp;nbsp;
                    </div>
                  </body>
                </html>
              </t:Body>
              <t:Size>881</t:Size>
              <t:DateTimeSent>2006-10-28T01:37:06Z</t:DateTimeSent>
              <t:DateTimeCreated>2006-10-28T01:37:06Z</t:DateTimeCreated>
              <t:ResponseObjects>
                <t:ReplyToItem />
                <t:ReplyAllToItem />
                <t:ForwardItem />
              </t:ResponseObjects>
              <t:HasAttachments>false</t:HasAttachments>
              <t:ToRecipients>
                <t:Mailbox>
                  <t:Name>User1</t:Name>
                  <t:EmailAddress>User1@example.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                </t:Mailbox>
              </t:ToRecipients>
              <t:IsReadReceiptRequested>false</t:IsReadReceiptRequested>
              <t:IsDeliveryReceiptRequested>false</t:IsDeliveryReceiptRequested>
              <t:From>
                <t:Mailbox>
                  <t:Name>User2</t:Name>
                  <t:EmailAddress>User2@example.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                </t:Mailbox>
              </t:From>
              <t:IsRead>false</t:IsRead>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="d671a-125">Kommentare</span><span class="sxs-lookup"><span data-stu-id="d671a-125">Comments</span></span>

<span data-ttu-id="d671a-126">Die MIME-Inhalten, Ordner und Element-IDs wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d671a-126">The MIME content, folder, and item identifiers have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="d671a-127">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="d671a-127">Successful response elements</span></span>

<span data-ttu-id="d671a-128">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="d671a-128">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="d671a-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d671a-129">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="d671a-130">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="d671a-130">GetItemResponse</span></span>](getitemresponse.md)
    
- [<span data-ttu-id="d671a-131">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d671a-131">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d671a-132">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d671a-132">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
    
- [<span data-ttu-id="d671a-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d671a-133">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d671a-134">Elemente</span><span class="sxs-lookup"><span data-stu-id="d671a-134">Items</span></span>](items.md)
    
- [<span data-ttu-id="d671a-135">Message</span><span class="sxs-lookup"><span data-stu-id="d671a-135">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="d671a-136">' MimeContent '</span><span class="sxs-lookup"><span data-stu-id="d671a-136">MimeContent</span></span>](mimecontent.md)
    
- [<span data-ttu-id="d671a-137">ItemId</span><span class="sxs-lookup"><span data-stu-id="d671a-137">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="d671a-138">Betreff</span><span class="sxs-lookup"><span data-stu-id="d671a-138">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="d671a-139">Vertraulichkeit</span><span class="sxs-lookup"><span data-stu-id="d671a-139">Sensitivity</span></span>](sensitivity.md)
    
- [<span data-ttu-id="d671a-140">Body</span><span class="sxs-lookup"><span data-stu-id="d671a-140">Body</span></span>](body.md)
    
- [<span data-ttu-id="d671a-141">Size</span><span class="sxs-lookup"><span data-stu-id="d671a-141">Size</span></span>](size.md)
    
- [<span data-ttu-id="d671a-142">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="d671a-142">DateTimeSent</span></span>](datetimesent.md)
    
- [<span data-ttu-id="d671a-143">"Datetimecreated"</span><span class="sxs-lookup"><span data-stu-id="d671a-143">DateTimeCreated</span></span>](datetimecreated.md)
    
- [<span data-ttu-id="d671a-144">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="d671a-144">ResponseObjects</span></span>](responseobjects.md)
    
- [<span data-ttu-id="d671a-145">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="d671a-145">ReplyToItem</span></span>](replytoitem.md)
    
- [<span data-ttu-id="d671a-146">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="d671a-146">ReplyAllToItem</span></span>](replyalltoitem.md)
    
- [<span data-ttu-id="d671a-147">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="d671a-147">ForwardItem</span></span>](forwarditem.md)
    
- [<span data-ttu-id="d671a-148">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="d671a-148">HasAttachments</span></span>](hasattachments.md)
    
- [<span data-ttu-id="d671a-149">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="d671a-149">ToRecipients</span></span>](torecipients.md)
    
- [<span data-ttu-id="d671a-150">Postfach</span><span class="sxs-lookup"><span data-stu-id="d671a-150">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="d671a-151">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="d671a-151">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="d671a-152">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="d671a-152">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="d671a-153">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="d671a-153">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="d671a-154">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="d671a-154">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md)
    
- [<span data-ttu-id="d671a-155">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="d671a-155">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md)
    
- [<span data-ttu-id="d671a-156">Von</span><span class="sxs-lookup"><span data-stu-id="d671a-156">From</span></span>](from.md)
    
- [<span data-ttu-id="d671a-157">IsRead</span><span class="sxs-lookup"><span data-stu-id="d671a-157">IsRead</span></span>](isread.md)
    
## <a name="getitem-e-mail-message-error-response-example"></a><span data-ttu-id="d671a-158">GetItem (e-Mail-Nachricht) Fehler antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="d671a-158">GetItem (E-mail Message) Error response example</span></span>

### <a name="description"></a><span data-ttu-id="d671a-159">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d671a-159">Description</span></span>

<span data-ttu-id="d671a-160">Das folgende Beispiel zeigt eine Fehlerantwort an eine GetItem-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d671a-160">The following example shows an error response to a GetItem request.</span></span> <span data-ttu-id="d671a-161">Der Fehler wurde durch ein Versuch, eine ungültige zusätzliche Eigenschaft abzurufen verursacht.</span><span class="sxs-lookup"><span data-stu-id="d671a-161">The error was caused by an attempt to get an invalid additional property.</span></span>
  
### <a name="code"></a><span data-ttu-id="d671a-162">Code</span><span class="sxs-lookup"><span data-stu-id="d671a-162">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Error">
          <m:MessageText>Property is not valid for this object type.</m:MessageText>
          <m:ResponseCode>ErrorInvalidPropertyRequest</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:MessageXml>
            <t:FieldURI FieldURI="meeting:AssociatedCalendarItemId" />
          </m:MessageXml>
          <m:Items />
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="d671a-163">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="d671a-163">Error response elements</span></span>

<span data-ttu-id="d671a-164">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="d671a-164">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="d671a-165">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d671a-165">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="d671a-166">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="d671a-166">GetItemResponse</span></span>](getitemresponse.md)
    
- [<span data-ttu-id="d671a-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d671a-167">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d671a-168">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d671a-168">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
    
- [<span data-ttu-id="d671a-169">MessageText</span><span class="sxs-lookup"><span data-stu-id="d671a-169">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="d671a-170">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d671a-170">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d671a-171">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d671a-171">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="d671a-172">MessageXml</span><span class="sxs-lookup"><span data-stu-id="d671a-172">MessageXml</span></span>](messagexml.md)
    
- [<span data-ttu-id="d671a-173">FieldURI</span><span class="sxs-lookup"><span data-stu-id="d671a-173">FieldURI</span></span>](fielduri.md)
    
## <a name="see-also"></a><span data-ttu-id="d671a-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d671a-174">See also</span></span>



[<span data-ttu-id="d671a-175">GetItem Operation</span><span class="sxs-lookup"><span data-stu-id="d671a-175">GetItem operation</span></span>](getitem-operation.md)

