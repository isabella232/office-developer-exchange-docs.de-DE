---
title: GetItem-Vorgang (Kontakt)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: 6b96dace-1260-4b83-869a-7c31c5583daa
description: Der GetItem-Vorgang wird zum Abrufen von Kontaktelementen aus dem Exchange-Informationsspeicher verwendet.
ms.openlocfilehash: 93e8dbe28e130ab64d4b8d12d2befde1f77ae8fa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460022"
---
# <a name="getitem-operation-contact"></a>GetItem-Vorgang (Kontakt)

Der GetItem-Vorgang wird zum Abrufen von Kontaktelementen aus dem Exchange-Informationsspeicher verwendet.
  
## <a name="getitem-contact-request-example"></a>GetItem (Contact)-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird gezeigt, wie ein Element aus dem Exchange-Informationsspeicher abgerufen wird.
  
### <a name="code"></a>Code

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns='https://schemas.microsoft.com/exchange/services/2006/messages'>
      <ItemShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="AAAtAE=" ChangeKey="EQAAABY" />
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

Die Anforderung zum Abrufen eines Elements aus dem Exchange-Informationsspeicher verwendet dasselbe Formular für alle Elementtypen. Die Antworten auf Anforderungen für unterschiedliche Elemente unterscheiden sich, da unterschiedliche Elemente basierend auf den Antwort-Shapes unterschiedliche Informationen zurückgeben.
  
> [!NOTE]
> Die Element-ID wurde verkürzt, um die Lesbarkeit beizubehalten. 
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [GetItem](getitem.md)
    
- [ItemShape](itemshape.md)
    
- [BaseShape](baseshape.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="successful-getitem-contact-response"></a>Erfolgreiche GetItem-Antwort (Kontakt)

### <a name="description"></a>Beschreibung

Das folgende Codebeispiel zeigt eine erfolgreiche GetItem-Antwort für die **allproperties**-[BaseShape](baseshape.md).
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Contact>
              <t:ItemId Id="AAAtAEA=" ChangeKey="EQAAABYq" />
              <t:ParentFolderId Id="AQAtAEFk==" ChangeKey="AQAAAA==" />
              <t:ItemClass>IPM.Contact</t:ItemClass>
              <t:Sensitivity>Normal</t:Sensitivity>
              <t:Body BodyType="Text" />
              <t:DateTimeReceived>2006-08-18T17:31:18Z</t:DateTimeReceived>
              <t:Size>382</t:Size>
              <t:Importance>Normal</t:Importance>
              <t:IsSubmitted>false</t:IsSubmitted>
              <t:IsDraft>true</t:IsDraft>
              <t:IsFromMe>false</t:IsFromMe>
              <t:IsResend>false</t:IsResend>
              <t:IsUnmodified>false</t:IsUnmodified>
              <t:DateTimeSent>2006-08-18T17:31:18Z</t:DateTimeSent>
              <t:DateTimeCreated>2006-08-18T17:31:18Z</t:DateTimeCreated>
              <t:HasAttachments>false</t:HasAttachments>
              <t:Culture>en</t:Culture>
              <t:FileAs>SampleContact</t:FileAs>
              <t:FileAsMapping>None</t:FileAsMapping>
              <t:DisplayName>Tanja Plate</t:DisplayName>
              <t:GivenName>Tanja</t:GivenName>
              <t:Initials>T.P.</t:Initials>
              <t:CompleteName>
                <t:FirstName>Tanja</t:FirstName>
                <t:LastName>Plate</t:LastName>
                <t:Initials>T.P.</t:Initials>
                <t:FullName>Tanja Plate</t:FullName>
              </t:CompleteName>
              <t:CompanyName>Northwind Traders</t:CompanyName>
              <t:EmailAddresses>
                <t:Entry Key="EmailAddress1">tplate@example.com</t:Entry>
                <t:Entry Key="EmailAddress2">tplate@example.com</t:Entry>
              </t:EmailAddresses>
              <t:PhysicalAddresses>
                <t:Entry Key="Business">
                  <t:Street>12345 67th Ave</t:Street>
                  <t:City>Whittier</t:City>
                  <t:State>CA</t:State>
                  <t:Country>USA</t:Country>
                </t:Entry>
              </t:PhysicalAddresses>
              <t:PhoneNumbers>
                <t:Entry Key="BusinessPhone">5625550199</t:Entry>
              </t:PhoneNumbers>
              <t:JobTitle>Project Manager</t:JobTitle>
              <t:Surname>Plate</t:Surname>
            </t:Contact>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

Die Element-ID wurde verkürzt, um die Lesbarkeit beizubehalten.
  
### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

Die folgenden Elemente werden in der Antwort für eine GetItem-Anforderung mit der Antwort Form **allproperties** für ein Kontaktelement verwendet. 
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetItemResponse](getitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetItemResponseMessage](getitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Elemente](items.md)
    
