---
title: Abrufen von benutzerfotos mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f86d1099-1f57-47dc-abf2-4d5ae4e900a9
description: Erfahren Sie, wie Sie Benutzerfotos abrufen können, die mit einem Postfach oder einem Kontakt verknüpft sind, indem Sie die verwaltete EWS-API oder EWS in Exchange verwenden.
ms.openlocfilehash: f0f5cddd41fc563fb9ed38e75b505830a3992411
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756929"
---
# <a name="get-user-photos-by-using-ews-in-exchange"></a><span data-ttu-id="9c634-103">Abrufen von benutzerfotos mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="9c634-103">Get user photos by using EWS in Exchange</span></span>

<span data-ttu-id="9c634-104">Erfahren Sie, wie Sie Benutzerfotos abrufen können, die mit einem Postfach oder einem Kontakt verknüpft sind, indem Sie die verwaltete EWS-API oder EWS in Exchange verwenden.</span><span class="sxs-lookup"><span data-stu-id="9c634-104">Learn how to get user photos that are associated with a mailbox or contact by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="9c634-p101">Es ist schön, einem Namen ein Gesicht zuordnen zu können. Wenn Ihre Benutzer Namen Gesichter zuordnen möchten, kann Ihre Anwendung ein Bild von Exchange anfordern, in der Regel ein Foto, das ein E-Mail-Konto darstellt. Sie können Ein Benutzerfoto abrufen, das auf einem Exchange-Server für ein Postfach gespeichert ist oder ein Kontaktfoto aus den im Postfach gespeicherten Kontakten abrufen.</span><span class="sxs-lookup"><span data-stu-id="9c634-p101">It's nice to put a face to a name. If your users like to put names to faces, your application can request an image, typically a photo, from Exchange that represents an email account. You can get a user photo stored on an Exchange server for a mailbox, or you can get a contact photo from contacts stored in your mailbox.</span></span>
  
<span data-ttu-id="9c634-p102">Zum Abrufen von Fotos aus Postfächern oder den Active Directory-Domänendiensten (AD DS) abrufen. Die optimale Option zum Abrufen eines Fotos hängt von der Art des Kontakts ab, von dem Sie ein Foto abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="9c634-p102">You can use several different technologies to get photos from mailboxes or Active Directory Domain Services (AD DS). The best way to get a photo depends on the type of contact that you want to get a photo from.</span></span> 
  
<span data-ttu-id="9c634-110">**Tabelle 1. Technologien zum Abrufen von Benutzerfotos auf Grundlage des Kontakttyps**</span><span class="sxs-lookup"><span data-stu-id="9c634-110">**Table 1. Technologies to use to get user photos based on contact type**</span></span>

