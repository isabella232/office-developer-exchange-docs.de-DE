---
title: ResolveNames-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: 6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb
description: Der ResolveNames-Vorgang löst mehrdeutige E-Mail-Adressen und Anzeigenamen auf.
ms.openlocfilehash: f5ab0e3ee23cc085d8aa425c6eeb0ac7c392b9bb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509448"
---
# <a name="resolvenames-operation"></a>ResolveNames-Vorgang

Der **ResolveNames-Vorgang** löst mehrdeutige E-Mail-Adressen und Anzeigenamen auf. 
  
## <a name="using-the-resolvenames-operation"></a>Verwenden des ResolveNames-Vorgangs

Dieser Vorgang kann verwendet werden, um Aliase zu überprüfen und Anzeigenamen für den entsprechenden Postfachbenutzer aufzulösen. Wenn mehrdeutige Namen vorhanden sind, stellt die **ResolveNames-Vorgangsantwort** Informationen zu jedem Postfachbenutzer bereit, sodass die Clientanwendung die Namen auflösen kann. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die ResolveNames-Antwort gibt maximal 100 Kandidaten zurück. Die 100 zurückgegebenen Kandidaten sind die ersten 100, die beim Nachschlagevorgang aufgetreten sind.
  
E-Mail-Adressen mit Routingtypen mit Präfix, z. B. SMTP oder SIP, werden in einem mehrwertigen Array gespeichert. Der **ResolveNames-Vorgang** führt eine partielle Übereinstimmung mit jedem Wert dieses Arrays aus, wenn Sie den Routingtyp am Anfang des nicht aufgelösten Namens hinzufügen, z. B. "sip:User1@Contoso.com". Wenn Sie keinen Routingtyp angeben, verwendet **ResolveNames** standardmäßig den Routingtyp von SMTP, gleicht ihn mit einer primären SMTP-Adresseigenschaft ab und durchsucht nicht das mehrwertige Array. 
  
In einer einzigen Anforderung kann nur ein mehrdeutiger Name angegeben werden. Active Directory wird zuerst durchsucht, und dann wird der Kontaktordner des Benutzers durchsucht. Aufgelöste Einträge aus dem Kontaktordner eines Benutzers weisen eine **ItemId-Eigenschaft** ungleich NULL auf, die dann in einer GetItem-Anforderung verwendet werden kann. Wenn es sich um die ID einer privaten Verteilerliste handelt, kann sie in einem [ExpandDL-Vorgang](expanddl-operation.md)verwendet werden. Wenn das **ReturnFullContactData-Attribut** auf **"true"** festgelegt ist, geben Active Directory-Einträge, die mit dem **ResolveNames-Vorgang** gefunden wurden, zusätzliche Eigenschaften zurück, die ein [Contact](contact.md)-Objekt beschreiben. Das **ReturnFullContactData-Attribut** wirkt sich nicht auf die Daten aus, die für Kontakte und private Verteilerlisten aus dem Kontaktordner des Benutzers zurückgegeben werden. 
  
## <a name="resolvenames-request-example"></a>ResolveNames-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer **ResolveNames-Anforderung** zeigt, wie der Eintrag des Benutzers aufgelöst wird.
  
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

Die Antwort auf diese Anforderung gibt alle Einträge zurück, die mit "Jo" oder "Mi" beginnen. Die zurückgegebenen Elemente sind öffentliche Postfächer, öffentliche und private Verteilerlisten und Kontakte.
  
> [!NOTE]
> Es werden nur Kontakte im persönlichen Standardordner "Kontakte" durchsucht. 
  
Es folgen die möglichen Ergebnisse für eine **ResolveNames-Anforderung:** 
  
- Antworten, die keine aufgelöste Entität enthalten, geben einen **ResponseClass-Attributwert** zurück, der dem **Fehler** entspricht. Das **MessageText-Element** enthält **"Keine Ergebnisse wurden gefunden".**
    
- Antworten, die eine einzelne aufgelöste Entität enthalten, geben einen **ResponseClass-Attributwert** zurück, der **"Success"** entspricht.
    
- Antworten, die mehrere mögliche Entitäten enthalten, geben einen **ResponseClass-Attributwert** zurück, der der **Warnung** entspricht. In diesem Fall konnte die Entität nicht in eine eindeutige Identität aufgelöst werden. Das **MessageText-Element** enthält "Mehrere Ergebnisse wurden gefunden". 
    
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [ResolveNames](resolvenames.md)
    
- [UnresolvedEntry](unresolvedentry.md)
    
## <a name="successful-resolvenames-operation-response-example"></a>Beispiel für erfolgreiche ResolveNames-Vorgangsantwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **ResolveNames-Anforderung.** 
  
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
    
## <a name="resolvenames-operation-error-response"></a>ResolveNames-Vorgang – Fehlerantwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **ResolveNames-Anforderung.** Der Fehler wird durch den Versuch verursacht, einen Namen aufzulösen, der nicht aufgelöst werden kann. 
  
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

