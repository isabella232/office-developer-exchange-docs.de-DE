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
# <a name="getuserphoto-operation"></a>GetUserPhoto-Vorgang

Hier finden Sie Informationen zum **GetUserPhoto** -EWS-Vorgang. 
  
Der **GetUserPhoto** -Vorgang ruft ein Benutzer Foto aus Active Directory-Domänendienste (AD DS) ab. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-getuserphoto-operation"></a>Verwenden des GetUserPhoto-Vorgangs

Der **RemoveContactFromImList** -Vorgang ist ein einfacher Vorgang, der die e-Mail-Adresse eines Benutzers und das angeforderte Fotoformat akzeptiert und den Fotostream in der Antwort zurückgibt. 
  
> [!NOTE]
> EWS verfügt sowohl über einen SOAP-als auch einen Rest-basierten Vorgang, um Benutzer Fotos zu erhalten. Informationen zur Rest-Schnittstelle finden Sie unter [Abrufen von Benutzer Fotos mithilfe von EWS in Exchange](https://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx). 
  
### <a name="getuserphoto-operation-soap-headers"></a>SOAP-Header des GetUserPhoto-Vorgangs

Der **GetUserPhoto** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="getuserphoto-operation-request-example-get-a-users-photo"></a>GetUserPhoto-Vorgangs Anforderungs Beispiel: Abrufen eines Benutzer Fotos

Im folgenden Beispiel einer **GetUserPhoto** -Vorgangsanforderung wird gezeigt, wie das Foto eines Benutzers abgerufen wird. In diesem Beispiel wird ein Benutzer Foto angefordert, bei dem es sich um 48x48 Pixel handelt. 
  
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

Die folgenden Elemente werden im SOAP-Anforderungstext Körper verwendet:
  
- [GetUserPhoto](getuserphoto.md)
    
- [E-Mail (Zeichenfolge)](email-string.md)
    
- [SizeRequested](sizerequested.md)
    
## <a name="successful-getuserphoto-operation-response"></a>Erfolgreiche Reaktion des GetUserPhoto-Vorgangs

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf einen **GetUserPhoto** -Vorgang, um das Foto eines Benutzers abzurufen. 
  
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

Die folgenden Elemente werden im SOAP-Antworttext Körper verwendet:
  
- [GetUserPhotoResponse](getuserphotoresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [HasChanged](haschanged.md)
    
- [GetUserPhotoResponse](getuserphotoresponse.md)
    
## <a name="getuserphoto-operation-error-response"></a>Fehlerantwort des GetUserPhoto-Vorgangs

Der SOAP-Umschlag gibt keinen Fehlercode zurück, wenn versucht wird, ein Benutzer Foto für eine e-Mail-Adresse abzurufen, die in der Organisation nicht vorhanden ist. Ein 500-HTTP-Statuscode wird in der Antwort zurückgegeben, um anzugeben, dass die Anforderung nicht erfolgreich war. 
  
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)   
- [Abrufen von Benutzerfotos mithilfe von EWS in Exchange](https://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx)
    

