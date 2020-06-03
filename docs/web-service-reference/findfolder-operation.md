---
title: FindFolder-Vorgang
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
description: Der FindFolder-Vorgang verwendet Exchange Webdienste zum Suchen von Unterordnern eines identifizierten Ordners und gibt eine Reihe von Eigenschaften zurück, die die Gruppe von Unterordnern beschreiben.
ms.openlocfilehash: f1cc199bdaf684d8d74687ed7f064eb66fee48ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462584"
---
# <a name="findfolder-operation"></a>FindFolder-Vorgang

Der **FindFolder** -Vorgang verwendet Exchange Webdienste zum Suchen von Unterordnern eines identifizierten Ordners und gibt eine Reihe von Eigenschaften zurück, die die Gruppe von Unterordnern beschreiben. 
  
## <a name="remarks"></a>Bemerkungen

FindFolder gibt nur die ersten 512 Bytes einer Streamable-Eigenschaft zurück. Bei Unicode werden nur die ersten 255 Zeichen mit einer Unicode-Zeichenfolge zurückgegeben, die mit null endet.
  
Tief greifende Abfragen können nicht für Öffentliche Ordner ausgeführt werden.
  
Einschränkungen sind zulässig und sollten nur die Ordner Eigenschaften und nicht die Elementeigenschaften verwenden. Sortierfunktionen stehen für **FindFolder** -Antworten nicht zur Verfügung. Gruppierte Abfragen stehen für **FindFolder** -Abfragen nicht zur Verfügung. 
  
 **Hinweis:** Der **FindFolder** -Vorgang wird auch verwendet, um verwaltete Ordner zu finden. 
  
### <a name="soap-headers"></a>SOAP-Header

Der **FindFolder** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt und beschrieben werden. 
  
|**Header**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|Identitätswechsel  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.  <br/> |
|MailboxCulture  <br/> |[MailboxCulture](mailboxculture.md) <br/> |Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird.  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.  <br/> |
|TimeZoneContext  <br/> |[TimeZoneContext](timezonecontext.md) <br/> |Gibt die Zeitzone für alle Antworten vom Server an.  <br/> |
   
## <a name="findfolder-request-example"></a>FindFolder-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer **FindFolder** -Anforderung wird gezeigt, wie eine Anforderung zum Auffinden aller Ordner in einem Posteingang bildet. 
  
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

Mit dem Standardwert für die [BaseShape](baseshape.md)gibt die Antwort den Ordnernamen, die Ordner-ID, die Anzahl der Unterordner, die Anzahl der untergeordneten Ordner im Ordner und die Anzahl der ungelesenen Elemente zurück.
  
### <a name="request-elements"></a>Anfordern von Elementen

Diese **FindFolder** -Anforderung umfasst die folgenden Elemente: 
  
- [FindFolder](findfolder.md)
    
- [FolderShape](foldershape.md)
    
- [BaseShape](baseshape.md)
    
- [ParentFolderIds](parentfolderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
 Weitere **FindFolder** -anforderungselemente finden Sie im Schema. 
  
## <a name="findfolder-response-example"></a>FindFolder-Antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Simple Object Access Protocol (SOAP) Body-Beispiel zeigt eine erfolgreiche Antwort auf die **FindFolder** -Anforderung. Die Antwort enthält die Elemente, die zurückgegeben werden, wenn der Standardwert für die [BaseShape](baseshape.md) verwendet wird. 
  
> [!NOTE]
> Die Ordner-ID und der Change-Schlüssel wurden verkürzt, um die Lesbarkeit zu erhalten. 
  
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

### <a name="response-elements"></a>Response-Elemente

Die Eigenschaften, die in der Antwort zurückgegeben werden, werden durch die [BaseShape](baseshape.md) und die [AdditionalProperties](additionalproperties.md) bestimmt, wenn Sie verwendet werden. Eine erfolgreiche **FindFolder** -Antwort umfasst die folgenden Elemente: 
  
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
    
- [Total count](totalcount.md)
    
- [ChildFolderCount](childfoldercount.md)
    
- [UnreadCount](unreadcount.md)
    
### <a name="comments"></a>Kommentare

 **FindFolder** -Antworten auf eine Anforderung mit dem Antwort-Shape **allproperties** geben nicht die [Total count](totalcount.md) -und [UnreadCount](unreadcount.md) -Elemente für die Suche nach öffentlichen Ordnern zurück. 
  
## <a name="findfolder-error-response-example"></a>FindFolder-Fehlerantwort Beispiel

### <a name="description"></a>Beschreibung

Das folgende SOAP Body-Beispiel zeigt eine Fehlermeldung, die auftritt, wenn Sie nach einem Ordner suchen, der durch eine fehlerhafte Ordner-ID identifiziert wird.
  
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

Die **FindFolder** -Fehlerantwort umfasst die folgenden Elemente: 
  
- [FindFolderResponse](findfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="additional-information"></a>Weitere Informationen

- Das Element Folder [DisplayName (String)](displayname-string.md) ist immer in der Standardform enthalten. 
    
- Das [UnreadCount](unreadcount.md) -Element ist in Aufgaben und Notizenordner enthalten. 
    
- Verwenden Sie den **PropertyTag** -Wert 0x672D mit dem Property-Typ **Integer** , um einen verwalteten Ordner mithilfe des [ExtendedFieldURI](extendedfielduri.md) -Elements zu identifizieren. 
    
## <a name="see-also"></a>Siehe auch



[Suchen von Ordnern](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

