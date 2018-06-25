---
title: UpdateFolder-Vorgang
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateFolder
api_type:
- schema
ms.assetid: 3494c996-b834-4813-b1ca-d99642d8b4e7
description: 'Der Vorgang UpdateFolder wird verwendet, um die Eigenschaften eines vorhandenen Elements im Exchange-Speicher zu ändern. Jede UpdateFolder-Operation besteht aus den folgenden:'
ms.openlocfilehash: b33937bb09f0dcbe3d3ed61bbf5233423f320d9c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839348"
---
# <a name="updatefolder-operation"></a><span data-ttu-id="ee387-104">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ee387-104">UpdateFolder operation</span></span>

<span data-ttu-id="ee387-105">Der Vorgang UpdateFolder wird verwendet, um die Eigenschaften eines vorhandenen Elements im Exchange-Speicher zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ee387-105">The UpdateFolder operation is used to modify properties of an existing item in the Exchange store.</span></span> <span data-ttu-id="ee387-106">Jede UpdateFolder-Operation besteht aus den folgenden:</span><span class="sxs-lookup"><span data-stu-id="ee387-106">Each UpdateFolder operation consists of the following:</span></span>
  
- <span data-ttu-id="ee387-107">Ein [FolderId](folderid.md) -Element, einen Ordner aktualisieren angibt.</span><span class="sxs-lookup"><span data-stu-id="ee387-107">A [FolderId](folderid.md) element that specifies a folder to update.</span></span> 
    
- <span data-ttu-id="ee387-108">Ein interner Pfad eines Elements im Ordner gemäß den Ordner-Shape, das zu aktualisierenden gibt.</span><span class="sxs-lookup"><span data-stu-id="ee387-108">An internal path of an element in the folder, as specified by the folder shape, which specifies the data to update.</span></span>
    
- <span data-ttu-id="ee387-109">Ein Ordner, der den neuen Wert des Felds aktualisierte enthält, wenn das Update nicht auf eine Löschung ist.</span><span class="sxs-lookup"><span data-stu-id="ee387-109">A folder that contains the new value of the updated field, if the update is not a deletion.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee387-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ee387-110">Remarks</span></span>

<span data-ttu-id="ee387-111">Drei grundlegende Update-Aktionen können für ein Element ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ee387-111">Three basic update actions can be performed on an item.</span></span> <span data-ttu-id="ee387-112">Diese Aktionen sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee387-112">These actions are listed in the following table.</span></span>
  
|<span data-ttu-id="ee387-113">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="ee387-113">**Action**</span></span>|<span data-ttu-id="ee387-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ee387-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ee387-115">Anfügeabfrage</span><span class="sxs-lookup"><span data-stu-id="ee387-115">Append</span></span>  <br/> |<span data-ttu-id="ee387-116">Die Append-Aktion hinzugefügt Daten auf eine vorhandene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ee387-116">The append action adds data to an existing property.</span></span> <span data-ttu-id="ee387-117">Beibehalten die Daten, die derzeit vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ee387-117">It preserves the data that is currently there.</span></span> <span data-ttu-id="ee387-118">Fügen Sie gilt nicht für alle Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ee387-118">Append is not applicable to all properties.</span></span>  <br/> |
|<span data-ttu-id="ee387-119">Gruppe</span><span class="sxs-lookup"><span data-stu-id="ee387-119">Set</span></span>  <br/> |<span data-ttu-id="ee387-120">Die Set-Aktion ersetzt Daten für eine Eigenschaft aus, wenn Daten enthält, oder die Eigenschaft erstellt und legt deren Wert fest, wenn er nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ee387-120">The set action replaces data for a property if it contains data, or creates the property and sets its value if it does not exist.</span></span> <span data-ttu-id="ee387-121">Die Set-Aktion gilt nur für schreibbaren Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ee387-121">The set action is only applicable to writable properties.</span></span>  <br/> |
|<span data-ttu-id="ee387-122">Löschen</span><span class="sxs-lookup"><span data-stu-id="ee387-122">Delete</span></span>  <br/> |<span data-ttu-id="ee387-123">Die Löschaktion entfernt eine Eigenschaft aus einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="ee387-123">The delete action removes a property from a folder.</span></span> <span data-ttu-id="ee387-124">Dies unterscheidet sich auf einen leeren Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="ee387-124">This is different than setting it to an empty value.</span></span> <span data-ttu-id="ee387-125">Nach Abschluss des Vorgangs ist die Eigenschaft für den Ordner nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ee387-125">When complete, the property does not exist for the folder.</span></span> <span data-ttu-id="ee387-126">Delete gilt nur für schreibbaren Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ee387-126">Delete is only applicable to writable properties.</span></span>  <br/> |
   
