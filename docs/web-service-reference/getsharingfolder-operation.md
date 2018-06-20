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
description: Der Vorgang GetSharingFolder Ruft den lokalen Ordner Bezeichner eines angegebenen freigegebenen Ordners ab.
ms.openlocfilehash: 23adb10b22623fcbc1dd6b33bd674afafdaa8b19
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829670"
---
# <a name="getsharingfolder-operation"></a><span data-ttu-id="21ef0-103">GetSharingFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="21ef0-103">GetSharingFolder operation</span></span>

<span data-ttu-id="21ef0-104">Der Vorgang **GetSharingFolder** Ruft den lokalen Ordner Bezeichner eines angegebenen freigegebenen Ordners ab.</span><span class="sxs-lookup"><span data-stu-id="21ef0-104">The **GetSharingFolder** operation gets the local folder identifier of a specified shared folder.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="21ef0-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="21ef0-105">SOAP Headers</span></span>

<span data-ttu-id="21ef0-106">Der Vorgang **GetSharingFolder** können die SOAP-Header, die aufgeführt und in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="21ef0-106">The **GetSharingFolder** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="21ef0-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="21ef0-107">**Header**</span></span>|<span data-ttu-id="21ef0-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="21ef0-108">**Element**</span></span>|<span data-ttu-id="21ef0-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="21ef0-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="21ef0-110">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="21ef0-110">RequestVersion</span></span>  <br/> |[<span data-ttu-id="21ef0-111">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="21ef0-111">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="21ef0-112">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="21ef0-112">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="21ef0-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="21ef0-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="21ef0-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="21ef0-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="21ef0-115">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="21ef0-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getsharingfolder-request-example"></a><span data-ttu-id="21ef0-116">Anforderungsbeispiel GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="21ef0-116">GetSharingFolder request example</span></span>

### <a name="getting-the-local-folder-identifier-by-specifying-the-sharedfolderid-element-of-the-folder-being-shared"></a><span data-ttu-id="21ef0-117">Abrufen des lokalen Ordner Bezeichners durch das SharedFolderId-Element des freigegebenen Ordners angeben</span><span class="sxs-lookup"><span data-stu-id="21ef0-117">Getting the Local Folder Identifier by Specifying the SharedFolderId Element of the Folder Being Shared</span></span>

<span data-ttu-id="21ef0-118">Im folgenden Codebeispiel wird veranschaulicht, wie auf eine Anforderung an den Bezeichner der den lokalen Ordner, der entspricht in dem Ordner abrufen, die gegenwärtig freigegebenen bilden.</span><span class="sxs-lookup"><span data-stu-id="21ef0-118">The following code example shows how to form a request to get the identifier of the local folder that corresponds to the folder that is being shared.</span></span> <span data-ttu-id="21ef0-119">Der Ordner, der gegenwärtig freigegebenen wird identifiziert, durch die SMTP-Adresse des Postfachs an, die den Ordner enthält, der gemeinsam genutzt werden und das [SharedFolderId](sharedfolderid.md) -Element, das den Bezeichner des Ordners darstellt.</span><span class="sxs-lookup"><span data-stu-id="21ef0-119">The folder that is being shared is identified by the SMTP address of the mailbox that contains the folder that is being shared and by the [SharedFolderId](sharedfolderid.md) element that represents the identifier of that folder.</span></span> <span data-ttu-id="21ef0-120">In diesem Beispiel gehört user1@contoso.com der Ordner, der freigegeben ist.</span><span class="sxs-lookup"><span data-stu-id="21ef0-120">In this example, the folder that is being shared is owned by user1@contoso.com.</span></span> 
  
### <a name="code"></a><span data-ttu-id="21ef0-121">Code</span><span class="sxs-lookup"><span data-stu-id="21ef0-121">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="getting-the-local-folder-identifier-by-specifying-the-datatype-element-of-the-folder-being-shared"></a><span data-ttu-id="21ef0-122">Abrufen des lokalen Ordner Bezeichners durch Angeben der DataType-Element des freigegebenen Ordners</span><span class="sxs-lookup"><span data-stu-id="21ef0-122">Getting the Local Folder Identifier by Specifying the DataType Element of the Folder Being Shared</span></span>

<span data-ttu-id="21ef0-123">Im folgenden Codebeispiel wird veranschaulicht, wie auf eine Anforderung an den Bezeichner der den lokalen Ordner, der entspricht in dem Ordner abrufen, die gegenwärtig freigegebenen bilden.</span><span class="sxs-lookup"><span data-stu-id="21ef0-123">The following code example shows how to form a request to get the identifier of the local folder that corresponds to the folder that is being shared.</span></span> <span data-ttu-id="21ef0-124">Der Ordner, der gegenwärtig freigegebenen wird identifiziert, durch die SMTP-Adresse des Postfachs an, die den Ordner enthält, der gemeinsam genutzt werden und die [DataType](datatype.md) -Element, das den Typ der Daten in diesem Ordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="21ef0-124">The folder that is being shared is identified by the SMTP address of the mailbox that contains the folder that is being shared and by the [DataType](datatype.md) element that represents the type of data in that folder.</span></span> <span data-ttu-id="21ef0-125">In diesem Beispiel ist der Ordner, der gegenwärtig freigegebenen Ordner Kontakte, der Besitzer user1@contoso.com ist.</span><span class="sxs-lookup"><span data-stu-id="21ef0-125">In this example, the folder that is being shared is the Contacts folder that is owned by user1@contoso.com.</span></span> 
  
### <a name="code"></a><span data-ttu-id="21ef0-126">Code</span><span class="sxs-lookup"><span data-stu-id="21ef0-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="21ef0-127">Kommentare</span><span class="sxs-lookup"><span data-stu-id="21ef0-127">Comments</span></span>

<span data-ttu-id="21ef0-128">Informationen zu den möglichen Werten des **DataType** -Elements finden Sie unter [DataType](datatype.md).</span><span class="sxs-lookup"><span data-stu-id="21ef0-128">For information about the possible values of the **DataType** element, see [DataType](datatype.md).</span></span>
  
## <a name="successful-getsharingfolder-response"></a><span data-ttu-id="21ef0-129">Erfolgreiche GetSharingFolder Antwort</span><span class="sxs-lookup"><span data-stu-id="21ef0-129">Successful GetSharingFolder Response</span></span>

### <a name="description"></a><span data-ttu-id="21ef0-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21ef0-130">Description</span></span>

<span data-ttu-id="21ef0-131">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **GetSharingFolder** .</span><span class="sxs-lookup"><span data-stu-id="21ef0-131">The following example shows a successful response to a **GetSharingFolder** request.</span></span> <span data-ttu-id="21ef0-132">Das **Id** -Attribut des Elements [SharingFolderId](sharingfolderid.md) stellt den Bezeichner des lokalen Ordner in die Beziehung.</span><span class="sxs-lookup"><span data-stu-id="21ef0-132">The **Id** attribute of the [SharingFolderId](sharingfolderid.md) element represents the identifier of the local folder in the sharing relationship.</span></span> 
  
### <a name="code"></a><span data-ttu-id="21ef0-133">Code</span><span class="sxs-lookup"><span data-stu-id="21ef0-133">Code</span></span>

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
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingFolderResponseMessage ResponseClass="Success"
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:SharingFolderId Id="AAMkAD=" ChangeKey="AwAAA=" />
    </GetSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

## <a name="getsharingfolder-error-response"></a><span data-ttu-id="21ef0-134">Fehlerantwort GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="21ef0-134">GetSharingFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="21ef0-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21ef0-135">Description</span></span>

<span data-ttu-id="21ef0-136">Das folgende Beispiel zeigt eine Fehlerantwort an eine **GetSharingFolder** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="21ef0-136">The following example shows an error response to a **GetSharingFolder** request.</span></span> <span data-ttu-id="21ef0-137">In diesem Beispiel wird der Fehler aufgetreten ist, da die Anforderung der [SharingFolderId](sharingfolderid.md) und die [DataType](datatype.md) -Elements angegeben.</span><span class="sxs-lookup"><span data-stu-id="21ef0-137">In this example, the error occurred because the request specified both the [SharingFolderId](sharingfolderid.md) and [DataType](datatype.md) elements.</span></span> <span data-ttu-id="21ef0-138">Beachten Sie, dass nur ein oder andere dieser zwei Elemente, jedoch nicht beide angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="21ef0-138">Note that only one or the other of those two elements can be specified, but not both.</span></span> 
  
### <a name="code"></a><span data-ttu-id="21ef0-139">Code</span><span class="sxs-lookup"><span data-stu-id="21ef0-139">Code</span></span>

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
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingFolderResponseMessage ResponseClass="Error" 
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:MessageText>Either DataType or SharedFolderId must be specified, but not both.</m:MessageText>
      <m:ResponseCode>ErrorInvalidGetSharingFolderRequest</m:ResponseCode>
      <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
    </GetSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="21ef0-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21ef0-140">See also</span></span>



[<span data-ttu-id="21ef0-141">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="21ef0-141">GetSharingFolder</span></span>](getsharingfolder.md)
  
[<span data-ttu-id="21ef0-142">GetSharingFolderType</span><span class="sxs-lookup"><span data-stu-id="21ef0-142">GetSharingFolderType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingFolderType.aspx)
  
[<span data-ttu-id="21ef0-143">GetSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="21ef0-143">GetSharingFolderResponseMessage</span></span>](getsharingfolderresponsemessage.md)
  
[<span data-ttu-id="21ef0-144">GetSharingFolderResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="21ef0-144">GetSharingFolderResponseMessageType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingFolderResponseMessageType.aspx)


[<span data-ttu-id="21ef0-145">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="21ef0-145">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="21ef0-146">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="21ef0-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

