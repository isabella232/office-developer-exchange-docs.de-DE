---
title: FindFolder Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindFolder
api_type:
- schema
ms.assetid: 7a9855aa-06cc-45ba-ad2a-645c15b7d031
description: Der Vorgang FindFolder mithilfe Exchange-Webdienste Unterordnern eines angegebenen Ordners gesucht und gibt einen Satz von Eigenschaften, mit die die Unterordner beschrieben werden.
ms.openlocfilehash: 655455b46d4a3192b294bee9d85352d95ded49ae
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758444"
---
# <a name="findfolder-operation"></a>FindFolder Operation

Der Vorgang **FindFolder** mithilfe Exchange-Webdienste Unterordnern eines angegebenen Ordners gesucht und gibt einen Satz von Eigenschaften, mit die die Unterordner beschrieben werden. 
  
## <a name="remarks"></a>Hinweise

FindFolder gibt nur die ersten 512 Byte einer beliebigen streamfähiges Eigenschaft zurück. Bei Unicode werden nur die ersten 255 Zeichen mit einer Unicode-Zeichenfolge zurückgegeben, die mit null endet.
  
Deep Traversal Abfragen können nicht auf Öffentliche Ordner ausgeführt werden.
  
Einschränkungen sind zulässig und sollten nur die Ordnereigenschaften, nicht die Eigenschaften des Elements verwenden. Sortierungsfunktionen ist nicht verfügbar für **FindFolder** Antworten. Gruppierte Abfragen sind nicht verfügbar für **FindFolder** Abfragen. 
  
 **Hinweis** Der Vorgang **FindFolder** wird auch verwendet, um verwaltete Ordner zu finden. 
  
### <a name="soap-headers"></a>SOAP-Header

Der Vorgang **FindFolder** können die SOAP-Header, die aufgeführt und in der folgenden Tabelle beschrieben. 
  
|**Header**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|Identitätswechsel  <br/> |["ExchangeImpersonation"](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.  <br/> |
|MailboxCulture  <br/> |[MailboxCulture](mailboxculture.md) <br/> |Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird.  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.  <br/> |
|TimeZoneContext  <br/> |[TimeZoneContext](timezonecontext.md) <br/> |Gibt die Zeitzone für alle Antworten vom Server an.  <br/> |
   
## <a name="findfolder-request-example"></a>FindFolder anforderungsbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung **FindFolder** veranschaulicht eine Anforderung an alle Ordner befindet sich im Posteingang suchen bilden. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>Kommentare

Verwenden den Standardwert für die [BaseShape](baseshape.md), gibt die Antwort den Ordnernamen, die Ordner-ID, die Anzahl der Unterordner, die Anzahl der untergeordneten Ordner in den Ordner und die Anzahl der ungelesenen Elemente zurück.
  
### <a name="request-elements"></a>Anfordern von Elementen

Diese Anforderung **FindFolder** umfasst die folgenden Elemente: 
  
- [FindFolder](findfolder.md)
    
- [FolderShape](foldershape.md)
    
- [BaseShape](baseshape.md)
    
- [ParentFolderIds](parentfolderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
 Zusätzliche **FindFolder** Anforderung Elemente finden Sie unter Schema. 
  
## <a name="findfolder-response-example"></a>FindFolder antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende (SOAP = Simple Object Access Protocol)-Body-Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung **FindFolder** . Die Antwort enthält die Elemente, die zurückgegeben werden, wenn der Standardwert für die [BaseShape](baseshape.md) verwendet wird. 
  
> [!NOTE]
> Die Ordner-ID und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu erhalten. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

Die Eigenschaften, die in der Antwort zurückgegeben werden werden durch die [BaseShape](baseshape.md) und die [AdditionalProperties](additionalproperties.md) bestimmt, wenn sie verwendet werden. Eine erfolgreiche Antwort **FindFolder** umfasst die folgenden Elemente: 
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [FindFolderResponse](findfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [FindFolderResponseMessage](findfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
- [TotalCount](totalcount.md)
    
- [ChildFolderCount](childfoldercount.md)
    
- [UnreadCount](unreadcount.md)
    
### <a name="comments"></a>Kommentare

 Antworten auf eine Anforderung mit dem **AllProperties** Antwort Shape **FindFolder** gibt nicht den [TotalCount](totalcount.md) und die [UnreadCount](unreadcount.md) Elemente für Öffentliche Ordner suchen zurück. 
  
## <a name="findfolder-error-response-example"></a>Antwortbeispiel FindFolder Fehler

### <a name="description"></a>Beschreibung

Das folgende SOAP-Body-Beispiel zeigt eine Fehlerantwort an, die auftritt, wenn für einen Ordner suchen, die durch eine fehlerhafte Ordner-ID identifiziert wird.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a>Fehler Antwortelemente

Die Fehlerantwort **FindFolder** umfasst die folgenden Elemente: 
  
- [FindFolderResponse](findfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="additional-information"></a>Zusätzliche Informationen

- Ordner [DisplayName (String)](displayname-string.md) -Elements ist immer in der Standardform enthalten. 
    
- Das [UnreadCount](unreadcount.md) -Element ist im Ordner Aufgaben und Notizen enthalten. 
    
- Verwenden Sie den Wert **' PropertyTag '** 0x672D mit Eigenschaftentyp **ganze Zahl** um einen verwalteten Ordner mit dem [ExtendedFieldURI](extendedfielduri.md) -Element zu identifizieren. 
    
## <a name="see-also"></a>Siehe auch



[Suchen nach Ordnern](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

