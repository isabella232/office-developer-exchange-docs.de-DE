---
title: SyncFolderHierarchy-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchy
api_type:
- schema
ms.assetid: b31916b1-bc6c-4451-a475-b7c5417f752d
description: Mit dem SyncFolderHierarchy-Vorgang werden die Ordner zwischen dem Computer mit Microsoft Exchange Server 2010 und dem Client synchronisiert.
ms.openlocfilehash: 1c7ad2413064161ba54e8a7a30bfcd6f23f218bd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456430"
---
# <a name="syncfolderhierarchy-operation"></a><span data-ttu-id="815ca-103">SyncFolderHierarchy-Vorgang</span><span class="sxs-lookup"><span data-stu-id="815ca-103">SyncFolderHierarchy operation</span></span>

<span data-ttu-id="815ca-104">Mit dem SyncFolderHierarchy-Vorgang werden die Ordner zwischen dem Computer mit Microsoft Exchange Server 2010 und dem Client synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="815ca-104">The SyncFolderHierarchy operation synchronizes folders between the computer that is running Microsoft Exchange Server 2010 and the client.</span></span>
  
> [!NOTE]
> <span data-ttu-id="815ca-105">Der SyncFolderHierarchy-Vorgang gibt keine Ordner zurück, wenn sich die Eigenschaften [UnreadCount](unreadcount.md) oder [Total count](totalcount.md) geändert haben.</span><span class="sxs-lookup"><span data-stu-id="815ca-105">The SyncFolderHierarchy operation does not return folders when the [UnreadCount](unreadcount.md) or [TotalCount](totalcount.md) properties have changed.</span></span> 
  
## <a name="syncfolderhierarchy-request-example"></a><span data-ttu-id="815ca-106">SyncFolderHierarchy-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="815ca-106">SyncFolderHierarchy request example</span></span>

### <a name="description"></a><span data-ttu-id="815ca-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="815ca-107">Description</span></span>

