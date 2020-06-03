---
title: GetUserPhoto-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e
description: Hier finden Sie Informationen zum GetUserPhoto-EWS-Vorgang.
ms.openlocfilehash: 6769842d31519f0aac2cf9bda10c1cab70558301
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461814"
---
# <a name="getuserphoto-operation"></a><span data-ttu-id="526d4-103">GetUserPhoto-Vorgang</span><span class="sxs-lookup"><span data-stu-id="526d4-103">GetUserPhoto operation</span></span>

<span data-ttu-id="526d4-104">Hier finden Sie Informationen zum **GetUserPhoto** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="526d4-104">Find information about the **GetUserPhoto** EWS operation.</span></span> 
  
<span data-ttu-id="526d4-105">Der **GetUserPhoto** -Vorgang ruft ein Benutzer Foto aus Active Directory-Domänendienste (AD DS) ab.</span><span class="sxs-lookup"><span data-stu-id="526d4-105">The **GetUserPhoto** operation gets a user photo from Active Directory Domain Services (AD DS).</span></span> 
  
<span data-ttu-id="526d4-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="526d4-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getuserphoto-operation"></a><span data-ttu-id="526d4-107">Verwenden des GetUserPhoto-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="526d4-107">Using the GetUserPhoto operation</span></span>

<span data-ttu-id="526d4-108">Der **RemoveContactFromImList** -Vorgang ist ein einfacher Vorgang, der die e-Mail-Adresse eines Benutzers und das angeforderte Fotoformat akzeptiert und den Fotostream in der Antwort zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="526d4-108">The **RemoveContactFromImList** operation is a simple operation that accepts a user's email address and the requested photo size and returns the photo stream in the response.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="526d4-109">EWS verfügt sowohl über einen SOAP-als auch einen Rest-basierten Vorgang, um Benutzer Fotos zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="526d4-109">EWS has both a SOAP and a REST-based operation to get user photos.</span></span> <span data-ttu-id="526d4-110">Informationen zur Rest-Schnittstelle finden Sie unter [Abrufen von Benutzer Fotos mithilfe von EWS in Exchange](https://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="526d4-110">For information about the REST interface, see [Get user photos by using EWS in Exchange](https://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx).</span></span> 
  
### <a name="getuserphoto-operation-soap-headers"></a><span data-ttu-id="526d4-111">SOAP-Header des GetUserPhoto-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="526d4-111">GetUserPhoto operation SOAP headers</span></span>

<span data-ttu-id="526d4-112">Der **GetUserPhoto** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="526d4-112">The **GetUserPhoto** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="526d4-113">**Headername**</span><span class="sxs-lookup"><span data-stu-id="526d4-113">**Header name**</span></span>|<span data-ttu-id="526d4-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="526d4-114">**Element**</span></span>|<span data-ttu-id="526d4-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="526d4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="526d4-116">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="526d4-116">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="526d4-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="526d4-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="526d4-118">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="526d4-118">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="526d4-119">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="526d4-119">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="526d4-120">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="526d4-120">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="526d4-121">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="526d4-121">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="526d4-122">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="526d4-122">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="526d4-123">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="526d4-123">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getuserphoto-operation-request-example-get-a-users-photo"></a><span data-ttu-id="526d4-124">GetUserPhoto-Vorgangs Anforderungs Beispiel: Abrufen eines Benutzer Fotos</span><span class="sxs-lookup"><span data-stu-id="526d4-124">GetUserPhoto operation request example: Get a user's photo</span></span>