- [Contact](contact.md)
    
- [ItemId](itemid.md)
    
- [ParentFolderId](parentfolderid.md)
    
- [ItemClass](itemclass.md)
    
- [Sensitivity](sensitivity.md)
    
- [Body](body.md)
    
- [DateTimeReceived](datetimereceived.md)
    
- [Größe](size.md)
    
- [Importance](importance.md)
    
- [Issubmitted](issubmitted.md)
    
- [IsDraft](isdraft.md)
    
- [Isfromme](isfromme.md)
    
- [IsResend](isresend.md)
    
- [IsUnmodified](isunmodified.md)
    
- [DateTimeSent](datetimesent.md)
    
- [DateTimeCreated](datetimecreated.md)
    
- [HasAttachments](hasattachments.md)
    
- [Kultur](culture.md)
    
- [FileAs](fileas.md)
    
- [FileAsMapping](fileasmapping.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
- [GivenName](givenname.md)
    
- [Initialen](initials.md)
    
- [Completename](completename.md)
    
- [FirstName](firstname.md)
    
- [LastName](lastname.md)
    
- [FullName](fullname.md)
    
- [CompanyName](companyname.md)
    
- [EmailAddresses](emailaddresses.md)
    
- [Eintrag (e-mailemail)](entry-emailaddress.md)
    
- [PhysicalAddresses](physicaladdresses.md)
    
- [Eintrag (PhysicalAddress)](entry-physicaladdress.md)
    
- [Straße](street.md)
    
- [City](city.md)
    
- [State](state-ex15websvcsotherref.md)
    
- [CountryOrRegion](countryorregion.md)
    
- [PhoneNumbers](phonenumbers.md)
    
- [Eingabe (Faxnummer)](entry-phonenumber.md)
    
- [JobTitle](jobtitle.md)
    
- [Nachname](surname.md)
    
## <a name="invalid-getitem-contact-request-example"></a>Ungültiges GetItem (Contact)-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Das folgende Codebeispiel zeigt eine ungültige Anforderung.
  
### <a name="code"></a>Code

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns='https://schemas.microsoft.com/exchange/services/2006/messages'>
      <ItemShape>
        <t:BaseShape>AllProperties</t:BaseShape>
        <t:IncludeMimeContent>true</t:IncludeMimeContent>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="AAAtAEF=" ChangeKey="EQAAABq" />
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

Element-IDs wurden verkürzt, um die Lesbarkeit zu erhalten.
  
## <a name="getitem-contact-error-response"></a>Fehlerantwort GetItem (Kontakt)

### <a name="description"></a>Beschreibung

Im folgenden Codebeispiel wird eine Fehlerantwort auf eine GetItem-Anforderung (Contact) angezeigt.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Error">
          <m:MessageText>Mime conversion is not supported for this item type.</m:MessageText>
          <m:ResponseCode>ErrorUnsupportedMimeConversion</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Items />
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Fehlerantwortelemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetItemResponse](getitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetItemResponseMessage](getitemresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Elemente](items.md)
    
## <a name="see-also"></a>Siehe auch



[GetItem-Vorgang](getitem-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

