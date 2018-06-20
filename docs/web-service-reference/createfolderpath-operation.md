---
title: CreateFolderPath-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5a10aa5e-3f25-4ec3-a0b9-284c30918a1f
description: Hier finden Sie Informationen über die CreateFolderPath EWS Vorgang.
ms.openlocfilehash: 22561e5086c144e25d7e04b68ec6674b87c4718d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757761"
---
# <a name="createfolderpath-operation"></a><span data-ttu-id="2b27c-103">CreateFolderPath-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2b27c-103">CreateFolderPath operation</span></span>

<span data-ttu-id="2b27c-104">Hier finden Sie Informationen zum **CreateFolderPath** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="2b27c-104">Find information about the **CreateFolderPath** EWS operation.</span></span> 
  
<span data-ttu-id="2b27c-105">Der Vorgang **CreateFolderPath** erstellt eine Ordnerhierarchie.</span><span class="sxs-lookup"><span data-stu-id="2b27c-105">The **CreateFolderPath** operation creates a folder hierarchy.</span></span> 
  
<span data-ttu-id="2b27c-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2b27c-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-createfolderpath-operation"></a><span data-ttu-id="2b27c-107">Verwenden des CreateFolderPath-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="2b27c-107">Using the CreateFolderPath operation</span></span>

<span data-ttu-id="2b27c-108">Die **CreateFolderPath** Vorgang Anforderung akzeptiert ein Array von Ordnern und einen Bezeichner der übergeordneten Ordner und erstellt eine Ordnerhierarchie basierend auf der Reihenfolge der Ordner im Array.</span><span class="sxs-lookup"><span data-stu-id="2b27c-108">The **CreateFolderPath** operation request takes an array of folders and a parent folder identifier and creates a folder hierarchy based on the order of the folders in the array.</span></span> 
  
### <a name="createfolderpath-operation-soap-headers"></a><span data-ttu-id="2b27c-109">CreateFolderPath Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="2b27c-109">CreateFolderPath operation SOAP headers</span></span>

<span data-ttu-id="2b27c-110">Der Vorgang **CreateFolderPath** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="2b27c-110">The **CreateFolderPath** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="2b27c-111">**Headername**</span><span class="sxs-lookup"><span data-stu-id="2b27c-111">**Header name**</span></span>|<span data-ttu-id="2b27c-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="2b27c-112">**Element**</span></span>|<span data-ttu-id="2b27c-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2b27c-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2b27c-114">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="2b27c-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="2b27c-115">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="2b27c-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="2b27c-116">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="2b27c-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="2b27c-117">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2b27c-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="2b27c-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="2b27c-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="2b27c-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="2b27c-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="2b27c-120">Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b27c-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="2b27c-121">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2b27c-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="2b27c-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="2b27c-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="2b27c-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="2b27c-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="2b27c-124">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="2b27c-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="2b27c-125">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2b27c-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="2b27c-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="2b27c-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="2b27c-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2b27c-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="2b27c-128">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="2b27c-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="2b27c-129">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="2b27c-129">This header is applicable to a response.</span></span>  <br/> |
|<span data-ttu-id="2b27c-130">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="2b27c-130">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="2b27c-131">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="2b27c-131">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="2b27c-132">Gibt den Bereich Zeitzone für **DateTime** -Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2b27c-132">Identifies the time zone scope for **DateTime** properties.</span></span> <span data-ttu-id="2b27c-133">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2b27c-133">This header is applicable to a request.</span></span>  <br/> |
   
## <a name="createfolderpath-operation-request-example-create-a-folder-hierarchy"></a><span data-ttu-id="2b27c-134">CreateFolderPath Vorgang-anforderungsbeispiel: erstellen eine Ordnerhierarchie</span><span class="sxs-lookup"><span data-stu-id="2b27c-134">CreateFolderPath operation request example: Create a folder hierarchy</span></span>

