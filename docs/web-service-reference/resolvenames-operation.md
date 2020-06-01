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
description: Mit dem ResolveNames-Vorgang werden Mehrdeutige e-Mail-Adressen und Anzeigenamen aufgelöst.
ms.openlocfilehash: 51728addddd2bfb9d35b874ae8c11e83a4c8629b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468278"
---
# <a name="resolvenames-operation"></a>ResolveNames-Vorgang

Mit dem **ResolveNames** -Vorgang werden Mehrdeutige e-Mail-Adressen und Anzeigenamen aufgelöst. 
  
## <a name="using-the-resolvenames-operation"></a>Verwenden des ResolveNames-Vorgangs

Dieser Vorgang kann verwendet werden, um Aliase zu überprüfen und Anzeigenamen in den entsprechenden Postfachbenutzer aufzulösen. Wenn keine eindeutigen Namen vorhanden sind, enthält die **ResolveNames** -Vorgangs Antwortinformationen zu den einzelnen Postfachbenutzern, sodass die Clientanwendung die Namen auflösen kann. 
  
## <a name="remarks"></a>Bemerkungen

Die ResolveNames-Antwort gibt maximal 100 Kandidaten zurück. Die 100 Kandidaten, die zurückgegeben werden, sind die ersten 100, die im Nachschlagevorgang gefunden werden.
  
E-Mail-Adressen mit vorfixierten Routing Typen wie SMTP oder SIP werden in einem mehrwertigen Array gespeichert. Der **ResolveNames** -Vorgang führt eine partielle Übereinstimmung mit jedem Wert dieses Arrays aus, wenn Sie den Routingtyp am Anfang des nicht aufgelösten namens hinzufügen, beispielsweise "SIP:user1@contoso.com". Wenn Sie keinen Routingtyp angeben, wird **ResolveNames** standardmäßig mit dem Routingtyp SMTP, mit einer primären SMTP-Adress Eigenschaft übereinstimmen und nicht mit dem mehrwertigen Array durchsuchen. 
  
In einer einzelnen Anforderung kann nur ein eindeutiger Name angegeben werden. Active Directory wird zuerst durchsucht, und dann wird der Kontaktordner des Benutzers durchsucht. Aufgelöste Einträge aus dem Kontaktordner eines Benutzers weisen eine **ItemID** -Eigenschaft ungleich NULL auf, die dann in einer GetItem-Anforderung verwendet werden kann. Wenn es sich um die ID einer privaten Verteilerliste handelt, kann Sie in einem ExpandDL- [Vorgang](expanddl-operation.md)verwendet werden. Wenn das **ReturnFullContactData** -Attribut auf **true**festgelegt ist, werden Active Directory Einträge, die mit dem **ResolveNames** -Vorgang gefunden werden, zusätzliche Eigenschaften zurückgegeben, die einen [Kontakt](contact.md)beschreiben. Das **ReturnFullContactData** -Attribut wirkt sich nicht auf die Daten aus, die für Kontakte und private Verteilerlisten aus dem Kontaktordner des Benutzers zurückgegeben werden. 
  
## <a name="resolvenames-request-example"></a>ResolveNames-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer **ResolveNames** -Anforderung zeigt, wie Sie den Eintrag des Benutzers auflösen.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>User2</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

Die Antwort auf diese Anforderung gibt alle Einträge zurück, die mit "Jo" oder "Mi" beginnen. Bei den zurückgegebenen Elementen handelt es sich um öffentliche Postfächer, öffentliche und private Verteilerlisten und Kontakte.
  
> [!NOTE]
> Es werden nur Kontakte im Standardordner für persönliche Kontakte durchsucht. 
  
Es folgen die möglichen Ergebnisse für eine **ResolveNames** -Anforderung: 
  
- Antworten, die keine aufgelöste Entität enthalten, geben einen **ResponseClass** -Attributwert zurück, der **Error**entspricht. Das **MessageText** -Element enthält " **keine Ergebnisse werden gefunden**".
    
- Antworten, die eine einzelne aufgelöste Entität enthalten, geben einen **ResponseClass** -Attributwert zurück, der " **Success**" entspricht.
    
- Antworten, die mehrere mögliche Entitäten enthalten, geben einen **ResponseClass** -Attributwert zurück, der der **Warnung**entspricht. In diesem Fall konnte die Entität nicht in eine eindeutige Identität aufgelöst werden. Das **MessageText** -Element enthält "mehrere Ergebnisse werden gefunden." 
    
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [ResolveNames](resolvenames.md)
    
- [UnresolvedEntry](unresolvedentry.md)
    
## <a name="successful-resolvenames-operation-response-example"></a>Beispiel für erfolgreiche ResolveNames-Vorgangs Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **ResolveNames** -Anforderung. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-resolvenames-response-elements"></a>Erfolgreiche ResolveNames-Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ResolveNamesResponse](resolvenamesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Resolutionset](resolutionset.md)
    
- [Lösung](resolution.md)
    
- [Postfach](mailbox.md)
    
- [Name (EmailAddressType)](name-emailaddresstype.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [Routingtype (e-mailemailtype)](routingtype-emailaddresstype.md)
    
- [MailboxType](mailboxtype.md)
    
- [Kontakt](contact.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
- [EmailAddresses](emailaddresses.md)
    
- [Eintrag (e-mailemail)](entry-emailaddress.md)
    
- [ContactSource](contactsource.md)
    
## <a name="resolvenames-operation-error-response"></a>Fehlerantwort des ResolveNames-Vorgangs

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **ResolveNames** -Anforderung. Der Fehler wird verursacht, indem versucht wird, einen Namen aufzulösen, der nicht aufgelöst werden kann. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a>Fehlerantwortelemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ResolveNamesResponse](resolvenamesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Siehe auch



[ExpandDL-Vorgang](expanddl-operation.md)


[Verwenden der Namensauflösung](https://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

