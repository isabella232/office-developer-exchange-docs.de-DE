---
title: AddNewTelUriContactToGroup-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c9688ce8-2465-45bb-8bd2-94b32ed4885c
description: Hier finden Sie Informationen zur Verwendung des EWS-Vorgangs "AddNewTelUriContactToGroup".
ms.openlocfilehash: 2ad0f55c044e92e2f18a1705ab53be467a804091
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544297"
---
# <a name="addnewteluricontacttogroup-operation"></a>AddNewTelUriContactToGroup-Vorgang

Hier finden Sie Informationen zur Verwendung des EWS-Vorgangs **"AddNewTelUriContactToGroup".** 
  
Der **AddNewTelUriContactToGroup-Vorgang** fügt einer Gruppe basierend auf der Telefonnummer eines Kontakts einen neuen Kontakt hinzu. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-addnewteluricontacttogroup-operation"></a>Verwenden des AddNewTelUriContactToGroup-Vorgangs

Eine **AddNewTelUriContactToGroup-Vorgangsanforderung** sendet den TEL-URI, DEN SIP-URI, die Telefonnummer und die Gruppe eines Kontakts, der der Kontakt hinzugefügt werden soll. Eine **AddNewTelUriContactToGroup-Vorgangsantwort** erstellt eine Persona für den neuen Kontakt. Mit diesem Vorgang können Clients einen neuen Kontakt hinzufügen, auch wenn der Kontakt keinen Namen hat. 
  
### <a name="addnewteluricontacttogroup-operation-soap-headers"></a>SOAP-Header des AddNewTelUriContactToGroup-Vorgangs

Der **AddNewTelUriContactToGroup-Vorgang** kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dieser Header gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifiziert die Kultur, wie in RFC 3066 definiert, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden soll. Dieser Header gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Dieser Header gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dieser Header gilt für eine Antwort.  <br/> |
   
## <a name="addnewteluricontacttogroup-operation-request-example-add-a-new-contact-to-a-group"></a>AddNewTelUriContactToGroup-Vorgangsanforderungsbeispiel: Hinzufügen eines neuen Kontakts zu einer Gruppe

Das folgende Beispiel einer **AddNewTelUriContactToGroup-Vorgangsanforderung** zeigt, wie Sie einen neuen Kontakt erstellen und den neuen Kontakt mithilfe der TEL- und SIP-URIs des Kontakts einer Chatgruppe hinzufügen. 
  
> [!NOTE]
> Alle Elementbezeichner und Änderungsschlüssel in diesem Artikel wurden gekürzt, um die Lesbarkeit zu gewährleisten. 
  
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
      <m:AddNewTelUriContactToGroup>
         <m:TelUriAddress>tel:5625550100</m:TelUriAddress>
         <m:ImContactSipUriAddress>sip:john@contoso.com</m:ImContactSipUriAddress>
         <m:ImTelephoneNumber>5625550100</m:ImTelephoneNumber>
         <m:GroupId Id="AAMkADEzOTm4QrAABY7+0GAAA="/>
      </m:AddNewTelUriContactToGroup>
   </soap:Body>
