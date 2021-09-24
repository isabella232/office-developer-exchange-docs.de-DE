---
title: ExpandDL-Vorgang
manager: sethgros
ms.date: 07/27/2018
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ExpandDL
api_type:
- schema
ms.assetid: 1f7837e7-9eff-4e10-9577-c40f7ed6af94
description: Der ExpandDL-Vorgang macht die vollständige Mitgliedschaft von Verteilerlisten verfügbar.
ms.openlocfilehash: 9878ecff0eeee1ef386c7bb26a092eec47f471de
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513780"
---
# <a name="expanddl-operation"></a>ExpandDL-Vorgang

Der ExpandDL-Vorgang macht die vollständige Mitgliedschaft von Verteilerlisten verfügbar.
  
## <a name="using-the-expanddl-web-method"></a>Verwenden der ExpandDL-Webmethode

Der ExpandDL-Vorgang verwendet den Webdienst, der sich in Exchange.asmx befindet. Diese Webdienstmethode akzeptiert ein [Mailbox-Element,](mailbox.md) das ein untergeordnetes [EmailAddress (NonEmptyStringType)-Element](emailaddress-nonemptystringtype.md) für eine Erweiterung einer öffentlichen Verteilerliste oder ein untergeordnetes [ItemId-Element](itemid.md) für die Erweiterung einer privaten Verteilerliste enthalten kann. 
  
Öffentliche Verteilerlisten können mit einer der folgenden Optionen erweitert werden:
  
1. Verteilerlistenalias
    
2. Die SMTP-Adresse (Simple Mail Transfer Protocol)
    
3. X400
    
4. X500
    
5. Exchange Legacyadresse
    
6. Der Name der Verteilerliste
    
7. Der Anzeigename
    
> [!IMPORTANT]
> Anzeigenamen sind nicht eindeutig. Mehrere Konten können denselben Anzeigenamen verwenden. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Rekursive Erweiterung wird nicht unterstützt. In einem einzigen Anruf kann nur eine Verteilerliste erweitert werden. Wenn mehrere Verteilerlisten den Kriterien entsprechen, meldet der Webdienst einen Fehler. Eine Clientanwendung kann mehrdeutige Namensauflösung (Ambiguous Name Resolution, ANR) verwenden, um mehrdeutige Verteilerlisten zu finden, und dann die richtige E-Mail-Adresse der erforderlichen Verteilerliste als Parameter für den [ExpandDL-Vorgang](expanddl-operation.md)auswählen. Weitere Informationen finden Sie unter [ResolveNames-Vorgang.](resolvenames-operation.md)
  
Öffentliche Verteilerlisten befinden sich in Active Directory. Dabei kann es sich um eine beliebige E-Mail-aktivierte oder dynamische Verteilergruppe handeln. Die Gruppe sollte nicht in der Adressliste ausgeblendet werden, und jedes Mitglied sollte über eine nicht leere E-Mail-Adresse verfügen. Mitglieder der Verteilerliste können E-Mail-aktivierte Benutzer und Kontakte, öffentliche Ordner und E-Mail-aktivierte Verteilerlisten und dynamische Gruppen sein.
  
Private Verteilerlisten befinden sich im Ordner "Kontakte" des Postfachs eines Benutzers. Private Verteilerlisten verfügen nicht über E-Mail-Adressen, sodass ihre Store-Elementbezeichner in einer ExpandDL-Anforderung verwendet werden. Mitglieder einer privaten Verteilerliste können beliebige E-Mail-aktivierte Benutzer, Kontakte oder Verteilerlisten aus Active Directory oder Kontakte oder private Verteilerlisten aus dem Kontaktordner eines Benutzers sein.
  
Bei Kontakten oder privaten Verteilerlisten werden die Elementbezeichner in der Antwort zurückgegeben. Dies kann verwendet werden, um Informationen über das Objekt abzurufen oder die Mitgliedschaft in einer privaten Verteilerliste zu erweitern.
  
## <a name="expanddl-private-distribution-list-request-example"></a>ExpandDL Private Distribution List -Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer ExpandDL-Anforderung zeigt, wie Sie eine Anforderung zum Erweitern einer privaten Verteilerliste erstellen.
  
### <a name="code"></a>Code

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:ExpandDL>
      <m:Mailbox>
       <t:EmailAddress>test</t:EmailAddress>
      </m:Mailbox>
    </m:ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

