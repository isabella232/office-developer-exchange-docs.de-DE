---
title: CreateItem-Vorgang (Kontakt)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: 417e994b-0a17-4c24-9527-04796b80b029
description: Der CreateItem-Vorgang wird verwendet, um Kontakte im Exchange-Speicher zu erstellen.
ms.openlocfilehash: 05e4715f3c6675401ae7afac852395f7459c02c9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757776"
---
# <a name="createitem-operation-contact"></a><span data-ttu-id="9fe9f-103">CreateItem-Vorgang (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="9fe9f-103">CreateItem operation (contact)</span></span>

<span data-ttu-id="9fe9f-104">Der CreateItem-Vorgang wird verwendet, um Kontakte im Exchange-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9fe9f-104">The CreateItem operation is used to create contacts in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9fe9f-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9fe9f-105">Remarks</span></span>

<span data-ttu-id="9fe9f-106">Die Erstellung des privaten Verteilerlisten wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9fe9f-106">The creation of private distribution lists is not supported.</span></span> <span data-ttu-id="9fe9f-107">Alle Eigenschaften innerhalb des Containers [CompleteName](completename.md) sind schreibgeschützt und können nicht auf ein Kontaktelement festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9fe9f-107">All properties within the [CompleteName](completename.md) container are read-only and cannot be set on a contact item.</span></span> 
  
## <a name="createitem-request-example"></a><span data-ttu-id="9fe9f-108">CreateItem anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="9fe9f-108">CreateItem request example</span></span>

### <a name="description"></a><span data-ttu-id="9fe9f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9fe9f-109">Description</span></span>

<span data-ttu-id="9fe9f-110">Im folgenden Beispiel wird eine gültige CreateItem SOAP-Anforderung zeigt, wie einen Kontakt in den Standardordner Kontakte erstellt.</span><span class="sxs-lookup"><span data-stu-id="9fe9f-110">The following example of a valid CreateItem SOAP request shows how to create a contact in the default Contacts folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="9fe9f-111">Code</span><span class="sxs-lookup"><span data-stu-id="9fe9f-111">Code</span></span>

