---
title: GetSharingFolder-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingFolder
api_type:
- schema
ms.assetid: 75fee92a-a7f8-4a62-ad2b-17acbaada186
description: Der GetSharingFolder-Vorgang ruft den lokalen Ordner Bezeichner eines angegebenen freigegebenen Ordners ab.
ms.openlocfilehash: cf66eb390b0287e89bb8402f26a2e728868a2b18
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460512"
---
# <a name="getsharingfolder-operation"></a><span data-ttu-id="5e98b-103">GetSharingFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5e98b-103">GetSharingFolder operation</span></span>

<span data-ttu-id="5e98b-104">Der **GetSharingFolder** -Vorgang ruft den lokalen Ordner Bezeichner eines angegebenen freigegebenen Ordners ab.</span><span class="sxs-lookup"><span data-stu-id="5e98b-104">The **GetSharingFolder** operation gets the local folder identifier of a specified shared folder.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="5e98b-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="5e98b-105">SOAP Headers</span></span>

<span data-ttu-id="5e98b-106">Der **GetSharingFolder** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt und beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="5e98b-106">The **GetSharingFolder** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="5e98b-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="5e98b-107">**Header**</span></span>|<span data-ttu-id="5e98b-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="5e98b-108">**Element**</span></span>|<span data-ttu-id="5e98b-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5e98b-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5e98b-110">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="5e98b-110">RequestVersion</span></span>  <br/> |[<span data-ttu-id="5e98b-111">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="5e98b-111">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="5e98b-112">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="5e98b-112">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="5e98b-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="5e98b-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="5e98b-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5e98b-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="5e98b-115">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="5e98b-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getsharingfolder-request-example"></a><span data-ttu-id="5e98b-116">GetSharingFolder-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="5e98b-116">GetSharingFolder request example</span></span>

### <a name="getting-the-local-folder-identifier-by-specifying-the-sharedfolderid-element-of-the-folder-being-shared"></a><span data-ttu-id="5e98b-117">Aufrufen der lokalen Ordner-ID durch Angabe des SharedFolderId-Elements des freigegebenen Ordners</span><span class="sxs-lookup"><span data-stu-id="5e98b-117">Getting the Local Folder Identifier by Specifying the SharedFolderId Element of the Folder Being Shared</span></span>

<span data-ttu-id="5e98b-118">Im folgenden Codebeispiel wird gezeigt, wie eine Anforderung zum Abrufen des Bezeichners des lokalen Ordners erstellt wird, der dem freizugebenden Ordner entspricht.</span><span class="sxs-lookup"><span data-stu-id="5e98b-118">The following code example shows how to form a request to get the identifier of the local folder that corresponds to the folder that is being shared.</span></span> <span data-ttu-id="5e98b-119">Der freigegebene Ordner wird durch die SMTP-Adresse des Postfachs identifiziert, das den freizugebenden Ordner und das [SharedFolderId](sharedfolderid.md) -Element enthält, das den Bezeichner dieses Ordners darstellt.</span><span class="sxs-lookup"><span data-stu-id="5e98b-119">The folder that is being shared is identified by the SMTP address of the mailbox that contains the folder that is being shared and by the [SharedFolderId](sharedfolderid.md) element that represents the identifier of that folder.</span></span> <span data-ttu-id="5e98b-120">In diesem Beispiel befindet sich der Ordner, der freigegeben wird, im Besitz von user1@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="5e98b-120">In this example, the folder that is being shared is owned by user1@contoso.com.</span></span> 
  
### <a name="code"></a><span data-ttu-id="5e98b-121">Code</span><span class="sxs-lookup"><span data-stu-id="5e98b-121">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <m:GetSharingFolder>
      <m:SmtpAddress>user1@contoso.com</m:SmtpAddress>
      <m:SharedFolderId>AAMkA=</m:SharedFolderId>
    </m:GetSharingFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="getting-the-local-folder-identifier-by-specifying-the-datatype-element-of-the-folder-being-shared"></a><span data-ttu-id="5e98b-122">Aufrufen der lokalen Ordner-ID durch Angabe des DataType-Elements des freigegebenen Ordners</span><span class="sxs-lookup"><span data-stu-id="5e98b-122">Getting the Local Folder Identifier by Specifying the DataType Element of the Folder Being Shared</span></span>

<span data-ttu-id="5e98b-123">Im folgenden Codebeispiel wird gezeigt, wie eine Anforderung zum Abrufen des Bezeichners des lokalen Ordners erstellt wird, der dem freizugebenden Ordner entspricht.</span><span class="sxs-lookup"><span data-stu-id="5e98b-123">The following code example shows how to form a request to get the identifier of the local folder that corresponds to the folder that is being shared.</span></span> <span data-ttu-id="5e98b-124">Der freigegebene Ordner wird durch die SMTP-Adresse des Postfachs identifiziert, das den freizugebenden Ordner und das [DataType](datatype.md) -Element enthält, das den Typ der Daten in diesem Ordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="5e98b-124">The folder that is being shared is identified by the SMTP address of the mailbox that contains the folder that is being shared and by the [DataType](datatype.md) element that represents the type of data in that folder.</span></span> <span data-ttu-id="5e98b-125">In diesem Beispiel ist der Ordner, der freigegeben wird, der Ordner Kontakte, der user1@contoso.com gehört.</span><span class="sxs-lookup"><span data-stu-id="5e98b-125">In this example, the folder that is being shared is the Contacts folder that is owned by user1@contoso.com.</span></span> 
  
### <a name="code"></a><span data-ttu-id="5e98b-126">Code</span><span class="sxs-lookup"><span data-stu-id="5e98b-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <m:GetSharingFolder>
      <m:SmtpAddress>user1@contoso.com</m:SmtpAddress>
      <m:DataType>Contacts</m:DataType>
    </m:GetSharingFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="5e98b-127">Comments</span><span class="sxs-lookup"><span data-stu-id="5e98b-127">Comments</span></span>

<span data-ttu-id="5e98b-128">Informationen zu den möglichen Werten des **DataType** -Elements finden Sie unter [DataType](datatype.md).</span><span class="sxs-lookup"><span data-stu-id="5e98b-128">For information about the possible values of the **DataType** element, see [DataType](datatype.md).</span></span>
  
## <a name="successful-getsharingfolder-response"></a><span data-ttu-id="5e98b-129">Erfolgreiche GetSharingFolder-Antwort</span><span class="sxs-lookup"><span data-stu-id="5e98b-129">Successful GetSharingFolder Response</span></span>

### <a name="description"></a><span data-ttu-id="5e98b-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e98b-130">Description</span></span>

<span data-ttu-id="5e98b-131">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetSharingFolder** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5e98b-131">The following example shows a successful response to a **GetSharingFolder** request.</span></span> <span data-ttu-id="5e98b-132">Das **ID-** Attribut des [SharingFolderId](sharingfolderid.md) -Elements stellt den Bezeichner des lokalen Ordners in der Freigabebeziehung dar.</span><span class="sxs-lookup"><span data-stu-id="5e98b-132">The **Id** attribute of the [SharingFolderId](sharingfolderid.md) element represents the identifier of the local folder in the sharing relationship.</span></span> 
  
### <a name="code"></a><span data-ttu-id="5e98b-133">Code</span><span class="sxs-lookup"><span data-stu-id="5e98b-133">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingFolderResponseMessage ResponseClass="Success"
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:SharingFolderId Id="AAMkAD=" ChangeKey="AwAAA=" />
    </GetSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

## <a name="getsharingfolder-error-response"></a><span data-ttu-id="5e98b-134">GetSharingFolder-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="5e98b-134">GetSharingFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="5e98b-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e98b-135">Description</span></span>

<span data-ttu-id="5e98b-136">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **GetSharingFolder** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5e98b-136">The following example shows an error response to a **GetSharingFolder** request.</span></span> <span data-ttu-id="5e98b-137">In diesem Beispiel ist der Fehler aufgetreten, da die Anforderung sowohl die [SharingFolderId](sharingfolderid.md) -als auch die [DataType](datatype.md) -Elemente angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="5e98b-137">In this example, the error occurred because the request specified both the [SharingFolderId](sharingfolderid.md) and [DataType](datatype.md) elements.</span></span> <span data-ttu-id="5e98b-138">Beachten Sie, dass nur das eine oder andere dieser beiden Elemente angegeben werden kann, jedoch nicht beides.</span><span class="sxs-lookup"><span data-stu-id="5e98b-138">Note that only one or the other of those two elements can be specified, but not both.</span></span> 
  
### <a name="code"></a><span data-ttu-id="5e98b-139">Code</span><span class="sxs-lookup"><span data-stu-id="5e98b-139">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingFolderResponseMessage ResponseClass="Error" 
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:MessageText>Either DataType or SharedFolderId must be specified, but not both.</m:MessageText>
      <m:ResponseCode>ErrorInvalidGetSharingFolderRequest</m:ResponseCode>
      <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
    </GetSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="5e98b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e98b-140">See also</span></span>



[<span data-ttu-id="5e98b-141">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="5e98b-141">GetSharingFolder</span></span>](getsharingfolder.md)
  
[<span data-ttu-id="5e98b-142">GetSharingFolderType</span><span class="sxs-lookup"><span data-stu-id="5e98b-142">GetSharingFolderType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingFolderType.aspx)
  
[<span data-ttu-id="5e98b-143">GetSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5e98b-143">GetSharingFolderResponseMessage</span></span>](getsharingfolderresponsemessage.md)
  
[<span data-ttu-id="5e98b-144">GetSharingFolderResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="5e98b-144">GetSharingFolderResponseMessageType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingFolderResponseMessageType.aspx)


[<span data-ttu-id="5e98b-145">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="5e98b-145">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="5e98b-146">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5e98b-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

