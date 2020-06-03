---
title: GetItem-Vorgang (e-Mail-Nachricht)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- GetItem
api_type:
- schema
ms.assetid: e8492e3b-1c8d-4b14-8070-9530f8306edd
description: Der GetItem-Vorgang ermöglicht dem Benutzer den Zugriff auf Informationen über e-Mail-Nachrichten.
localization_priority: Priority
ms.openlocfilehash: f8be01cad3d4c4534f66593cbe8bcee477726972
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459994"
---
# <a name="getitem-operation-email-message"></a><span data-ttu-id="4d8f0-103">GetItem-Vorgang (e-Mail-Nachricht)</span><span class="sxs-lookup"><span data-stu-id="4d8f0-103">GetItem operation (email message)</span></span>

<span data-ttu-id="4d8f0-104">Der GetItem-Vorgang ermöglicht dem Benutzer den Zugriff auf Informationen über e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="4d8f0-104">The GetItem operation allows the user to access information about e-mail messages.</span></span>
  
## <a name="using-the-getitem-operation-for-messages"></a><span data-ttu-id="4d8f0-105">Verwenden des GetItem-Vorgangs für Nachrichten</span><span class="sxs-lookup"><span data-stu-id="4d8f0-105">Using the GetItem Operation for Messages</span></span>

<span data-ttu-id="4d8f0-106">Die GetItem-Anforderung muss über die folgenden Informationen verfügen:</span><span class="sxs-lookup"><span data-stu-id="4d8f0-106">The GetItem request must have the following information:</span></span>
  
- <span data-ttu-id="4d8f0-107">Das [ItemID](itemid.md) -Element zum Identifizieren der zurückzugebenden Elementinformationen.</span><span class="sxs-lookup"><span data-stu-id="4d8f0-107">The [ItemId](itemid.md) element to identify the item information to return.</span></span> 
    
- <span data-ttu-id="4d8f0-108">Das [ItemShape](itemshape.md) -Element, um die zurückzugebenden Elementeigenschaften zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4d8f0-108">The [ItemShape](itemshape.md) element to identify the item properties to return.</span></span> 
    
## <a name="getitem-request-example"></a><span data-ttu-id="4d8f0-109">GetItem-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="4d8f0-109">GetItem request example</span></span>

### <a name="description"></a><span data-ttu-id="4d8f0-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d8f0-110">Description</span></span>

<span data-ttu-id="4d8f0-111">Im folgenden Beispiel einer GetItem-Anforderung wird gezeigt, wie auf Informationen zu e-Mail-Nachrichten zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="4d8f0-111">The following example of a GetItem request shows how to access information about e-mail messages.</span></span>
  
### <a name="code"></a><span data-ttu-id="4d8f0-112">Code</span><span class="sxs-lookup"><span data-stu-id="4d8f0-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xmlns:xsd="http://www.w3.org/2001/XMLSchema"
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem
      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="request-elements"></a><span data-ttu-id="4d8f0-113">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="4d8f0-113">Request elements</span></span>

<span data-ttu-id="4d8f0-114">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="4d8f0-114">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="4d8f0-115">GetItem</span><span class="sxs-lookup"><span data-stu-id="4d8f0-115">GetItem</span></span>](getitem.md)
    
- [<span data-ttu-id="4d8f0-116">ItemShape</span><span class="sxs-lookup"><span data-stu-id="4d8f0-116">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="4d8f0-117">BaseShape</span><span class="sxs-lookup"><span data-stu-id="4d8f0-117">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="4d8f0-118">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="4d8f0-118">IncludeMimeContent</span></span>](includemimecontent.md)
    
- [<span data-ttu-id="4d8f0-119">ItemIds</span><span class="sxs-lookup"><span data-stu-id="4d8f0-119">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="4d8f0-120">ItemId</span><span class="sxs-lookup"><span data-stu-id="4d8f0-120">ItemId</span></span>](itemid.md)
    
## <a name="successful-getitem-e-mail-message-response-example"></a><span data-ttu-id="4d8f0-121">Erfolgreiches GetItem (e-Mail-Nachricht)-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="4d8f0-121">Successful GetItem (E-mail Message) response example</span></span>

### <a name="description"></a><span data-ttu-id="4d8f0-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d8f0-122">Description</span></span>

<span data-ttu-id="4d8f0-123">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die GetItem-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4d8f0-123">The following example shows a successful response to the GetItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="4d8f0-124">Code</span><span class="sxs-lookup"><span data-stu-id="4d8f0-124">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="4d8f0-125">Comments</span><span class="sxs-lookup"><span data-stu-id="4d8f0-125">Comments</span></span>

<span data-ttu-id="4d8f0-126">Die MIME-Inhalte, Ordner und Element-IDs wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4d8f0-126">The MIME content, folder, and item identifiers have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="4d8f0-127">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="4d8f0-127">Successful response elements</span></span>

<span data-ttu-id="4d8f0-128">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="4d8f0-128">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="4d8f0-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="4d8f0-129">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="4d8f0-130">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="4d8f0-130">GetItemResponse</span></span>](getitemresponse.md)
    
