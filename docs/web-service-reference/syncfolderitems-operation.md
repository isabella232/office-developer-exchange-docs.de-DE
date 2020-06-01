---
title: SyncFolderItems-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderItems
api_type:
- schema
ms.assetid: 7f0de089-8876-47ec-a871-df118ceae75d
description: Mit dem SyncFolderItems-Vorgang werden Elemente zwischen dem Exchange-Server und dem Client synchronisiert.
ms.openlocfilehash: 1a28d895eda11dd43f77ec2662a60a426cfc463c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468145"
---
# <a name="syncfolderitems-operation"></a><span data-ttu-id="626e7-103">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="626e7-103">SyncFolderItems operation</span></span>

<span data-ttu-id="626e7-104">Mit dem SyncFolderItems-Vorgang werden Elemente zwischen dem Exchange-Server und dem Client synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="626e7-104">The SyncFolderItems operation synchronizes items between the Exchange server and the client.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="626e7-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="626e7-105">Remarks</span></span>

<span data-ttu-id="626e7-106">Der SyncFolderItems-Vorgang gibt maximal 512 Änderungen zurück.</span><span class="sxs-lookup"><span data-stu-id="626e7-106">The SyncFolderItems operation will return a maximum of 512 changes.</span></span> <span data-ttu-id="626e7-107">Nachfolgende SyncFolderItems-Anforderungen müssen durchgeführt werden, um weitere Änderungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="626e7-107">Subsequent SyncFolderItems requests must be performed to get additional changes.</span></span> 
  
<span data-ttu-id="626e7-108">SyncFolderItems ähnelt dem FindItem-Vorgang insofern, als es keine Eigenschaften wie Body oder Attachments zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="626e7-108">SyncFolderItems is similar to the FindItem operation in that it cannot return properties like Body or Attachments.</span></span> <span data-ttu-id="626e7-109">Wenn der SyncFolderItems-Vorgang nicht die benötigten Eigenschaften zurückgibt, können Sie den [GetItem-Vorgang](getitem-operation.md) verwenden, um einen bestimmten Eigenschaftentyp für jedes Element abzurufen, das von SyncFolderItems zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="626e7-109">If the SyncFolderItems operation does not return the properties that you need, you can use the [GetItem operation](getitem-operation.md) to get a specific set of properties for each item that it returned by SyncFolderItems.</span></span> 
  
## <a name="syncfolderitems-request-example"></a><span data-ttu-id="626e7-110">SyncFolderItems-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="626e7-110">SyncFolderItems request example</span></span>

### <a name="description"></a><span data-ttu-id="626e7-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="626e7-111">Description</span></span>

<span data-ttu-id="626e7-112">Im folgenden Beispiel einer SyncFolderItems-Anforderung wird gezeigt, wie Elemente in einem Ordner synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="626e7-112">The following example of a SyncFolderItems request shows how to synchronize items in a folder.</span></span> <span data-ttu-id="626e7-113">In diesem Beispiel wird die Synchronisierung eines Ordnerelements gezeigt, bei der es sich nicht um die erste Synchronisierung handelt, die für den Ordner "Gesendete Elemente" aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="626e7-113">This example shows a folder item's synchronization that is not the first synchronization to have occurred for the Sent Items folder.</span></span> <span data-ttu-id="626e7-114">Das [von "SyncState](syncstate-ex15websvcsotherref.md) -Element ist nicht in der Anforderung für den ersten Versuch, einen Client mit dem Exchange-Server zu synchronisieren, enthalten.</span><span class="sxs-lookup"><span data-stu-id="626e7-114">The [SyncState](syncstate-ex15websvcsotherref.md) element is not included in the request for the first attempt to synchronize a client with the Exchange server.</span></span> <span data-ttu-id="626e7-115">Beim ersten Versuch, die Elemente in einer Ordnerhierarchie zu synchronisieren, werden alle Elemente im Postfach zurückgegeben, ausgenommen Elemente, die im [Ignore](ignore.md) -Element angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="626e7-115">The first attempt to synchronize the items in a folder hierarchy will return all the items in the mailbox, excluding items that are identified in the [Ignore](ignore.md) element.</span></span> <span data-ttu-id="626e7-116">Diese SyncFolderItems-Anforderung versucht, alle Änderungen an den Ordnerelementen seit der letzten Synchronisierung zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="626e7-116">This SyncFolderItems request will try to synchronize all changes to the folder items since the last synchronization.</span></span> <span data-ttu-id="626e7-117">Bei dieser Anforderung wird der Versuch, das eine Element zu synchronisieren, das im [Ignore](ignore.md) -Element identifiziert wird, ignoriert.</span><span class="sxs-lookup"><span data-stu-id="626e7-117">This request will ignore the attempt to synchronize the one item that is identified in the [Ignore](ignore.md) element.</span></span> 
  
