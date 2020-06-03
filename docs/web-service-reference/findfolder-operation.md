---
title: FindFolder-Vorgang
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
description: Der FindFolder-Vorgang verwendet Exchange Webdienste zum Suchen von Unterordnern eines identifizierten Ordners und gibt eine Reihe von Eigenschaften zurück, die die Gruppe von Unterordnern beschreiben.
ms.openlocfilehash: f1cc199bdaf684d8d74687ed7f064eb66fee48ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462584"
---
# <a name="findfolder-operation"></a><span data-ttu-id="c7ec4-103">FindFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c7ec4-103">FindFolder operation</span></span>

<span data-ttu-id="c7ec4-104">Der **FindFolder** -Vorgang verwendet Exchange Webdienste zum Suchen von Unterordnern eines identifizierten Ordners und gibt eine Reihe von Eigenschaften zurück, die die Gruppe von Unterordnern beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-104">The **FindFolder** operation uses Exchange Web Services to find subfolders of an identified folder and returns a set of properties that describe the set of subfolders.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c7ec4-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7ec4-105">Remarks</span></span>

<span data-ttu-id="c7ec4-106">FindFolder gibt nur die ersten 512 Bytes einer Streamable-Eigenschaft zurück.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-106">FindFolder returns only the first 512 bytes of any streamable property.</span></span> <span data-ttu-id="c7ec4-107">Bei Unicode werden nur die ersten 255 Zeichen mit einer Unicode-Zeichenfolge zurückgegeben, die mit null endet.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-107">For Unicode, it returns the first 255 characters by using a null-terminated Unicode string.</span></span>
  
<span data-ttu-id="c7ec4-108">Tief greifende Abfragen können nicht für Öffentliche Ordner ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-108">Deep traversal queries cannot be performed on public folders.</span></span>
  
<span data-ttu-id="c7ec4-109">Einschränkungen sind zulässig und sollten nur die Ordner Eigenschaften und nicht die Elementeigenschaften verwenden.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-109">Restrictions are permitted and should use only the folder properties, not the item properties.</span></span> <span data-ttu-id="c7ec4-110">Sortierfunktionen stehen für **FindFolder** -Antworten nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-110">Sorting functionality is not available for **FindFolder** responses.</span></span> <span data-ttu-id="c7ec4-111">Gruppierte Abfragen stehen für **FindFolder** -Abfragen nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-111">Grouped queries are not available for **FindFolder** queries.</span></span> 
  
 <span data-ttu-id="c7ec4-112">**Hinweis:** Der **FindFolder** -Vorgang wird auch verwendet, um verwaltete Ordner zu finden.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-112">**Note** The **FindFolder** operation is also used to find managed folders.</span></span> 
  
### <a name="soap-headers"></a><span data-ttu-id="c7ec4-113">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="c7ec4-113">SOAP Headers</span></span>