## <a name="updatefolder-request-example"></a><span data-ttu-id="ee387-127">Anforderungsbeispiel UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="ee387-127">UpdateFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="ee387-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee387-128">Description</span></span>

<span data-ttu-id="ee387-129">Im folgenden Beispiel wird einer Anforderung UpdateFolder veranschaulicht einen Anzeigenamen für den Ordner zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ee387-129">The following example of an UpdateFolder request shows how to update a folder display name.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ee387-130">Code</span><span class="sxs-lookup"><span data-stu-id="ee387-130">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="AScA" ChangeKey="GO3u/"/>
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:DisplayName"/>
              <t:Folder>
                <t:DisplayName>NewFolderName</t:DisplayName>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </FolderChanges>
    </UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="ee387-131">Kommentare</span><span class="sxs-lookup"><span data-stu-id="ee387-131">Comments</span></span>

<span data-ttu-id="ee387-132">In diesem Beispiel wird der Anzeigename des Ordners auf NeuerOrdnername geändert.</span><span class="sxs-lookup"><span data-stu-id="ee387-132">This example changes the display name of the folder to NewFolderName.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ee387-133">Die Werte der **Id** und **ChangeKey** Attribute des Elements [FolderId](folderid.md) wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="ee387-133">The values of the **Id** and **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened for readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="ee387-134">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="ee387-134">Request elements</span></span>

<span data-ttu-id="ee387-135">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="ee387-135">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="ee387-136">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="ee387-136">UpdateFolder</span></span>](updatefolder.md)
    
- [<span data-ttu-id="ee387-137">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="ee387-137">FolderChanges</span></span>](folderchanges.md)
    
- [<span data-ttu-id="ee387-138">FolderChange</span><span class="sxs-lookup"><span data-stu-id="ee387-138">FolderChange</span></span>](folderchange.md)
    
- [<span data-ttu-id="ee387-139">FolderId</span><span class="sxs-lookup"><span data-stu-id="ee387-139">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="ee387-140">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="ee387-140">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="ee387-141">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="ee387-141">SetFolderField</span></span>](setfolderfield.md)
    
- [<span data-ttu-id="ee387-142">FieldURI</span><span class="sxs-lookup"><span data-stu-id="ee387-142">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="ee387-143">Folder</span><span class="sxs-lookup"><span data-stu-id="ee387-143">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="ee387-144">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="ee387-144">DisplayName (string)</span></span>](displayname-string.md)
    
<span data-ttu-id="ee387-145">Finden Sie im Schema für zusätzliche Elemente, die Sie verwenden können, um eine Anforderung UpdateFolder bilden.</span><span class="sxs-lookup"><span data-stu-id="ee387-145">See the schema for additional elements that you can use to form an UpdateFolder request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ee387-146">Der Standardspeicherort des Schemas ist in das virtuelle EWS-Verzeichnis auf dem Computer, der die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ee387-146">The default location of the schema is in the EWS virtual directory on the computer that has the Client Access server role installed.</span></span> 
  
## <a name="updatefolder-response-example"></a><span data-ttu-id="ee387-147">UpdateFolder antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="ee387-147">UpdateFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="ee387-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee387-148">Description</span></span>

