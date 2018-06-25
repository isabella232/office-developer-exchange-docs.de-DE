---
title: FindFolder Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindFolder
api_type:
- schema
ms.assetid: 7a9855aa-06cc-45ba-ad2a-645c15b7d031
description: Der Vorgang FindFolder mithilfe Exchange-Webdienste Unterordnern eines angegebenen Ordners gesucht und gibt einen Satz von Eigenschaften, mit die die Unterordner beschrieben werden.
ms.openlocfilehash: 655455b46d4a3192b294bee9d85352d95ded49ae
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758444"
---
# <a name="findfolder-operation"></a><span data-ttu-id="c7a5c-103">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="c7a5c-103">FindFolder operation</span></span>

<span data-ttu-id="c7a5c-104">Der Vorgang **FindFolder** mithilfe Exchange-Webdienste Unterordnern eines angegebenen Ordners gesucht und gibt einen Satz von Eigenschaften, mit die die Unterordner beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-104">The **FindFolder** operation uses Exchange Web Services to find subfolders of an identified folder and returns a set of properties that describe the set of subfolders.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c7a5c-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c7a5c-105">Remarks</span></span>

<span data-ttu-id="c7a5c-106">FindFolder gibt nur die ersten 512 Byte einer beliebigen streamfähiges Eigenschaft zurück.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-106">FindFolder returns only the first 512 bytes of any streamable property.</span></span> <span data-ttu-id="c7a5c-107">Bei Unicode werden nur die ersten 255 Zeichen mit einer Unicode-Zeichenfolge zurückgegeben, die mit null endet.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-107">For Unicode, it returns the first 255 characters by using a null-terminated Unicode string.</span></span>
  
<span data-ttu-id="c7a5c-108">Deep Traversal Abfragen können nicht auf Öffentliche Ordner ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-108">Deep traversal queries cannot be performed on public folders.</span></span>
  
<span data-ttu-id="c7a5c-109">Einschränkungen sind zulässig und sollten nur die Ordnereigenschaften, nicht die Eigenschaften des Elements verwenden.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-109">Restrictions are permitted and should use only the folder properties, not the item properties.</span></span> <span data-ttu-id="c7a5c-110">Sortierungsfunktionen ist nicht verfügbar für **FindFolder** Antworten.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-110">Sorting functionality is not available for **FindFolder** responses.</span></span> <span data-ttu-id="c7a5c-111">Gruppierte Abfragen sind nicht verfügbar für **FindFolder** Abfragen.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-111">Grouped queries are not available for **FindFolder** queries.</span></span> 
  
 <span data-ttu-id="c7a5c-112">**Hinweis** Der Vorgang **FindFolder** wird auch verwendet, um verwaltete Ordner zu finden.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-112">**Note** The **FindFolder** operation is also used to find managed folders.</span></span> 
  
### <a name="soap-headers"></a><span data-ttu-id="c7a5c-113">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="c7a5c-113">SOAP Headers</span></span>