<span data-ttu-id="815ca-108">Im folgenden Beispiel einer SyncFolderHierarchy-Anforderung wird gezeigt, wie eine Clientordner Hierarchie mit dem Exchange-Server synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="815ca-108">The following example of a SyncFolderHierarchy request shows how to synchronize a client folder hierarchy with the Exchange server.</span></span> <span data-ttu-id="815ca-109">Dieses Beispiel zeigt eine Ordnerhierarchie, die bereits mindestens einmal synchronisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="815ca-109">This example shows a folder hierarchy that has already been synchronized at least one time.</span></span> <span data-ttu-id="815ca-110">Das [von "SyncState](syncstate-ex15websvcsotherref.md) -Element ist nicht in der Anforderung für den ersten Versuch, einen Client mit dem Exchange-Server zu synchronisieren, enthalten.</span><span class="sxs-lookup"><span data-stu-id="815ca-110">The [SyncState](syncstate-ex15websvcsotherref.md) element is not included in the request for the first attempt to synchronize a client with the Exchange server.</span></span> <span data-ttu-id="815ca-111">Die erste Anforderung gibt alle Ordner im Postfach zurück.</span><span class="sxs-lookup"><span data-stu-id="815ca-111">The first request will return all the folders in the mailbox.</span></span> <span data-ttu-id="815ca-112">Das [von "SyncState](syncstate-ex15websvcsotherref.md) -Element wird in der [SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="815ca-112">The [SyncState](syncstate-ex15websvcsotherref.md) element will be returned in the [SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md).</span></span> <span data-ttu-id="815ca-113">Dieses Element wird verwendet, um den Status für nachfolgende SyncFolderHierarchy-Anforderungen zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="815ca-113">This element is used to synchronize the state for subsequent SyncFolderHierarchy requests.</span></span>
  
### <a name="code"></a><span data-ttu-id="815ca-114">Code</span><span class="sxs-lookup"><span data-stu-id="815ca-114">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SyncFolderHierarchy  xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </FolderShape>
      <SyncState>H4sIA=</SyncState>
    </SyncFolderHierarchy>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="815ca-115">Comments</span><span class="sxs-lookup"><span data-stu-id="815ca-115">Comments</span></span>

<span data-ttu-id="815ca-116">Die Base64-codierten Daten des [von "SyncState](syncstate-ex15websvcsotherref.md) -Elements wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="815ca-116">The [SyncState](syncstate-ex15websvcsotherref.md) element base64-encoded data has been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="815ca-117">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="815ca-117">Request elements</span></span>

<span data-ttu-id="815ca-118">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="815ca-118">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="815ca-119">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="815ca-119">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md)
    
- [<span data-ttu-id="815ca-120">FolderShape</span><span class="sxs-lookup"><span data-stu-id="815ca-120">FolderShape</span></span>](foldershape.md)
    
- [<span data-ttu-id="815ca-121">BaseShape</span><span class="sxs-lookup"><span data-stu-id="815ca-121">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="815ca-122">Von "SyncState</span><span class="sxs-lookup"><span data-stu-id="815ca-122">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
> [!NOTE]
> <span data-ttu-id="815ca-123">Das Schema, in dem diese Elemente beschrieben werden, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="815ca-123">The schema that describes these elements is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="successful-syncfolderhierarchy-response"></a><span data-ttu-id="815ca-124">Erfolgreiche SyncFolderHierarchy-Antwort</span><span class="sxs-lookup"><span data-stu-id="815ca-124">Successful SyncFolderHierarchy Response</span></span>

### <a name="description"></a><span data-ttu-id="815ca-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="815ca-125">Description</span></span>

<span data-ttu-id="815ca-126">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die SyncFolderHierarchy-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="815ca-126">The following example shows a successful response to the SyncFolderHierarchy request.</span></span> <span data-ttu-id="815ca-127">In diesem Beispiel wurde ein neuer Ordner synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="815ca-127">In this example, a new folder has been synchronized.</span></span>
  
### <a name="code"></a><span data-ttu-id="815ca-128">Code</span><span class="sxs-lookup"><span data-stu-id="815ca-128">Code</span></span>

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
    <SyncFolderHierarchyResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAA==</m:SyncState>
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
          <m:Changes>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AQApAHR=" ChangeKey="AQAAABY" />
                <t:ParentFolderId Id="AQApA=" ChangeKey="AQAAAA==" />
                <t:FolderClass>IPF.Note</t:FolderClass>
                <t:DisplayName>NewFolder</t:DisplayName>
                <t:TotalCount>0</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Create>
          </m:Changes>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </SyncFolderHierarchyResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="815ca-129">Comments</span><span class="sxs-lookup"><span data-stu-id="815ca-129">Comments</span></span>

<span data-ttu-id="815ca-130">Die Base64-codierten Daten des [von "SyncState](syncstate-ex15websvcsotherref.md) -Elements und die Ordner-ID-Daten wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="815ca-130">The [SyncState](syncstate-ex15websvcsotherref.md) element base64-encoded data and the folder identifier data have been shortened to preserve readability.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="815ca-131">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="815ca-131">Successful response elements</span></span>

<span data-ttu-id="815ca-132">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="815ca-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="815ca-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="815ca-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="815ca-134">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="815ca-134">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
    
- [<span data-ttu-id="815ca-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="815ca-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="815ca-136">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="815ca-136">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
    
- [<span data-ttu-id="815ca-137">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="815ca-137">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="815ca-138">Von "SyncState</span><span class="sxs-lookup"><span data-stu-id="815ca-138">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="815ca-139">IncludesLastFolderInRange</span><span class="sxs-lookup"><span data-stu-id="815ca-139">IncludesLastFolderInRange</span></span>](includeslastfolderinrange.md)
    
- [<span data-ttu-id="815ca-140">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="815ca-140">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
    
- [<span data-ttu-id="815ca-141">Erstellen (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="815ca-141">Create (FolderSync)</span></span>](create-foldersync.md)
    
- [<span data-ttu-id="815ca-142">Folder</span><span class="sxs-lookup"><span data-stu-id="815ca-142">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="815ca-143">FolderId</span><span class="sxs-lookup"><span data-stu-id="815ca-143">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="815ca-144">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="815ca-144">ParentFolderId</span></span>](parentfolderid.md)
    
- [<span data-ttu-id="815ca-145">FolderClass</span><span class="sxs-lookup"><span data-stu-id="815ca-145">FolderClass</span></span>](folderclass.md)
    
- [<span data-ttu-id="815ca-146">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="815ca-146">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="815ca-147">Total count</span><span class="sxs-lookup"><span data-stu-id="815ca-147">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="815ca-148">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="815ca-148">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="815ca-149">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="815ca-149">UnreadCount</span></span>](unreadcount.md)
    
## <a name="syncfolderhierarchy-error-response"></a><span data-ttu-id="815ca-150">SyncFolderHierarchy-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="815ca-150">SyncFolderHierarchy error response</span></span>

### <a name="description"></a><span data-ttu-id="815ca-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="815ca-151">Description</span></span>

<span data-ttu-id="815ca-152">Das folgende Beispiel zeigt eine Fehlerantwort auf eine SyncFolderHierarchy-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="815ca-152">The following example shows an error response to a SyncFolderHierarchy request.</span></span> <span data-ttu-id="815ca-153">Dieser Fehler wurde durch ein ungültiges von "SyncState verursacht.</span><span class="sxs-lookup"><span data-stu-id="815ca-153">This error was caused by an invalid SyncState.</span></span>
  
### <a name="code"></a><span data-ttu-id="815ca-154">Code</span><span class="sxs-lookup"><span data-stu-id="815ca-154">Code</span></span>

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
    <SyncFolderHierarchyResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Error">
          <m:MessageText>Synchronization state data is corrupted or otherwise invalid.</m:MessageText>
          <m:ResponseCode>ErrorInvalidSyncStateData</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:SyncState />
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </SyncFolderHierarchyResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="815ca-155">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="815ca-155">Error response elements</span></span>

<span data-ttu-id="815ca-156">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="815ca-156">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="815ca-157">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="815ca-157">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="815ca-158">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="815ca-158">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
    
- [<span data-ttu-id="815ca-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="815ca-159">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="815ca-160">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="815ca-160">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
    
- [<span data-ttu-id="815ca-161">MessageText</span><span class="sxs-lookup"><span data-stu-id="815ca-161">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="815ca-162">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="815ca-162">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="815ca-163">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="815ca-163">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="815ca-164">Von "SyncState</span><span class="sxs-lookup"><span data-stu-id="815ca-164">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="815ca-165">IncludesLastFolderInRange</span><span class="sxs-lookup"><span data-stu-id="815ca-165">IncludesLastFolderInRange</span></span>](includeslastfolderinrange.md)
    
## <a name="see-also"></a><span data-ttu-id="815ca-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="815ca-166">See also</span></span>



- [<span data-ttu-id="815ca-167">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="815ca-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