Um eine private Verteilerliste zu erweitern, enthält das [Mailbox-Element](mailbox.md) das [ItemId-Element,](itemid.md) das eine private Verteilerliste im Postfach des Benutzers identifiziert. 
  
## <a name="expanddl-public-distribution-list-request-example"></a>Beispiel für anforderungsbasierte ExpandDL Public Distribution List

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer ExpandDL-Anforderung zeigt, wie Sie eine Anforderung zum Erweitern einer öffentlichen Verteilerliste erstellen. Das Beispiel zeigt die Verwendung eines Anzeigenamens zum Erweitern einer Verteilerliste.
  
### <a name="code"></a>Code

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
        <t:Mailbox>
          <t:EmailAddress>TheDistributionList</t:EmailAddress>
        </t:Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

Die Antwort auf diese Anforderung enthält **Postfachelemente,** die jedes Postfach in der Verteilerliste identifizieren. Wenn eine Verteilerliste in einer Verteilerliste enthalten ist, muss eine separate Verteilerlistenerweiterung für die eingebettete Verteilerliste ausgeführt werden. Wenn die Verteilerliste keine Mitglieder hat oder die angeforderte Verteilerliste nicht vorhanden ist, enthält das **ResponseClass-Attribut** den Wert "Success". 
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [ExpandDL](expanddl.md)
    
- [Postfach](mailbox.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) wird verwendet, um öffentliche Verteilerlisten zu identifizieren. Das [ItemId-Element](itemid.md) wird verwendet, um private Verteilerlisten zu identifizieren. 
    
> [!NOTE]
> Das Schema, das diese Elemente beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem MicrosoftExchange Server 2007 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist. 
  
## <a name="successful-expanddl-response-example"></a>Beispiel für erfolgreiche ExpandDL-Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer ExpandDL-Antwort zeigt eine Antwort auf die oben beschriebene Anforderung. Die Erweiterung der Verteilerliste beschreibt Folgendes: 
  
- Die Anzahl der Mitglieder der Verteilerliste, die in der Antwort zurückgegeben werden.
    
- Gibt an, ob die Antwort alle Mitglieder der Verteilerliste enthält.
    
- Der Name des Postfachs.
    
- Die E-Mail-Adresse des Postfachs.
    
- Der Routingtyp für das Postfach.
    
- Der Postfachtyp.
    
> [!NOTE]
> Der Name der Verteilerliste ist in der Antwort nicht enthalten. Daher müssen Sie den Namen aus der Anforderung nachverfolgen. 
  
### <a name="code"></a>Code

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ExpandDLResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DLExpansion TotalItemsInView="3" IncludesLastItemInRange="true">
            <t:Mailbox>
              <t:Name>Dan Park</t:Name>
              <t:EmailAddress>dpark@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
            <t:Mailbox>
              <t:Name>Jeff Price</t:Name>
              <t:EmailAddress>jprice@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
            <t:Mailbox>
              <t:Name>Tanja Plate</t:Name>
              <t:EmailAddress>tplate@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
          </m:DLExpansion>
        </m:ExpandDLResponseMessage>
      </m:ResponseMessages>
    </ExpandDLResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ExpandDLResponse](expanddlresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [DLExpansion](dlexpansion.md)
    
- [Postfach](mailbox.md)
    
- [Name (EmailAddressType)](name-emailaddresstype.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)
    
- [MailboxType](mailboxtype.md)
    
Weitere Optionen für die Antwortnachricht des ExpandDL-Vorgangs finden Sie in der Schemahierarchie. Beginnen Sie mit dem [ExpandDLResponse-Element.](expanddlresponse.md) 
  
## <a name="expanddl-error-response"></a>ExpandDL-Fehlerantwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort auf eine ExpandDL-Anforderung.
  
### <a name="code"></a>Code

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ExpandDLResponseMessage ResponseClass="Error">
          <m:MessageText>No results are found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionNoResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ExpandDLResponseMessage>
      </m:ResponseMessages>
    </ExpandDLResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Fehlerantwortelemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ExpandDLResponse](expanddlresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Weitere Optionen für die Antwortnachricht des ExpandDL-Vorgangs finden Sie in der Schemahierarchie. Beginnen Sie mit dem [ExpandDLResponse-Element.](expanddlresponse.md) 
  
## <a name="see-also"></a>Siehe auch

- [ResolveNames-Vorgang](resolvenames-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