<span data-ttu-id="c7ec4-114">Der **FindFolder** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt und beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-114">The **FindFolder** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="c7ec4-115">**Header**</span><span class="sxs-lookup"><span data-stu-id="c7ec4-115">**Header**</span></span>|<span data-ttu-id="c7ec4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c7ec4-116">**Element**</span></span>|<span data-ttu-id="c7ec4-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c7ec4-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c7ec4-118">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="c7ec4-118">Impersonation</span></span>  <br/> |[<span data-ttu-id="c7ec4-119">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="c7ec4-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="c7ec4-120">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-120">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="c7ec4-121">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="c7ec4-121">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="c7ec4-122">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="c7ec4-122">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="c7ec4-123">Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-123">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="c7ec4-124">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="c7ec4-124">RequestVersion</span></span>  <br/> |[<span data-ttu-id="c7ec4-125">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="c7ec4-125">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="c7ec4-126">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-126">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="c7ec4-127">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="c7ec4-127">ServerVersion</span></span>  <br/> |[<span data-ttu-id="c7ec4-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c7ec4-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="c7ec4-129">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-129">Identifies the version of the server that responded to the request.</span></span>  <br/> |
|<span data-ttu-id="c7ec4-130">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="c7ec4-130">TimeZoneContext</span></span>  <br/> |[<span data-ttu-id="c7ec4-131">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="c7ec4-131">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="c7ec4-132">Gibt die Zeitzone für alle Antworten vom Server an.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-132">Identifies the time zone to be used for all responses from the server.</span></span>  <br/> |
   
## <a name="findfolder-request-example"></a><span data-ttu-id="c7ec4-133">FindFolder-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="c7ec4-133">FindFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="c7ec4-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7ec4-134">Description</span></span>

<span data-ttu-id="c7ec4-135">Im folgenden Beispiel einer **FindFolder** -Anforderung wird gezeigt, wie eine Anforderung zum Auffinden aller Ordner in einem Posteingang bildet.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-135">The following example of a **FindFolder** request shows how to form a request to find all the folders located in an Inbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c7ec4-136">Code</span><span class="sxs-lookup"><span data-stu-id="c7ec4-136">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="c7ec4-137">Comments</span><span class="sxs-lookup"><span data-stu-id="c7ec4-137">Comments</span></span>

<span data-ttu-id="c7ec4-138">Mit dem Standardwert für die [BaseShape](baseshape.md)gibt die Antwort den Ordnernamen, die Ordner-ID, die Anzahl der Unterordner, die Anzahl der untergeordneten Ordner im Ordner und die Anzahl der ungelesenen Elemente zurück.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-138">Using the Default value for the [BaseShape](baseshape.md), the response returns the folder name, the folder ID, the number of subfolders, the number of child folders found in the folder, and the count of unread items.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="c7ec4-139">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="c7ec4-139">Request elements</span></span>

<span data-ttu-id="c7ec4-140">Diese **FindFolder** -Anforderung umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="c7ec4-140">This **FindFolder** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="c7ec4-141">FindFolder</span><span class="sxs-lookup"><span data-stu-id="c7ec4-141">FindFolder</span></span>](findfolder.md)
    
- [<span data-ttu-id="c7ec4-142">FolderShape</span><span class="sxs-lookup"><span data-stu-id="c7ec4-142">FolderShape</span></span>](foldershape.md)
    
- [<span data-ttu-id="c7ec4-143">BaseShape</span><span class="sxs-lookup"><span data-stu-id="c7ec4-143">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="c7ec4-144">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="c7ec4-144">ParentFolderIds</span></span>](parentfolderids.md)
    
- [<span data-ttu-id="c7ec4-145">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="c7ec4-145">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
 <span data-ttu-id="c7ec4-146">Weitere **FindFolder** -anforderungselemente finden Sie im Schema.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-146">For additional **FindFolder** request elements, see the schema.</span></span> 
  
## <a name="findfolder-response-example"></a><span data-ttu-id="c7ec4-147">FindFolder-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="c7ec4-147">FindFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="c7ec4-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7ec4-148">Description</span></span>

<span data-ttu-id="c7ec4-149">Das folgende Simple Object Access Protocol (SOAP) Body-Beispiel zeigt eine erfolgreiche Antwort auf die **FindFolder** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-149">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **FindFolder** request.</span></span> <span data-ttu-id="c7ec4-150">Die Antwort enthält die Elemente, die zurückgegeben werden, wenn der Standardwert für die [BaseShape](baseshape.md) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-150">The response contains the elements that are returned when the Default value for the [BaseShape](baseshape.md) is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c7ec4-151">Die Ordner-ID und der Change-Schlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-151">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c7ec4-152">Code</span><span class="sxs-lookup"><span data-stu-id="c7ec4-152">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="response-elements"></a><span data-ttu-id="c7ec4-153">Response-Elemente</span><span class="sxs-lookup"><span data-stu-id="c7ec4-153">Response elements</span></span>

<span data-ttu-id="c7ec4-154">Die Eigenschaften, die in der Antwort zurückgegeben werden, werden durch die [BaseShape](baseshape.md) und die [AdditionalProperties](additionalproperties.md) bestimmt, wenn Sie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-154">The properties that are returned in the response are determined by the [BaseShape](baseshape.md) and the [AdditionalProperties](additionalproperties.md) if they are used.</span></span> <span data-ttu-id="c7ec4-155">Eine erfolgreiche **FindFolder** -Antwort umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="c7ec4-155">A successful **FindFolder** response includes the following elements:</span></span> 
  
- [<span data-ttu-id="c7ec4-156">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c7ec4-156">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="c7ec4-157">FindFolderResponse</span><span class="sxs-lookup"><span data-stu-id="c7ec4-157">FindFolderResponse</span></span>](findfolderresponse.md)
    
- [<span data-ttu-id="c7ec4-158">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c7ec4-158">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c7ec4-159">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c7ec4-159">FindFolderResponseMessage</span></span>](findfolderresponsemessage.md)
    
- [<span data-ttu-id="c7ec4-160">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c7ec4-160">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c7ec4-161">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="c7ec4-161">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
    
- [<span data-ttu-id="c7ec4-162">Ordner</span><span class="sxs-lookup"><span data-stu-id="c7ec4-162">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="c7ec4-163">Ordner</span><span class="sxs-lookup"><span data-stu-id="c7ec4-163">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="c7ec4-164">FolderId</span><span class="sxs-lookup"><span data-stu-id="c7ec4-164">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="c7ec4-165">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="c7ec4-165">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="c7ec4-166">Total count</span><span class="sxs-lookup"><span data-stu-id="c7ec4-166">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="c7ec4-167">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="c7ec4-167">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="c7ec4-168">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="c7ec4-168">UnreadCount</span></span>](unreadcount.md)
    
### <a name="comments"></a><span data-ttu-id="c7ec4-169">Kommentare</span><span class="sxs-lookup"><span data-stu-id="c7ec4-169">Comments</span></span>

 <span data-ttu-id="c7ec4-170">**FindFolder** -Antworten auf eine Anforderung mit dem Antwort-Shape **allproperties** geben nicht die [Total count](totalcount.md) -und [UnreadCount](unreadcount.md) -Elemente für die Suche nach öffentlichen Ordnern zurück.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-170">**FindFolder** responses to a request with the **AllProperties** response shape will not return the [TotalCount](totalcount.md) and [UnreadCount](unreadcount.md) elements for public folder searches.</span></span> 
  
## <a name="findfolder-error-response-example"></a><span data-ttu-id="c7ec4-171">FindFolder-Fehlerantwort Beispiel</span><span class="sxs-lookup"><span data-stu-id="c7ec4-171">FindFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="c7ec4-172">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7ec4-172">Description</span></span>

<span data-ttu-id="c7ec4-173">Das folgende SOAP Body-Beispiel zeigt eine Fehlermeldung, die auftritt, wenn Sie nach einem Ordner suchen, der durch eine fehlerhafte Ordner-ID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-173">The following SOAP body example shows an error response that occurs when you search for a folder that is identified by a malformed folder identifier.</span></span>
  
### <a name="code"></a><span data-ttu-id="c7ec4-174">Code</span><span class="sxs-lookup"><span data-stu-id="c7ec4-174">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="c7ec4-175">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="c7ec4-175">Error response elements</span></span>

<span data-ttu-id="c7ec4-176">Die **FindFolder** -Fehlerantwort umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="c7ec4-176">The **FindFolder** error response includes the following elements:</span></span> 
  
- [<span data-ttu-id="c7ec4-177">FindFolderResponse</span><span class="sxs-lookup"><span data-stu-id="c7ec4-177">FindFolderResponse</span></span>](findfolderresponse.md)
    
- [<span data-ttu-id="c7ec4-178">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c7ec4-178">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c7ec4-179">MessageText</span><span class="sxs-lookup"><span data-stu-id="c7ec4-179">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="c7ec4-180">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c7ec4-180">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c7ec4-181">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c7ec4-181">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="additional-information"></a><span data-ttu-id="c7ec4-182">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c7ec4-182">Additional Information</span></span>

- <span data-ttu-id="c7ec4-183">Das Element Folder [DisplayName (String)](displayname-string.md) ist immer in der Standardform enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-183">The folder [DisplayName (string)](displayname-string.md) element is always included in the default shape.</span></span> 
    
- <span data-ttu-id="c7ec4-184">Das [UnreadCount](unreadcount.md) -Element ist in Aufgaben und Notizenordner enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-184">The [UnreadCount](unreadcount.md) element is included in Tasks and Notes folders.</span></span> 
    
- <span data-ttu-id="c7ec4-185">Verwenden Sie den **PropertyTag** -Wert 0x672D mit dem Property-Typ **Integer** , um einen verwalteten Ordner mithilfe des [ExtendedFieldURI](extendedfielduri.md) -Elements zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c7ec4-185">Use the **PropertyTag** value of 0x672D with a property type of **Integer** to identify a managed folder by using the [ExtendedFieldURI](extendedfielduri.md) element.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c7ec4-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7ec4-186">See also</span></span>



[<span data-ttu-id="c7ec4-187">Suchen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="c7ec4-187">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

