---
title: ConvertId-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 47d96cf6-9e2f-4fc0-9682-7258d3fbf918
description: Hier finden Sie Informationen über die ConvertId EWS Vorgang.
ms.openlocfilehash: 5f1bcd8a9f0adc25b7c598ef10cc6bb139dfe02d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757710"
---
# <a name="convertid-operation"></a>ConvertId-Vorgang

Hier finden Sie Informationen zum **ConvertId** EWS-Vorgang. 
  
Der Vorgang des **ConvertId** Exchange-Webdienste (EWS) konvertiert Element- und Bezeichner zwischen Formate, die von Exchange Online, Exchange Online als Teil von Office 365, akzeptiert werden und lokale Versionen von Exchange, beginnend mit Exchange Server 2013. 
  
## <a name="using-the-convertid-operation"></a>Verwenden des ConvertId-Vorgangs
<a name="bk_usingConvertId"> </a>

Sie können die folgenden Bezeichner mithilfe des Vorgangs **ConvertId** konvertieren: 
  
- Das Format Bezeichner für EWS in der ursprünglich freigegebenen Version von Exchange 2007. Wird dies durch die `EwsLegacyId` -Enumerationswert in der [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) -Aufzählung. 
    
- Das Format der Bezeichner für EWS in Exchange 2007 SP1 oder Exchange 2010. Wird dies durch die `EwsId` in [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)-Enumerationswert ab.
    
- Der MAPI-Bezeichner, wie in der **PR_ENTRYID** -Eigenschaft. Wird dies durch die `EntryId` -Enumerationswert in der [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) -Aufzählung. 
    
- Der Bezeichner der Verfügbarkeit Kalender-Ereignis. Dies ist eine Hexadezimalzahl-codierte Darstellung der **PR_ENTRYID** -Eigenschaft. Wird dies durch die `HexEntryId` in [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)-Enumerationswert ab.
    
- Der Bezeichner für den Exchange-Speicher. Wird dies durch die `StoreId` in [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)-Enumerationswert ab. Der Vorgang **ConvertId** konvertiert nicht öffentliche Ordner-IDs aus der EWS-ID auf den Store-Bezeichner. 
    
- Der Outlook Web App-Bezeichner. Wird dies durch die `OwaId` -Enumerationswert in [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)
    
    Die Übergabe von URLs, die von dieser Bezeichner auf Outlook Web App erstellt werden, wird nicht unterstützt. Die Outlook Web App-ID gilt für Exchange 2007 und Exchange 2010. Outlook Web App für Exchange Online und Versionen von Exchange beginnend mit Exchange Server 2013 verwendet EWS-Bezeichner.
    
Der Vorgang **ConvertId** funktioniert nicht wie erwartet beim Konvertieren von Öffentliche Ordner-IDs aus der EWS-ID in der Store-ID in Exchange Online und Exchange 2013. Sie können die ID, die zur Umgehung dieses Problems zurückgegeben wird, manuell aktualisieren. Den Bezeichner manuell zu aktualisieren: 
  
1. Bestimmen Sie in Ihrem Anwendungscode, ob der Zielordner/Element in einem öffentlichen Ordner. 
    
2. Decodiert die Base64-codierte Bezeichnerzeichenfolge.
    
3. Überprüfen Sie, ob der Typ Byte (21. Byte) hat den Wert 7. Der Wert 7 gibt an, dass der Bezeichner in der falschen Format ist.
    
4. Überspringen Sie die ersten vier Bytes. Sie müssen auf 0 (null) festgelegt werden.
    
5. Aktualisieren Sie die folgenden 16-Byte mit der folgenden GUID: 1A447390AA6611CD9BC800AA002FC45A
    
6. Aktualisieren Sie das nächste Byte (Typ Byte) mit einem Wert von 9.
    
7. Ändern Sie den Bezeichner in eine Base64-codierte Zeichenfolge.
    
> [!NOTE]
> Der Vorgang **ConvertId** überprüft, dass eine angegebene SMTP-Adresse ein gültiges Format hat. Der Vorgang ermittelt nicht, ob eine SMTP-Adresse ein gültiges Postfach darstellt. 
  
