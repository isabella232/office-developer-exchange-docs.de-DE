---
title: CreateFolderPath-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5a10aa5e-3f25-4ec3-a0b9-284c30918a1f
description: Hier finden Sie Informationen zum CreateFolderPath-EWS-Vorgang.
ms.openlocfilehash: a8d42cbef854d900c5fb6b72c730dd1e2b903aec
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458901"
---
# <a name="createfolderpath-operation"></a><span data-ttu-id="c1101-103">CreateFolderPath-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c1101-103">CreateFolderPath operation</span></span>

<span data-ttu-id="c1101-104">Hier finden Sie Informationen zum **CreateFolderPath** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c1101-104">Find information about the **CreateFolderPath** EWS operation.</span></span> 
  
<span data-ttu-id="c1101-105">Mit dem **CreateFolderPath** -Vorgang wird eine Ordnerhierarchie erstellt.</span><span class="sxs-lookup"><span data-stu-id="c1101-105">The **CreateFolderPath** operation creates a folder hierarchy.</span></span> 
  
<span data-ttu-id="c1101-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c1101-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-createfolderpath-operation"></a><span data-ttu-id="c1101-107">Verwenden des CreateFolderPath-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="c1101-107">Using the CreateFolderPath operation</span></span>

<span data-ttu-id="c1101-108">Die **CreateFolderPath** -Vorgangsanforderung verwendet ein Array von Ordnern und eine übergeordnete Ordner-ID und erstellt eine Ordnerhierarchie basierend auf der Reihenfolge der Ordner im Array.</span><span class="sxs-lookup"><span data-stu-id="c1101-108">The **CreateFolderPath** operation request takes an array of folders and a parent folder identifier and creates a folder hierarchy based on the order of the folders in the array.</span></span> 
  
### <a name="createfolderpath-operation-soap-headers"></a><span data-ttu-id="c1101-109">SOAP-Header des CreateFolderPath-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="c1101-109">CreateFolderPath operation SOAP headers</span></span>

<span data-ttu-id="c1101-110">Der **CreateFolderPath** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c1101-110">The **CreateFolderPath** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="c1101-111">**Headername**</span><span class="sxs-lookup"><span data-stu-id="c1101-111">**Header name**</span></span>|<span data-ttu-id="c1101-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1101-112">**Element**</span></span>|<span data-ttu-id="c1101-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1101-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c1101-114">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="c1101-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="c1101-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="c1101-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="c1101-116">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="c1101-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="c1101-117">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c1101-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c1101-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="c1101-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="c1101-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="c1101-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="c1101-120">Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c1101-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="c1101-121">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c1101-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c1101-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="c1101-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="c1101-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="c1101-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="c1101-124">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="c1101-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="c1101-125">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c1101-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c1101-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="c1101-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="c1101-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c1101-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="c1101-128">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="c1101-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="c1101-129">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="c1101-129">This header is applicable to a response.</span></span>  <br/> |
|<span data-ttu-id="c1101-130">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="c1101-130">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="c1101-131">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="c1101-131">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="c1101-132">Gibt den Zeit zonenbereich für **DateTime** -Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="c1101-132">Identifies the time zone scope for **DateTime** properties.</span></span> <span data-ttu-id="c1101-133">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c1101-133">This header is applicable to a request.</span></span>  <br/> |
   
## <a name="createfolderpath-operation-request-example-create-a-folder-hierarchy"></a><span data-ttu-id="c1101-134">CreateFolderPath-Vorgangs Anforderungs Beispiel: Erstellen einer Ordnerhierarchie</span><span class="sxs-lookup"><span data-stu-id="c1101-134">CreateFolderPath operation request example: Create a folder hierarchy</span></span>

<span data-ttu-id="c1101-135">Im folgenden Beispiel einer **CreateFolderPath** -Vorgangsanforderung wird gezeigt, wie Sie eine Ordnerhierarchie erstellen, die drei Ordner tief im standardmäßigen Posteingangsordner ist.</span><span class="sxs-lookup"><span data-stu-id="c1101-135">The following example of a **CreateFolderPath** operation request shows how to create a folder hierarchy that is three folders deep in the default Inbox folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c1101-136">Alle Element-IDs und Änderungsschlüssel in diesem Artikel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c1101-136">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="c1101-137">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="c1101-137">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c1101-138">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="c1101-138">CreateFolderPath</span></span>](createfolderpath.md)
    
- [<span data-ttu-id="c1101-139">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="c1101-139">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)
    
