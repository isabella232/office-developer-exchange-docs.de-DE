---
title: FindFolder-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FindFolder
api_type:
- schema
ms.assetid: 7a9855aa-06cc-45ba-ad2a-645c15b7d031
description: Der FindFolder-Vorgang verwendet Exchange Webdienste, um Unterordner eines bestimmten Ordners zu suchen, und gibt einen Satz von Eigenschaften zurück, die den Satz von Unterordnern beschreiben.
ms.openlocfilehash: 8c2776a9d60244fe77b6012a09ffbad230d86f63
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518470"
---
# <a name="findfolder-operation"></a>FindFolder-Vorgang

Der **FindFolder-Vorgang** verwendet Exchange Webdienste, um Unterordner eines bestimmten Ordners zu suchen, und gibt einen Satz von Eigenschaften zurück, die den Satz von Unterordnern beschreiben. 
  
## <a name="remarks"></a>HinwBemerkungeneise

FindFolder gibt nur die ersten 512 Bytes einer streambaren Eigenschaft zurück. Bei Unicode werden nur die ersten 255 Zeichen mit einer Unicode-Zeichenfolge zurückgegeben, die mit null endet.
  
Tiefendurchlaufabfragen können für öffentliche Ordner nicht ausgeführt werden.
  
Einschränkungen sind zulässig und sollten nur die Ordnereigenschaften und nicht die Elementeigenschaften verwenden. Sortierfunktionen sind für **FindFolder-Antworten** nicht verfügbar. Gruppierte Abfragen sind für **FindFolder-Abfragen** nicht verfügbar. 
  
 **Hinweis** Der **FindFolder-Vorgang** wird auch zum Suchen nach verwalteten Ordnern verwendet. 
  
### <a name="soap-headers"></a>SOAP-Header

Der **FindFolder-Vorgang** kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt und beschrieben sind. 
  
|**Header**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|Identitätswechsel  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.  <br/> |
|MailboxCulture  <br/> |[MailboxCulture](mailboxculture.md) <br/> |Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird.  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.  <br/> |
|TimeZoneContext  <br/> |[TimeZoneContext](timezonecontext.md) <br/> |Gibt die Zeitzone für alle Antworten vom Server an.  <br/> |
   
## <a name="findfolder-request-example"></a>FindFolder-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer **FindFolder-Anforderung** zeigt, wie Sie eine Anforderung zum Suchen aller Ordner in einem Posteingang erstellen. 
  
### <a name="code"></a>Code

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

### <a name="comments"></a>Comments

Unter Verwendung des Standardwerts für die [BaseShape](baseshape.md)gibt die Antwort den Ordnernamen, die Ordner-ID, die Anzahl der Unterordner, die Anzahl der im Ordner gefundenen untergeordneten Ordner und die Anzahl der ungelesenen Elemente zurück.
  
### <a name="request-elements"></a>Anfordern von Elementen

Diese **FindFolder-Anforderung** enthält die folgenden Elemente: 
  
- [FindFolder](findfolder.md)
    
- [FolderShape](foldershape.md)
    
- [BaseShape](baseshape.md)
    
- [ParentFolderIds](parentfolderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
 Weitere **FindFolder-Anforderungselemente** finden Sie im Schema. 
  
## <a name="findfolder-response-example"></a>FindFolder-Antwortbeispiel

### <a name="description"></a>Beschreibung

Der folgende SOAP-Text (Simple Object Access Protocol) zeigt eine erfolgreiche Antwort auf die **FindFolder-Anforderung.** Die Antwort enthält die Elemente, die zurückgegeben werden, wenn der Standardwert für die [BaseShape](baseshape.md) verwendet wird. 
  
> [!NOTE]
> Die Ordner-ID und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu gewährleisten. 
  
### <a name="code"></a>Code

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

### <a name="response-elements"></a>Antwortelemente

Die eigenschaften, die in der Antwort zurückgegeben werden, werden durch die [BaseShape](baseshape.md) und die [AdditionalProperties](additionalproperties.md) bestimmt, wenn sie verwendet werden. Eine erfolgreiche **FindFolder-Antwort** enthält die folgenden Elemente: 
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [FindFolderResponse](findfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [FindFolderResponseMessage](findfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
- [Ordner](folder.md)
    
- [FolderId](folderid.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
- [TotalCount](totalcount.md)
    
- [ChildFolderCount](childfoldercount.md)
    
- [UnreadCount](unreadcount.md)
    
### <a name="comments"></a>Kommentare

 **FindFolder-Antworten** auf eine Anforderung mit dem **AllProperties-Antwort-Shape** geben nicht die [Elemente TotalCount](totalcount.md) und [UnreadCount](unreadcount.md) für Suchvorgänge in öffentlichen Ordnern zurück. 
  
## <a name="findfolder-error-response-example"></a>Beispiel für FindFolder-Fehlerantwort

### <a name="description"></a>Beschreibung

Das folgende SOAP-Textkörperbeispiel zeigt eine Fehlerantwort, die auftritt, wenn Sie nach einem Ordner suchen, der durch einen falsch formatierten Ordnerbezeichner identifiziert wird.
  
### <a name="code"></a>Code

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

### <a name="error-response-elements"></a>Fehlerantwortelemente

Die **FindFolder-Fehlerantwort** enthält die folgenden Elemente: 
  
- [FindFolderResponse](findfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="additional-information"></a>Weitere Informationen

- Das [DisplayName-Element (Zeichenfolge)](displayname-string.md) des Ordners ist immer im Standard-Shape enthalten. 
    
- Das [UnreadCount-Element](unreadcount.md) ist in Aufgaben- und Notizenordnern enthalten. 
    
- Verwenden Sie den **PropertyTag-Wert** von 0x672D mit dem Eigenschaftstyp **Integer,** um einen verwalteten Ordner mithilfe des [ExtendedFieldURI-Elements](extendedfielduri.md) zu identifizieren. 
    
## <a name="see-also"></a>Siehe auch



[Suchen von Ordnern](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