### <a name="code"></a><span data-ttu-id="626e7-118">Code</span><span class="sxs-lookup"><span data-stu-id="626e7-118">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SyncFolderItems xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>Default</t:BaseShape>
      </ItemShape>
      <SyncFolderId>
        <t:DistinguishedFolderId Id="sentitems"/>
      </SyncFolderId>
      <SyncState>AEbJ94eMOAAA=</SyncState>
      <Ignore>
        <t:ItemId Id="AQApAHRAA==" ChangeKey="CQAAABY"/>
      </Ignore>
      <MaxChangesReturned>100</MaxChangesReturned>
    </SyncFolderItems>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="626e7-119">Comments</span><span class="sxs-lookup"><span data-stu-id="626e7-119">Comments</span></span>

<span data-ttu-id="626e7-120">Die Base64-codierten Daten des [von "SyncState](syncstate-ex15websvcsotherref.md) -Elements und das [ItemID](itemid.md) -Element- **ID** -Attribut wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="626e7-120">The [SyncState](syncstate-ex15websvcsotherref.md) element base64-encoded data and the [ItemId](itemid.md) element **Id** attribute have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="626e7-121">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="626e7-121">Request elements</span></span>

<span data-ttu-id="626e7-122">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="626e7-122">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="626e7-123">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="626e7-123">SyncFolderItems</span></span>](syncfolderitems.md)
    
- [<span data-ttu-id="626e7-124">ItemShape</span><span class="sxs-lookup"><span data-stu-id="626e7-124">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="626e7-125">BaseShape</span><span class="sxs-lookup"><span data-stu-id="626e7-125">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="626e7-126">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="626e7-126">SyncFolderId</span></span>](syncfolderid.md)
    