</soap:Envelope>
```

Der SOAP-Anforderungstext enthält die folgenden Elemente:
  
- [AddNewTelUriContactToGroup](addnewteluricontacttogroup.md)
    
- [TelUriAddress](teluriaddress.md)
    
- [ImContactSipUriAddress](imcontactsipuriaddress.md)
    
- [ImTelephoneNumber](imtelephonenumber.md)
    
- [GroupId](groupid.md)
    
## <a name="successful-addnewteluricontacttogroup-operation-response"></a>Erfolgreiche AddNewTelUriContactToGroup-Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **AddNewTelUriContactToGroup-Vorgangsanforderung** zum Erstellen eines Kontakts. Die Antwort enthält die zugeordnete Persona-ID für den Kontakt, den Anzeigenamen der Persona, die in diesem Fall auf der Telefonnummer des Kontakts basiert, und den Elementbezeichner des Kontakts, der als Teil der Quellbezeichnerzuordnung angezeigt wird. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/"                           
            xmlns:xsd="http://www.w3.org/2001/XMLSchema"
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" />
   </s:Header>
   <s:Body>
      <AddNewTelUriContactToGroupResponse ResponseClass="Success" 
                                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <Persona>
            <t:PersonaId Id="AAQkADE686dX3s="/>
            <t:PersonaType>Person</t:PersonaType>
            <t:CreationTime>2012-10-29T23:10:13Z</t:CreationTime>
            <t:DisplayName/>
            <t:DisplayNameFirstLast>5625550100</t:DisplayNameFirstLast>
            <t:DisplayNameLastFirst>5625550100</t:DisplayNameLastFirst>
            <t:FileAs/>
            <t:FileAsId >None</t:FileAsId>
            <t:RelevanceScore >2147483647</t:RelevanceScore>
            <t:Attributions>
               <t:Attribution>
                  <t:Id>0</t:Id>
                  <t:SourceId Id="ABhHuhCAAA=" ChangeKey="EQAAABxFU"/>
                  <t:DisplayName>Lync Contacts</t:DisplayName>
                  <t:IsWritable>false</t:IsWritable>
                  <t:IsQuickContact>true</t:IsQuickContact>
                  <t:IsHidden>false</t:IsHidden>
               </t:Attribution>
            </t:Attributions>
            <t:FileAsIds>
               <t:StringAttributedValue>
                  <t:Value>None</t:Value>
                  <t:Attributions>
                     <t:Attribution>0</t:Attribution>
                  </t:Attributions>
               </t:StringAttributedValue>
            </t:FileAsIds>
            <t:OtherTelephones>
               <t:PhoneNumberAttributedValue>
                  <t:Value>
                     <t:Number>5625550100</t:Number>
                     <t:Type>Other</t:Type>
                  </t:Value>
                  <t:Attributions>
                     <t:Attribution>0</t:Attribution>
                  </t:Attributions>
               </t:PhoneNumberAttributedValue>
            </t:OtherTelephones>
         </Persona>
      </AddNewTelUriContactToGroupResponse>
   </s:Body>
</s:Envelope>
```

Der SOAP-Antworttext enthält die folgenden Elemente:
  
- [AddNewTelUriContactToGroupResponse](addnewteluricontacttogroupresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [Persona](persona.md)
    
- [PersonaId](personaid.md)
    
- [PersonaType](personatype.md)
    
- [CreationTime](creationtime.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
- [DisplayNameFirstLast](displaynamefirstlast.md)
    
- [DisplayNameLastFirst](displaynamelastfirst.md)
    
- [FileAs](fileas.md)
    
- [FileAsId](fileasid.md)
    
- [RelevanceScore](relevancescore.md)
    
- [Attributions (ArrayOfPersonaAttributionsType)](attributions-arrayofpersonaattributionstype.md)
    
- [Attribution (PersonaAttributionType)](attribution-personaattributiontype.md)
    
- [ID (Zeichenfolge)](id-string.md)
    
- [SourceId](sourceid.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
- [IsWritable](iswritable.md)
    
- [IsQuickContact](isquickcontact.md)
    
- [IsHidden](ishidden.md)
    
- [FileAsIds](fileasids.md)
    
- [StringAttributedValue](stringattributedvalue.md)
    
- [Wert](value.md)
    
- [Attributions (ArrayOfValueAttributionsType)](attributions-arrayofvalueattributionstype.md)
    
- [Attribution (Zeichenfolge)](attribution-string.md)
    
- [OtherTelephones](othertelephones.md)
    
- [PhoneNumberAttributedValue](phonenumberattributedvalue.md)
    
- [Wert](value.md)
    
- [Number](number.md)
    
- [Typ (Zeichenfolge)](type-string.md)
    
- [Attributions (ArrayOfValueAttributionsType)](attributions-arrayofvalueattributionstype.md)
    
- [Attribution (Zeichenfolge)](attribution-string.md)
    
## <a name="addnewteluricontacttogroup-operation-error-response-example"></a>Beispiel für AddNewTelUriContactToGroup-Vorgangsfehlerantwort

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **AddNewTelUriContactToGroup-Vorgangsanforderung,** wenn der Gruppenbezeichner einen wohlgeformten Wert enthält, der keine Gruppe im Postfach identifiziert. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddNewTelUriContactToGroupResponse ResponseClass="Error" 
                                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </AddNewTelUriContactToGroupResponse>
   </s:Body>
</s:Envelope>

```

Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:
  
- [AddNewTelUriContactToGroupResponse](addnewteluricontacttogroupresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
    
- [Personen und Kontakte in EWS in Exchange](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    

