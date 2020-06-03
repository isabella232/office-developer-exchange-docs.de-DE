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
description: 'Der UpdateFolder-Vorgang wird verwendet, um die Eigenschaften eines vorhandenen Elements in der Exchange-Informationsspeicher zu ändern. Jeder UpdateFolder-Vorgang besteht aus folgenden Elementen:'
ms.openlocfilehash: fb894d9f42358b67f81e9fe8ae41ba61e6f46460
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467361"
---
# <a name="updatefolder-operation"></a><span data-ttu-id="d80fe-104">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d80fe-104">UpdateFolder operation</span></span>

<span data-ttu-id="d80fe-105">Der UpdateFolder-Vorgang wird verwendet, um die Eigenschaften eines vorhandenen Elements in der Exchange-Informationsspeicher zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d80fe-105">The UpdateFolder operation is used to modify properties of an existing item in the Exchange store.</span></span> <span data-ttu-id="d80fe-106">Jeder UpdateFolder-Vorgang besteht aus folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="d80fe-106">Each UpdateFolder operation consists of the following:</span></span>
  
- <span data-ttu-id="d80fe-107">Ein [Folder](folderid.md) -Element, mit dem ein zu aktualisierbarer Ordner angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d80fe-107">A [FolderId](folderid.md) element that specifies a folder to update.</span></span> 
    
- <span data-ttu-id="d80fe-108">Ein interner Pfad eines Elements im Ordner, wie durch die Ordner Form angegeben, die die zu aktualisierende Daten angibt.</span><span class="sxs-lookup"><span data-stu-id="d80fe-108">An internal path of an element in the folder, as specified by the folder shape, which specifies the data to update.</span></span>
    
- <span data-ttu-id="d80fe-109">Ein Ordner, der den neuen Wert des aktualisierten Felds enthält, wenn es sich bei der Aktualisierung nicht um eine Löschung handelt.</span><span class="sxs-lookup"><span data-stu-id="d80fe-109">A folder that contains the new value of the updated field, if the update is not a deletion.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d80fe-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d80fe-110">Remarks</span></span>

<span data-ttu-id="d80fe-111">Für ein Element können drei grundlegende Updateaktionen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d80fe-111">Three basic update actions can be performed on an item.</span></span> <span data-ttu-id="d80fe-112">Diese Aktionen sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d80fe-112">These actions are listed in the following table.</span></span>
  
|<span data-ttu-id="d80fe-113">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="d80fe-113">**Action**</span></span>|<span data-ttu-id="d80fe-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d80fe-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d80fe-115">Append</span><span class="sxs-lookup"><span data-stu-id="d80fe-115">Append</span></span>  <br/> |<span data-ttu-id="d80fe-116">Mit der Append-Aktion werden einer vorhandenen Eigenschaft Daten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d80fe-116">The append action adds data to an existing property.</span></span> <span data-ttu-id="d80fe-117">Die Daten, die derzeit vorhanden sind, werden beibehalten.</span><span class="sxs-lookup"><span data-stu-id="d80fe-117">It preserves the data that is currently there.</span></span> <span data-ttu-id="d80fe-118">Append gilt nicht für alle Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d80fe-118">Append is not applicable to all properties.</span></span>  <br/> |
|<span data-ttu-id="d80fe-119">Satz</span><span class="sxs-lookup"><span data-stu-id="d80fe-119">Set</span></span>  <br/> |<span data-ttu-id="d80fe-120">Die Set-Aktion ersetzt Daten für eine Eigenschaft, wenn Sie Daten enthält, oder erstellt die Eigenschaft und legt ihren Wert fest, wenn Sie nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d80fe-120">The set action replaces data for a property if it contains data, or creates the property and sets its value if it does not exist.</span></span> <span data-ttu-id="d80fe-121">Die Aktion festlegen gilt nur für schreibbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d80fe-121">The set action is only applicable to writable properties.</span></span>  <br/> |
|<span data-ttu-id="d80fe-122">Löschen</span><span class="sxs-lookup"><span data-stu-id="d80fe-122">Delete</span></span>  <br/> |<span data-ttu-id="d80fe-123">Die DELETE-Aktion entfernt eine Eigenschaft aus einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="d80fe-123">The delete action removes a property from a folder.</span></span> <span data-ttu-id="d80fe-124">Dies unterscheidet sich von der Einstellung auf einen leeren Wert.</span><span class="sxs-lookup"><span data-stu-id="d80fe-124">This is different than setting it to an empty value.</span></span> <span data-ttu-id="d80fe-125">Wenn dieser Vorgang abgeschlossen ist, ist die Eigenschaft für den Ordner nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d80fe-125">When complete, the property does not exist for the folder.</span></span> <span data-ttu-id="d80fe-126">DELETE gilt nur für schreibbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d80fe-126">Delete is only applicable to writable properties.</span></span>  <br/> |
   
