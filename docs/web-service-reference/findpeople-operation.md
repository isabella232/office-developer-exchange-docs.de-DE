---
title: FindPeople-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 446106b7-ff2d-4107-90c1-29f4d38ba128
description: Hier finden Sie Informationen über die FindPeople EWS Vorgang.
ms.openlocfilehash: 97c34d7df590d20513e8f1ad476d62f16815a42b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758474"
---
# <a name="findpeople-operation"></a>FindPeople-Vorgang

Hier finden Sie Informationen zum **FindPeople** EWS-Vorgang. 
  
Der Vorgang **FindPeople** alle Persona-Objekte aus einem angegebenen Kontakteordner zurückgegeben oder abgerufen Kontakte, die mit eine Zeichenfolge der angegebenen Abfrage übereinstimmen. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-findpeople-operation"></a>Verwenden des FindPeople-Vorgangs

Der Vorgang **FindPeople** gibt aggregierten Kontaktinformationen zurück. 
  
Der Vorgang **FindPeople** basiert auf der vorhandenen Funktionalität der [Einschränkung](restriction.md) und [BaseShape](baseshape.md) komplexen Typen durch Hinzufügen einer Einschränkung Aggregation und die Möglichkeit, zusätzliche Eigenschaften zurückgeben. Mithilfe einer Einschränkung kann einen Client wie beispielsweise "nur Ergebnisse zurück, die eine IM-Adresse haben" Filter angeben. Das Standardverhalten für die Suche beruht auf das angegebene Postfach des Benutzers persönliche und der globalen Adressliste (GAL). Bei der Suche der globalen Adressliste als primäre Suchordner müssen Sie eine Abfragezeichenfolge anstelle einer Einschränkung angeben, da dieser Vorgang nicht, zum Durchsuchen der globalen Adressliste zulässt. 
  
### <a name="findpeople-operation-soap-headers"></a>FindPeople Vorgang SOAP-Header

Der Vorgang **FindPeople** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |["ExchangeImpersonation"](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="findpeople-operation-request-example"></a>FindPeople Vorgang anforderungsbeispiel

Im folgenden Beispiel wird eine **FindPeople** Vorgang Anforderung zeigt, wie die ersten 100 Kontakte aus dem Ordner Kontakte zurückgegeben. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:FindPeople>
         <m:IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="100" Offset="0"/>
         <m:ParentFolderId>
            <t:DistinguishedFolderId Id="contacts"/>
         </m:ParentFolderId>
      </m:FindPeople>
   </soap:Body>
</soap:Envelope>
```

Die Anforderung SOAP-Text enthält die folgenden Elemente:
  
- [FindPeople](findpeople.md)
    
- [IndexedPageItemView](indexedpageitemview.md)
    
- [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
Im folgenden Beispiel wird eine **FindPeople** Vorgang Anforderung veranschaulicht die ersten 100 Kontakte aus der globalen Adressliste zurückgeben, indem Sie eine Abfragezeichenfolge. Festlegen der **DistinguishedFolderId** "Verzeichnis" wird die globalen Adressliste als primäre Datenquelle Rollen gesucht. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
    <m:FindPeople>
      <m:PersonaShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="persona:DisplayName"/>
          <t:FieldURI FieldURI="persona:Title"/>
        </t:AdditionalProperties>
      </m:PersonaShape>
      <m:IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="100" Offset="0"/>
      <m:ParentFolderId>
        <t:DistinguishedFolderId Id="directory"/>
      </m:ParentFolderId>
      <m:QueryString>adams</m:QueryString>
    </m:FindPeople>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-findpeople-operation-response"></a>Erfolgreiche FindPeople Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **FindPeople** Vorgang an. 
  
```XML
<?xml version="1.0" encoding="utf-8"?><s:Envelope 
   xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="349" 
                         MinorBuildNumber="0" 
                         Version="Exchange2013" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <FindPeopleResponse ResponseClass="Success" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <People>
        <Persona xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <PersonaId Id="AAQkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04ZjU5LWI3MTYzNGNkZmRkYQAQAOjFqObcLmtOlzlRnHdXQjo=" />
          <CreationTime>2012-01-11T22:25:37Z</CreationTime>
          <DisplayName>Terry Adams</DisplayName>
          <DisplayNameFirstLast>Terry Adams</DisplayNameFirstLast>
          <DisplayNameLastFirst>Adams Terry</DisplayNameLastFirst>
          <FileAs>Adams, Terry</FileAs>
          <GivenName>Terry</GivenName>
          <Surname>Adams</Surname>
          <EmailAddress>
            <Name>terry@litwareinc.com</Name>
            <EmailAddress>terry@litwareinc.com</EmailAddress>
            <RoutingType>SMTP</RoutingType>
          </EmailAddress>
          <EmailAddresses>
            <EmailAddress>
              <Name>terry@litwareinc.com</Name>
              <EmailAddress>terry@litwareinc.com</EmailAddress>
              <RoutingType>SMTP</RoutingType>
            </EmailAddress>
            <EmailAddress>
              <Name>tadams@contoso.com</Name>
              <EmailAddress>tadams@contoso.com</EmailAddress>
              <RoutingType>SMTP</RoutingType>
            </EmailAddress>
          </EmailAddresses>
          <RelevanceScore>2147483647</RelevanceScore>
        </Persona>
      </People>
      <TotalNumberOfPeopleInView>1</TotalNumberOfPeopleInView>
    </FindPeopleResponse>
  </s:Body>
</s:Envelope>
```

Die Antwort SOAP-Text enthält die folgenden Elemente:
  
- [FindPeopleResponse](findpeopleresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [Personen](people.md)
    
- [Rolle](persona.md)
    
- [PersonaId](personaid.md)
    
- [CreationTime](creationtime.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
- [DisplayNameFirstLast](displaynamefirstlast.md)
    
- [DisplayNameLastFirst](displaynamelastfirst.md)
    
- [FileAs](fileas.md)
    
- [Vorname](givenname.md)
    
- [Nachname](surname.md)
    
- [EmailAddresses (ArrayOfEmailAddressesType)](emailaddresses-arrayofemailaddressestype.md)
    
- [EmailAddress (EmailAddressType)](emailaddress-emailaddresstype.md)
    
- [Name (EmailAddressType)](name-emailaddresstype.md)
    
- [EmailAddress (EmailAddressType)](emailaddress-emailaddresstype.md)
    
- [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)
    
- [RelevanceScore](relevancescore.md)
    
- [TotalNumberOfPeopleInView](totalnumberofpeopleinview.md)
    
## <a name="findpeople-operation-error-response"></a>FindPeople Vorgang Fehlerantwort

Fehlercodes, die für EWS generisch sind, finden Sie unter [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Siehe auch

- [Benutzer und Kontakte in EWS in Exchange](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [GetPersona-Vorgang](getpersona-operation.md)
    

