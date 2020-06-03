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
description: Der UpdateItem-Vorgang wird zum Aktualisieren der Eigenschaften von Kontaktelementen in der Exchange-Informationsspeicher verwendet.
ms.openlocfilehash: 66e1b91ea3154d8a501339aed7b398970e8f5392
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459826"
---
# <a name="updateitem-operation-contact"></a><span data-ttu-id="6c333-103">UpdateItem-Vorgang (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="6c333-103">UpdateItem operation (contact)</span></span>

<span data-ttu-id="6c333-104">Der UpdateItem-Vorgang wird zum Aktualisieren der Eigenschaften von Kontaktelementen in der Exchange-Informationsspeicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c333-104">The UpdateItem operation is used to update contact item properties in the Exchange store.</span></span>
  
## <a name="updateitem-contact-request-example"></a><span data-ttu-id="6c333-105">UpdateItem (Kontakt)-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="6c333-105">UpdateItem (Contact) request example</span></span>

### <a name="description"></a><span data-ttu-id="6c333-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c333-106">Description</span></span>

<span data-ttu-id="6c333-107">Im folgenden Codebeispiel wird veranschaulicht, wie die e-Mail-Adresse eines Kontakts aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6c333-107">The following code example shows how to update the e-mail address of a contact.</span></span>
  
### <a name="code"></a><span data-ttu-id="6c333-108">Code</span><span class="sxs-lookup"><span data-stu-id="6c333-108">Code</span></span>

```XML
<soap:Envelope
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
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

### <a name="comments"></a><span data-ttu-id="6c333-109">Comments</span><span class="sxs-lookup"><span data-stu-id="6c333-109">Comments</span></span>

<span data-ttu-id="6c333-110">Die Element-ID wurde verkürzt, um die Lesbarkeit beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="6c333-110">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="6c333-111">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="6c333-111">Request elements</span></span>

<span data-ttu-id="6c333-112">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="6c333-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="6c333-113">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="6c333-113">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="6c333-114">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="6c333-114">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="6c333-115">ItemChange</span><span class="sxs-lookup"><span data-stu-id="6c333-115">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="6c333-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="6c333-116">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="6c333-117">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="6c333-117">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="6c333-118">SetItemField</span><span class="sxs-lookup"><span data-stu-id="6c333-118">SetItemField</span></span>](setitemfield.md)
    
- [<span data-ttu-id="6c333-119">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="6c333-119">IndexedFieldURI</span></span>](indexedfielduri.md)
    
- [<span data-ttu-id="6c333-120">Contact</span><span class="sxs-lookup"><span data-stu-id="6c333-120">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="6c333-121">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="6c333-121">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="6c333-122">Eintrag (e-mailemail)</span><span class="sxs-lookup"><span data-stu-id="6c333-122">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
## <a name="successful-updateitem-contact-response"></a><span data-ttu-id="6c333-123">Erfolgreiche UpdateItem-Antwort (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="6c333-123">Successful UpdateItem (Contact) Response</span></span>

### <a name="description"></a><span data-ttu-id="6c333-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c333-124">Description</span></span>

<span data-ttu-id="6c333-125">Das folgende Codebeispiel zeigt eine erfolgreiche UpdateItem-Antwort.</span><span class="sxs-lookup"><span data-stu-id="6c333-125">The following code example shows a successful UpdateItem response.</span></span>
  
### <a name="code"></a><span data-ttu-id="6c333-126">Code</span><span class="sxs-lookup"><span data-stu-id="6c333-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UpdateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="6c333-127">Comments</span><span class="sxs-lookup"><span data-stu-id="6c333-127">Comments</span></span>

<span data-ttu-id="6c333-128">Die Element-ID wurde verkürzt, um die Lesbarkeit beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="6c333-128">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="6c333-129">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="6c333-129">Successful response elements</span></span>

<span data-ttu-id="6c333-130">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="6c333-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="6c333-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="6c333-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="6c333-132">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="6c333-132">UpdateItemResponse</span></span>](updateitemresponse.md)
    
- [<span data-ttu-id="6c333-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6c333-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="6c333-134">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6c333-134">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
    
- [<span data-ttu-id="6c333-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6c333-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="6c333-136">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="6c333-136">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="6c333-137">Contact</span><span class="sxs-lookup"><span data-stu-id="6c333-137">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="6c333-138">ItemId</span><span class="sxs-lookup"><span data-stu-id="6c333-138">ItemId</span></span>](itemid.md)
    
## <a name="invalid-updateitem-contact-request-example"></a><span data-ttu-id="6c333-139">Ungültiges UpdateItem (Contact)-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="6c333-139">Invalid UpdateItem (Contact) request example</span></span>

### <a name="description"></a><span data-ttu-id="6c333-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c333-140">Description</span></span>

<span data-ttu-id="6c333-141">Das folgende Codebeispiel zeigt eine ungültige Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6c333-141">The following code example shows an invalid request.</span></span>
  
### <a name="code"></a><span data-ttu-id="6c333-142">Code</span><span class="sxs-lookup"><span data-stu-id="6c333-142">Code</span></span>

```XML
<soap:Envelope
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
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

