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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457123"
---
# <a name="createitem-operation-contact"></a><span data-ttu-id="89bdf-103">CreateItem-Vorgang (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="89bdf-103">CreateItem operation (contact)</span></span>

<span data-ttu-id="89bdf-104">Der CreateItem-Vorgang wird zum Erstellen von Kontakten im Exchange-Informationsspeicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="89bdf-104">The CreateItem operation is used to create contacts in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="89bdf-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89bdf-105">Remarks</span></span>

<span data-ttu-id="89bdf-106">Das Erstellen privater Verteilerlisten wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89bdf-106">The creation of private distribution lists is not supported.</span></span> <span data-ttu-id="89bdf-107">Alle Eigenschaften im Container [completename](completename.md) sind schreibgeschützt und können für ein Kontaktelement nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="89bdf-107">All properties within the [CompleteName](completename.md) container are read-only and cannot be set on a contact item.</span></span> 
  
## <a name="createitem-request-example"></a><span data-ttu-id="89bdf-108">CreateItem-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="89bdf-108">CreateItem request example</span></span>

### <a name="description"></a><span data-ttu-id="89bdf-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89bdf-109">Description</span></span>

<span data-ttu-id="89bdf-110">Im folgenden Beispiel einer gültigen CreateItem-SOAP-Anforderung wird gezeigt, wie ein Kontakt im Standardordner Kontakte erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="89bdf-110">The following example of a valid CreateItem SOAP request shows how to create a contact in the default Contacts folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="89bdf-111">Code</span><span class="sxs-lookup"><span data-stu-id="89bdf-111">Code</span></span>

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

### <a name="request-elements"></a><span data-ttu-id="89bdf-112">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="89bdf-112">Request elements</span></span>

<span data-ttu-id="89bdf-113">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="89bdf-113">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="89bdf-114">CreateItem</span><span class="sxs-lookup"><span data-stu-id="89bdf-114">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="89bdf-115">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="89bdf-115">SavedItemFolderId</span></span>](saveditemfolderid.md)
    
- [<span data-ttu-id="89bdf-116">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="89bdf-116">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="89bdf-117">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="89bdf-117">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="89bdf-118">Kontakt</span><span class="sxs-lookup"><span data-stu-id="89bdf-118">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="89bdf-119">FileAs</span><span class="sxs-lookup"><span data-stu-id="89bdf-119">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="89bdf-120">GivenName</span><span class="sxs-lookup"><span data-stu-id="89bdf-120">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="89bdf-121">CompanyName</span><span class="sxs-lookup"><span data-stu-id="89bdf-121">CompanyName</span></span>](companyname.md)
    