Der Vorgang **ConvertId** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind. 
  
**In Tabelle 1. ConvertId Vorgang SOAP-Header**

|**Header**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|Identitätswechsel  <br/> |["ExchangeImpersonation"](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dies gilt für eine Anforderung.  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifiziert die Schemaversion für die Anforderung Vorgang, dass sich dies auf eine Anforderung anwendbar ist.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dies gilt für eine Antwort.  <br/> |
   
## <a name="convertid-operation-request-example"></a>ConvertId Vorgang anforderungsbeispiel
<a name="bk_usingConvertId"> </a>

Im folgenden Beispiel wird eine Anforderung **ConvertId** veranschaulicht, wie ein EWS-Bezeichner in einer Outlook Web App-Bezeichner konvertiert. 
  
Das [RequestServerVersion](requestserverversion.md) -Element im SOAP-Header muss Exchange2007_SP1 oder höher für diesen Vorgang funktioniert festgelegt werden. 
  
> [!NOTE]
> Der Elementbezeichner wurde gekürzt, um die Lesbarkeit zu erhalten. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <ConvertId xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               DestinationFormat="OwaId">
      <SourceIds>
        <t:AlternateId Format="EwsId" Id="AAMkAGZhN2IxYTA0LWNiNzItN="
                       Mailbox="user1@example.com"/>
      </SourceIds>
    </ConvertId>
  </soap:Body>
</soap:Envelope>
```

## <a name="convertid-operation-response-example"></a>ConvertId Vorgang antwortbeispiel
<a name="bk_usingConvertId"> </a>

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **ConvertId** . In diesem antwortbeispiel enthält einen Outlook Web App-Bezeichner. 
  
> [!NOTE]
> Die Outlook Web App-ID wurde gekürzt, um die Lesbarkeit zu erhalten. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                         MajorBuildNumber="191" MinorBuildNumber="0" 
                         Version="Exchange2010" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <ConvertIdResponseMessage ResponseClass="Success">
          <ResponseCode>NoError</ResponseCode>
          <AlternateId xsi:type="t:AlternateIdType" Format="OwaId" Id="RgAAAAAS2%2" 
                         Mailbox="user@example.com" />
        </ConvertIdResponseMessage>
      </ResponseMessages>
    </ConvertIdResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="convertid-operation-error-response-example"></a>ConvertId Vorgang Fehler antwortbeispiel
<a name="bk_usingConvertId"> </a>

Das folgende Beispiel zeigt die Antwort auf eine Anforderung, die den falschen Typ des Formats Bezeichner enthält.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                       MajorBuildNumber="206" MinorBuildNumber="0"
                       Version="Exchange2010" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <ConvertIdResponseMessage ResponseClass="Error">
          <MessageText>Id is malformed.</MessageText>
          <ResponseCode>ErrorInvalidIdMalformed</ResponseCode>
          <DescriptiveLinkKey>0</DescriptiveLinkKey>
        </ConvertIdResponseMessage>
      </ResponseMessages>
    </ConvertIdResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="version-differences"></a>Versionsunterschiede
<a name="bk_ConvertIdVersionDiff"> </a>

Das Format von EWS zwischen der ursprünglich freigegebenen Version von Exchange 2007 und Exchange 2007 Service Pack 1 (SP1) geändert. Exchange Online als Teil von Office 365, Exchange Online und lokale Versionen von Exchange, beginnend mit Exchange 2010 verwenden das gleiche Bezeichner-Format, das Exchange 2007 SP1 verwendet.
  
Der Vorgang **ConvertId** konvertiert für Öffentliche Ordner-IDs aus der EWS-ID in der Store-ID in Exchange 2007 und Exchange 2010. 
  
## <a name="see-also"></a>Siehe auch
<a name="bk_ConvertIdVersionDiff"> </a>

- [Konvertieren von Bezeichnern](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)
    
- [ConvertIdType](https://msdn.microsoft.com/library/ExchangeWebServices.ConvertIdType.aspx)
    
- [ConvertId](https://msdn.microsoft.com/library/ExchangeWebServices.ExchangeServiceBinding.ConvertId.aspx)
    