## <a name="updatefolder-request-example"></a><span data-ttu-id="d80fe-127">UpdateFolder-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="d80fe-127">UpdateFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="d80fe-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d80fe-128">Description</span></span>

<span data-ttu-id="d80fe-129">Im folgenden Beispiel einer UpdateFolder-Anforderung wird gezeigt, wie ein Ordneranzeige Name aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d80fe-129">The following example of an UpdateFolder request shows how to update a folder display name.</span></span> 
  
### <a name="code"></a><span data-ttu-id="d80fe-130">Code</span><span class="sxs-lookup"><span data-stu-id="d80fe-130">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="d80fe-131">Comments</span><span class="sxs-lookup"><span data-stu-id="d80fe-131">Comments</span></span>

<span data-ttu-id="d80fe-132">In diesem Beispiel wird der Anzeigename des Ordners in "neuer FolderName" geändert.</span><span class="sxs-lookup"><span data-stu-id="d80fe-132">This example changes the display name of the folder to NewFolderName.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d80fe-133">Die Werte der Attribute **ID** und **ChangeKey** des [Folder](folderid.md) -Elements wurden zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="d80fe-133">The values of the **Id** and **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened for readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="d80fe-134">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="d80fe-134">Request elements</span></span>

<span data-ttu-id="d80fe-135">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="d80fe-135">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="d80fe-136">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="d80fe-136">UpdateFolder</span></span>](updatefolder.md)
    
- [<span data-ttu-id="d80fe-137">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="d80fe-137">FolderChanges</span></span>](folderchanges.md)
    
- [<span data-ttu-id="d80fe-138">FolderChange</span><span class="sxs-lookup"><span data-stu-id="d80fe-138">FolderChange</span></span>](folderchange.md)
    
- [<span data-ttu-id="d80fe-139">FolderId</span><span class="sxs-lookup"><span data-stu-id="d80fe-139">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="d80fe-140">Updates (Ordner)</span><span class="sxs-lookup"><span data-stu-id="d80fe-140">Updates (Folder)</span></span>](updates-folder.md)
    
- [<span data-ttu-id="d80fe-141">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="d80fe-141">SetFolderField</span></span>](setfolderfield.md)
    
- [<span data-ttu-id="d80fe-142">FieldURI</span><span class="sxs-lookup"><span data-stu-id="d80fe-142">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="d80fe-143">Ordner</span><span class="sxs-lookup"><span data-stu-id="d80fe-143">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="d80fe-144">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="d80fe-144">DisplayName (string)</span></span>](displayname-string.md)
    
<span data-ttu-id="d80fe-145">Weitere Elemente, die Sie zum Erstellen einer UpdateFolder-Anforderung verwenden können, finden Sie im Schema.</span><span class="sxs-lookup"><span data-stu-id="d80fe-145">See the schema for additional elements that you can use to form an UpdateFolder request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d80fe-146">Der Standardspeicherort des Schemas befindet sich im virtuellen Verzeichnis EWS auf dem Computer, auf dem die Client Zugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d80fe-146">The default location of the schema is in the EWS virtual directory on the computer that has the Client Access server role installed.</span></span> 
  