- [<span data-ttu-id="89bdf-122">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="89bdf-122">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="89bdf-123">Eintrag (e-mailemail)</span><span class="sxs-lookup"><span data-stu-id="89bdf-123">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
- [<span data-ttu-id="89bdf-124">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="89bdf-124">PhysicalAddresses</span></span>](physicaladdresses.md)
    
- [<span data-ttu-id="89bdf-125">Eintrag (PhysicalAddress)</span><span class="sxs-lookup"><span data-stu-id="89bdf-125">Entry (PhysicalAddress)</span></span>](entry-physicaladdress.md)
    
- [<span data-ttu-id="89bdf-126">Straße</span><span class="sxs-lookup"><span data-stu-id="89bdf-126">Street</span></span>](street.md)
    
- [<span data-ttu-id="89bdf-127">City</span><span class="sxs-lookup"><span data-stu-id="89bdf-127">City</span></span>](city.md)
    
- [<span data-ttu-id="89bdf-128">State</span><span class="sxs-lookup"><span data-stu-id="89bdf-128">State</span></span>](state-ex15websvcsotherref.md)
    
- [<span data-ttu-id="89bdf-129">CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="89bdf-129">CountryOrRegion</span></span>](countryorregion.md)
    
- [<span data-ttu-id="89bdf-130">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="89bdf-130">PhoneNumbers</span></span>](phonenumbers.md)
    
- [<span data-ttu-id="89bdf-131">Eingabe (Faxnummer)</span><span class="sxs-lookup"><span data-stu-id="89bdf-131">Entry (PhoneNumber)</span></span>](entry-phonenumber.md)
    
- [<span data-ttu-id="89bdf-132">JobTitle</span><span class="sxs-lookup"><span data-stu-id="89bdf-132">JobTitle</span></span>](jobtitle.md)
    
- [<span data-ttu-id="89bdf-133">Nachname</span><span class="sxs-lookup"><span data-stu-id="89bdf-133">Surname</span></span>](surname.md)
    
## <a name="successful-createitem-request"></a><span data-ttu-id="89bdf-134">Erfolgreiche CreateItem-Anforderung</span><span class="sxs-lookup"><span data-stu-id="89bdf-134">Successful CreateItem Request</span></span>

### <a name="description"></a><span data-ttu-id="89bdf-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89bdf-135">Description</span></span>

<span data-ttu-id="89bdf-136">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die CreateItem-Anforderung, die einen Kontakt erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="89bdf-136">The following example shows a successful response to the CreateItem request that created a contact.</span></span> <span data-ttu-id="89bdf-137">In diesem Beispiel enthält die Antwort den Bezeichner des neu erstellten Elements.</span><span class="sxs-lookup"><span data-stu-id="89bdf-137">In this example, the response contains the identifier of the newly created item.</span></span>
  
### <a name="code"></a><span data-ttu-id="89bdf-138">Code</span><span class="sxs-lookup"><span data-stu-id="89bdf-138">Code</span></span>

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

### <a name="comments"></a><span data-ttu-id="89bdf-139">Comments</span><span class="sxs-lookup"><span data-stu-id="89bdf-139">Comments</span></span>

<span data-ttu-id="89bdf-140">Die Element-ID wurde verkürzt, um die Lesbarkeit beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="89bdf-140">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="89bdf-141">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="89bdf-141">Successful response elements</span></span>

<span data-ttu-id="89bdf-142">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="89bdf-142">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="89bdf-143">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="89bdf-143">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="89bdf-144">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="89bdf-144">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="89bdf-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="89bdf-145">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="89bdf-146">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="89bdf-146">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="89bdf-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="89bdf-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="89bdf-148">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="89bdf-148">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="89bdf-149">Kontakt</span><span class="sxs-lookup"><span data-stu-id="89bdf-149">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="89bdf-150">ItemId</span><span class="sxs-lookup"><span data-stu-id="89bdf-150">ItemId</span></span>](itemid.md)
    
## <a name="invalid-createitem-request-example"></a><span data-ttu-id="89bdf-151">Ungültiges CreateItem-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="89bdf-151">Invalid CreateItem request example</span></span>

### <a name="description"></a><span data-ttu-id="89bdf-152">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89bdf-152">Description</span></span>

<span data-ttu-id="89bdf-153">Das folgende Beispiel zeigt eine Anforderung, die gültige XML-, aber inkompatible Anweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="89bdf-153">The following example shows a request that contains valid XML but incompatible instructions.</span></span> <span data-ttu-id="89bdf-154">Ein Kontakt kann nicht in einem Suchordner erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="89bdf-154">A contact cannot be created in a search folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="89bdf-155">Code</span><span class="sxs-lookup"><span data-stu-id="89bdf-155">Code</span></span>

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

## <a name="createitem-contact-error-response"></a><span data-ttu-id="89bdf-156">Fehlerantwort "CreateItem" (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="89bdf-156">CreateItem (Contact) error response</span></span>

### <a name="description"></a><span data-ttu-id="89bdf-157">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89bdf-157">Description</span></span>

<span data-ttu-id="89bdf-158">Im folgenden Beispiel wird eine Fehlerantwort auf eine CreateItem-Anforderung (Kontakt) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89bdf-158">The following example shows an error response to a CreateItem (Contact) request.</span></span>
  
### <a name="code"></a><span data-ttu-id="89bdf-159">Code</span><span class="sxs-lookup"><span data-stu-id="89bdf-159">Code</span></span>

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

### <a name="error-response-elements"></a><span data-ttu-id="89bdf-160">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="89bdf-160">Error response elements</span></span>

<span data-ttu-id="89bdf-161">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="89bdf-161">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="89bdf-162">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="89bdf-162">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="89bdf-163">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="89bdf-163">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="89bdf-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="89bdf-164">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="89bdf-165">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="89bdf-165">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="89bdf-166">MessageText</span><span class="sxs-lookup"><span data-stu-id="89bdf-166">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="89bdf-167">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="89bdf-167">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="89bdf-168">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="89bdf-168">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="89bdf-169">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="89bdf-169">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
## <a name="see-also"></a><span data-ttu-id="89bdf-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89bdf-170">See also</span></span>



[<span data-ttu-id="89bdf-171">CreateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="89bdf-171">CreateItem operation</span></span>](createitem-operation.md)