```XML
<soap:Envelope
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" >
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id="contacts"/>
      </SavedItemFolderId>
      <Items>
        <t:Contact>
          <t:FileAs>SampleContact</t:FileAs>
          <t:GivenName>Tanja</t:GivenName>
          <t:CompanyName>Blue Yonder Airlines</t:CompanyName>
          <t:EmailAddresses>
            <t:Entry Key="EmailAddress1">tplate@example.com</t:Entry>
          </t:EmailAddresses>
          <t:PhysicalAddresses>
            <t:Entry Key="Business">
              <t:Street>1234 56th Ave</t:Street>
              <t:City>La Habra</t:City>
              <t:State>CA</t:State>
              <t: CountryOrRegion>USA</t: CountryOrRegion>
            </t:Entry>
          </t:PhysicalAddresses>
          <t:PhoneNumbers>
            <t:Entry Key="BusinessPhone">4255550199</t:Entry>
          </t:PhoneNumbers>
          <t:JobTitle>Manager</t:JobTitle>
          <t:Surname>Plate</t:Surname>
        </t:Contact>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="9fe9f-112">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="9fe9f-112">Request elements</span></span>

<span data-ttu-id="9fe9f-113">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="9fe9f-113">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="9fe9f-114">CreateItem</span><span class="sxs-lookup"><span data-stu-id="9fe9f-114">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="9fe9f-115">Des SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="9fe9f-115">SavedItemFolderId</span></span>](saveditemfolderid.md)
    
- [<span data-ttu-id="9fe9f-116">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="9fe9f-116">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="9fe9f-117">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="9fe9f-117">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="9fe9f-118">Contact</span><span class="sxs-lookup"><span data-stu-id="9fe9f-118">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="9fe9f-119">FileAs</span><span class="sxs-lookup"><span data-stu-id="9fe9f-119">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="9fe9f-120">Vorname</span><span class="sxs-lookup"><span data-stu-id="9fe9f-120">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="9fe9f-121">Firma</span><span class="sxs-lookup"><span data-stu-id="9fe9f-121">CompanyName</span></span>](companyname.md)
    
- [<span data-ttu-id="9fe9f-122">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="9fe9f-122">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="9fe9f-123">Eintrag (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="9fe9f-123">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
- [<span data-ttu-id="9fe9f-124">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="9fe9f-124">PhysicalAddresses</span></span>](physicaladdresses.md)
    
- [<span data-ttu-id="9fe9f-125">Eintrag (physikalische Adresse)</span><span class="sxs-lookup"><span data-stu-id="9fe9f-125">Entry (PhysicalAddress)</span></span>](entry-physicaladdress.md)
    
- [<span data-ttu-id="9fe9f-126">Straße</span><span class="sxs-lookup"><span data-stu-id="9fe9f-126">Street</span></span>](street.md)
    
- [<span data-ttu-id="9fe9f-127">City</span><span class="sxs-lookup"><span data-stu-id="9fe9f-127">City</span></span>](city.md)
    
- [<span data-ttu-id="9fe9f-128">State</span><span class="sxs-lookup"><span data-stu-id="9fe9f-128">State</span></span>](state-ex15websvcsotherref.md)
    
- [<span data-ttu-id="9fe9f-129">CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="9fe9f-129">CountryOrRegion</span></span>](countryorregion.md)
    
- [<span data-ttu-id="9fe9f-130">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="9fe9f-130">PhoneNumbers</span></span>](phonenumbers.md)
    
- [<span data-ttu-id="9fe9f-131">Eintrag ("PhoneNumber")</span><span class="sxs-lookup"><span data-stu-id="9fe9f-131">Entry (PhoneNumber)</span></span>](entry-phonenumber.md)
    
- [<span data-ttu-id="9fe9f-132">JobTitle</span><span class="sxs-lookup"><span data-stu-id="9fe9f-132">JobTitle</span></span>](jobtitle.md)
    
- [<span data-ttu-id="9fe9f-133">Nachname</span><span class="sxs-lookup"><span data-stu-id="9fe9f-133">Surname</span></span>](surname.md)
    
## <a name="successful-createitem-request"></a><span data-ttu-id="9fe9f-134">Erfolgreiche CreateItem-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fe9f-134">Successful CreateItem Request</span></span>

### <a name="description"></a><span data-ttu-id="9fe9f-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9fe9f-135">Description</span></span>

<span data-ttu-id="9fe9f-136">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die CreateItem-Anforderung, die ein Kontakt erstellt.</span><span class="sxs-lookup"><span data-stu-id="9fe9f-136">The following example shows a successful response to the CreateItem request that created a contact.</span></span> <span data-ttu-id="9fe9f-137">In diesem Beispiel enthält die Antwort den Bezeichner des das neu erstellte Element.</span><span class="sxs-lookup"><span data-stu-id="9fe9f-137">In this example, the response contains the identifier of the newly created item.</span></span>
  
### <a name="code"></a><span data-ttu-id="9fe9f-138">Code</span><span class="sxs-lookup"><span data-stu-id="9fe9f-138">Code</span></span>

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
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Contact>
              <t:ItemId Id="AAAtA=" ChangeKey="EQAAAB" />
            </t:Contact>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="9fe9f-139">Kommentare</span><span class="sxs-lookup"><span data-stu-id="9fe9f-139">Comments</span></span>

<span data-ttu-id="9fe9f-140">Der Elementbezeichner wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9fe9f-140">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="9fe9f-141">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="9fe9f-141">Successful response elements</span></span>

<span data-ttu-id="9fe9f-142">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="9fe9f-142">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="9fe9f-143">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="9fe9f-143">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="9fe9f-144">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="9fe9f-144">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="9fe9f-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9fe9f-145">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="9fe9f-146">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9fe9f-146">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="9fe9f-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9fe9f-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="9fe9f-148">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="9fe9f-148">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="9fe9f-149">Contact</span><span class="sxs-lookup"><span data-stu-id="9fe9f-149">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="9fe9f-150">ItemId</span><span class="sxs-lookup"><span data-stu-id="9fe9f-150">ItemId</span></span>](itemid.md)
    
## <a name="invalid-createitem-request-example"></a><span data-ttu-id="9fe9f-151">Ungültige CreateItem anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="9fe9f-151">Invalid CreateItem request example</span></span>

### <a name="description"></a><span data-ttu-id="9fe9f-152">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9fe9f-152">Description</span></span>

<span data-ttu-id="9fe9f-153">Das folgende Beispiel zeigt eine Anforderung, die gültigen XML-Code aber nicht kompatibel Anweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="9fe9f-153">The following example shows a request that contains valid XML but incompatible instructions.</span></span> <span data-ttu-id="9fe9f-154">Ein Kontakt kann nicht in einem Suchordner erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9fe9f-154">A contact cannot be created in a search folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="9fe9f-155">Code</span><span class="sxs-lookup"><span data-stu-id="9fe9f-155">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns='http://schemas.microsoft.com/exchange/services/2006/messages'>
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id='searchfolders'/>
      </SavedItemFolderId>
      <Items>
        <t:Contact>
          <t:ItemClass>IPM.Contact</t:ItemClass>
        </t:Contact>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="createitem-contact-error-response"></a><span data-ttu-id="9fe9f-156">Fehlerantwort CreateItem (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="9fe9f-156">CreateItem (Contact) error response</span></span>

### <a name="description"></a><span data-ttu-id="9fe9f-157">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9fe9f-157">Description</span></span>

<span data-ttu-id="9fe9f-158">Das folgende Beispiel zeigt eine Fehlerantwort an eine Anforderung CreateItem (Kontakt).</span><span class="sxs-lookup"><span data-stu-id="9fe9f-158">The following example shows an error response to a CreateItem (Contact) request.</span></span>
  
### <a name="code"></a><span data-ttu-id="9fe9f-159">Code</span><span class="sxs-lookup"><span data-stu-id="9fe9f-159">Code</span></span>

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
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Error">
          <m:MessageText>Cannot create a contact in a non-contact Folder.</m:MessageText>
          <m:ResponseCode>ErrorCannotCreateContactInNonContactFolder</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Items />
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="9fe9f-160">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="9fe9f-160">Error response elements</span></span>

<span data-ttu-id="9fe9f-161">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="9fe9f-161">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="9fe9f-162">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="9fe9f-162">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="9fe9f-163">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="9fe9f-163">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="9fe9f-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9fe9f-164">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="9fe9f-165">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9fe9f-165">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="9fe9f-166">MessageText</span><span class="sxs-lookup"><span data-stu-id="9fe9f-166">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="9fe9f-167">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9fe9f-167">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="9fe9f-168">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9fe9f-168">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="9fe9f-169">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="9fe9f-169">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
## <a name="see-also"></a><span data-ttu-id="9fe9f-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fe9f-170">See also</span></span>



[<span data-ttu-id="9fe9f-171">CreateItem Operation</span><span class="sxs-lookup"><span data-stu-id="9fe9f-171">CreateItem operation</span></span>](createitem-operation.md)

