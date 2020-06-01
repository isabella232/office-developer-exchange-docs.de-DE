---
title: Abrufen von Benutzerfotos mithilfe von EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: f86d1099-1f57-47dc-abf2-4d5ae4e900a9
description: Erfahren Sie, wie Sie Benutzerfotos abrufen können, die mit einem Postfach oder einem Kontakt verknüpft sind, indem Sie die verwaltete EWS-API oder EWS in Exchange verwenden.
localization_priority: Priority
ms.openlocfilehash: 14f2bc6bef1ce3c3529f03e213e3ada7c45a5a71
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455786"
---
# <a name="get-user-photos-by-using-ews-in-exchange"></a>Abrufen von Benutzerfotos mithilfe von EWS in Exchange

Erfahren Sie, wie Sie Benutzerfotos abrufen können, die mit einem Postfach oder einem Kontakt verknüpft sind, indem Sie die verwaltete EWS-API oder EWS in Exchange verwenden.
  
Es ist schön, einem Namen ein Gesicht zuordnen zu können. Wenn Ihre Benutzer Namen Gesichter zuordnen möchten, kann Ihre Anwendung ein Bild von Exchange anfordern, in der Regel ein Foto, das ein E-Mail-Konto darstellt. Sie können Ein Benutzerfoto abrufen, das auf einem Exchange-Server für ein Postfach gespeichert ist oder ein Kontaktfoto aus den im Postfach gespeicherten Kontakten abrufen.
  
Zum Abrufen von Fotos aus Postfächern oder den Active Directory-Domänendiensten (AD DS) abrufen. Die optimale Option zum Abrufen eines Fotos hängt von der Art des Kontakts ab, von dem Sie ein Foto abrufen möchten. 
  
**Tabelle 1. Technologien zum Abrufen von Benutzerfotos auf Grundlage des Kontakttyps**