- [<span data-ttu-id="626e7-127">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="626e7-127">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="626e7-128">Von "SyncState</span><span class="sxs-lookup"><span data-stu-id="626e7-128">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="626e7-129">Ignore</span><span class="sxs-lookup"><span data-stu-id="626e7-129">Ignore</span></span>](ignore.md)
    
- [<span data-ttu-id="626e7-130">ItemId</span><span class="sxs-lookup"><span data-stu-id="626e7-130">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="626e7-131">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="626e7-131">MaxChangesReturned</span></span>](maxchangesreturned.md)
    
## <a name="successful-syncfolderitems-response"></a><span data-ttu-id="626e7-132">Erfolgreiche SyncFolderItems-Antwort</span><span class="sxs-lookup"><span data-stu-id="626e7-132">Successful SyncFolderItems Response</span></span>

### <a name="description"></a><span data-ttu-id="626e7-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="626e7-133">Description</span></span>

<span data-ttu-id="626e7-134">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die SyncFolderItems-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="626e7-134">The following example shows a successful response to the SyncFolderItems request.</span></span> <span data-ttu-id="626e7-135">In diesem Beispiel wird eine Besprechungsanfrage aus dem Ordner "Gesendete Elemente" synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="626e7-135">In this example, a meeting request is synchronized from the Sent Items folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="626e7-136">Code</span><span class="sxs-lookup"><span data-stu-id="626e7-136">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SyncFolderItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                             xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SyncFolderItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAAAA=</m:SyncState>
          <m:IncludesLastItemInRange>true</m:IncludesLastItemInRange>
          <m:Changes>
            <t:Create>
              <t:MeetingRequest>
                <t:ItemId Id="AQApAHRwA==" ChangeKey="CwAAABYA" />
                <t:Subject>Budget Q3</t:Subject>
                <t:Sensitivity>Normal</t:Sensitivity>
                <t:IsOutOfDate>false</t:IsOutOfDate>
                <t:HasBeenProcessed>true</t:HasBeenProcessed>
                <t:ResponseType>NoResponseReceived</t:ResponseType>
                <t:IntendedFreeBusyStatus>Busy</t:IntendedFreeBusyStatus>
                <t:Start>2006-08-02T17:30:00Z</t:Start>
                <t:End>2006-08-02T19:30:00Z</t:End>
                <t:Location>Conference Room 2</t:Location>
                <t:Organizer>
                  <t:Mailbox>
                    <t:Name>Dan Park</t:Name>
                    <t:EmailAddress>dpark@example.com</t:EmailAddress>
                    <t:RoutingType>SMTP</t:RoutingType>
                  </t:Mailbox>
                </t:Organizer>
              </t:MeetingRequest>
            </t:Create>
          </m:Changes>
        </m:SyncFolderItemsResponseMessage>
      </m:ResponseMessages>
    </SyncFolderItemsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="626e7-137">Comments</span><span class="sxs-lookup"><span data-stu-id="626e7-137">Comments</span></span>

<span data-ttu-id="626e7-138">Die Base64-codierten Daten des [von "SyncState](syncstate-ex15websvcsotherref.md) -Elements und das [ItemID](itemid.md) -Element- **ID** -Attribut wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="626e7-138">The [SyncState](syncstate-ex15websvcsotherref.md) element base64-encoded data and the [ItemId](itemid.md) element **Id** attribute have been shortened to preserve readability.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="626e7-139">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="626e7-139">Successful response elements</span></span>

<span data-ttu-id="626e7-140">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="626e7-140">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="626e7-141">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="626e7-141">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="626e7-142">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="626e7-142">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
    
- [<span data-ttu-id="626e7-143">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="626e7-143">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="626e7-144">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="626e7-144">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
    
- [<span data-ttu-id="626e7-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="626e7-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="626e7-146">Von "SyncState</span><span class="sxs-lookup"><span data-stu-id="626e7-146">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="626e7-147">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="626e7-147">IncludesLastItemInRange</span></span>](includeslastiteminrange.md)
    
- [<span data-ttu-id="626e7-148">Änderungen (Elemente)</span><span class="sxs-lookup"><span data-stu-id="626e7-148">Changes (Items)</span></span>](changes-items.md)
    
- [<span data-ttu-id="626e7-149">Erstellen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="626e7-149">Create (ItemSync)</span></span>](create-itemsync.md)
    
- [<span data-ttu-id="626e7-150">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="626e7-150">MeetingRequest</span></span>](meetingrequest.md)
    
- [<span data-ttu-id="626e7-151">ItemId</span><span class="sxs-lookup"><span data-stu-id="626e7-151">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="626e7-152">Betreff</span><span class="sxs-lookup"><span data-stu-id="626e7-152">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="626e7-153">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="626e7-153">Sensitivity</span></span>](sensitivity.md)
    
- [<span data-ttu-id="626e7-154">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="626e7-154">IsOutOfDate</span></span>](isoutofdate.md)
    
- [<span data-ttu-id="626e7-155">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="626e7-155">HasBeenProcessed</span></span>](hasbeenprocessed.md)
    
- [<span data-ttu-id="626e7-156">ResponseType</span><span class="sxs-lookup"><span data-stu-id="626e7-156">ResponseType</span></span>](responsetype.md)
    
- [<span data-ttu-id="626e7-157">IntendedFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="626e7-157">IntendedFreeBusyStatus</span></span>](intendedfreebusystatus.md)
    
- [<span data-ttu-id="626e7-158">Start</span><span class="sxs-lookup"><span data-stu-id="626e7-158">Start</span></span>](start.md)
    
- [<span data-ttu-id="626e7-159">End</span><span class="sxs-lookup"><span data-stu-id="626e7-159">End </span></span>](end-ex15websvcsotherref.md)
    
- [<span data-ttu-id="626e7-160">Standort</span><span class="sxs-lookup"><span data-stu-id="626e7-160">Location</span></span>](location.md)
    
- [<span data-ttu-id="626e7-161">Organisator</span><span class="sxs-lookup"><span data-stu-id="626e7-161">Organizer</span></span>](organizer.md)
    
- [<span data-ttu-id="626e7-162">Postfach</span><span class="sxs-lookup"><span data-stu-id="626e7-162">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="626e7-163">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="626e7-163">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="626e7-164">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="626e7-164">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="626e7-165">Routingtype (e-mailemailtype)</span><span class="sxs-lookup"><span data-stu-id="626e7-165">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
## <a name="syncfolderitems-error-response"></a><span data-ttu-id="626e7-166">SyncFolderItems-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="626e7-166">SyncFolderItems error response</span></span>

### <a name="description"></a><span data-ttu-id="626e7-167">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="626e7-167">Description</span></span>

<span data-ttu-id="626e7-168">Das folgende Beispiel zeigt eine Fehlerantwort auf eine SyncFolderItems-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="626e7-168">The following example shows an error response to a SyncFolderItems request.</span></span> <span data-ttu-id="626e7-169">Dieser Fehler wurde durch ein ungültiges von "SyncState verursacht.</span><span class="sxs-lookup"><span data-stu-id="626e7-169">This error was caused by an invalid SyncState.</span></span>
  
### <a name="code"></a><span data-ttu-id="626e7-170">Code</span><span class="sxs-lookup"><span data-stu-id="626e7-170">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SyncFolderItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                             xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SyncFolderItemsResponseMessage ResponseClass="Error">
          <m:MessageText>Synchronization state data is corrupt or otherwise invalid.</m:MessageText>
          <m:ResponseCode>ErrorInvalidSyncStateData</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:SyncState />
          <m:IncludesLastItemInRange>true</m:IncludesLastItemInRange>
        </m:SyncFolderItemsResponseMessage>
      </m:ResponseMessages>
    </SyncFolderItemsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="626e7-171">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="626e7-171">Error response elements</span></span>

<span data-ttu-id="626e7-172">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="626e7-172">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="626e7-173">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="626e7-173">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="626e7-174">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="626e7-174">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
    
- [<span data-ttu-id="626e7-175">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="626e7-175">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="626e7-176">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="626e7-176">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
    
- [<span data-ttu-id="626e7-177">MessageText</span><span class="sxs-lookup"><span data-stu-id="626e7-177">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="626e7-178">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="626e7-178">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="626e7-179">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="626e7-179">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="626e7-180">Von "SyncState</span><span class="sxs-lookup"><span data-stu-id="626e7-180">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="626e7-181">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="626e7-181">IncludesLastItemInRange</span></span>](includeslastiteminrange.md)
    
## <a name="see-also"></a><span data-ttu-id="626e7-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="626e7-182">See also</span></span>



- [<span data-ttu-id="626e7-183">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="626e7-183">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