<span data-ttu-id="526d4-125">Im folgenden Beispiel einer **GetUserPhoto** -Vorgangsanforderung wird gezeigt, wie das Foto eines Benutzers abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="526d4-125">The following example of a **GetUserPhoto** operation request shows how to get a user's photo.</span></span> <span data-ttu-id="526d4-126">In diesem Beispiel wird ein Benutzer Foto angefordert, bei dem es sich um 48x48 Pixel handelt.</span><span class="sxs-lookup"><span data-stu-id="526d4-126">This example requests a user photo that is 48x48 pixels.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013"/>
   </soap:Header>
   <soap:Body>
      <m:GetUserPhoto>
         <m:Email>user1@contoso.com</m:Email>
         <m:SizeRequested>HR48x48</m:SizeRequested>
      </m:GetUserPhoto>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="526d4-127">Die folgenden Elemente werden im SOAP-Anforderungstext Körper verwendet:</span><span class="sxs-lookup"><span data-stu-id="526d4-127">The following elements are used in the request SOAP body:</span></span>
  
- [<span data-ttu-id="526d4-128">GetUserPhoto</span><span class="sxs-lookup"><span data-stu-id="526d4-128">GetUserPhoto</span></span>](getuserphoto.md)
    
- [<span data-ttu-id="526d4-129">E-Mail (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="526d4-129">Email (String)</span></span>](email-string.md)
    
- [<span data-ttu-id="526d4-130">SizeRequested</span><span class="sxs-lookup"><span data-stu-id="526d4-130">SizeRequested</span></span>](sizerequested.md)
    
## <a name="successful-getuserphoto-operation-response"></a><span data-ttu-id="526d4-131">Erfolgreiche Reaktion des GetUserPhoto-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="526d4-131">Successful GetUserPhoto operation response</span></span>

<span data-ttu-id="526d4-132">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf einen **GetUserPhoto** -Vorgang, um das Foto eines Benutzers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="526d4-132">The following example shows a successful response to a **GetUserPhoto** operation to get a user's photo.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetUserPhotoResponse ResponseClass="Success" 
                            xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <HasChanged>true</HasChanged>
         <PictureData>/9j/4AAQSkZJRgABAQEAYABgAAD/02</PictureData>
      </GetUserPhotoResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="526d4-133">Die folgenden Elemente werden im SOAP-Antworttext Körper verwendet:</span><span class="sxs-lookup"><span data-stu-id="526d4-133">The following elements are used in the response SOAP body:</span></span>
  
- [<span data-ttu-id="526d4-134">GetUserPhotoResponse</span><span class="sxs-lookup"><span data-stu-id="526d4-134">GetUserPhotoResponse</span></span>](getuserphotoresponse.md)
    
- [<span data-ttu-id="526d4-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="526d4-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="526d4-136">HasChanged</span><span class="sxs-lookup"><span data-stu-id="526d4-136">HasChanged</span></span>](haschanged.md)
    
- [<span data-ttu-id="526d4-137">GetUserPhotoResponse</span><span class="sxs-lookup"><span data-stu-id="526d4-137">GetUserPhotoResponse</span></span>](getuserphotoresponse.md)
    
## <a name="getuserphoto-operation-error-response"></a><span data-ttu-id="526d4-138">Fehlerantwort des GetUserPhoto-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="526d4-138">GetUserPhoto operation error response</span></span>

<span data-ttu-id="526d4-139">Der SOAP-Umschlag gibt keinen Fehlercode zurück, wenn versucht wird, ein Benutzer Foto für eine e-Mail-Adresse abzurufen, die in der Organisation nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="526d4-139">The SOAP envelope will not return an error code if an attempt is made to get a user photo for an email address that doesn't exist in the organization.</span></span> <span data-ttu-id="526d4-140">Ein 500-HTTP-Statuscode wird in der Antwort zurückgegeben, um anzugeben, dass die Anforderung nicht erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="526d4-140">A 500 HTTP status code will be returned in the response to indicate that the request was unsuccessful.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="526d4-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="526d4-141">See also</span></span>

- [<span data-ttu-id="526d4-142">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="526d4-142">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)   
- [<span data-ttu-id="526d4-143">Abrufen von Benutzerfotos mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="526d4-143">Get user photos by using EWS in Exchange</span></span>](https://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx)
    

