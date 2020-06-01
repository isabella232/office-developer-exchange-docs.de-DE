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
description: Hier finden Sie Informationen zum EWS-Vorgang der Convert-Funktion.
ms.openlocfilehash: 36bd47d3fc7c7ca7cea7b38222abb25fba6074ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452552"
---
# <a name="convertid-operation"></a>ConvertId-Vorgang

Hier finden Sie Informationen zum EWS-Vorgang der **Convert** -Funktion. 
  
Der Exchange-Webdienste-Vorgang **convertType** konvertiert Element-und Ordner Bezeichner zwischen Formaten, die von Exchange Online akzeptiert werden, Exchange Online im Rahmen von Office 365 und lokalen Versionen von Exchange, die mit Exchange Server 2013 beginnen. 
  
## <a name="using-the-convertid-operation"></a>Verwenden des Convert-Vorgangs
<a name="bk_usingConvertId"> </a>

Sie können die folgenden Bezeichner mithilfe des **Convert** -Vorgangs konvertieren: 
  
- Das ID-Format für EWS in der ersten Version von Exchange 2007. Dies wird durch den `EwsLegacyId` Aufzählungswert in der [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) -Aufzählung dargestellt. 
    
- Das ID-Format für EWS in Exchange 2007 SP1 oder Exchange 2010. Dies wird durch den `EwsId` Aufzählungswert in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)dargestellt.
    
- Der MAPI-Bezeichner, wie in der **PR_ENTRYID** -Eigenschaft. Dies wird durch den `EntryId` Aufzählungswert in der [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) -Aufzählung dargestellt. 
    
- Die Ereignis-ID des Verfügbarkeitskalenders. Dies ist eine hexadezimal codierte Darstellung der **PR_ENTRYID** -Eigenschaft. Dies wird durch den `HexEntryId` Aufzählungswert in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)dargestellt.
    
- Die Exchange-Informationsspeicher-ID. Dies wird durch den `StoreId` Aufzählungswert in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)dargestellt. Der **Convert** -ID-Vorgang konvertiert keine Bezeichner für Öffentliche Ordner aus dem EWS-Bezeichner in die Speicher-ID. 
    
- Die Outlook Web App-ID. Dies wird durch den `OwaId` Aufzählungswert in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) dargestellt.
    
    Die Übergabe von URLs, die von diesem Bezeichner an Outlook Web App erstellt werden, wird nicht unterstützt. Der Outlook Web App Bezeichner gilt für Exchange 2007 und Exchange 2010. Outlook Web App für Exchange Online und Versionen von Exchange, die mit Exchange Server 2013 beginnen, werden EWS-IDs verwendet.
    
Der **Convert** -ID-Vorgang funktioniert nicht wie erwartet beim Konvertieren von Bezeichnern für Öffentliche Ordner aus der EWS-ID in die Speicher-ID in Exchange Online und Exchange 2013. Zur Problemumgehung können Sie die zurückgegebene Kennung manuell anpassen. So aktualisieren Sie den Bezeichner manuell: 
  
1. Bestimmen Sie im Anwendungscode, ob sich das Zielelement/der Ordner in einem öffentlichen Ordner befindet. 
    
2. Decodieren Sie die Base64-codierte Bezeichner-Zeichenfolge.
    
3. Stellen Sie sicher, dass das Typ Byte (21. Byte) den Wert 7 aufweist. Der Wert 7 gibt an, dass der Bezeichner das falsche Format aufweist.
    
4. Überspringen Sie die ersten vier Bytes. Sie müssen auf NULL festgelegt werden.
    
5. Aktualisieren der nächsten 16 Bytes mit der folgenden GUID: 1A447390AA6611CD9BC800AA002FC45A
    
6. Aktualisieren Sie das nächste Byte (Typ Byte) mit dem Wert 9.
    
7. Ändern Sie den Bezeichner in eine Base64-codierte Zeichenfolge.
    
> [!NOTE]
> Der **Convert** -Vorgang überprüft, ob eine bestimmte SMTP-Adresse ein gültiges Format aufweist. Der Vorgang bestimmt nicht, ob eine SMTP-Adresse ein gültiges Postfach darstellt. 
  
Der **Convert** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
**Tabelle 1. SOAP-Header für Convert-Operation**

|**Header**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|Identitätswechsel  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dies gilt für eine Anforderung.  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an, die für eine Anforderung gilt.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dies gilt für eine Antwort.  <br/> |
   
## <a name="convertid-operation-request-example"></a>Convert-Vorgangsanforderung (Beispiel)
<a name="bk_usingConvertId"> </a>

Das folgende Beispiel einer **Konvertierungs** Anforderung zeigt, wie eine EWS-ID in einen Outlook Web App Bezeichner konvertiert wird. 
  
Das [RequestServerVersion](requestserverversion.md) -Element im SOAP-Header muss auf Exchange2007_SP1 oder höher festgelegt sein, damit dieser Vorgang funktioniert. 
  
> [!NOTE]
> Die Element-ID wurde verkürzt, um die Lesbarkeit beizubehalten. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <ConvertId xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               DestinationFormat="OwaId">
      <SourceIds>
        <t:AlternateId Format="EwsId" Id="AAMkAGZhN2IxYTA0LWNiNzItN="
                       Mailbox="user1@example.com"/>
      </SourceIds>
    </ConvertId>
  </soap:Body>
</soap:Envelope>
```

## <a name="convertid-operation-response-example"></a>Beispiel für eine Convert-Vorgangs Antwort
<a name="bk_usingConvertId"> </a>

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **Convert** -Anforderung. Dieses Antwortbeispiel enthält einen Outlook Web App Bezeichner. 
  
> [!NOTE]
> Die Outlook Web App-ID wurde verkürzt, um die Lesbarkeit zu erhalten. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                         MajorBuildNumber="191" MinorBuildNumber="0" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="convertid-operation-error-response-example"></a>Fehlerantwort Beispiel für Convert-Operation
<a name="bk_usingConvertId"> </a>

Das folgende Beispiel zeigt die Antwort auf eine Anforderung, die den falschen Typ des Bezeichnerformat enthält.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                       MajorBuildNumber="206" MinorBuildNumber="0"
                       Version="Exchange2010" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

Das EWS-Bezeichnerformat wurde zwischen der ursprünglichen Veröffentlichungsversion von Exchange 2007 und Exchange 2007 Service Pack 1 (SP1) geändert. Exchange Online im Rahmen von Office 365, Exchange Online und lokalen Versionen von Exchange, die mit Exchange 2010 beginnen, verwenden dasselbe von Exchange 2007 SP1 verwendete ID-Format.
  
Mit dem **Konvertierungs** -ID-Vorgang werden Bezeichner für Öffentliche Ordner aus dem EWS-Bezeichner in die Speicher-ID in Exchange 2007 und Exchange 2010 konvertiert. 
  
## <a name="see-also"></a>Siehe auch
<a name="bk_ConvertIdVersionDiff"> </a>

- [Konvertieren von Bezeichnern](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)
    
- [ConvertIdType](https://msdn.microsoft.com/library/ExchangeWebServices.ConvertIdType.aspx)
    
- [ConvertId](https://msdn.microsoft.com/library/ExchangeWebServices.ExchangeServiceBinding.ConvertId.aspx)
    

