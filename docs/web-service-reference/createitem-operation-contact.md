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
description: Der CreateItem-Vorgang wird zum Erstellen von Kontakten im Exchange-Informationsspeicher verwendet.
ms.openlocfilehash: e1d78392b94d328cf687655cd93e6c9568f6274f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457123"
---
# <a name="createitem-operation-contact"></a><span data-ttu-id="1f16d-103">CreateItem-Vorgang (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="1f16d-103">CreateItem operation (contact)</span></span>

<span data-ttu-id="1f16d-104">Der CreateItem-Vorgang wird zum Erstellen von Kontakten im Exchange-Informationsspeicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f16d-104">The CreateItem operation is used to create contacts in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1f16d-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f16d-105">Remarks</span></span>

<span data-ttu-id="1f16d-106">Das Erstellen privater Verteilerlisten wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1f16d-106">The creation of private distribution lists is not supported.</span></span> <span data-ttu-id="1f16d-107">Alle Eigenschaften im Container [completename](completename.md) sind schreibgeschützt und können für ein Kontaktelement nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1f16d-107">All properties within the [CompleteName](completename.md) container are read-only and cannot be set on a contact item.</span></span> 
  
## <a name="createitem-request-example"></a><span data-ttu-id="1f16d-108">CreateItem-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="1f16d-108">CreateItem request example</span></span>

### <a name="description"></a><span data-ttu-id="1f16d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f16d-109">Description</span></span>

<span data-ttu-id="1f16d-110">Im folgenden Beispiel einer gültigen CreateItem-SOAP-Anforderung wird gezeigt, wie ein Kontakt im Standardordner Kontakte erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1f16d-110">The following example of a valid CreateItem SOAP request shows how to create a contact in the default Contacts folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="1f16d-111">Code</span><span class="sxs-lookup"><span data-stu-id="1f16d-111">Code</span></span>