|**Kontakttyp**|**Zu verwendende Technologie**|
|:-----|:-----|
|Postfach-Benutzerfoto  <br/> |[Abrufen eines Benutzerfotos eines Postfachs mithilfe von REST](#bk_REST)<br/><br/> [Abrufen eines Benutzerfotos mithilfe von EWS](#bk_EWS) <br/> |
|Kontakt-Benutzerfoto  <br/> |[Abrufen eines Benutzerfotos eines Kontakts mithilfe der verwalteten EWS-API](#bk_EWSMA)<br/><br/> [Abrufen eines Benutzerfotos mithilfe von EWS](#bk_EWS) <br/> |

<a name="bk_REST"> </a>

## <a name="get-a-mailbox-user-photo-by-using-rest"></a>Abrufen eines Benutzerfotos eines Postfachs mithilfe von REST

Sie können Benutzerfotos von einem Exchange-Server mit einer standardmäßigen HTTPS- **GET**-Anforderung abrufen. Geben Sie in der Anforderung die E-Mail-Kontoadresse und einen Größencode für das Bild an, wie im folgenden Beispiel veranschaulicht. 
  
```HTML
https://Exchange Server/ews/Exchange.asmx/s/GetUserPhoto?email=email address&amp;size=size code
```

Verwenden Sie den AutoErmittlungsdienst-[GetUserSettings](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)-Vorgang, um die **ExternalEwsUrl**-Einstellung abzurufen, die die URL des Endpunkts der Exchange-Webdienste (EWS) und den Speicherort des **Exchange.asmx** HTTP-Handlers, der die Benutzerfotos zurückgibt. 
  
In den Größencodes wird die Höhe und Breite des Bilds in Pixel angegeben. Der Größencode **HR48x48** gibt beispielsweise ein Bild zurück, das 48 Pixel hoch und 48 Pixel breit ist. Die möglichen Werte für den Größencodeparameter entsprechen den möglichen Werten für das [SizeRequested](https://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx)-Element. Wenn die Anforderung eine nicht verfügbare Größe angibt, wird das größtmögliche Foto zurückgegeben. Wenn kein Foto auf dem Exchange-Server gespeichert ist, wird das in AD DS für das Konto gespeicherte Bild zurückgegeben. 
  
> [!NOTE]
> Der **HR48x48**-Größencode gibt immer das AD DS-Vorschaubild zurück, falls verfügbar. 
  
Im folgenden Beispiel wird veranschaulicht, wie Sie die GET-Anforderung verwenden können, um das Benutzerfoto für Sadie abzurufen und auf Ihrem lokalen Computer zu speichern.
  
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

Die Anforderung gibt eine HTTP-Antwort zurück. 
  
**Tabelle 2. Antwortcodes für eine GetUserPhoto-Anforderung**

|**Antwortcode**|**Beschreibung**|
|:-----|:-----|
|200  <br/> |Für das angegebene E-Mail-Konto ist ein Bild verfügbar und das binäre Bild ist in der Antwort enthalten.  <br/> |
|304  <br/> |Das Bild hat sich seit der letzten **ETag**-Rückgabe an die Anwendung nicht geändert.  <br/> |
|404  <br/> |Für das angegebene E-Mail-Konto ist kein Bild verfügbar.  <br/> |

<a name="bk_REST"> </a>

## <a name="cache-user-photos"></a>Zwischenspeichern von Benutzerfotos

Exchange gibt die Daten mit dem Inhaltstyp Bild/jpeg und einer Sammlung von Headerwerten zurück. Der **ETag**-Header ähnelt einem Änderungsschlüssel. Der Wert ist eine Zeichenfolge, der den letzten Zeitpunkt darstellt, zu dem das Foto aktualisiert wurde. **ETag** bleibt für das Benutzerfoto gleich, bis das Foto geändert wird. Sie können diesen **ETag**-Wert in der HTTPS- **GET**-Anforderung in einem **If-None-Match**-Header an den Server senden. Wenn sich das Foto seit der letzten Anforderung nicht geändert hat, antwortet der Server mit einer HTTP 304-Antwort, in der Entsprechendes angegeben ist. Das heißt, Sie können das zuvor angeforderte und gespeicherte Foto verwenden, statt ein neues nutzen zu müssen. 

<a name="bk_EWSMA"> </a>

## <a name="get-a-contact-user-photo-by-using-ews-managed-api"></a>Abrufen eines Benutzerfotos eines Kontakts mithilfe der verwalteten EWS-API

Ihre Anwendung kann die verwaltete EWS-API zum Abrufen von Fotos für Kontakte, wenn der Kontakt in einem Kontaktordner im Postfach des Benutzers gespeichert ist. Suchen Sie dazu nach dem **ItemId** für den Kontakt, den Sie verwenden möchten. Nachdem Sie eine Bindung zu diesem Kontakt erstellt haben, können Sie ihn in die Anlagensammlung laden. Wenn zu dem Kontakt ein Foto vorhanden ist, befindet sich das Foto unter den Anlagen. Gehen Sie die Anlagensammmlung durch und überprüfen Sie den Wert der **IsContactPhoto**-Eigenschaft. Nachdem Sie das Kontaktfoto gefunden haben, können Sie es auf Ihrem lokalen Computer speichern, und Ihre Anwendung kann darauf zugreifen. 
  
Im folgenden Beispiel wird dieser Prozess veranschaulicht. In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer sich an einem Exchange-Server authentifizieren kann. 
  
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

<a name="bk_EWS"> </a>

## <a name="get-a-user-photo-by-using-ews"></a>Abrufen eines Benutzerfotos mithilfe von EWS

Wenn Sie ein Benutzerfoto aus AD DS abrufen, können Sie die [GetUserPhoto](https://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx)- (wenn die E-Mail-Adresse bekannt ist) oder die [ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx)-Operation verwenden (wenn die E-Mail-Adresse nicht bekannt ist). Wenn Sie ein Benutzerfoto aus einem Kontaktordner im Postfach abrufen, verwenden Sie die [GetItem](https://msdn.microsoft.com/library/6b96dace-1260-4b83-869a-7c31c5583daa%28Office.15%29.aspx) -Operation gefolgt von der [GetAttachment](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)-Operation. In beiden Fällen wird das Foto als Base64-codierte Zeichenfolge in der XML-Antwort zurückgegeben. 
  
### <a name="get-a-mailbox-user-photo-by-using-the-getuserphoto-operation"></a>Abrufen eines Benutzerfotos für ein Postfach mithilfe der GetUserPhoto-Operation

Das Verwenden der **GetUserPhoto**-Operation ist selbsterklärend. Geben Sie in der XML-Anforderung die E-Mail-Adresse des Benutzers und die [Größe des zurückzugebenden Fotos](https://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx) an (im [SizeRequested](https://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx)-Element). In der folgenden XML-Beispielanforderung wird veranschaulicht, wie ein Foto für Sadie Daniels abgerufen werden kann, das 360 Pixel breit und 360 Pixel hoch ist. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

Im Folgenden finden Sie die XML-Antwort. Das Base64-codierte Foto ist im [PictureData](https://msdn.microsoft.com/library/1124eac3-ebf2-4b81-96d3-96838c840433%28Office.15%29.aspx)-Element (der Inhalt wurde zur besseren Lesbarkeit gekürzt) enthalten. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetUserPhotoResponse ResponseClass="Success" 
         xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <HasChanged>true</HasChanged>
      <PictureData>/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAAg... wATRRRSuB//2Q==</PictureData>
    </GetUserPhotoResponse>
  </s:Body>
</s:Envelope>

```

### <a name="get-a-mailbox-user-photo-by-using-the-resolvenames-operation"></a>Abrufen eins Benutzerfotos für ein Postfach mithilfe der ResolveNames-Operation

Wenn Sie die E-Mail-Adresse des Benutzers nicht kennen, für den Sie ein Foto abrufen, können [die ResolveNames-Operation](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md) verwenden, um Kandidaten für eine möglicher Übereinstimmung abzurufen. Wenn Sie für das **ContactDataShape**-Attribut des [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx)-Elements „AllProperties" angeben, werden für die einzelnen Kandidaten viele Daten einschließlich der Benutzerfotos zurückgegeben. Im folgenden Beispiel wird die XML-Anforderung zum Auflösen des Namens „Sadie" und Zurückgeben aller Eigenschaften für die einzelnen Kandidaten veranschaulicht. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

Es werden viele Daten in der Antwort zurückgegeben. Im folgenden Beispiel werden nur die für das Benutzerfoto relevanten Daten veranschaulicht. Das **Photo**-Element enthält das Base64-codierte Benutzerfoto (der Inhalt wurde zur besseren Lesbarkeit gekürzt). 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="get-a-contact-user-photo-by-using-the-getattachment-operation"></a>Abrufen eines Benutzerfotos für einen Kontakt mithilfe der GetAttachment-Operation

Sie können zum Abrufen von Fotos aus den in Ihrem Postfach gespeicherten Kontakten EWS verwenden. Zunächst müssen Sie die **GetItem**-Operation zum Zurückgeben aller Eigenschaften verwenden, damit Sie nach Fotos suchen können. Im folgenden Beispiel wird eine XML-Anforderung zum Abrufen eines Kontaktelements veranschaulicht. Die Element-ID wurde zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns='https://schemas.microsoft.com/exchange/services/2006/messages'>
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

Suchen Sie nach dem [HasPicture](https://msdn.microsoft.com/library/922a43fe-01bd-49f2-9261-e00e4699b8da%28Office.15%29.aspx)-Element, um zu überprüfen, ob dem Kontakt ein Foto zugeordnet ist. Durchsuchen Sie anschließend die Anlagensammlung nach demjenigen, bei dem ein Wert für das [IsContactPhoto](https://msdn.microsoft.com/library/ae36b5f9-a787-4863-9dbc-258ad724801d%28Office.15%29.aspx)-Element „true" lautet. Im folgenden Antwortbeispiel werden nur die relevanten Daten dargestellt. Die ID-Werte sind zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

Verwenden Sie als Nächstes die **GetAttachment**-Operation mit der **AttachmentId**, um die Anlage mit dem Kontaktfoto anzufordern. Im folgenden Beispiel wird die XML-Anforderung zum Abrufen der Anlage dargestellt. Die ID wird zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape/>
      <AttachmentIds>
         <t:AttachmentId Id="1LGlhgpgoA="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>

```

Im folgenden Beispiel wird die XML-Antwort mit den Informationen zu der angeforderten Anlage veranschaulicht. Das [Inhalts](https://msdn.microsoft.com/library/24f8c54a-505f-4fc0-b7e7-93ad50b97070%28Office.15%29.aspx)-Element enthält die Base64-codierte Zeichenfolge für das Benutzerfoto, die in diesem Beispiel zur besseren Lesbarkeit gekürzt wurde. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<a name="bk_EWS"> </a>

## <a name="decode-a-base64-encoded-string"></a>Decodieren einer Base64-codierten Zeichenfolge

Unabhängig von der zum Abrufen eines Benutzerfotos verwendeten Operation müssen Sie die Zeichenfolge decodieren, damit Sie sie in Ihrer Anwendung verwenden können. Im folgenden Beispiel wird veranschaulicht, wie die Zeichenfolge decodiert und anschließend auf Ihrem lokalen Computer gespeichert werden kann, sodass Ihre Anwendung zu einem späteren Zeitpunkt darauf zugreifen kann.
  
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

## <a name="see-also"></a>Siehe auch

- [Personen und Kontakte in EWS in Exchange](people-and-contacts-in-ews-in-exchange.md)    
- [Auflösen von mehrdeutigen Namen mithilfe der EWS Exchange 2013](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)    
- [Verarbeiten von Kontakten in Batches mithilfe von EWS in Exchange](how-to-process-contacts-in-batches-by-using-ews-in-exchange.md)
    

