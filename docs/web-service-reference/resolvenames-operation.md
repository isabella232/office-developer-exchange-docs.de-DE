---
title: ResolveNames-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: 6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb
description: Die ResolveNames Vorgang löst keine eindeutige e-Mail-Adressen und Anzeigenamen.
ms.openlocfilehash: 8443cf834dfdf104daeaaa92fdee3742c3fa3719
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831162"
---
# <a name="resolvenames-operation"></a>ResolveNames-Vorgang

Die **ResolveNames** Vorgang löst keine eindeutige e-Mail-Adressen und Anzeigenamen. 
  
## <a name="using-the-resolvenames-operation"></a>Verwenden des Vorgangs ResolveNames

Dieser Vorgang kann Aliase überprüfen und beheben Anzeigenamen auf den entsprechenden Postfachbenutzer verwendet werden. Wenn mehrdeutige Namen vorhanden ist, enthält die Antwort auf einen Vorgang **ResolveNames** Informationen zu jedem Postfachbenutzer, damit die Namen die Clientanwendung aufgelöst werden kann. 
  
## <a name="remarks"></a>Hinweise

Die Antwort ResolveNames gibt maximal 100 Kandidaten zurück. Die 100 Kandidaten, die zurückgegeben werden, sind die ersten 100, die bei der Suche Konflikte auftreten.
  
E-Mail-Adressen mit vorangestellter routing Typen, wie die SMTP- oder Sip, werden in einem mehrwertigen Array gespeichert. Der **ResolveNames** Vorgang ausführt eine teilweise Übereinstimmung mit jeder Wert eines Arrays aus, wenn Sie den Routingtyp am Anfang der aufgelöste Name, beispielsweise "sip:User1@Contoso.com" hinzufügen. Wenn Sie eine Routingtyp nicht angeben, wird **ResolveNames** standardmäßig auf den Routingtyp von smtp, es zu einer primären SMTP-Adresse-Eigenschaft entspricht und nicht durchsucht das mehrwertige Array. 
  
In einer einzelnen Anforderung kann nur ein mehrdeutiger Name angegeben werden. Active Directory wird zuerst durchsucht, und dann Kontaktordner des Benutzers gesucht wird. Aufgelösten Einträge aus Kontaktordner eines Benutzers haben eine ungleich Null- **ItemId** -Eigenschaft, die dann in einer GetItem-Anforderung verwendet werden kann. Wenn es sich um die ID einer privaten Verteilerliste handelt, kann sie in einem [der ExpandDL-Vorgang](expanddl-operation.md)verwendet werden. Wenn das **ReturnFullContactData** -Attribut auf **true**festgelegt ist, gibt Active Directory-Einträge mit dem Vorgang **ResolveNames** gefunden zusätzliche Eigenschaften zurück, die einem [Kontakt](contact.md)zu beschreiben. Das Attribut **ReturnFullContactData** wirkt sich nicht auf die Daten, die für Kontakte und Private zurückgegeben wird Verteilerlisten aus Kontaktordner des Benutzers. 
  
## <a name="resolvenames-request-example"></a>ResolveNames anforderungsbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung **ResolveNames** veranschaulicht den Eintrag des Benutzers zu beheben.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>User2</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Kommentare

Die Antwort auf diese Anforderung werden alle Einträge zurückgegeben, die beginnen mit "Jo" oder "Mi". Die zurückgegebenen Elemente sind öffentliche Postfächer, öffentliche und private Verteilerlisten und Kontakte.
  
> [!NOTE]
> Es werden nur Kontakte in den Standardordner für persönliche Kontakte durchsucht. 
  
Im folgenden sind die möglichen Ergebnisse für eine Anforderung **ResolveNames** : 
  
- Antworten, die eine aufgelöste Entität nicht enthalten, gibt einen Attributwert **ResponseClass** **Fehler**gleich zurück. Das Element **MessageText** enthält " **keine Ergebnisse gefunden werden**."
    
- Antworten mit einer einzelnen aufgelöst Entität gibt den Attributwert **ResponseClass** **Erfolg**gleich zurück.
    
- Antworten, die mehrere mögliche Entitäten enthalten, gibt einen Attributwert **ResponseClass** **Warnung**gleich zurück. In diesem Fall konnte die Entität nicht in eine eindeutige Identität aufgelöst werden. Das Element **MessageText** enthält "mehrere Ergebnisse gefunden werden." 
    
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [ResolveNames](resolvenames.md)
    
- [UnresolvedEntry](unresolvedentry.md)
    
## <a name="successful-resolvenames-operation-response-example"></a>Erfolgreiche ResolveNames Vorgang antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **ResolveNames** . 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ResolutionSet TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Resolution>
              <t:Mailbox>
                <t:Name>User2</t:Name>
                <t:EmailAddress>User2@example.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Mailbox</t:MailboxType>
              </t:Mailbox>
              <t:Contact>
                <t:DisplayName>User2</t:DisplayName>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress1">SMTP:User2@example.com</t:Entry>
                </t:EmailAddresses>
                <t:ContactSource>ActiveDirectory</t:ContactSource>
              </t:Contact>
            </t:Resolution>
          </m:ResolutionSet>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-resolvenames-response-elements"></a>Erfolgreiche ResolveNames Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ResolveNamesResponse](resolvenamesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [ResolutionSet](resolutionset.md)
    
- [Lösung](resolution.md)
    
- [Postfach](mailbox.md)
    
- [Name (EmailAddressType)](name-emailaddresstype.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)
    
- [MailboxType](mailboxtype.md)
    
- [Contact](contact.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
- [EmailAddresses](emailaddresses.md)
    
- [Eintrag (EmailAddress)](entry-emailaddress.md)
    
- [ContactSource](contactsource.md)
    
## <a name="resolvenames-operation-error-response"></a>ResolveNames Vorgang Fehlerantwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort an eine Anforderung **ResolveNames** . Durch den Versuch, einen Namen aufzulösen, der nicht aufgelöst werden kann, wird der Fehler verursacht. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Error">
          <m:MessageText>No results were found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionNoResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Fehler Antwortelemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ResolveNamesResponse](resolvenamesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Siehe auch



[Der ExpandDL-Vorgang](expanddl-operation.md)


[Verwenden von namensauflösung](http://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