## <a name="updatefolder-response-example"></a><span data-ttu-id="d80fe-147">UpdateFolder-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="d80fe-147">UpdateFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="d80fe-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d80fe-148">Description</span></span>

<span data-ttu-id="d80fe-149">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die UpdateFolder-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d80fe-149">The following example shows a successful response to the UpdateFolder request.</span></span> <span data-ttu-id="d80fe-150">In diesem Beispiel wird der neue Änderungsschlüssel zurückgegeben, um den aktualisierten Status des Ordners widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="d80fe-150">In this example, the new change key is returned to reflect the updated status of the folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="d80fe-151">Code</span><span class="sxs-lookup"><span data-stu-id="d80fe-151">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UpdateFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="d80fe-152">Comments</span><span class="sxs-lookup"><span data-stu-id="d80fe-152">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="d80fe-153">Die Ordner-ID und der Change-Schlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d80fe-153">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="d80fe-154">Die in der Antwort zurückgegebene Ordner-ID stellt den aktualisierten Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="d80fe-154">The folder ID that is returned in the response represents the updated folder.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="d80fe-155">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="d80fe-155">Successful response elements</span></span>

<span data-ttu-id="d80fe-156">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="d80fe-156">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="d80fe-157">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d80fe-157">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="d80fe-158">UpdateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="d80fe-158">UpdateFolderResponse</span></span>](updatefolderresponse.md)
    
- [<span data-ttu-id="d80fe-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d80fe-159">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d80fe-160">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d80fe-160">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md)
    
- [<span data-ttu-id="d80fe-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d80fe-161">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d80fe-162">Ordner</span><span class="sxs-lookup"><span data-stu-id="d80fe-162">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="d80fe-163">Ordner</span><span class="sxs-lookup"><span data-stu-id="d80fe-163">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="d80fe-164">FolderId</span><span class="sxs-lookup"><span data-stu-id="d80fe-164">FolderId</span></span>](folderid.md)
    
## <a name="updatefolder-error-response-example"></a><span data-ttu-id="d80fe-165">UpdateFolder-Fehlerantwort Beispiel</span><span class="sxs-lookup"><span data-stu-id="d80fe-165">UpdateFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="d80fe-166">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d80fe-166">Description</span></span>

<span data-ttu-id="d80fe-167">Das folgende Beispiel zeigt eine Fehlerantwort auf eine UpdateFolder-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d80fe-167">The following example shows an error response to an UpdateFolder request.</span></span>
  
### <a name="code"></a><span data-ttu-id="d80fe-168">Code</span><span class="sxs-lookup"><span data-stu-id="d80fe-168">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UpdateFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="d80fe-169">Comments</span><span class="sxs-lookup"><span data-stu-id="d80fe-169">Comments</span></span>

<span data-ttu-id="d80fe-170">Dieses Beispiel zeigt eine Fehlerantwort, die durch ein ungültiges **ChangeKey** -Attribut in der Anforderung verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="d80fe-170">This example shows an error response that is caused by an invalid **ChangeKey** attribute in the request.</span></span> 
  
### <a name="error-response-elements"></a><span data-ttu-id="d80fe-171">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="d80fe-171">Error response elements</span></span>

<span data-ttu-id="d80fe-172">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="d80fe-172">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="d80fe-173">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d80fe-173">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="d80fe-174">UpdateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="d80fe-174">UpdateFolderResponse</span></span>](updatefolderresponse.md)
    
- [<span data-ttu-id="d80fe-175">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d80fe-175">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d80fe-176">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d80fe-176">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md)
    
- [<span data-ttu-id="d80fe-177">MessageText</span><span class="sxs-lookup"><span data-stu-id="d80fe-177">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="d80fe-178">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d80fe-178">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d80fe-179">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d80fe-179">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="d80fe-180">Ordner</span><span class="sxs-lookup"><span data-stu-id="d80fe-180">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="d80fe-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d80fe-181">See also</span></span>



- [<span data-ttu-id="d80fe-182">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d80fe-182">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