<span data-ttu-id="ee387-149">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung UpdateFolder.</span><span class="sxs-lookup"><span data-stu-id="ee387-149">The following example shows a successful response to the UpdateFolder request.</span></span> <span data-ttu-id="ee387-150">In diesem Beispiel wird der neue Änderungsschlüssel gemäß den aktualisierten Status des Ordners zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ee387-150">In this example, the new change key is returned to reflect the updated status of the folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="ee387-151">Code</span><span class="sxs-lookup"><span data-stu-id="ee387-151">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UpdateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AAAlAFVz" ChangeKey="AQAAAB" />
            </t:Folder>
          </m:Folders>
        </m:UpdateFolderResponseMessage>
      </m:ResponseMessages>
    </UpdateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="ee387-152">Kommentare</span><span class="sxs-lookup"><span data-stu-id="ee387-152">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="ee387-153">Die Ordner-ID und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ee387-153">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="ee387-154">Die Ordner-ID, die in der Antwort zurückgegeben wird, stellt aktualisierten Ordner.</span><span class="sxs-lookup"><span data-stu-id="ee387-154">The folder ID that is returned in the response represents the updated folder.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="ee387-155">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="ee387-155">Successful response elements</span></span>

<span data-ttu-id="ee387-156">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="ee387-156">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="ee387-157">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ee387-157">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="ee387-158">UpdateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="ee387-158">UpdateFolderResponse</span></span>](updatefolderresponse.md)
    
- [<span data-ttu-id="ee387-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ee387-159">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ee387-160">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ee387-160">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md)
    
- [<span data-ttu-id="ee387-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ee387-161">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ee387-162">Ordner</span><span class="sxs-lookup"><span data-stu-id="ee387-162">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="ee387-163">Folder</span><span class="sxs-lookup"><span data-stu-id="ee387-163">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="ee387-164">FolderId</span><span class="sxs-lookup"><span data-stu-id="ee387-164">FolderId</span></span>](folderid.md)
    
## <a name="updatefolder-error-response-example"></a><span data-ttu-id="ee387-165">Antwortbeispiel UpdateFolder-Fehler</span><span class="sxs-lookup"><span data-stu-id="ee387-165">UpdateFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="ee387-166">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee387-166">Description</span></span>

<span data-ttu-id="ee387-167">Das folgende Beispiel zeigt eine Fehlerantwort an eine UpdateFolder-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ee387-167">The following example shows an error response to an UpdateFolder request.</span></span>
  
### <a name="code"></a><span data-ttu-id="ee387-168">Code</span><span class="sxs-lookup"><span data-stu-id="ee387-168">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UpdateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateFolderResponseMessage ResponseClass="Error">
          <m:MessageText>The change key is invalid.</m:MessageText>
          <m:ResponseCode>ErrorInvalidChangeKey</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:UpdateFolderResponseMessage>
      </m:ResponseMessages>
    </UpdateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="ee387-169">Kommentare</span><span class="sxs-lookup"><span data-stu-id="ee387-169">Comments</span></span>

<span data-ttu-id="ee387-170">Dieses Beispiel zeigt eine Fehlerantwort an, die durch ein ungültiges **ChangeKey** -Attribut in der Anforderung verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="ee387-170">This example shows an error response that is caused by an invalid **ChangeKey** attribute in the request.</span></span> 
  
### <a name="error-response-elements"></a><span data-ttu-id="ee387-171">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="ee387-171">Error response elements</span></span>

<span data-ttu-id="ee387-172">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="ee387-172">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="ee387-173">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ee387-173">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="ee387-174">UpdateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="ee387-174">UpdateFolderResponse</span></span>](updatefolderresponse.md)
    
- [<span data-ttu-id="ee387-175">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ee387-175">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ee387-176">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ee387-176">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md)
    
- [<span data-ttu-id="ee387-177">MessageText</span><span class="sxs-lookup"><span data-stu-id="ee387-177">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="ee387-178">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ee387-178">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ee387-179">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ee387-179">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="ee387-180">Ordner</span><span class="sxs-lookup"><span data-stu-id="ee387-180">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="ee387-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee387-181">See also</span></span>



- [<span data-ttu-id="ee387-182">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ee387-182">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

