---
title: GetUserPhoto-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e
description: Hier finden Sie Informationen über die GetUserPhoto EWS Vorgang.
ms.openlocfilehash: 4465ac7115d96f5b6ef39e467663c9bf1c70e99e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829694"
---
# <a name="getuserphoto-operation"></a>GetUserPhoto-Vorgang

Hier finden Sie Informationen zum **GetUserPhoto** EWS-Vorgang. 
  
Der Vorgang **GetUserPhoto** Ruft ein benutzerfoto aus Active Directory-Domänendienste (AD DS) ab. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-getuserphoto-operation"></a>Verwenden des GetUserPhoto-Vorgangs

Der **RemoveContactFromImList** -Vorgang ist ein einfacher Vorgang, der e-Mail-Adresse des Benutzers und die Größe des angeforderten Fotos akzeptiert Datenstrom und gibt das Foto in der Antwort. 
  
> [!NOTE]
> EWS hat sowohl eine SOAP und einen Vorgang REST-basierte benutzerfotos abzurufen. Informationen über die REST-Schnittstelle finden Sie unter [Abrufen benutzerfotos mithilfe der EWS in Exchange](http://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx). 
  
### <a name="getuserphoto-operation-soap-headers"></a>GetUserPhoto Vorgang SOAP-Header

Der Vorgang **GetUserPhoto** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="getuserphoto-operation-request-example-get-a-users-photo"></a>GetUserPhoto Vorgang-anforderungsbeispiel: Abrufen eines Benutzers Foto

Im folgenden Beispiel wird eine **GetUserPhoto** Vorgang Anforderung veranschaulicht Foto des Benutzers abzurufen. In diesem Beispiel fordert ein benutzerfoto, das 48 x 48 Pixel ist. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

Die folgenden Elemente werden in der Anforderung SOAP-Body verwendet:
  
- [GetUserPhoto](getuserphoto.md)
    
- [E-Mail (Zeichenfolge)](email-string.md)
    
- [SizeRequested](sizerequested.md)
    
## <a name="successful-getuserphoto-operation-response"></a>Erfolgreiche GetUserPhoto Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetUserPhoto** Operation Foto des Benutzers abgerufen. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetUserPhotoResponse ResponseClass="Success" 
                            xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <HasChanged>true</HasChanged>
         <PictureData>/9j/4AAQSkZJRgABAQEAYABgAAD/02</PictureData>
      </GetUserPhotoResponse>
   </s:Body>
</s:Envelope>

```

Die folgenden Elemente werden in der Antwort SOAP-Body verwendet:
  
- [GetUserPhotoResponse](getuserphotoresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [HasChanged](haschanged.md)
    
- [GetUserPhotoResponse](getuserphotoresponse.md)
    
## <a name="getuserphoto-operation-error-response"></a>GetUserPhoto Vorgang Fehlerantwort

SOAP-Umschlag gibt einen Fehlercode zurück, wenn versucht wird, um ein benutzerfoto für eine e-Mail-Adresse zu erhalten, die in der Organisation nicht vorhanden ist. 500 HTTP-Statuscode wird zurückgegeben werden soll, in der Antwort, um anzugeben, dass die Anforderung nicht erfolgreich war. 
  
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)   
- [Abrufen von benutzerfotos mithilfe der EWS in Exchange](http://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx)
    

