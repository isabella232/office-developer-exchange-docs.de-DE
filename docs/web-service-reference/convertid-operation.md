---
title: ConvertId-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 47d96cf6-9e2f-4fc0-9682-7258d3fbf918
description: Hier finden Sie Informationen zum ConvertId EWS-Vorgang.
ms.openlocfilehash: 04f20d8446ab3117adb3f00ea17f93c068eeffb9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59536631"
---
# <a name="convertid-operation"></a>ConvertId-Vorgang

Hier finden Sie Informationen zum **ConvertId** EWS-Vorgang. 
  
Der EWS-Vorgang **(ConvertId** Exchange Web Services) konvertiert Element- und Ordnerbezeichner zwischen Formaten, die von Exchange Online akzeptiert werden, Exchange Online als Teil von Office 365 und lokalen Versionen von Exchange ab Exchange Server 2013. 
  
## <a name="using-the-convertid-operation"></a>Verwenden des ConvertId-Vorgangs
<a name="bk_usingConvertId"> </a>

Sie können die folgenden Bezeichner mithilfe des **ConvertId-Vorgangs** konvertieren: 
  
- Das Bezeichnerformat für EWS in der ersten Version von Exchange 2007. Dies wird durch den  `EwsLegacyId` Enumerationswert in der [IdFormat -Enumeration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) dargestellt. 
    
- Das Bezeichnerformat für EWS in Exchange 2007 SP1 oder Exchange 2010. Dies wird durch den  `EwsId` Enumerationswert in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)dargestellt.
    
- Der MAPI-Bezeichner, wie in der **PR_ENTRYID-Eigenschaft.** Dies wird durch den  `EntryId` Enumerationswert in der [IdFormat -Enumeration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) dargestellt. 
    
- Der Ereignisbezeichner des Verfügbarkeitskalenders. Dies ist eine hexadezimal codierte Darstellung der **PR_ENTRYID-Eigenschaft.** Dies wird durch den  `HexEntryId` Enumerationswert in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)dargestellt.
    
- Der Exchange-Speicherbezeichner. Dies wird durch den  `StoreId` Enumerationswert in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)dargestellt. Der **ConvertId-Vorgang** konvertiert keine Bezeichner für öffentliche Ordner vom EWS-Bezeichner in den Speicherbezeichner. 
    
- Der bezeichner Outlook Web App. Dies wird durch den `OwaId` Enumerationswert in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) dargestellt.
    
    Die Übergabe von URLs, die von diesem Bezeichner an Outlook Web App erstellt werden, wird nicht unterstützt. Die Outlook Web App-ID gilt für Exchange 2007 und Exchange 2010. Outlook Web App für Exchange Online und Versionen von Exchange ab Exchange Server 2013 verwendet EWS-Bezeichner.
    
Der **ConvertId-Vorgang** funktioniert beim Konvertieren von Bezeichnern öffentlicher Ordner vom EWS-Bezeichner in den Speicherbezeichner in Exchange Online und Exchange 2013 nicht wie erwartet. Zur Problemumgehung können Sie die zurückgegebene Kennung manuell anpassen. So aktualisieren Sie den Bezeichner manuell: 
  
1. Ermitteln Sie in Ihrem Anwendungscode, ob sich das Zielelement/der Zielordner in einem öffentlichen Ordner befindet. 
    
2. Decodieren Sie die Base64-codierte Bezeichnerzeichenfolge.
    
3. Stellen Sie sicher, dass der Typ Byte (21. Byte) den Wert 7 aufweist. Der Wert 7 gibt an, dass der Bezeichner das falsche Format aufweist.
    
4. Überspringen Sie die ersten vier Bytes. Sie müssen auf Null festgelegt werden.
    
5. Aktualisieren Sie die nächsten 16 Bytes mit der folgenden GUID: 1A447390AA6611CD9BC800AA002FC45A
    
6. Aktualisieren Sie das nächste Byte (Typbyte) mit dem Wert 9.
    
7. Ändern Sie den Bezeichner in eine Base64-codierte Zeichenfolge.
    
> [!NOTE]
> Der **ConvertId-Vorgang** überprüft, ob eine bestimmte SMTP-Adresse ein gültiges Format aufweist. Der Vorgang bestimmt nicht, ob eine SMTP-Adresse ein gültiges Postfach darstellt. 
  
Der **ConvertId-Vorgang** kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
**Tabelle 1. SOAP-Header des ConvertId-Vorgangs**

|**Header**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|Identitätswechsel  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dies gilt für eine Anforderung.  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Dies gilt für eine Anforderung.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dies gilt für eine Antwort.  <br/> |
   
## <a name="convertid-operation-request-example"></a>ConvertId-Vorgangsanforderungsbeispiel
<a name="bk_usingConvertId"> </a>

Das folgende Beispiel einer **ConvertId-Anforderung** zeigt, wie sie von einem EWS-Bezeichner in einen Outlook Web App Bezeichner konvertiert wird. 
  
Das [RequestServerVersion-Element](requestserverversion.md) im SOAP-Header muss auf Exchange2007_SP1 oder höher festgelegt werden, damit dieser Vorgang funktioniert. 
  
> [!NOTE]
> Der Elementbezeichner wurde gekürzt, um die Lesbarkeit zu gewährleisten. 
  
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

## <a name="convertid-operation-response-example"></a>Beispiel für ConvertId-Vorgangsantwort
<a name="bk_usingConvertId"> </a>

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **ConvertId-Anforderung.** Dieses Antwortbeispiel enthält einen Outlook Web App Bezeichner. 
  
> [!NOTE]
> Die Outlook Web App-ID wurde gekürzt, um die Lesbarkeit zu gewährleisten. 
  
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

## <a name="convertid-operation-error-response-example"></a>Fehlerantwortbeispiel für ConvertId-Vorgang
<a name="bk_usingConvertId"> </a>

Das folgende Beispiel zeigt die Antwort auf eine Anforderung, die den falschen Bezeichnerformattyp enthält.
  
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

Das EWS-Bezeichnerformat wurde zwischen der ersten Version von Exchange 2007 und Exchange 2007 Service Pack 1 (SP1) geändert. Exchange Online als Teil von Office 365, Exchange Online und lokalen Versionen von Exchange ab Exchange 2010 verwenden das gleiche Bezeichnerformat, das Exchange 2007 SP1 verwendet.
  
Der **ConvertId-Vorgang** konvertiert Bezeichner öffentlicher Ordner vom EWS-Bezeichner in den Speicherbezeichner in Exchange 2007 und Exchange 2010. 
  
## <a name="see-also"></a>Siehe auch
<a name="bk_ConvertIdVersionDiff"> </a>

- [Konvertieren von Bezeichnern](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)
    
- [ConvertIdType](https://msdn.microsoft.com/library/ExchangeWebServices.ConvertIdType.aspx)
    
- [ConvertId](https://msdn.microsoft.com/library/ExchangeWebServices.ExchangeServiceBinding.ConvertId.aspx)
    

