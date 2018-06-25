---
title: GetImItems-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 51186691-46d2-4d5c-b8bc-4ee2bb20fbe7
description: Hier finden Sie Informationen über die GetImItems EWS Vorgang.
ms.openlocfilehash: 4335cc22b22dc5f102f2221f7fdb22a506ba026f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758701"
---
# <a name="getimitems-operation"></a>GetImItems-Vorgang

Hier finden Sie Informationen zum **GetImItems** EWS-Vorgang. 
  
Der Vorgang **GetImItems** werden Informationen zu instant messaging (IM) Gruppen abgerufen und Sofortnachrichten wenden Sie sich an Rollen. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-getimitems-operation"></a>Verwenden des GetImItems-Vorgangs

Der **GetImItems** -Vorgang akzeptiert, Gruppen- und Element-IDs und gibt einen Satz von Informationen zu den Gruppen und Kontakte. Die in der Antwort zurückgegebenen Eigenschaftensätze werden durch erweiterte Eigenschaften, mehrere Kontakt-IDs, Gruppen-IDs identifiziert und erweiterte Eigenschaftsdefinitionen als Argumente. 
  
### <a name="getimitems-operation-soap-headers"></a>GetImItems Vorgang SOAP-Header

Der Vorgang **GetImItems** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |["ExchangeImpersonation"](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="getimitems-operation-request-example-get-detailed-information-about-im-contacts-and-groups"></a>GetImItems Vorgang-anforderungsbeispiel: Abrufen detaillierter Informationen zu Instant Messaging-Kontakten und Gruppen

Im folgenden Beispiel wird eine **GetImItems** Vorgang Anforderung veranschaulicht, wie zur Anforderung detaillierte Informationen zu Instant Messaging-Kontakte und Gruppen. Ein Vorgang **GetImItems** kann anfordern mindestens einen Kontakt oder eine Gruppe von Details. Sie können auch erweiterte Eigenschaften verwenden, benutzerdefinierte Eigenschaften auf Gruppen und Kontakte abgerufen. Wenn eine angeforderte erweiterte Eigenschaft nicht für ein Element vorhanden ist, wird die Antwort ignorieren angeforderte Eigenschaft und die Antwort für die standardmäßigen-Eigenschaft zurückgegeben. Dieses Beispiel zeigt, wie den Anzeigenamen mithilfe von erweiterten Eigenschaften abrufen. 
  
> [!NOTE]
> Bezeichner für alle Elemente aus, und Ändern von Schlüsseln in diesem Artikel wurde gekürzt, um die Lesbarkeit zu erhalten. Notiz, die Tasten ändern, werden vom Dienst für diesen Vorgang ignoriert. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

Die Anforderung SOAP-Text enthält die folgenden Elemente:
  
- [GetImItems](getimitems.md)
    
- [ContactIds](contactids.md)
    
- [ItemId](itemid.md)
    
- [GroupIds](groupids.md)
    
- [ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)](extendedproperties-nonemptyarrayofextendedfielduris.md)
    
- [ExtendedProperty (PathToExtendedFieldType)](extendedproperty-pathtoextendedfieldtype.md)
    
## <a name="successful-getimitems-operation-response"></a>Erfolgreiche GetImItems Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **GetImItems** , um eine im-Kontakt und Gruppe zu erhalten. Der Anzeigename wird in einer erweiterten Eigenschaft angefordert. Im-Kontakte werden in Form einer Rolle zurückgegeben. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetImItemsResponse ResponseClass="Success" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <ImItemList>
            <Groups xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
            <Personas xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

Die Antwort SOAP-Text enthält die folgenden Elemente:
  
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
    
- [Rollen](personas-ex15websvcsotherref.md)
    
- [PersonaId](personaid.md)
    
- [PersonaType](personatype.md)
    
- [CreationTime](creationtime.md)
    
- [DisplayNameFirstLast](displaynamefirstlast.md)
    
- [DisplayNameLastFirst](displaynamelastfirst.md)
    
- [FileAs](fileas.md)
    
- [FileAsId](fileasid.md) FileAsId 
    
- [ImAddress (Zeichenfolge)](imaddress-string.md)
    
- [RelevanceScore](relevancescore.md)
    
- [Hinweise (ArrayOfPersonaAttributionsType)](attributions-arrayofpersonaattributionstype.md)
    
- [Zuweisung (PersonaAttributionType)](attribution-personaattributiontype.md)
    
- [ID (Zeichenfolge)](id-string.md)
    
- [SourceId](sourceid.md)
    
- [IsWritable](iswritable.md)
    
- [IsQuickContact](isquickcontact.md)
    
- [IsHidden](ishidden.md)
    
- [StringAttributedValue](stringattributedvalue.md)
    
- [FileAsIds](fileasids.md)
    
- [ImAddresses](imaddresses.md)
    
- [Wert (ExtendedPropertyType)](value-extendedpropertytype.md)
    
## <a name="getimitems-operation-error-response"></a>GetImItems Vorgang Fehlerantwort

Der Vorgang **GetImItems** Bezeichner wird nicht validiert und wird nicht die erwarteten Fehlerantwort **ErrorInvalidImContactId** oder **ErrorInvalidImGroupId** zurück, wenn Sie einen ungültigen Kontakt oder eine Gruppen-ID mit dem Dienst bereitgestellt wird. 
  
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
    
- [GetImItemList-Vorgang](getimitemlist-operation.md)
    