<span data-ttu-id="2b27c-135">Im folgenden Beispiel wird eine **CreateFolderPath** Vorgang Anforderung zeigt, wie eine Ordnerhierarchie erstellen, die drei Ordner ist in den Standardordner Posteingang.</span><span class="sxs-lookup"><span data-stu-id="2b27c-135">The following example of a **CreateFolderPath** operation request shows how to create a folder hierarchy that is three folders deep in the default Inbox folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2b27c-136">Bezeichner für alle Elemente aus, und Ändern von Schlüsseln in diesem Artikel wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2b27c-136">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
      <t:TimeZoneContext>
         <t:TimeZoneDefinition Id="GMT Standard Time"/>
      </t:TimeZoneContext>
   </soap:Header>
   <soap:Body >
      <m:CreateFolderPath>
         <m:ParentFolderId>
            <t:DistinguishedFolderId Id="inbox"/>
         </m:ParentFolderId>
         <m:RelativeFolderPath>
            <t:Folder>
               <t:DisplayName>MyFirstLevelFolder</t:DisplayName>
            </t:Folder>
            <t:Folder>
               <t:DisplayName>MySecondLevelFolder</t:DisplayName>
            </t:Folder>
            <t:Folder>
               <t:DisplayName>MyThirdLevelFolder</t:DisplayName>
            </t:Folder>
         </m:RelativeFolderPath>
      </m:CreateFolderPath>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="2b27c-137">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="2b27c-137">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="2b27c-138">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="2b27c-138">CreateFolderPath</span></span>](createfolderpath.md)
    
- [<span data-ttu-id="2b27c-139">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="2b27c-139">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)
    
- [<span data-ttu-id="2b27c-140">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="2b27c-140">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="2b27c-141">RelativeFolderPath</span><span class="sxs-lookup"><span data-stu-id="2b27c-141">RelativeFolderPath</span></span>](relativefolderpath.md)
    
- [<span data-ttu-id="2b27c-142">Folder</span><span class="sxs-lookup"><span data-stu-id="2b27c-142">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="2b27c-143">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="2b27c-143">DisplayName (string)</span></span>](displayname-string.md)
    
## <a name="successful-createfolderpath-operation-response"></a><span data-ttu-id="2b27c-144">Erfolgreiche CreateFolderPath Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="2b27c-144">Successful CreateFolderPath operation response</span></span>

<span data-ttu-id="2b27c-145">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **CreateFolderPath** Vorgang Anforderung zum Erstellen eines Ordners drei Hierarchieordner in den Standardordner Posteingang.</span><span class="sxs-lookup"><span data-stu-id="2b27c-145">The following example shows a successful response to a **CreateFolderPath** operation request to create a folder hierarchy three folders deep in the default Inbox folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:CreateFolderPathResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:CreateFolderPathResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Folders>
                  <t:Folder>
                     <t:FolderId Id="AAMkADEzOTExYisXAAA=" ChangeKey="AQAAABYAABq6Wxb"/>
                     <t:DisplayName>MyFirstLevelFolder</t:DisplayName>
                     <t:TotalCount>0</t:TotalCount>
                     <t:ChildFolderCount>0</t:ChildFolderCount>
                     <t:UnreadCount>0</t:UnreadCount>
                  </t:Folder>
               </m:Folders>
            </m:CreateFolderPathResponseMessage>
            <m:CreateFolderPathResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Folders>
                  <t:Folder>
                     <t:FolderId Id="AAMkADEzOTExm4QrAABqxisYAAA=" ChangeKey="AQAAABYAAAm4QrAABq6Wxg"/>
                     <t:DisplayName>MySecondLevelFolder</t:DisplayName>
                     <t:TotalCount>0</t:TotalCount>
                     <t:ChildFolderCount>0</t:ChildFolderCount>
                     <t:UnreadCount>0</t:UnreadCount>
                  </t:Folder>
               </m:Folders>
            </m:CreateFolderPathResponseMessage>
            <m:CreateFolderPathResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Folders>
                  <t:Folder>
                     <t:FolderId Id="AAMkADEzOTAABqxisZAAA=" ChangeKey="AQAAABYAA6Wxl"/>
                     <t:DisplayName>MyThirdLevelFolder</t:DisplayName>
                     <t:TotalCount>0</t:TotalCount>
                     <t:ChildFolderCount>0</t:ChildFolderCount>
                     <t:UnreadCount>0</t:UnreadCount>
                  </t:Folder>
               </m:Folders>
            </m:CreateFolderPathResponseMessage>
         </m:ResponseMessages>
      </m:CreateFolderPathResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="2b27c-146">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="2b27c-146">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="2b27c-147">CreateFolderPathResponse</span><span class="sxs-lookup"><span data-stu-id="2b27c-147">CreateFolderPathResponse</span></span>](createfolderpathresponse.md)
    
