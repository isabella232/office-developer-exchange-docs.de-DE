---
title: GetFolder-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- GetFolder
api_type:
- schema
ms.assetid: 355bcf93-dc71-4493-b177-622afac5fdb9
description: Der GetFolder-Vorgang ruft Ordner aus dem Exchange-Informationsspeicher ab.
localization_priority: Priority
ms.openlocfilehash: 9d511f309b9210fd9b5a49ff6c60bc7982992973
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459181"
---
# <a name="getfolder-operation"></a><span data-ttu-id="2f855-103">GetFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2f855-103">GetFolder operation</span></span>

<span data-ttu-id="2f855-104">Der **GetFolder** -Vorgang ruft Ordner aus dem Exchange-Informationsspeicher ab.</span><span class="sxs-lookup"><span data-stu-id="2f855-104">The **GetFolder** operation gets folders from the Exchange store.</span></span> 
  
## <a name="getfolder-request-example"></a><span data-ttu-id="2f855-105">GetFolder-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="2f855-105">GetFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="2f855-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f855-106">Description</span></span>

<span data-ttu-id="2f855-107">Im folgenden Beispiel einer **GetFolder** -Anforderung wird gezeigt, wie eine Ordner-ID, ein Anzeigename, die Anzahl der Elemente in diesem Ordner, die Anzahl der untergeordneten Ordner und die Anzahl der ungelesenen Elemente im Ordner abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2f855-107">The following example of a **GetFolder** request shows how to obtain a folder identifier, display name, the count of items in that folder, the count of child folders, and the number of unread items in the folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2f855-108">Code</span><span class="sxs-lookup"><span data-stu-id="2f855-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
   xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <FolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </FolderIds>
    </GetFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="2f855-109">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="2f855-109">Request elements</span></span>

<span data-ttu-id="2f855-110">Diese **GetFolder** -Anforderung umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="2f855-110">This **GetFolder** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="2f855-111">GetFolder</span><span class="sxs-lookup"><span data-stu-id="2f855-111">GetFolder</span></span>](getfolder.md)
    
- [<span data-ttu-id="2f855-112">FolderShape</span><span class="sxs-lookup"><span data-stu-id="2f855-112">FolderShape</span></span>](foldershape.md)
    
- [<span data-ttu-id="2f855-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="2f855-113">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="2f855-114">FolderIds</span><span class="sxs-lookup"><span data-stu-id="2f855-114">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="2f855-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="2f855-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
<span data-ttu-id="2f855-116">Weitere Elemente, die Sie zum Erstellen einer **GetFolder** -Anforderung verwenden können, finden Sie im Schema.</span><span class="sxs-lookup"><span data-stu-id="2f855-116">See the schema for additional elements that you can use to form a **GetFolder** request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2f855-117">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2f855-117">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span> 
  
## <a name="getfolder-response-example"></a><span data-ttu-id="2f855-118">GetFolder-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="2f855-118">GetFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="2f855-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f855-119">Description</span></span>

<span data-ttu-id="2f855-120">Das folgende Simple Object Access Protocol (SOAP) Body-Beispiel zeigt eine erfolgreiche Antwort auf die **GetFolder** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2f855-120">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **GetFolder** request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2f855-121">Die Ordner-ID und der Change-Schlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2f855-121">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2f855-122">Code</span><span class="sxs-lookup"><span data-stu-id="2f855-122">Code</span></span>

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AQApA=" ChangeKey="AQAAAB" />
              <t:DisplayName>Inbox</t:DisplayName>
              <t:TotalCount>2</t:TotalCount>
              <t:ChildFolderCount>0</t:ChildFolderCount>
              <t:UnreadCount>2</t:UnreadCount>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </GetFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="2f855-123">Response-Elemente</span><span class="sxs-lookup"><span data-stu-id="2f855-123">Response elements</span></span>

<span data-ttu-id="2f855-124">Diese **GetFolder** -Antwort umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="2f855-124">This **GetFolder** response includes the following elements:</span></span> 
  
- [<span data-ttu-id="2f855-125">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="2f855-125">GetFolderResponse</span></span>](getfolderresponse.md)
    
- [<span data-ttu-id="2f855-126">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2f855-126">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="2f855-127">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2f855-127">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
    
- [<span data-ttu-id="2f855-128">Ordner</span><span class="sxs-lookup"><span data-stu-id="2f855-128">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="2f855-129">Ordner</span><span class="sxs-lookup"><span data-stu-id="2f855-129">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="2f855-130">FolderId</span><span class="sxs-lookup"><span data-stu-id="2f855-130">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="2f855-131">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="2f855-131">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="2f855-132">Total count</span><span class="sxs-lookup"><span data-stu-id="2f855-132">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="2f855-133">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="2f855-133">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="2f855-134">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="2f855-134">UnreadCount</span></span>](unreadcount.md)
    
## <a name="getfolder-error-response-example"></a><span data-ttu-id="2f855-135">GetFolder-Fehlerantwort (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="2f855-135">GetFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="2f855-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f855-136">Description</span></span>

<span data-ttu-id="2f855-137">Das folgende SOAP Body-Beispiel zeigt eine Fehlerantwort, die durch eine falsche [Folder](folderid.md) -Wert in der Anforderung verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="2f855-137">The following SOAP body example shows an error response that is caused by an incorrect [FolderId](folderid.md) in the request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2f855-138">Code</span><span class="sxs-lookup"><span data-stu-id="2f855-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </GetFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="2f855-139">Response-Elemente</span><span class="sxs-lookup"><span data-stu-id="2f855-139">Response elements</span></span>

<span data-ttu-id="2f855-140">Diese **GetFolder** -Fehlerantwort umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="2f855-140">This **GetFolder** error response includes the following elements:</span></span> 
  
- [<span data-ttu-id="2f855-141">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="2f855-141">GetFolderResponse</span></span>](getfolderresponse.md)
    
- [<span data-ttu-id="2f855-142">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2f855-142">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="2f855-143">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2f855-143">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
    
- [<span data-ttu-id="2f855-144">MessageText</span><span class="sxs-lookup"><span data-stu-id="2f855-144">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="2f855-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2f855-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2f855-146">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2f855-146">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="2f855-147">Ordner</span><span class="sxs-lookup"><span data-stu-id="2f855-147">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="version-differences"></a><span data-ttu-id="2f855-148">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="2f855-148">Version differences</span></span>

<span data-ttu-id="2f855-149">Für Anwendungen, die auf Exchange Online Zielen, Exchange Online im Rahmen von Office 365 oder einer lokalen Exchange-Version, die mit Exchange 2013 beginnt, werden Ordnerberechtigungen nicht zurückgegeben, wenn das [BaseShape](baseshape.md) -Element den Wert **allproperties** in der [GetFolder](getfolder-operation.md) -Vorgangsanforderung aufweist.</span><span class="sxs-lookup"><span data-stu-id="2f855-149">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="2f855-150">Zum Abrufen von Ordnerberechtigungen fügen Sie dem [AdditionalProperties](additionalproperties.md) -Element in der **GetFolder** -Anforderung das [PermissionSet-Element (permissionsettype)](permissionset-permissionsettype.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="2f855-150">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2f855-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f855-151">See also</span></span>



- [<span data-ttu-id="2f855-152">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2f855-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

