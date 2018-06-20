---
title: GetFolder Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetFolder
api_type:
- schema
ms.assetid: 355bcf93-dc71-4493-b177-622afac5fdb9
description: GetFolder-Vorgang ruft Ordnern aus dem Exchange-Speicher ab.
ms.openlocfilehash: 1d2806e4febb6059b8a866d585bc70f49befbdef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758684"
---
# <a name="getfolder-operation"></a><span data-ttu-id="95228-103">GetFolder Operation</span><span class="sxs-lookup"><span data-stu-id="95228-103">GetFolder operation</span></span>

<span data-ttu-id="95228-104">**GetFolder** -Vorgang ruft Ordnern aus dem Exchange-Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="95228-104">The **GetFolder** operation gets folders from the Exchange store.</span></span> 
  
## <a name="getfolder-request-example"></a><span data-ttu-id="95228-105">GetFolder-anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="95228-105">GetFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="95228-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95228-106">Description</span></span>

<span data-ttu-id="95228-107">Im folgenden Beispiel wird eine Anforderung **GetFolder** veranschaulicht erhalten eine Ordner-ID, Name, die Anzahl der Elemente in dem Ordner, die Anzahl der untergeordneten Ordner und die Anzahl der ungelesenen Elemente im Ordner anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="95228-107">The following example of a **GetFolder** request shows how to obtain a folder identifier, display name, the count of items in that folder, the count of child folders, and the number of unread items in the folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="95228-108">Code</span><span class="sxs-lookup"><span data-stu-id="95228-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
   xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="request-elements"></a><span data-ttu-id="95228-109">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="95228-109">Request elements</span></span>

<span data-ttu-id="95228-110">Diese **GetFolder** -Anforderung enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="95228-110">This **GetFolder** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="95228-111">GetFolder</span><span class="sxs-lookup"><span data-stu-id="95228-111">GetFolder</span></span>](getfolder.md)
    
- [<span data-ttu-id="95228-112">FolderShape</span><span class="sxs-lookup"><span data-stu-id="95228-112">FolderShape</span></span>](foldershape.md)
    
- [<span data-ttu-id="95228-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="95228-113">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="95228-114">FolderIds</span><span class="sxs-lookup"><span data-stu-id="95228-114">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="95228-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="95228-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
<span data-ttu-id="95228-116">Finden Sie im Schema für zusätzliche Elemente, die Sie verwenden können, um eine Anforderung **GetFolder** bilden.</span><span class="sxs-lookup"><span data-stu-id="95228-116">See the schema for additional elements that you can use to form a **GetFolder** request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="95228-117">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="95228-117">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span> 
  
## <a name="getfolder-response-example"></a><span data-ttu-id="95228-118">GetFolder-Antwort-Beispiel</span><span class="sxs-lookup"><span data-stu-id="95228-118">GetFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="95228-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95228-119">Description</span></span>

<span data-ttu-id="95228-120">Das folgende (SOAP = Simple Object Access Protocol)-Body-Beispiel zeigt eine erfolgreiche Antwort auf die **GetFolder** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="95228-120">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **GetFolder** request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="95228-121">Die Ordner-ID und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="95228-121">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="95228-122">Code</span><span class="sxs-lookup"><span data-stu-id="95228-122">Code</span></span>

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="response-elements"></a><span data-ttu-id="95228-123">Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="95228-123">Response elements</span></span>

<span data-ttu-id="95228-124">Dieser Antwort **GetFolder** umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="95228-124">This **GetFolder** response includes the following elements:</span></span> 
  
- [<span data-ttu-id="95228-125">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="95228-125">GetFolderResponse</span></span>](getfolderresponse.md)
    
- [<span data-ttu-id="95228-126">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="95228-126">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="95228-127">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="95228-127">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
    
- [<span data-ttu-id="95228-128">Ordner</span><span class="sxs-lookup"><span data-stu-id="95228-128">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="95228-129">Folder</span><span class="sxs-lookup"><span data-stu-id="95228-129">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="95228-130">FolderId</span><span class="sxs-lookup"><span data-stu-id="95228-130">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="95228-131">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="95228-131">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="95228-132">TotalCount</span><span class="sxs-lookup"><span data-stu-id="95228-132">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="95228-133">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="95228-133">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="95228-134">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="95228-134">UnreadCount</span></span>](unreadcount.md)
    
## <a name="getfolder-error-response-example"></a><span data-ttu-id="95228-135">GetFolder-Fehler antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="95228-135">GetFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="95228-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95228-136">Description</span></span>

<span data-ttu-id="95228-137">Das folgende SOAP-Body-Beispiel zeigt eine Fehlerantwort an, die durch eine falsche [FolderId](folderid.md) in der Anforderung verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="95228-137">The following SOAP body example shows an error response that is caused by an incorrect [FolderId](folderid.md) in the request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="95228-138">Code</span><span class="sxs-lookup"><span data-stu-id="95228-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="response-elements"></a><span data-ttu-id="95228-139">Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="95228-139">Response elements</span></span>

<span data-ttu-id="95228-140">Diese **GetFolder** -Fehlerantwort umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="95228-140">This **GetFolder** error response includes the following elements:</span></span> 
  
- [<span data-ttu-id="95228-141">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="95228-141">GetFolderResponse</span></span>](getfolderresponse.md)
    
- [<span data-ttu-id="95228-142">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="95228-142">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="95228-143">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="95228-143">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
    
- [<span data-ttu-id="95228-144">MessageText</span><span class="sxs-lookup"><span data-stu-id="95228-144">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="95228-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="95228-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="95228-146">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="95228-146">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="95228-147">Ordner</span><span class="sxs-lookup"><span data-stu-id="95228-147">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="version-differences"></a><span data-ttu-id="95228-148">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="95228-148">Version differences</span></span>

<span data-ttu-id="95228-149">Für Applikationen werden, Exchange Online abzielen, Exchange Online als Teil von Office 365 oder eine lokale Version von Exchange beginnend mit Exchange 2013 Ordnerberechtigungen nicht zurückgegeben, wenn das Element [BaseShape](baseshape.md) **AllProperties** Wert hat in der Anforderung [GetFolder](getfolder-operation.md) -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="95228-149">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="95228-150">Um Ordnerberechtigungen abzurufen, fügen Sie dem [AdditionalProperties](additionalproperties.md) -Element in der Anforderung **GetFolder** die [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) -Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="95228-150">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="95228-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95228-151">See also</span></span>



- [<span data-ttu-id="95228-152">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="95228-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

