---
title: UpdateItem-Vorgang (Kontakt)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 298fdd71-a83d-4407-9728-4f0a8e2d857c
description: Der Vorgang UpdateItem wird verwendet, um Eigenschaften für Kontaktelemente im Exchange-Speicher zu aktualisieren.
ms.openlocfilehash: f2a501ce8e69068cd30b58011adf4defc68ce365
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839372"
---
# <a name="updateitem-operation-contact"></a><span data-ttu-id="61010-103">UpdateItem-Vorgang (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="61010-103">UpdateItem operation (contact)</span></span>

<span data-ttu-id="61010-104">Der Vorgang UpdateItem wird verwendet, um Eigenschaften für Kontaktelemente im Exchange-Speicher zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="61010-104">The UpdateItem operation is used to update contact item properties in the Exchange store.</span></span>
  
## <a name="updateitem-contact-request-example"></a><span data-ttu-id="61010-105">Anforderungsbeispiel UpdateItem (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="61010-105">UpdateItem (Contact) request example</span></span>

### <a name="description"></a><span data-ttu-id="61010-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61010-106">Description</span></span>

<span data-ttu-id="61010-107">Im folgenden Codebeispiel wird veranschaulicht, wie die e-Mail-Adresse eines Kontakts zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="61010-107">The following code example shows how to update the e-mail address of a contact.</span></span>
  
### <a name="code"></a><span data-ttu-id="61010-108">Code</span><span class="sxs-lookup"><span data-stu-id="61010-108">Code</span></span>

```XML
<soap:Envelope
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                ConflictResolution="AlwaysOverwrite">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAA=" ChangeKey="EQAAABYi" />
          <t:Updates>
            <t:SetItemField>
              <t:IndexedFieldURI FieldURI="contacts:EmailAddress" FieldIndex="EmailAddress1"/>
              <t:Contact>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress1">changedemail@example.com</t:Entry>
                </t:EmailAddresses>
              </t:Contact>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="61010-109">Kommentare</span><span class="sxs-lookup"><span data-stu-id="61010-109">Comments</span></span>

<span data-ttu-id="61010-110">Der Elementbezeichner wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="61010-110">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="61010-111">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="61010-111">Request elements</span></span>

<span data-ttu-id="61010-112">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="61010-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="61010-113">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="61010-113">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="61010-114">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="61010-114">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="61010-115">ItemChange</span><span class="sxs-lookup"><span data-stu-id="61010-115">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="61010-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="61010-116">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="61010-117">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="61010-117">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="61010-118">SetItemField</span><span class="sxs-lookup"><span data-stu-id="61010-118">SetItemField</span></span>](setitemfield.md)
    
- [<span data-ttu-id="61010-119">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="61010-119">IndexedFieldURI</span></span>](indexedfielduri.md)
    
- [<span data-ttu-id="61010-120">Contact</span><span class="sxs-lookup"><span data-stu-id="61010-120">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="61010-121">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="61010-121">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="61010-122">Eintrag (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="61010-122">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
## <a name="successful-updateitem-contact-response"></a><span data-ttu-id="61010-123">Antwort erfolgreich UpdateItem (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="61010-123">Successful UpdateItem (Contact) Response</span></span>

### <a name="description"></a><span data-ttu-id="61010-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61010-124">Description</span></span>

<span data-ttu-id="61010-125">Das folgende Codebeispiel zeigt eine erfolgreiche Antwort UpdateItem.</span><span class="sxs-lookup"><span data-stu-id="61010-125">The following code example shows a successful UpdateItem response.</span></span>
  
### <a name="code"></a><span data-ttu-id="61010-126">Code</span><span class="sxs-lookup"><span data-stu-id="61010-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UpdateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Contact>
              <t:ItemId Id="AAAtAE=" ChangeKey="EQAAABYx" />
            </t:Contact>
          </m:Items>
        </m:UpdateItemResponseMessage>
      </m:ResponseMessages>
    </UpdateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="61010-127">Kommentare</span><span class="sxs-lookup"><span data-stu-id="61010-127">Comments</span></span>

<span data-ttu-id="61010-128">Der Elementbezeichner wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="61010-128">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="61010-129">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="61010-129">Successful response elements</span></span>

<span data-ttu-id="61010-130">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="61010-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="61010-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="61010-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="61010-132">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="61010-132">UpdateItemResponse</span></span>](updateitemresponse.md)
    
- [<span data-ttu-id="61010-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="61010-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="61010-134">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="61010-134">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
    
- [<span data-ttu-id="61010-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="61010-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="61010-136">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="61010-136">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="61010-137">Contact</span><span class="sxs-lookup"><span data-stu-id="61010-137">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="61010-138">ItemId</span><span class="sxs-lookup"><span data-stu-id="61010-138">ItemId</span></span>](itemid.md)
    
## <a name="invalid-updateitem-contact-request-example"></a><span data-ttu-id="61010-139">Ungültige UpdateItem (Kontakt) anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="61010-139">Invalid UpdateItem (Contact) request example</span></span>

### <a name="description"></a><span data-ttu-id="61010-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61010-140">Description</span></span>

<span data-ttu-id="61010-141">Das folgende Codebeispiel zeigt eine ungültige Anforderung.</span><span class="sxs-lookup"><span data-stu-id="61010-141">The following code example shows an invalid request.</span></span>
  
### <a name="code"></a><span data-ttu-id="61010-142">Code</span><span class="sxs-lookup"><span data-stu-id="61010-142">Code</span></span>

```XML
<soap:Envelope
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                ConflictResolution="AlwaysOverwrite">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEF=" ChangeKey="EQAAABYi" />
          <t:Updates>
            <t:SetItemField>
              <t:IndexedFieldURI FieldURI="contacts:EmailAddress" FieldIndex="EmailAddress4"/>
              <t:Contact>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress4">changedemail2@example.com</t:Entry>
                </t:EmailAddresses>
              </t:Contact>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="61010-143">Kommentare</span><span class="sxs-lookup"><span data-stu-id="61010-143">Comments</span></span>