### <a name="comments"></a><span data-ttu-id="6c333-143">Comments</span><span class="sxs-lookup"><span data-stu-id="6c333-143">Comments</span></span>

<span data-ttu-id="6c333-144">Die Element-ID wurde verkürzt, um die Lesbarkeit beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="6c333-144">The item identifier has been shortened to preserve readability.</span></span>
  
## <a name="updateitem-contact-error-response"></a><span data-ttu-id="6c333-145">UpdateItem (Kontakt)-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="6c333-145">UpdateItem (Contact) error response</span></span>

### <a name="description"></a><span data-ttu-id="6c333-146">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c333-146">Description</span></span>

<span data-ttu-id="6c333-147">Das folgende Codebeispiel zeigt eine Fehlerantwort auf eine UpdateItem (Contact)-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6c333-147">The following code example shows an error response to an UpdateItem (Contact) request.</span></span>
  
### <a name="code"></a><span data-ttu-id="6c333-148">Code</span><span class="sxs-lookup"><span data-stu-id="6c333-148">Code</span></span>

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <soap:Fault>
      <soap:faultcode>Client</soap:faultcode>
      <soap:faultstring>The request failed schema validation.</soap:faultstring>
      <detail>
        <e:ResponseCode xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">ErrorSchemaValidation</e:ResponseCode>
        <e:Message xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">The 'Key' attribute is invalid - The value 'EmailAddress4' is invalid according to its data type 'https://schemas.microsoft.com/exchange/services/2006/types:EmailAddressKeyType' - The Enumeration constraint failed.</e:Message>
        <e:Line xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">17</e:Line>
        <e:Position xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">19</e:Position>
      </detail>
    </soap:Fault>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="6c333-149">Comments</span><span class="sxs-lookup"><span data-stu-id="6c333-149">Comments</span></span>

<span data-ttu-id="6c333-150">Einige Elemente, die im SOAP-Textkörper einer Fehlerantwort verwendet werden, die durch einen Schemaüberprüfungsfehler verursacht wird, sind nicht in den Schemas "Nachrichten" oder "Typen" definiert.</span><span class="sxs-lookup"><span data-stu-id="6c333-150">Some elements that are used in the SOAP body of an error response that is caused by a schema validation error are not defined in the messages or types schemas.</span></span> <span data-ttu-id="6c333-151">Das **Detail** -Element enthält Informationen zum Fehler.</span><span class="sxs-lookup"><span data-stu-id="6c333-151">The **detail** element contains information about the error.</span></span> <span data-ttu-id="6c333-152">Das [Response Code](responsecode.md) -Element enthält den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6c333-152">The [ResponseCode](responsecode.md) element contains the error code.</span></span> <span data-ttu-id="6c333-153">Das [Message](message-ex15websvcsotherref.md) -Element enthält eine Erklärung für den Fehler, sofern einer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6c333-153">The [Message](message-ex15websvcsotherref.md) element contains an explanation for the error, if one is available.</span></span> <span data-ttu-id="6c333-154">Das Element " **Position** " beschreibt die Nummer der Nummer, in der der Schemaüberprüfungsfehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="6c333-154">The **Line** element describes the line number where the schema validation error occurred.</span></span> <span data-ttu-id="6c333-155">Das **Position** -Element beschreibt die Position vom äußersten linken Zeichen des XML-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="6c333-155">The **Position** element describes the position from the leftmost character of the XML document.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6c333-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c333-156">See also</span></span>



[<span data-ttu-id="6c333-157">UpdateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6c333-157">UpdateItem operation</span></span>](updateitem-operation.md)