```XML
<soap:Envelope
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" >
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

### <a name="request-elements"></a><span data-ttu-id="1f16d-112">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="1f16d-112">Request elements</span></span>

<span data-ttu-id="1f16d-113">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="1f16d-113">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="1f16d-114">CreateItem</span><span class="sxs-lookup"><span data-stu-id="1f16d-114">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="1f16d-115">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="1f16d-115">SavedItemFolderId</span></span>](saveditemfolderid.md)
    
- [<span data-ttu-id="1f16d-116">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="1f16d-116">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="1f16d-117">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="1f16d-117">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="1f16d-118">Contact</span><span class="sxs-lookup"><span data-stu-id="1f16d-118">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="1f16d-119">FileAs</span><span class="sxs-lookup"><span data-stu-id="1f16d-119">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="1f16d-120">GivenName</span><span class="sxs-lookup"><span data-stu-id="1f16d-120">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="1f16d-121">CompanyName</span><span class="sxs-lookup"><span data-stu-id="1f16d-121">CompanyName</span></span>](companyname.md)
    
- [<span data-ttu-id="1f16d-122">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="1f16d-122">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="1f16d-123">Eintrag (e-mailemail)</span><span class="sxs-lookup"><span data-stu-id="1f16d-123">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
- [<span data-ttu-id="1f16d-124">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="1f16d-124">PhysicalAddresses</span></span>](physicaladdresses.md)
    
- [<span data-ttu-id="1f16d-125">Eintrag (PhysicalAddress)</span><span class="sxs-lookup"><span data-stu-id="1f16d-125">Entry (PhysicalAddress)</span></span>](entry-physicaladdress.md)
    
- [<span data-ttu-id="1f16d-126">Straße</span><span class="sxs-lookup"><span data-stu-id="1f16d-126">Street</span></span>](street.md)
    
- [<span data-ttu-id="1f16d-127">City</span><span class="sxs-lookup"><span data-stu-id="1f16d-127">City</span></span>](city.md)
    
- [<span data-ttu-id="1f16d-128">State</span><span class="sxs-lookup"><span data-stu-id="1f16d-128">State</span></span>](state-ex15websvcsotherref.md)
    
- [<span data-ttu-id="1f16d-129">CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="1f16d-129">CountryOrRegion</span></span>](countryorregion.md)
    
- [<span data-ttu-id="1f16d-130">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="1f16d-130">PhoneNumbers</span></span>](phonenumbers.md)
    
- [<span data-ttu-id="1f16d-131">Eingabe (Faxnummer)</span><span class="sxs-lookup"><span data-stu-id="1f16d-131">Entry (PhoneNumber)</span></span>](entry-phonenumber.md)
    
- [<span data-ttu-id="1f16d-132">JobTitle</span><span class="sxs-lookup"><span data-stu-id="1f16d-132">JobTitle</span></span>](jobtitle.md)
    
- [<span data-ttu-id="1f16d-133">Nachname</span><span class="sxs-lookup"><span data-stu-id="1f16d-133">Surname</span></span>](surname.md)
    
## <a name="successful-createitem-request"></a><span data-ttu-id="1f16d-134">Erfolgreiche CreateItem-Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f16d-134">Successful CreateItem Request</span></span>

### <a name="description"></a><span data-ttu-id="1f16d-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f16d-135">Description</span></span>

<span data-ttu-id="1f16d-136">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die CreateItem-Anforderung, die einen Kontakt erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="1f16d-136">The following example shows a successful response to the CreateItem request that created a contact.</span></span> <span data-ttu-id="1f16d-137">In diesem Beispiel enthält die Antwort den Bezeichner des neu erstellten Elements.</span><span class="sxs-lookup"><span data-stu-id="1f16d-137">In this example, the response contains the identifier of the newly created item.</span></span>
  
### <a name="code"></a><span data-ttu-id="1f16d-138">Code</span><span class="sxs-lookup"><span data-stu-id="1f16d-138">Code</span></span>

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
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="1f16d-139">Comments</span><span class="sxs-lookup"><span data-stu-id="1f16d-139">Comments</span></span>

<span data-ttu-id="1f16d-140">Die Element-ID wurde verkürzt, um die Lesbarkeit beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="1f16d-140">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="1f16d-141">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="1f16d-141">Successful response elements</span></span>

<span data-ttu-id="1f16d-142">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="1f16d-142">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="1f16d-143">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="1f16d-143">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="1f16d-144">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="1f16d-144">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="1f16d-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1f16d-145">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="1f16d-146">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1f16d-146">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="1f16d-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1f16d-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="1f16d-148">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="1f16d-148">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="1f16d-149">Contact</span><span class="sxs-lookup"><span data-stu-id="1f16d-149">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="1f16d-150">ItemId</span><span class="sxs-lookup"><span data-stu-id="1f16d-150">ItemId</span></span>](itemid.md)
    
## <a name="invalid-createitem-request-example"></a><span data-ttu-id="1f16d-151">Ungültiges CreateItem-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="1f16d-151">Invalid CreateItem request example</span></span>

### <a name="description"></a><span data-ttu-id="1f16d-152">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f16d-152">Description</span></span>

<span data-ttu-id="1f16d-153">Das folgende Beispiel zeigt eine Anforderung, die gültige XML-, aber inkompatible Anweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="1f16d-153">The following example shows a request that contains valid XML but incompatible instructions.</span></span> <span data-ttu-id="1f16d-154">Ein Kontakt kann nicht in einem Suchordner erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1f16d-154">A contact cannot be created in a search folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="1f16d-155">Code</span><span class="sxs-lookup"><span data-stu-id="1f16d-155">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns='https://schemas.microsoft.com/exchange/services/2006/messages'>
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

## <a name="createitem-contact-error-response"></a><span data-ttu-id="1f16d-156">Fehlerantwort "CreateItem" (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="1f16d-156">CreateItem (Contact) error response</span></span>

### <a name="description"></a><span data-ttu-id="1f16d-157">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f16d-157">Description</span></span>

<span data-ttu-id="1f16d-158">Im folgenden Beispiel wird eine Fehlerantwort auf eine CreateItem-Anforderung (Kontakt) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1f16d-158">The following example shows an error response to a CreateItem (Contact) request.</span></span>
  
### <a name="code"></a><span data-ttu-id="1f16d-159">Code</span><span class="sxs-lookup"><span data-stu-id="1f16d-159">Code</span></span>

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
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="1f16d-160">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="1f16d-160">Error response elements</span></span>

<span data-ttu-id="1f16d-161">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="1f16d-161">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="1f16d-162">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="1f16d-162">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="1f16d-163">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="1f16d-163">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="1f16d-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1f16d-164">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="1f16d-165">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1f16d-165">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="1f16d-166">MessageText</span><span class="sxs-lookup"><span data-stu-id="1f16d-166">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="1f16d-167">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1f16d-167">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="1f16d-168">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="1f16d-168">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="1f16d-169">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="1f16d-169">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
## <a name="see-also"></a><span data-ttu-id="1f16d-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f16d-170">See also</span></span>



[<span data-ttu-id="1f16d-171">CreateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1f16d-171">CreateItem operation</span></span>](createitem-operation.md)