<span data-ttu-id="61010-144">Der Elementbezeichner wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="61010-144">The item identifier has been shortened to preserve readability.</span></span>
  
## <a name="updateitem-contact-error-response"></a><span data-ttu-id="61010-145">Fehlerantwort UpdateItem (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="61010-145">UpdateItem (Contact) error response</span></span>

### <a name="description"></a><span data-ttu-id="61010-146">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61010-146">Description</span></span>

<span data-ttu-id="61010-147">Das folgende Codebeispiel zeigt eine Fehlerantwort auf eine Anforderung UpdateItem (Kontakt).</span><span class="sxs-lookup"><span data-stu-id="61010-147">The following code example shows an error response to an UpdateItem (Contact) request.</span></span>
  
### <a name="code"></a><span data-ttu-id="61010-148">Code</span><span class="sxs-lookup"><span data-stu-id="61010-148">Code</span></span>

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <soap:Fault>
      <soap:faultcode>Client</soap:faultcode>
      <soap:faultstring>The request failed schema validation.</soap:faultstring>
      <detail>
        <e:ResponseCode xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">ErrorSchemaValidation</e:ResponseCode>
        <e:Message xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">The 'Key' attribute is invalid - The value 'EmailAddress4' is invalid according to its data type 'http://schemas.microsoft.com/exchange/services/2006/types:EmailAddressKeyType' - The Enumeration constraint failed.</e:Message>
        <e:Line xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">17</e:Line>
        <e:Position xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">19</e:Position>
      </detail>
    </soap:Fault>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="61010-149">Kommentare</span><span class="sxs-lookup"><span data-stu-id="61010-149">Comments</span></span>

<span data-ttu-id="61010-150">Einige Elemente, die in der SOAP-Body einer Fehlerantwort verwendet werden, die durch ein Schemavalidierungsfehler verursacht wird sind nicht in den Nachrichten oder Arten-Schemas definiert.</span><span class="sxs-lookup"><span data-stu-id="61010-150">Some elements that are used in the SOAP body of an error response that is caused by a schema validation error are not defined in the messages or types schemas.</span></span> <span data-ttu-id="61010-151">Das **Detail** -Element enthält Informationen zu dem Fehler.</span><span class="sxs-lookup"><span data-stu-id="61010-151">The **detail** element contains information about the error.</span></span> <span data-ttu-id="61010-152">Das [ResponseCode](responsecode.md) -Element enthält den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="61010-152">The [ResponseCode](responsecode.md) element contains the error code.</span></span> <span data-ttu-id="61010-153">Das [Nachricht](message-ex15websvcsotherref.md) -Element enthält eine Beschreibung für den Fehler, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="61010-153">The [Message](message-ex15websvcsotherref.md) element contains an explanation for the error, if one is available.</span></span> <span data-ttu-id="61010-154">Das **Zeile** -Element beschreibt die Zeilennummer, in dem der Schema-Validierungsfehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="61010-154">The **Line** element describes the line number where the schema validation error occurred.</span></span> <span data-ttu-id="61010-155">Das **Position** -Element beschreibt die Position der äußersten linken Zeichen des XML-Dokuments aus.</span><span class="sxs-lookup"><span data-stu-id="61010-155">The **Position** element describes the position from the leftmost character of the XML document.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="61010-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61010-156">See also</span></span>



[<span data-ttu-id="61010-157">UpdateItem Operation</span><span class="sxs-lookup"><span data-stu-id="61010-157">UpdateItem operation</span></span>](updateitem-operation.md)