- [<span data-ttu-id="4d8f0-131">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4d8f0-131">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="4d8f0-132">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4d8f0-132">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
    
- [<span data-ttu-id="4d8f0-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4d8f0-133">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="4d8f0-134">Elemente</span><span class="sxs-lookup"><span data-stu-id="4d8f0-134">Items</span></span>](items.md)
    
- [<span data-ttu-id="4d8f0-135">Message</span><span class="sxs-lookup"><span data-stu-id="4d8f0-135">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="4d8f0-136">MimeContent</span><span class="sxs-lookup"><span data-stu-id="4d8f0-136">MimeContent</span></span>](mimecontent.md)
    
- [<span data-ttu-id="4d8f0-137">ItemId</span><span class="sxs-lookup"><span data-stu-id="4d8f0-137">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="4d8f0-138">Betreff</span><span class="sxs-lookup"><span data-stu-id="4d8f0-138">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="4d8f0-139">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="4d8f0-139">Sensitivity</span></span>](sensitivity.md)
    
- [<span data-ttu-id="4d8f0-140">Body</span><span class="sxs-lookup"><span data-stu-id="4d8f0-140">Body</span></span>](body.md)
    
- [<span data-ttu-id="4d8f0-141">Größe</span><span class="sxs-lookup"><span data-stu-id="4d8f0-141">Size</span></span>](size.md)
    
- [<span data-ttu-id="4d8f0-142">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="4d8f0-142">DateTimeSent</span></span>](datetimesent.md)
    
- [<span data-ttu-id="4d8f0-143">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="4d8f0-143">DateTimeCreated</span></span>](datetimecreated.md)
    
- [<span data-ttu-id="4d8f0-144">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="4d8f0-144">ResponseObjects</span></span>](responseobjects.md)
    
- [<span data-ttu-id="4d8f0-145">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="4d8f0-145">ReplyToItem</span></span>](replytoitem.md)
    
- [<span data-ttu-id="4d8f0-146">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="4d8f0-146">ReplyAllToItem</span></span>](replyalltoitem.md)
    
- [<span data-ttu-id="4d8f0-147">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="4d8f0-147">ForwardItem</span></span>](forwarditem.md)
    
- [<span data-ttu-id="4d8f0-148">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="4d8f0-148">HasAttachments</span></span>](hasattachments.md)
    
- [<span data-ttu-id="4d8f0-149">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="4d8f0-149">ToRecipients</span></span>](torecipients.md)
    
- [<span data-ttu-id="4d8f0-150">Postfach</span><span class="sxs-lookup"><span data-stu-id="4d8f0-150">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="4d8f0-151">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="4d8f0-151">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="4d8f0-152">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="4d8f0-152">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="4d8f0-153">Routingtype (e-mailemailtype)</span><span class="sxs-lookup"><span data-stu-id="4d8f0-153">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="4d8f0-154">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="4d8f0-154">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md)
    
- [<span data-ttu-id="4d8f0-155">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="4d8f0-155">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md)
    
- [<span data-ttu-id="4d8f0-156">From</span><span class="sxs-lookup"><span data-stu-id="4d8f0-156">From</span></span>](from.md)
    
- [<span data-ttu-id="4d8f0-157">IsRead</span><span class="sxs-lookup"><span data-stu-id="4d8f0-157">IsRead</span></span>](isread.md)
    
## <a name="getitem-e-mail-message-error-response-example"></a><span data-ttu-id="4d8f0-158">Fehlerantwort-Beispiel für GetItem (e-Mail-Nachricht)</span><span class="sxs-lookup"><span data-stu-id="4d8f0-158">GetItem (E-mail Message) Error response example</span></span>

### <a name="description"></a><span data-ttu-id="4d8f0-159">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d8f0-159">Description</span></span>

<span data-ttu-id="4d8f0-160">Das folgende Beispiel zeigt eine Fehlerantwort auf eine GetItem-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4d8f0-160">The following example shows an error response to a GetItem request.</span></span> <span data-ttu-id="4d8f0-161">Der Fehler wurde durch einen Versuch verursacht, eine ungültige zusätzliche Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4d8f0-161">The error was caused by an attempt to get an invalid additional property.</span></span>
  
### <a name="code"></a><span data-ttu-id="4d8f0-162">Code</span><span class="sxs-lookup"><span data-stu-id="4d8f0-162">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="4d8f0-163">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="4d8f0-163">Error response elements</span></span>

<span data-ttu-id="4d8f0-164">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="4d8f0-164">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="4d8f0-165">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="4d8f0-165">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="4d8f0-166">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="4d8f0-166">GetItemResponse</span></span>](getitemresponse.md)
    
- [<span data-ttu-id="4d8f0-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4d8f0-167">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="4d8f0-168">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4d8f0-168">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
    
- [<span data-ttu-id="4d8f0-169">MessageText</span><span class="sxs-lookup"><span data-stu-id="4d8f0-169">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="4d8f0-170">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4d8f0-170">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="4d8f0-171">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="4d8f0-171">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="4d8f0-172">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="4d8f0-172">MessageXml</span></span>](messagexml.md)
    
- [<span data-ttu-id="4d8f0-173">FieldURI</span><span class="sxs-lookup"><span data-stu-id="4d8f0-173">FieldURI</span></span>](fielduri.md)
    
## <a name="see-also"></a><span data-ttu-id="4d8f0-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d8f0-174">See also</span></span>



[<span data-ttu-id="4d8f0-175">GetItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4d8f0-175">GetItem operation</span></span>](getitem-operation.md)