- [<span data-ttu-id="c1101-140">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="c1101-140">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="c1101-141">RelativeFolderPath</span><span class="sxs-lookup"><span data-stu-id="c1101-141">RelativeFolderPath</span></span>](relativefolderpath.md)
    
- [<span data-ttu-id="c1101-142">Folder</span><span class="sxs-lookup"><span data-stu-id="c1101-142">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="c1101-143">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="c1101-143">DisplayName (string)</span></span>](displayname-string.md)
    
## <a name="successful-createfolderpath-operation-response"></a><span data-ttu-id="c1101-144">Erfolgreiche Reaktion des CreateFolderPath-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="c1101-144">Successful CreateFolderPath operation response</span></span>

<span data-ttu-id="c1101-145">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **CreateFolderPath** -Vorgangsanforderung zum Erstellen einer Ordnerhierarchie mit drei Ordnern, die sich tief im Standardordner "Posteingang" befinden.</span><span class="sxs-lookup"><span data-stu-id="c1101-145">The following example shows a successful response to a **CreateFolderPath** operation request to create a folder hierarchy three folders deep in the default Inbox folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:CreateFolderPathResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="c1101-146">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="c1101-146">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c1101-147">CreateFolderPathResponse</span><span class="sxs-lookup"><span data-stu-id="c1101-147">CreateFolderPathResponse</span></span>](createfolderpathresponse.md)
    
- [<span data-ttu-id="c1101-148">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c1101-148">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c1101-149">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c1101-149">CreateFolderPathResponseMessage</span></span>](createfolderpathresponsemessage.md)
    
- [<span data-ttu-id="c1101-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c1101-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c1101-151">Ordner</span><span class="sxs-lookup"><span data-stu-id="c1101-151">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="c1101-152">Folder</span><span class="sxs-lookup"><span data-stu-id="c1101-152">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="c1101-153">FolderId</span><span class="sxs-lookup"><span data-stu-id="c1101-153">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="c1101-154">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="c1101-154">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="c1101-155">Total count</span><span class="sxs-lookup"><span data-stu-id="c1101-155">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="c1101-156">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="c1101-156">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="c1101-157">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="c1101-157">UnreadCount</span></span>](unreadcount.md)
    
## <a name="createfolderpath-operation-error-response"></a><span data-ttu-id="c1101-158">Fehlerantwort des CreateFolderPath-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="c1101-158">CreateFolderPath operation error response</span></span>

<span data-ttu-id="c1101-159">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **CreateFolderPath** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="c1101-159">The following example shows an error response to a **CreateFolderPath** operation request.</span></span> <span data-ttu-id="c1101-160">Dies ist eine Antwort auf eine Anforderung zum Erstellen von zwei Ordnern, von denen die erste nicht über eine Anzeigename-Eigenschaft festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c1101-160">This is a response to a request to create two folders, the first of which does not have a display name property set.</span></span> <span data-ttu-id="c1101-161">Der erste Ordner in der Hierarchiekann nicht ohne eine Anzeigename-Eigenschaft erstellt werden, und der zweite Ordner kann nicht erstellt werden, da der übergeordnete Ordner in der Hierarchie nicht erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c1101-161">The first folder in the hierarchy cannot be created without a display name property, and the second folder cannot be created because the parent folder in the hierarchy was not created.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:CreateFolderPathResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="c1101-162">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="c1101-162">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c1101-163">CreateFolderPathResponse</span><span class="sxs-lookup"><span data-stu-id="c1101-163">CreateFolderPathResponse</span></span>](createfolderpathresponse.md)
    
- [<span data-ttu-id="c1101-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c1101-164">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c1101-165">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c1101-165">CreateFolderPathResponseMessage</span></span>](createfolderpathresponsemessage.md)
    
- [<span data-ttu-id="c1101-166">MessageText</span><span class="sxs-lookup"><span data-stu-id="c1101-166">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="c1101-167">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c1101-167">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c1101-168">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c1101-168">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="c1101-169">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="c1101-169">MessageXml</span></span>](messagexml.md)
    
- [<span data-ttu-id="c1101-170">FieldURI</span><span class="sxs-lookup"><span data-stu-id="c1101-170">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="c1101-171">Ordner</span><span class="sxs-lookup"><span data-stu-id="c1101-171">Folders</span></span>](folders-ex15websvcsotherref.md)
    
<span data-ttu-id="c1101-172">Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="c1101-172">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c1101-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1101-173">See also</span></span>

- [<span data-ttu-id="c1101-174">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="c1101-174">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="c1101-175">FindFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c1101-175">FindFolder operation</span></span>](findfolder-operation.md)
    