<span data-ttu-id="c7a5c-114">Der Vorgang **FindFolder** können die SOAP-Header, die aufgeführt und in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-114">The **FindFolder** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="c7a5c-115">**Header**</span><span class="sxs-lookup"><span data-stu-id="c7a5c-115">**Header**</span></span>|<span data-ttu-id="c7a5c-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c7a5c-116">**Element**</span></span>|<span data-ttu-id="c7a5c-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c7a5c-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c7a5c-118">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="c7a5c-118">Impersonation</span></span>  <br/> |[<span data-ttu-id="c7a5c-119">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="c7a5c-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="c7a5c-120">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-120">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="c7a5c-121">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="c7a5c-121">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="c7a5c-122">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="c7a5c-122">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="c7a5c-123">Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-123">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="c7a5c-124">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="c7a5c-124">RequestVersion</span></span>  <br/> |[<span data-ttu-id="c7a5c-125">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="c7a5c-125">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="c7a5c-126">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-126">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="c7a5c-127">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="c7a5c-127">ServerVersion</span></span>  <br/> |[<span data-ttu-id="c7a5c-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c7a5c-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="c7a5c-129">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-129">Identifies the version of the server that responded to the request.</span></span>  <br/> |
|<span data-ttu-id="c7a5c-130">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="c7a5c-130">TimeZoneContext</span></span>  <br/> |[<span data-ttu-id="c7a5c-131">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="c7a5c-131">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="c7a5c-132">Gibt die Zeitzone für alle Antworten vom Server an.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-132">Identifies the time zone to be used for all responses from the server.</span></span>  <br/> |
   
## <a name="findfolder-request-example"></a><span data-ttu-id="c7a5c-133">FindFolder anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="c7a5c-133">FindFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="c7a5c-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7a5c-134">Description</span></span>

<span data-ttu-id="c7a5c-135">Im folgenden Beispiel wird eine Anforderung **FindFolder** veranschaulicht eine Anforderung an alle Ordner befindet sich im Posteingang suchen bilden.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-135">The following example of a **FindFolder** request shows how to form a request to find all the folders located in an Inbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c7a5c-136">Code</span><span class="sxs-lookup"><span data-stu-id="c7a5c-136">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="c7a5c-137">Kommentare</span><span class="sxs-lookup"><span data-stu-id="c7a5c-137">Comments</span></span>

<span data-ttu-id="c7a5c-138">Verwenden den Standardwert für die [BaseShape](baseshape.md), gibt die Antwort den Ordnernamen, die Ordner-ID, die Anzahl der Unterordner, die Anzahl der untergeordneten Ordner in den Ordner und die Anzahl der ungelesenen Elemente zurück.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-138">Using the Default value for the [BaseShape](baseshape.md), the response returns the folder name, the folder ID, the number of subfolders, the number of child folders found in the folder, and the count of unread items.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="c7a5c-139">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="c7a5c-139">Request elements</span></span>

<span data-ttu-id="c7a5c-140">Diese Anforderung **FindFolder** umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="c7a5c-140">This **FindFolder** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="c7a5c-141">FindFolder</span><span class="sxs-lookup"><span data-stu-id="c7a5c-141">FindFolder</span></span>](findfolder.md)
    
- [<span data-ttu-id="c7a5c-142">FolderShape</span><span class="sxs-lookup"><span data-stu-id="c7a5c-142">FolderShape</span></span>](foldershape.md)
    
- [<span data-ttu-id="c7a5c-143">BaseShape</span><span class="sxs-lookup"><span data-stu-id="c7a5c-143">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="c7a5c-144">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="c7a5c-144">ParentFolderIds</span></span>](parentfolderids.md)
    
- [<span data-ttu-id="c7a5c-145">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="c7a5c-145">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
 <span data-ttu-id="c7a5c-146">Zusätzliche **FindFolder** Anforderung Elemente finden Sie unter Schema.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-146">For additional **FindFolder** request elements, see the schema.</span></span> 
  
## <a name="findfolder-response-example"></a><span data-ttu-id="c7a5c-147">FindFolder antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="c7a5c-147">FindFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="c7a5c-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7a5c-148">Description</span></span>

<span data-ttu-id="c7a5c-149">Das folgende (SOAP = Simple Object Access Protocol)-Body-Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung **FindFolder** .</span><span class="sxs-lookup"><span data-stu-id="c7a5c-149">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **FindFolder** request.</span></span> <span data-ttu-id="c7a5c-150">Die Antwort enthält die Elemente, die zurückgegeben werden, wenn der Standardwert für die [BaseShape](baseshape.md) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-150">The response contains the elements that are returned when the Default value for the [BaseShape](baseshape.md) is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c7a5c-151">Die Ordner-ID und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-151">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c7a5c-152">Code</span><span class="sxs-lookup"><span data-stu-id="c7a5c-152">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Folders>
              <t:Folder>
                <t:FolderId Id="AQAnAH" ChangeKey="AQAAABY" />
                <t:DisplayName>TestFolder</t:DisplayName>
                <t:TotalCount>0</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </FindFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="c7a5c-153">Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="c7a5c-153">Response elements</span></span>

<span data-ttu-id="c7a5c-154">Die Eigenschaften, die in der Antwort zurückgegeben werden werden durch die [BaseShape](baseshape.md) und die [AdditionalProperties](additionalproperties.md) bestimmt, wenn sie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-154">The properties that are returned in the response are determined by the [BaseShape](baseshape.md) and the [AdditionalProperties](additionalproperties.md) if they are used.</span></span> <span data-ttu-id="c7a5c-155">Eine erfolgreiche Antwort **FindFolder** umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="c7a5c-155">A successful **FindFolder** response includes the following elements:</span></span> 
  
- [<span data-ttu-id="c7a5c-156">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c7a5c-156">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="c7a5c-157">FindFolderResponse</span><span class="sxs-lookup"><span data-stu-id="c7a5c-157">FindFolderResponse</span></span>](findfolderresponse.md)
    
- [<span data-ttu-id="c7a5c-158">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c7a5c-158">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c7a5c-159">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c7a5c-159">FindFolderResponseMessage</span></span>](findfolderresponsemessage.md)
    
- [<span data-ttu-id="c7a5c-160">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c7a5c-160">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c7a5c-161">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="c7a5c-161">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
    
- [<span data-ttu-id="c7a5c-162">Ordner</span><span class="sxs-lookup"><span data-stu-id="c7a5c-162">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="c7a5c-163">Folder</span><span class="sxs-lookup"><span data-stu-id="c7a5c-163">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="c7a5c-164">FolderId</span><span class="sxs-lookup"><span data-stu-id="c7a5c-164">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="c7a5c-165">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="c7a5c-165">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="c7a5c-166">TotalCount</span><span class="sxs-lookup"><span data-stu-id="c7a5c-166">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="c7a5c-167">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="c7a5c-167">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="c7a5c-168">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="c7a5c-168">UnreadCount</span></span>](unreadcount.md)
    
### <a name="comments"></a><span data-ttu-id="c7a5c-169">Kommentare</span><span class="sxs-lookup"><span data-stu-id="c7a5c-169">Comments</span></span>

 <span data-ttu-id="c7a5c-170">Antworten auf eine Anforderung mit dem **AllProperties** Antwort Shape **FindFolder** gibt nicht den [TotalCount](totalcount.md) und die [UnreadCount](unreadcount.md) Elemente für Öffentliche Ordner suchen zurück.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-170">**FindFolder** responses to a request with the **AllProperties** response shape will not return the [TotalCount](totalcount.md) and [UnreadCount](unreadcount.md) elements for public folder searches.</span></span> 
  
## <a name="findfolder-error-response-example"></a><span data-ttu-id="c7a5c-171">Antwortbeispiel FindFolder Fehler</span><span class="sxs-lookup"><span data-stu-id="c7a5c-171">FindFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="c7a5c-172">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7a5c-172">Description</span></span>

<span data-ttu-id="c7a5c-173">Das folgende SOAP-Body-Beispiel zeigt eine Fehlerantwort an, die auftritt, wenn für einen Ordner suchen, die durch eine fehlerhafte Ordner-ID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-173">The following SOAP body example shows an error response that occurs when you search for a folder that is identified by a malformed folder identifier.</span></span>
  
### <a name="code"></a><span data-ttu-id="c7a5c-174">Code</span><span class="sxs-lookup"><span data-stu-id="c7a5c-174">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </FindFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="c7a5c-175">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="c7a5c-175">Error response elements</span></span>

<span data-ttu-id="c7a5c-176">Die Fehlerantwort **FindFolder** umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="c7a5c-176">The **FindFolder** error response includes the following elements:</span></span> 
  
- [<span data-ttu-id="c7a5c-177">FindFolderResponse</span><span class="sxs-lookup"><span data-stu-id="c7a5c-177">FindFolderResponse</span></span>](findfolderresponse.md)
    
- [<span data-ttu-id="c7a5c-178">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c7a5c-178">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c7a5c-179">MessageText</span><span class="sxs-lookup"><span data-stu-id="c7a5c-179">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="c7a5c-180">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c7a5c-180">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c7a5c-181">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c7a5c-181">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="additional-information"></a><span data-ttu-id="c7a5c-182">Zusätzliche Informationen</span><span class="sxs-lookup"><span data-stu-id="c7a5c-182">Additional Information</span></span>

- <span data-ttu-id="c7a5c-183">Ordner [DisplayName (String)](displayname-string.md) -Elements ist immer in der Standardform enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-183">The folder [DisplayName (string)](displayname-string.md) element is always included in the default shape.</span></span> 
    
- <span data-ttu-id="c7a5c-184">Das [UnreadCount](unreadcount.md) -Element ist im Ordner Aufgaben und Notizen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-184">The [UnreadCount](unreadcount.md) element is included in Tasks and Notes folders.</span></span> 
    
- <span data-ttu-id="c7a5c-185">Verwenden Sie den Wert **' PropertyTag '** 0x672D mit Eigenschaftentyp **ganze Zahl** um einen verwalteten Ordner mit dem [ExtendedFieldURI](extendedfielduri.md) -Element zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c7a5c-185">Use the **PropertyTag** value of 0x672D with a property type of **Integer** to identify a managed folder by using the [ExtendedFieldURI](extendedfielduri.md) element.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c7a5c-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7a5c-186">See also</span></span>



[<span data-ttu-id="c7a5c-187">Suchen nach Ordnern</span><span class="sxs-lookup"><span data-stu-id="c7a5c-187">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