- [<span data-ttu-id="2b27c-148">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2b27c-148">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="2b27c-149">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2b27c-149">CreateFolderPathResponseMessage</span></span>](createfolderpathresponsemessage.md)
    
- [<span data-ttu-id="2b27c-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2b27c-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2b27c-151">Ordner</span><span class="sxs-lookup"><span data-stu-id="2b27c-151">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="2b27c-152">Folder</span><span class="sxs-lookup"><span data-stu-id="2b27c-152">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="2b27c-153">FolderId</span><span class="sxs-lookup"><span data-stu-id="2b27c-153">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="2b27c-154">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="2b27c-154">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="2b27c-155">TotalCount</span><span class="sxs-lookup"><span data-stu-id="2b27c-155">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="2b27c-156">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="2b27c-156">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="2b27c-157">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="2b27c-157">UnreadCount</span></span>](unreadcount.md)
    
## <a name="createfolderpath-operation-error-response"></a><span data-ttu-id="2b27c-158">CreateFolderPath Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="2b27c-158">CreateFolderPath operation error response</span></span>

<span data-ttu-id="2b27c-159">Das folgende Beispiel zeigt eine Fehlerantwort an eine **CreateFolderPath** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2b27c-159">The following example shows an error response to a **CreateFolderPath** operation request.</span></span> <span data-ttu-id="2b27c-160">Dies ist eine Antwort auf eine Anforderung zum Erstellen von zwei Ordnern, von denen die erste keine Display Name-Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2b27c-160">This is a response to a request to create two folders, the first of which does not have a display name property set.</span></span> <span data-ttu-id="2b27c-161">Der erste Ordner in der Hierarchie kann nicht erstellt werden, ohne eine Display Name-Eigenschaft, und der zweite Ordner kann nicht erstellt werden, da nicht des übergeordneten Ordners in der Hierarchie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2b27c-161">The first folder in the hierarchy cannot be created without a display name property, and the second folder cannot be created because the parent folder in the hierarchy was not created.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:CreateFolderPathResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:CreateFolderPathResponseMessage ResponseClass="Error">
               <m:MessageText>The folder save operation failed due to invalid property values.</m:MessageText>
               <m:ResponseCode>ErrorFolderSavePropertyError</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
               <m:MessageXml>
                  <t:FieldURI FieldURI="folder:DisplayName"/>
               </m:MessageXml>
               <m:Folders/>
            </m:CreateFolderPathResponseMessage>
            <m:CreateFolderPathResponseMessage ResponseClass="Error">
               <m:MessageText>The specified parent folder could not be found.</m:MessageText>
               <m:ResponseCode>ErrorParentFolderNotFound</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
               <m:Folders/>
            </m:CreateFolderPathResponseMessage>
         </m:ResponseMessages>
      </m:CreateFolderPathResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="2b27c-162">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="2b27c-162">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="2b27c-163">CreateFolderPathResponse</span><span class="sxs-lookup"><span data-stu-id="2b27c-163">CreateFolderPathResponse</span></span>](createfolderpathresponse.md)
    
- [<span data-ttu-id="2b27c-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2b27c-164">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="2b27c-165">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2b27c-165">CreateFolderPathResponseMessage</span></span>](createfolderpathresponsemessage.md)
    
- [<span data-ttu-id="2b27c-166">MessageText</span><span class="sxs-lookup"><span data-stu-id="2b27c-166">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="2b27c-167">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2b27c-167">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2b27c-168">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2b27c-168">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="2b27c-169">MessageXml</span><span class="sxs-lookup"><span data-stu-id="2b27c-169">MessageXml</span></span>](messagexml.md)
    
- [<span data-ttu-id="2b27c-170">FieldURI</span><span class="sxs-lookup"><span data-stu-id="2b27c-170">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="2b27c-171">Ordner</span><span class="sxs-lookup"><span data-stu-id="2b27c-171">Folders</span></span>](folders-ex15websvcsotherref.md)
    
<span data-ttu-id="2b27c-172">Zusätzliche Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="2b27c-172">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2b27c-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b27c-173">See also</span></span>

- [<span data-ttu-id="2b27c-174">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="2b27c-174">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="2b27c-175">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="2b27c-175">FindFolder operation</span></span>](findfolder-operation.md)
    