|<span data-ttu-id="9c634-111">**Kontakttyp**</span><span class="sxs-lookup"><span data-stu-id="9c634-111">**Contact type**</span></span>|<span data-ttu-id="9c634-112">**Zu verwendende Technologie**</span><span class="sxs-lookup"><span data-stu-id="9c634-112">**Technologies to use**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9c634-113">Postfach-Benutzerfoto</span><span class="sxs-lookup"><span data-stu-id="9c634-113">Mailbox user photo</span></span>  <br/> |[<span data-ttu-id="9c634-114">Abrufen eines Postfach-Benutzerfotos mithilfe von REST</span><span class="sxs-lookup"><span data-stu-id="9c634-114">Get a mailbox user photo by using REST</span></span>](#bk_REST)<br/><br/> [<span data-ttu-id="9c634-115">Abrufen einer benutzerfoto mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="9c634-115">Get a user photo by using EWS</span></span>](#bk_EWS) <br/> |
|<span data-ttu-id="9c634-116">Kontakt-Benutzerfoto</span><span class="sxs-lookup"><span data-stu-id="9c634-116">Contact user photo</span></span>  <br/> |[<span data-ttu-id="9c634-117">Rufen Sie ein benutzerfoto des Kontakts mithilfe der EWS Managed API ab</span><span class="sxs-lookup"><span data-stu-id="9c634-117">Get a contact user photo by using EWS Managed API</span></span>](#bk_EWSMA)<br/><br/> [<span data-ttu-id="9c634-118">Abrufen einer benutzerfoto mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="9c634-118">Get a user photo by using EWS</span></span>](#bk_EWS) <br/> |

<span data-ttu-id="9c634-119"><a name="bk_REST"> </a></span><span class="sxs-lookup"><span data-stu-id="9c634-119"></span></span>

## <a name="get-a-mailbox-user-photo-by-using-rest"></a><span data-ttu-id="9c634-120">Abrufen eines Postfach-Benutzerfotos mithilfe von REST</span><span class="sxs-lookup"><span data-stu-id="9c634-120">Get a mailbox user photo by using REST</span></span>

<span data-ttu-id="9c634-p103">Sie können Benutzerfotos von einem Exchange-Server mit einer standardmäßigen HTTPS- **GET**-Anforderung abrufen. Geben Sie in der Anforderung die E-Mail-Kontoadresse und einen Größencode für das Bild an, wie im folgenden Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="9c634-p103">You can request user photos from an Exchange server by using a standard HTTPS **GET** request. In the request, specify the email account address and a size code for the image, as shown in the following example.</span></span> 
  
```HTML
https://Exchange Server/ews/Exchange.asmx/s/GetUserPhoto?email=email address&amp;size=size code
```

<span data-ttu-id="9c634-123">Verwenden Sie den AutoErmittlungsdienst-[GetUserSettings](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)-Vorgang, um die **ExternalEwsUrl**-Einstellung abzurufen, die die URL des Endpunkts der Exchange-Webdienste (EWS) und den Speicherort des **Exchange.asmx** HTTP-Handlers, der die Benutzerfotos zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9c634-123">Use the Autodiscover service [GetUserSettings](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) operation to retrieve the **ExternalEwsUrl** setting, which contains the URL of the Exchange Web Services (EWS) endpoint and the location of the **Exchange.asmx** HTTP handler that returns the user photos.</span></span> 
  
<span data-ttu-id="9c634-p104">In den Größencodes wird die Höhe und Breite des Bilds in Pixel angegeben. Der Größencode **HR48x48** gibt beispielsweise ein Bild zurück, das 48 Pixel hoch und 48 Pixel breit ist. Die möglichen Werte für den Größencodeparameter entsprechen den möglichen Werten für das [SizeRequested](http://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx)-Element. Wenn die Anforderung eine nicht verfügbare Größe angibt, wird das größtmögliche Foto zurückgegeben. Wenn kein Foto auf dem Exchange-Server gespeichert ist, wird das in AD DS für das Konto gespeicherte Bild zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c634-p104">Each size code indicates the height and width of the image in pixels. For example, the size code **HR48x48** returns an image that is 48 pixels high by 48 pixels wide. The possible values for the size code parameter are the same as the possible values for the [SizeRequested](http://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx) element. If the request specifies a size that is not available, the largest available photo will be returned. If no photo is stored on the Exchange server, the thumbnail image stored in AD DS for the account will be returned.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9c634-129">[!HINWEIS] Der **HR48x48**-Größencode gibt immer das AD DS-Vorschaubild zurück, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9c634-129">The **HR48x48** size code always returns the AD DS thumbnail image if it is available.</span></span> 
  
<span data-ttu-id="9c634-130">Im folgenden Beispiel wird veranschaulicht, wie Sie die GET-Anforderung verwenden können, um das Benutzerfoto für Sadie abzurufen und auf Ihrem lokalen Computer zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9c634-130">The following example shows how you can use the GET request to retrieve the user photo for Sadie and save it to your local computer.</span></span>
  
```cs
// Create the web request with the REST URL.
HttpWebRequest request = 
   WebRequest.Create("https://www.contoso.com/ews/exchange.asmx/s/GetUserPhoto?email=sadie@contoso.com&amp;size=HR240x240") 
   as HttpWebRequest;
// Submit the request.
using (HttpWebResponse resp = request.GetResponse() as HttpWebResponse)
{
   // Take the response and save it as an image.
   Bitmap image = new Bitmap(resp.GetResponseStream());
   image.Save("Sadie.jpg");
}

```

<span data-ttu-id="9c634-131">Die Anforderung gibt eine HTTP-Antwort zurück.</span><span class="sxs-lookup"><span data-stu-id="9c634-131">The request will return an HTTP response.</span></span> 
  
<span data-ttu-id="9c634-132">**Tabelle 2. Antwortcodes für eine GetUserPhoto-Anforderung**</span><span class="sxs-lookup"><span data-stu-id="9c634-132">**Table 2. Response codes for a GetUserPhoto request**</span></span>

|<span data-ttu-id="9c634-133">**Antwortcode**</span><span class="sxs-lookup"><span data-stu-id="9c634-133">**Response code**</span></span>|<span data-ttu-id="9c634-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9c634-134">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9c634-135">200</span><span class="sxs-lookup"><span data-stu-id="9c634-135">200</span></span>  <br/> |<span data-ttu-id="9c634-136">Für das angegebene E-Mail-Konto ist ein Bild verfügbar und das binäre Bild ist in der Antwort enthalten.</span><span class="sxs-lookup"><span data-stu-id="9c634-136">An image is available for the specified email account and the binary image is contained in the response.</span></span>  <br/> |
|<span data-ttu-id="9c634-137">304</span><span class="sxs-lookup"><span data-stu-id="9c634-137">304</span></span>  <br/> |<span data-ttu-id="9c634-138">Das Bild hat sich seit der letzten **ETag**-Rückgabe an die Anwendung nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="9c634-138">The image has not changed since the last time the **ETag** was returned to the application.</span></span>  <br/> |
|<span data-ttu-id="9c634-139">404</span><span class="sxs-lookup"><span data-stu-id="9c634-139">404</span></span>  <br/> |<span data-ttu-id="9c634-140">Für das angegebene E-Mail-Konto ist kein Bild verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9c634-140">No image is available for the specified email account.</span></span>  <br/> |

<span data-ttu-id="9c634-141"><a name="bk_REST"> </a></span><span class="sxs-lookup"><span data-stu-id="9c634-141"></span></span>

## <a name="cache-user-photos"></a><span data-ttu-id="9c634-142">Cache benutzerfotos</span><span class="sxs-lookup"><span data-stu-id="9c634-142">Cache user photos</span></span>

<span data-ttu-id="9c634-p105">Exchange gibt die Daten mit dem Inhaltstyp Bild/jpeg und einer Sammlung von Headerwerten zurück. Der **ETag**-Header ähnelt einem Änderungsschlüssel. Der Wert ist eine Zeichenfolge, der den letzten Zeitpunkt darstellt, zu dem das Foto aktualisiert wurde. **ETag** bleibt für das Benutzerfoto gleich, bis das Foto geändert wird. Sie können diesen **ETag**-Wert in der HTTPS- **GET**-Anforderung in einem **If-None-Match**-Header an den Server senden. Wenn sich das Foto seit der letzten Anforderung nicht geändert hat, antwortet der Server mit einer HTTP 304-Antwort, in der Entsprechendes angegeben ist. Das heißt, Sie können das zuvor angeforderte und gespeicherte Foto verwenden, statt ein neues nutzen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="9c634-p105">Exchange returns the data with a content type of image/jpeg, along with a collection of header values. The **ETag** header is similar to a change key. The value is a string that represents the last time the photo was updated. The **ETag** remains the same for the user photo until the photo is changed. You can send this **ETag** value to the server in the HTTPS **GET** request in an **If-None-Match** header. If the photo hasn't changed since the last request, the server will respond with an HTTP 304 response that indicates as such. This means that you can use the user photo that you previously requested and saved rather than processing a new one.</span></span> 

<span data-ttu-id="9c634-150"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="9c634-150"></span></span>

## <a name="get-a-contact-user-photo-by-using-ews-managed-api"></a><span data-ttu-id="9c634-151">Abrufen eines Benutzerfotos eines Kontakts mithilfe der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="9c634-151">Get a contact user photo by using EWS Managed API</span></span>

<span data-ttu-id="9c634-p106">Ihre Anwendung kann die verwaltete EWS-API zum Abrufen von Fotos für Kontakte, wenn der Kontakt in einem Kontaktordner im Postfach des Benutzers gespeichert ist. Suchen Sie dazu nach dem **ItemId** für den Kontakt, den Sie verwenden möchten. Nachdem Sie eine Bindung zu diesem Kontakt erstellt haben, können Sie ihn in die Anlagensammlung laden. Wenn zu dem Kontakt ein Foto vorhanden ist, befindet sich das Foto unter den Anlagen. Gehen Sie die Anlagensammmlung durch und überprüfen Sie den Wert der **IsContactPhoto**-Eigenschaft. Nachdem Sie das Kontaktfoto gefunden haben, können Sie es auf Ihrem lokalen Computer speichern, und Ihre Anwendung kann darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="9c634-p106">Your application can use the EWS Managed API to retrieve photos for contacts, if the contact is stored in a contact folder in the user's mailbox. To do this, first, find the **ItemId** for the contact you want use. Then, after you bind to that contact, load it to the attachments collection. If the contact has a photo, the photo will be one of the attachments. Loop through the attachments collection, checking the value of the **IsContactPhoto** property. When you find the contact photo, you can save it to your local computer, and your application can access it.</span></span> 
  
<span data-ttu-id="9c634-p107">Im folgenden Beispiel wird dieser Prozess veranschaulicht. In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer sich an einem Exchange-Server authentifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="9c634-p107">The following example shows this process. This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
private static void GetContactPhoto(ExchangeService service, string ItemId)
{
   // Bind to an existing contact by using the ItemId passed into this function.
   Contact contact = Contact.Bind(service, ItemId);
   // Load the contact to get access to the collection of attachments.
   contact.Load(new PropertySet(ContactSchema.Attachments));
   // Loop through the attachments looking for a contact photo.
   foreach (Attachment attachment in contact.Attachments)
   {
      if ((attachment as FileAttachment).IsContactPhoto)
      {
         // Load the attachment to access the content.
         attachment.Load();
      }
   }
   FileAttachment photo = contact.GetContactPictureAttachment();
   // Create a file stream and save the contact photo to your computer.
   using (FileStream file = new FileStream(photo.Name, FileMode.Create, System.IO.FileAccess.Write))
   {
      photo.Load(file);
   }
}

```

<span data-ttu-id="9c634-160"><a name="bk_EWS"> </a></span><span class="sxs-lookup"><span data-stu-id="9c634-160"></span></span>

## <a name="get-a-user-photo-by-using-ews"></a><span data-ttu-id="9c634-161">Abrufen einer benutzerfoto mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="9c634-161">Get a user photo by using EWS</span></span>

<span data-ttu-id="9c634-p108">Wenn Sie ein Benutzerfoto aus AD DS abrufen, können Sie die [GetUserPhoto](http://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx)- (wenn die E-Mail-Adresse bekannt ist) oder die [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx)-Operation verwenden (wenn die E-Mail-Adresse nicht bekannt ist). Wenn Sie ein Benutzerfoto aus einem Kontaktordner im Postfach abrufen, verwenden Sie die [GetItem](http://msdn.microsoft.com/library/6b96dace-1260-4b83-869a-7c31c5583daa%28Office.15%29.aspx) -Operation gefolgt von der [GetAttachment](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)-Operation. In beiden Fällen wird das Foto als Base64-codierte Zeichenfolge in der XML-Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c634-p108">If you're getting a user photo from AD DS, you can use the [GetUserPhoto](http://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx) operation (if you know the email address) or the [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) operation (if you don't know the email address). If you're getting a user photo from a contacts folder in the mailbox, use the [GetItem](http://msdn.microsoft.com/library/6b96dace-1260-4b83-869a-7c31c5583daa%28Office.15%29.aspx) operation followed by the [GetAttachment](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) operation. In either case, the photo is returned as a Base64-encoded string in the XML response.</span></span> 
  
### <a name="get-a-mailbox-user-photo-by-using-the-getuserphoto-operation"></a><span data-ttu-id="9c634-165">Abrufen eines Benutzerfotos für ein Postfach mithilfe der GetUserPhoto-Operation</span><span class="sxs-lookup"><span data-stu-id="9c634-165">Get a mailbox user photo by using the GetUserPhoto operation</span></span>

<span data-ttu-id="9c634-p109">Das Verwenden der **GetUserPhoto**-Operation ist selbsterklärend. Geben Sie in der XML-Anforderung die E-Mail-Adresse des Benutzers und die [Größe des zurückzugebenden Fotos](http://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx) an (im [SizeRequested](http://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx)-Element). In der folgenden XML-Beispielanforderung wird veranschaulicht, wie ein Foto für Sadie Daniels abgerufen werden kann, das 360 Pixel breit und 360 Pixel hoch ist.</span><span class="sxs-lookup"><span data-stu-id="9c634-p109">Using the **GetUserPhoto** operation is straightforward. In the XML request, specify the email address of the user, and the [size of the photo](http://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx) to return (in the [SizeRequested](http://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx) element). The following XML request example shows how to get a photo for Sadie Daniels that's 360 pixels wide by 360 pixels high.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013 "/>
   </soap:Header>
   <soap:Body>
      <m:GetUserPhoto>
         <m:Email>sadie@contoso.com</m:Email>
         <m:SizeRequested>HR360x360</m:SizeRequested>
      </m:GetUserPhoto>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="9c634-p110">Im Folgenden finden Sie die XML-Antwort. Das Base64-codierte Foto ist im [PictureData](http://msdn.microsoft.com/library/1124eac3-ebf2-4b81-96d3-96838c840433%28Office.15%29.aspx)-Element (der Inhalt wurde zur besseren Lesbarkeit gekürzt) enthalten.</span><span class="sxs-lookup"><span data-stu-id="9c634-p110">The following is the XML response. The Base64-encoded photo is contained in the [PictureData](http://msdn.microsoft.com/library/1124eac3-ebf2-4b81-96d3-96838c840433%28Office.15%29.aspx) element (the content has been shortened for readability).</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetUserPhotoResponse ResponseClass="Success" 
         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <HasChanged>true</HasChanged>
      <PictureData>/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAAg... wATRRRSuB//2Q==</PictureData>
    </GetUserPhotoResponse>
  </s:Body>
</s:Envelope>

```

### <a name="get-a-mailbox-user-photo-by-using-the-resolvenames-operation"></a><span data-ttu-id="9c634-171">Abrufen eins Benutzerfotos für ein Postfach mithilfe der ResolveNames-Operation</span><span class="sxs-lookup"><span data-stu-id="9c634-171">Get a mailbox user photo by using the ResolveNames operation</span></span>

<span data-ttu-id="9c634-p111">Wenn Sie die E-Mail-Adresse des Benutzers nicht kennen, für den Sie ein Foto abrufen, können [die ResolveNames-Operation](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md) verwenden, um Kandidaten für eine möglicher Übereinstimmung abzurufen. Wenn Sie für das **ContactDataShape**-Attribut des [ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx)-Elements „AllProperties" angeben, werden für die einzelnen Kandidaten viele Daten einschließlich der Benutzerfotos zurückgegeben. Im folgenden Beispiel wird die XML-Anforderung zum Auflösen des Namens „Sadie" und Zurückgeben aller Eigenschaften für die einzelnen Kandidaten veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="9c634-p111">If you don't know the email address of the user for whom you are getting a photo, you can [use the ResolveNames operation](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md) to get candidates for a possible match. If you specify "AllProperties" for the **ContactDataShape** attribute of the [ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) element, a lot of data, including user photos, will be returned for each candidate. The following example shows the XML request to resolve the name "Sadie" and return all the properties for each candidate.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
<soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>  
<soap:Body>
  <m:ResolveNames ReturnFullContactData="true" ContactDataShape="AllProperties">
      <m:UnresolvedEntry>sadie</m:UnresolvedEntry>
    </m:ResolveNames>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="9c634-p112">Es werden viele Daten in der Antwort zurückgegeben. Im folgenden Beispiel werden nur die für das Benutzerfoto relevanten Daten veranschaulicht. Das **Photo**-Element enthält das Base64-codierte Benutzerfoto (der Inhalt wurde zur besseren Lesbarkeit gekürzt).</span><span class="sxs-lookup"><span data-stu-id="9c634-p112">A lot of data will be returned in the response. The following example shows only the data that is relevant to the user photo. The **Photo** element contains the Base64-encoded user photo (the content has been shortened for readability).</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ResolutionSet TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Resolution>
              <t:Mailbox>
                <t:Name>Sadie Daniels</t:Name>
                <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Mailbox</t:MailboxType>
              </t:Mailbox>
              <t:Contact>
                <t:DisplayName>Sadie Daniels</t:DisplayName>
                <t:GivenName>Sadie</t:GivenName>
                <t:Initials/>
                <t:CompanyName>CONTOSO</t:CompanyName>
......
                <t:Photo>/9j/4AAQSkZJRgABAQE...qKKKAP/2Q==</t:Photo>
......
              </t:Contact>
            </t:Resolution>
          </m:ResolutionSet>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </m:ResolveNamesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="get-a-contact-user-photo-by-using-the-getattachment-operation"></a><span data-ttu-id="9c634-178">Abrufen eines Benutzerfotos für einen Kontakt mithilfe der GetAttachment-Operation</span><span class="sxs-lookup"><span data-stu-id="9c634-178">Get a contact user photo by using the GetAttachment operation</span></span>

<span data-ttu-id="9c634-p113">Sie können zum Abrufen von Fotos aus den in Ihrem Postfach gespeicherten Kontakten EWS verwenden. Zunächst müssen Sie die **GetItem**-Operation zum Zurückgeben aller Eigenschaften verwenden, damit Sie nach Fotos suchen können. Im folgenden Beispiel wird eine XML-Anforderung zum Abrufen eines Kontaktelements veranschaulicht. Die Element-ID wurde zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="9c634-p113">You can use EWS to get photos from contacts stored in your mailbox. First, you use the **GetItem** operation to return all properties so you can look for photos. The following example shows an XML request to get a contact item. The item ID has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns='http://schemas.microsoft.com/exchange/services/2006/messages'>
      <ItemShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="AAAAGECXAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AABLzXRv"/>
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="9c634-p114">Suchen Sie nach dem [HasPicture](http://msdn.microsoft.com/library/922a43fe-01bd-49f2-9261-e00e4699b8da%28Office.15%29.aspx)-Element, um zu überprüfen, ob dem Kontakt ein Foto zugeordnet ist. Durchsuchen Sie anschließend die Anlagensammlung nach demjenigen, bei dem ein Wert für das [IsContactPhoto](http://msdn.microsoft.com/library/ae36b5f9-a787-4863-9dbc-258ad724801d%28Office.15%29.aspx)-Element „true" lautet. Im folgenden Antwortbeispiel werden nur die relevanten Daten dargestellt. Die ID-Werte sind zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="9c634-p114">Look for the [HasPicture](http://msdn.microsoft.com/library/922a43fe-01bd-49f2-9261-e00e4699b8da%28Office.15%29.aspx) element to verify that the contact has an associated photo. Then look through the collection of attachments for one that has a value of true for the [IsContactPhoto](http://msdn.microsoft.com/library/ae36b5f9-a787-4863-9dbc-258ad724801d%28Office.15%29.aspx) element. The following response example shows only the relevant data. The ID values are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Contact>
              <t:ItemId Id="AAAAGECXAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AABLzXRv"/>
              <t:ParentFolderId Id="nIxIAAA=" ChangeKey="AQAAAA=="/>
              <t:ItemClass>IPM.Contact</t:ItemClass>
              <t:Subject>Hope Gross</t:Subject>
              <t:Sensitivity>Normal</t:Sensitivity>
......
              <t:Attachments>
                <t:FileAttachment>
                  <t:AttachmentId Id="1LGlhgpgoA="/>
                  <t:Name>ContactPicture.jpg</t:Name>
                  <t:Size>6260</t:Size>
                  <t:LastModifiedTime>2011-03-09T16:55:55</t:LastModifiedTime>
                  <t:IsInline>false</t:IsInline>
                  <t:IsContactPhoto>true</t:IsContactPhoto>
                </t:FileAttachment>
              </t:Attachments>
......
              <t:HasPicture>true</t:HasPicture>
            </t:Contact>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>

```

<span data-ttu-id="9c634-p115">Verwenden Sie als Nächstes die **GetAttachment**-Operation mit der **AttachmentId**, um die Anlage mit dem Kontaktfoto anzufordern. Im folgenden Beispiel wird die XML-Anforderung zum Abrufen der Anlage dargestellt. Die ID wird zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="9c634-p115">Next, use the **GetAttachment** operation with the **AttachmentId** to request the attachment that has the contact photo. The following example shows the XML request to get the attachment. The ID is shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape/>
      <AttachmentIds>
         <t:AttachmentId Id="1LGlhgpgoA="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="9c634-p116">Im folgenden Beispiel wird die XML-Antwort mit den Informationen zu der angeforderten Anlage veranschaulicht. Das [Inhalts](http://msdn.microsoft.com/library/24f8c54a-505f-4fc0-b7e7-93ad50b97070%28Office.15%29.aspx)-Element enthält die Base64-codierte Zeichenfolge für das Benutzerfoto, die in diesem Beispiel zur besseren Lesbarkeit gekürzt wurde.</span><span class="sxs-lookup"><span data-stu-id="9c634-p116">The following example shows the XML response with the information about the attachment you requested. The [Content](http://msdn.microsoft.com/library/24f8c54a-505f-4fc0-b7e7-93ad50b97070%28Office.15%29.aspx) element contains the Base64-encoded string for the user photo, shortened in this example for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="+KsDBEr1LGlhgpgoA="/>
              <t:Name>ContactPicture.jpg</t:Name>
              <t:Content>/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAAg...D//2Q==</t:Content>
            </t:FileAttachment>
          </m:Attachments>
        </m:GetAttachmentResponseMessage>
      </m:ResponseMessages>
    </m:GetAttachmentResponse>
  </s:Body>
</s:Envelope>

```

<span data-ttu-id="9c634-192"><a name="bk_EWS"> </a></span><span class="sxs-lookup"><span data-stu-id="9c634-192"></span></span>

## <a name="decode-a-base64-encoded-string"></a><span data-ttu-id="9c634-193">Dekodiert eine Base64-codierte Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9c634-193">Decode a Base64-encoded string</span></span>

<span data-ttu-id="9c634-p117">Unabhängig von der zum Abrufen eines Benutzerfotos verwendeten Operation müssen Sie die Zeichenfolge decodieren, damit Sie sie in Ihrer Anwendung verwenden können. Im folgenden Beispiel wird veranschaulicht, wie die Zeichenfolge decodiert und anschließend auf Ihrem lokalen Computer gespeichert werden kann, sodass Ihre Anwendung zu einem späteren Zeitpunkt darauf zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="9c634-p117">Regardless of the operation you use to get a user photo, you'll need to decode that string so you can use it in your application. The following example shows how to decode the string, and then save it to your local computer so you application can access it later.</span></span>
  
```cs
// Convert the encoded string into a byte array.
byte[] data = System.Convert.FromBase64String(Photo);
// Create a memory stream to read the data.
MemoryStream ms = new MemoryStream(data);
// Save the data on your local computer as a JPG image.
using (FileStream file = new FileStream(ContactName + ".jpg", FileMode.Create, System.IO.FileAccess.Write))
{
   byte[] bytes = new byte[ms.Length];
   ms.Read(bytes, 0, (int)ms.Length);
   file.Write(bytes, 0, bytes.Length);
   ms.Close();
}

```

## <a name="see-also"></a><span data-ttu-id="9c634-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c634-196">See also</span></span>

- [<span data-ttu-id="9c634-197">Benutzer und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="9c634-197">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)    
- [<span data-ttu-id="9c634-198">Lösen Sie mehrdeutige Namen auf, mithilfe von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9c634-198">Resolve ambiguous names by using EWS in Exchange 2013</span></span>](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)    
- [<span data-ttu-id="9c634-199">Prozess Kontakte in Batches mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="9c634-199">Process contacts in batches by using EWS in Exchange</span></span>](how-to-process-contacts-in-batches-by-using-ews-in-exchange.md)
    

