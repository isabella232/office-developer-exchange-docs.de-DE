---
title: GetImItems-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 51186691-46d2-4d5c-b8bc-4ee2bb20fbe7
description: Hier finden Sie Informationen zum GetImItems EWS-Vorgang.
ms.openlocfilehash: fb9368d825880f5763ade8893585639e9b267540
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509854"
---
# <a name="getimitems-operation"></a>GetImItems-Vorgang

Hier finden Sie Informationen zum **GetImItems** EWS-Vorgang. 
  
Der **GetImItems-Vorgang** ruft Informationen zu Chatgruppen und Chatkontaktpersonas ab. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-getimitems-operation"></a>Verwenden des GetImItems-Vorgangs

Der **GetImItems-Vorgang** akzeptiert Gruppen- und Kontaktelementbezeichner und gibt eine Reihe von Informationen zu den Gruppen und Kontakten zurück. Die in der Antwort zurückgegebenen Eigenschaftensätze werden durch erweiterte Eigenschaften, mehrere Kontaktbezeichner, Gruppenbezeichner und erweiterte Eigenschaftsdefinitionen als Argumente identifiziert. 
  
### <a name="getimitems-operation-soap-headers"></a>SOAP-Header des GetImItems-Vorgangs

Der **GetImItems-Vorgang** kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dieser Header gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifiziert die Kultur, wie in RFC 3066 definiert, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden soll. Dieser Header gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Dieser Header gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dieser Header gilt für eine Antwort.  <br/> |
   
## <a name="getimitems-operation-request-example-get-detailed-information-about-im-contacts-and-groups"></a>GetImItems-Vorgangsanforderungsbeispiel: Abrufen detaillierter Informationen zu Chatkontakten und -gruppen

Das folgende Beispiel einer **GetImItems-Vorgangsanforderung** zeigt, wie Detaillierte Informationen zu Chatkontakten und -gruppen angefordert werden. Ein **GetImItems-Vorgang** kann einen oder mehrere Kontakt- oder Gruppendetails anfordern. Sie können auch erweiterte Eigenschaften verwenden, um benutzerdefinierte Eigenschaften für Gruppen und Kontakte abzurufen. Wenn für ein Element keine angeforderte erweiterte Eigenschaft vorhanden ist, ignoriert die Antwort die angeforderte Eigenschaft und gibt die Antwort für den Standardeigenschaftensatz zurück. In diesem Beispiel wird gezeigt, wie Sie den Anzeigenamen mithilfe erweiterter Eigenschaften abrufen. 
  
> [!NOTE]
> Alle Elementbezeichner und Änderungsschlüssel in diesem Artikel wurden gekürzt, um die Lesbarkeit zu gewährleisten. Beachten Sie, dass Änderungsschlüssel vom Dienst für diesen Vorgang ignoriert werden. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:GetImItems>
         <m:ContactIds>
            <t:ItemId Id="AAMkADEzOTExYACABmEhpSAAA=" ChangeKey="EQAAABBmNDjF"/>
         </m:ContactIds>
         <m:GroupIds>
            <t:ItemId Id="AAMkADEzOTExYjJkBY7+0EAAA=" ChangeKey="EgAAAA=="/>
         </m:GroupIds>         
         <m:ExtendedProperties>
            <t:ExtendedProperty PropertyTag="0x3001" PropertyType="String"/>
         </m:ExtendedProperties>
      </m:GetImItems>
   </soap:Body>
