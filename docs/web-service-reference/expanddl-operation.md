---
title: Der ExpandDL-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExpandDL
api_type:
- schema
ms.assetid: 1f7837e7-9eff-4e10-9577-c40f7ed6af94
description: Der Vorgang der ExpandDL werden sämtliche Mitglieder von Verteilerlisten verfügbar gemacht.
ms.openlocfilehash: e4654120881f81a79358e0e7c0ab016f94db3288
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758321"
---
# <a name="expanddl-operation"></a>Der ExpandDL-Vorgang

Der Vorgang der ExpandDL werden sämtliche Mitglieder von Verteilerlisten verfügbar gemacht.
  
## <a name="using-the-expanddl-web-method"></a>Verwenden der Web der ExpandDL-Methode

Der Vorgang der ExpandDL verwendet den Webdienst, der sich in besteht befindet. Diese Webdienstmethode akzeptiert ein [Postfach](mailbox.md) -Element, das entweder ein untergeordnetes Element [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) , für eine Erweiterung von Verteilerlisten öffentlichen oder ein untergeordnetes Element [ItemId](itemid.md) , für die Erweiterung von einem privaten enthalten kann Verteilerliste. 
  
Öffentliche Verteilerlisten können mithilfe einer der folgenden erweitert werden:
  
1. Verteilung Liste alias
    
2. Die Adresse des Simple Mail Transfer Protocol (SMTP)
    
3. X400
    
4. X500
    
5. Exchange-Legacy-Adresse
    
6. Der Name der Verteilerliste
    
7. Der Anzeigename
    
> [!IMPORTANT]
> Anzeigenamen sind nicht eindeutig. Mehrere Konten können demselben Anzeigenamen freigeben. 
  
## <a name="remarks"></a>Hinweise

Rekursive Erweiterung wird nicht unterstützt. In einem einzigen Aufruf kann nur eine Verteilerliste erweitert werden. Wenn mehr als eine Verteilerliste die Kriterien übereinstimmen, meldet der Webdienst einen Fehler. Eine Clientanwendung können Auflösung nicht eindeutiger Namen (ANR), um mehrdeutige Verteilung aufgelistet und ausgewählt haben die richtige E-mail-Adresse der erforderlichen Verteilerliste als Parameter für den [Vorgang der ExpandDL](expanddl-operation.md)zu erhalten. Weitere Informationen finden Sie unter [ResolveNames Vorgang](resolvenames-operation.md).
  
Öffentliche Verteilerlisten befinden sich in Active Directory. Sie können eine beliebige e-Mail-aktivierten oder dynamische Verteilergruppe sein. Die Gruppe aus der Liste nicht ausgeblendet werden sollen, und jedes Element eine nicht leere E-mail-Adresse haben. Mitglieder der Verteilerliste können e-Mail-aktivierte Benutzer und Kontakte, öffentlichen Ordnern und e-Mail-aktivierten Verteilerlisten und dynamische Gruppen sein.
  
Private Verteilerlisten befinden sich im Ordner Kontakte des Postfachs eines Benutzers. Private Verteilerlisten haben keine e-Mail-Adressen, so dass ihre Store Element-IDs in einer Anforderung der ExpandDL verwendet werden. Mitglieder von Verteilerlisten private können eine beliebige e-Mail-aktivierten Benutzer, Kontakte oder Verteilerlisten aus Active Directory oder Kontakte oder private Verteilerlisten aus Kontakteordner eines Benutzers enthält.
  
Element-IDs werden für Kontakte oder private Verteilerlisten in der Antwort zurückgegeben. Dies kann zum Abrufen von Informationen über das Objekt oder die Mitgliedschaft in einer privaten Verteilerliste erweitern verwendet werden.
  
## <a name="expanddl-private-distribution-list-request-example"></a>Anforderungsbeispiel der ExpandDL Private Verteilerliste

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird einer der ExpandDL Anforderung veranschaulicht eine Anforderung an eine Verteilerliste privat erweitert bilden.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
        <t:Mailbox>
          <t:ItemId Id="xASUAd==" ChangeKey="AAts0Q=="/>
        </t:Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Kommentare

Um eine private Verteilerliste zu erweitern, wird das [Postfach](mailbox.md) -Element das [ItemId](itemid.md) -Element enthalten, das eine private Verteilerliste in das Postfach des Benutzers bezeichnet. 
  
## <a name="expanddl-public-distribution-list-request-example"></a>Öffentliche Verteilerliste der ExpandDL anforderungsbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird einer der ExpandDL Anforderung veranschaulicht eine Anforderung an eine öffentliche Verteilerliste erweitern bilden. Im Beispiel wird die Verwendung eines Anzeigenamens erweitern eine Verteilerliste.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
        <t:Mailbox>
          <t:EmailAddress>TheDistributionList</t:EmailAddress>
        </t:Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Kommentare

Die Antwort auf diese Anforderung wird **Postfach** Elemente enthalten, die jedes Postfach in der Verteilerliste zu identifizieren. Wenn eine Verteilerliste in einer Verteilerliste enthalten ist, muss eine separate Verteilerlistenerweiterung auf die eingebettete Verteilerliste ausgeführt werden. Wenn die Verteilerliste keine Mitglieder enthält, oder die angeforderte Verteilerliste ist nicht vorhanden, wird das Attribut **ResponseClass** einen Erfolg gleich Wert enthalten. 
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [Der ExpandDL](expanddl.md)
    
- [Postfach](mailbox.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) wird verwendet, um öffentliche Verteilerlisten zu identifizieren. Das [ItemId](itemid.md) -Element wird verwendet, um private Verteilerlisten zu identifizieren. 
    
> [!NOTE]
> Das Schema, das diese Elemente beschreibt, befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem MicrosoftExchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist. 
  
## <a name="successful-expanddl-response-example"></a>Erfolgreiche der ExpandDL antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel für eine Antwort der ExpandDL zeigt eine Antwort auf die oben beschriebenen Anforderung. Die Erweiterung der Verteilerliste wird Folgendes beschrieben: 
  
- Die Anzahl der Mitglieder der Verteilerliste, die in der Antwort zurückgegeben werden.
    
- Gibt an, ob die Antwort alle Mitglieder der Verteilerliste enthält.
    
- Der Name des Postfachs an.
    
- Die e-Mail-Adresse des Postfachs an.
    
- Der Routingtyp für das Postfach.
    
- Der Typ des Postfachs.
    
> [!NOTE]
> Der Name der Verteilerliste ist nicht in der Antwort enthalten; aus diesem Grund, Sie müssen den Namen aus der Anforderung mitverfolgen. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a>Elemente einer erfolgreichen Antwort

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
    
Wenn andere Optionen für die Antwortnachricht des Vorgangs der ExpandDL suchen möchten, verwenden Sie die Schemahierarchie. Starten Sie das [ExpandDLResponse](expanddlresponse.md) -Element. 
  
## <a name="expanddl-error-response"></a>Der ExpandDL Fehlerantwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort auf eine Anforderung der ExpandDL.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a>Fehler Antwortelemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ExpandDLResponse](expanddlresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Wenn andere Optionen für die Antwortnachricht des Vorgangs der ExpandDL suchen möchten, verwenden Sie die Schemahierarchie. Starten Sie das [ExpandDLResponse](expanddlresponse.md) -Element. 
  
## <a name="see-also"></a>Siehe auch

- [ResolveNames-Vorgang](resolvenames-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