</soap:Envelope>
```

Der SOAP-Anforderungstext enthält die folgenden Elemente:
  
- [GetImItems](getimitems.md)
    
- [ContactIds](contactids.md)
    
- [ItemId](itemid.md)
    
- [GroupIds](groupids.md)
    
- [ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)](extendedproperties-nonemptyarrayofextendedfielduris.md)
    
- [ExtendedProperty (PathToExtendedFieldType)](extendedproperty-pathtoextendedfieldtype.md)
    
## <a name="successful-getimitems-operation-response"></a>Erfolgreiche GetImItems-Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetImItems-Anforderung** zum Abrufen eines Chatkontakts und einer Gruppe. Der Anzeigename wird in einer erweiterten Eigenschaft angefordert. Chatkontakte werden in Form einer Persona zurückgegeben. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetImItemsResponse ResponseClass="Success" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <ImItemList>
            <Groups xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <ImGroup>
                  <DisplayName>Exchange SDK Team</DisplayName>
                  <GroupType>IPM.DistList.MOC.UserGroup</GroupType>
                  <ExchangeStoreId Id="AAMkADEzQrAABY7+0EAAA=" ChangeKey="EgAAAA=="/>
                  <MemberCorrelationKey>
                     <ItemId Id="AAMkADEzOTExYjeGgGqm4QrAABmEhpSAAA=" ChangeKey="EQAAAA=="/>
                  </MemberCorrelationKey>
                  <ExtendedProperties>
                     <ExtendedProperty>
                        <ExtendedFieldURI PropertyTag="0x3001" PropertyType="String"/>
                        <Value>Exchange SDK Team</Value>
                     </ExtendedProperty>
                  </ExtendedProperties>
               </ImGroup>
            </Groups>
            <Personas xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Persona>
                  <PersonaId Id="AAQkADEzOTBZImBzN5J/uHXc="/>
                  <PersonaType>Person</PersonaType>
                  <CreationTime>2012-11-07T00:10:35Z</CreationTime>
                  <DisplayName>Tony Smith</DisplayName>
                  <DisplayNameFirstLast>Tony Smith</DisplayNameFirstLast>
                  <DisplayNameLastFirst>Tony Smith</DisplayNameLastFirst>
                  <FileAs/>
                  <FileAsId>None</FileAsId>
                  <ImAddress>tsmith@contoso.com</ImAddress>
                  <RelevanceScore>2147483647</RelevanceScore>
                  <Attributions>
                     <Attribution>
                        <Id>0</Id>
                        <SourceId Id="AAMkADEzhQaoeGgGqm4QrAABmEhpSAAA=" ChangeKey="EQArAABmNDjF"/>
                        <DisplayName>Lync Contacts</DisplayName>
                        <IsWritable>false</IsWritable>
                        <IsQuickContact>true</IsQuickContact>
                        <IsHidden>false</IsHidden>
                     </Attribution>
                  </Attributions>
                  <DisplayNames>
                     <StringAttributedValue>
                        <Value>Tony Smith</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </DisplayNames>
                  <FileAsIds>
                     <StringAttributedValue>
                        <Value>None</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </FileAsIds>
                  <ImAddresses>
                     <StringAttributedValue>
                        <Value>tsmith@contoso.com</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </ImAddresses>
                  <ExtendedProperties>
                     <ExtendedPropertyAttributedValue>
                        <Value>
                           <ExtendedFieldURI PropertyTag="0x3001" PropertyType="String"/>
                           <Value>Tony Smith</Value>
                        </Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </ExtendedPropertyAttributedValue>
                  </ExtendedProperties>
               </Persona>
            </Personas>
         </ImItemList>
      </GetImItemsResponse>
   </s:Body>
</s:Envelope>
```

Der SOAP-Antworttext enthält die folgenden Elemente:
  
- [GetImItemsResponse](getimitemsresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [ImItemList](imitemlist.md)
    
- [Gruppen (ArrayOfImGroupType)](groups-arrayofimgrouptype.md)
    
- [ImGroup](imgroup.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
- [GroupType](grouptype.md)
    
- [ExchangeStoreId](exchangestoreid.md)
    
- [MemberCorrelationKey](membercorrelationkey.md)
    
- [ItemId](itemid.md)
    
- [ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)](extendedproperties-nonemptyarrayofextendedfielduris.md)
    
- [ExtendedProperty (PathToExtendedFieldType)](extendedproperty-pathtoextendedfieldtype.md)
    
- [Personas](personas-ex15websvcsotherref.md)
    
- [PersonaId](personaid.md)
    
- [PersonaType](personatype.md)
    
- [CreationTime](creationtime.md)
    
- [DisplayNameFirstLast](displaynamefirstlast.md)
    
- [DisplayNameLastFirst](displaynamelastfirst.md)
    
- [FileAs](fileas.md)
    
- [FileAsId](fileasid.md) FileAsId 
    
- [ImAddress (Zeichenfolge)](imaddress-string.md)
    
- [RelevanceScore](relevancescore.md)
    
- [Attributions (ArrayOfPersonaAttributionsType)](attributions-arrayofpersonaattributionstype.md)
    
- [Attribution (PersonaAttributionType)](attribution-personaattributiontype.md)
    
- [ID (Zeichenfolge)](id-string.md)
    
- [SourceId](sourceid.md)
    
- [IsWritable](iswritable.md)
    
- [IsQuickContact](isquickcontact.md)
    
- [IsHidden](ishidden.md)
    
- [StringAttributedValue](stringattributedvalue.md)
    
- [FileAsIds](fileasids.md)
    
- [ImAddresses](imaddresses.md)
    
- [Wert (ExtendedPropertyType)](value-extendedpropertytype.md)
    
## <a name="getimitems-operation-error-response"></a>GetImItems-Vorgang – Fehlerantwort

Der **GetImItems-Vorgang** überprüft keine Bezeichner und gibt nicht die erwartete **ErrorInvalidImContactId-** oder **ErrorInvalidImGroupId-Fehlerantwort** zurück, wenn dem Dienst ein ungültiger Kontakt- oder Gruppenbezeichner bereitgestellt wird. 
  
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
    
- [GetImItemList-Vorgang](getimitemlist-operation.md)
    

