---
title: MarkAsJunk-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1f71f04d-56a9-4fee-a4e7-d1034438329e
description: Hier finden Sie Informationen zum MarkAsJunk EWS-Vorgang.
ms.openlocfilehash: b165b415ce9380846b49d15dd321bfddba72b749
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524735"
---
# <a name="markasjunk-operation"></a>MarkAsJunk-Vorgang

Hier finden Sie Informationen zum **MarkAsJunk** EWS-Vorgang. 
  
Der **MarkAsJunk-Vorgang** fügt Benutzer aus der Liste blockierter E-Mails hinzu und entfernt sie und verschiebt E-Mail-Nachrichten in den Junk-E-Mail-Ordner. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-markasjunk-operation"></a>Verwenden des MarkAsJunk-Vorgangs

Der **MarkAsJunk-Vorgang** enthält zwei boolesche Optionen, um anzugeben, ob ein E-Mail-Absender zur Liste der blockierten Absender hinzugefügt werden soll und ob die Ziel-E-Mail-Nachricht in den Standardmäßigen Junk-E-Mail-Ordner oder den Posteingangsordner verschoben werden soll. Die Aktionen werden durch die Werte der **Attribute "IsJunk"** und **"MoveItem"** bestimmt. Nachfolgend sind die möglichen Aktionen aufgeführt, die auf den Wertkombinationen für die Attribute **"IsJunk"** und **"MoveItem"** basieren: 
  
- Wenn das **IsJunk-Attribut** auf **"true"** und das **MoveItem-Attribut** auf **"true"** festgelegt ist, wird der Absender der Ziel-E-Mail-Nachricht der Liste der blockierten Absender hinzugefügt, und die E-Mail-Nachricht wird in den Junk-Dmail-Ordner verschoben.
    
- Wenn das **IsJunk-Attribut** auf **"true"** und das **MoveItem-Attribut** auf **"false"** festgelegt ist, wird der Absender der Ziel-E-Mail-Nachricht der Liste der blockierten Absender hinzugefügt, und die E-Mail-Nachricht wird nicht aus dem Ordner verschoben.
    
- Wenn das **IsJunk-Attribut** auf **"false"** und das **MoveItem-Attribut** auf **"true"** festgelegt ist, wird der Absender der Ziel-E-Mail-Nachricht aus der Liste der blockierten Absender entfernt, und die E-Mail-Nachricht wird in den Ordner Posteingang verschoben.
    
- Wenn das **IsJunk-Attribut** auf **"false"** und das **MoveItem-Attribut** auf **"false"** festgelegt ist, wird der Absender der Ziel-E-Mail-Nachricht aus der Liste der blockierten Absender entfernt, und die E-Mail-Nachricht wird nicht aus dem Ordner verschoben.
    
> [!IMPORTANT]
> Der Inhalt der Liste blockierter Absender kann von EWS nicht gefunden werden. Wenn ein Absender zur Liste der blockierten Absender hinzugefügt wird, müssen Sie eine Kopie einer E-Mail-Nachricht, die vom blockierten Absender gesendet wurde, beibehalten, um die Blockierung des Absenders in Zukunft aufzuheben. 
  
### <a name="markasjunk-operation-soap-headers"></a>SOAP-Header des MarkAsJunk-Vorgangs

Der **MarkAsJunk-Vorgang** kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dieser Header gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifiziert die Kultur, wie in RFC 3066 definiert, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden soll. Dieser Header gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Dieser Header gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dieser Header gilt für eine Antwort.  <br/> |
   
## <a name="markasjunk-operation-request-example-add-a-sender-to-the-blocked-sender-list"></a>Beispiel für MarkAsJunk-Vorgangsanforderung: Hinzufügen eines Absenders zur Liste blockierter Absender

Das folgende Beispiel einer **MarkAsJunk-Vorgangsanforderung** zeigt, wie der Absender einer E-Mail zur Liste der blockierten Absender hinzugefügt und die E-Mail in den Junk-E-Mail-Ordner verschoben wird. Der **MarkAsJunk-Vorgang** akzeptiert den eindeutigen E-Mail-Nachrichtenbezeichner, um die E-Mail zu identifizieren, die verwendet wird, um auf den Absender zu verweisen, der der Liste der blockierten Absender hinzugefügt wird. 
  
> [!NOTE]
> Alle Elementbezeichner und Änderungsschlüssel in diesem Artikel wurden gekürzt, um die Lesbarkeit zu gewährleisten. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
        <t:RequestServerVersion Version="Exchange2013" />
    </soap:Header>
    <soap:Body>
        <m:MarkAsJunk IsJunk="true" MoveItem="true">
            <m:ItemIds>
                <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYA" />
            </m:ItemIds>
        </m:MarkAsJunk>
    </soap:Body>
</soap:Envelope>

```

Der SOAP-Anforderungstext enthält die folgenden Elemente:
  
- [MarkAsJunk](markasjunk.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="successful-markasjunk-operation-response"></a>Erfolgreiche MarkAsJunk-Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **MarkAsJunk-Vorgangsanforderung,** um einen Absender zur Liste der blockierten Absender hinzuzufügen und die E-Mail-Nachricht in den Junk-E-Mail-Ordner zu verschieben. 
  
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
                             xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema">
        <m:MarkAsJunkResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
           <m:ResponseMessages>
               <m:MarkAsJunkResponseMessage ResponseClass="Success">
                  <m:ResponseCode>NoError</m:ResponseCode>
                 <m:MovedItemId Id="AAMkAD=" ChangeKey="CQAAABYu" />
               </m:MarkAsJunkResponseMessage>
           </m:ResponseMessages>
        </m:MarkAsJunkResponse>
    </s:Body>
</s:Envelope>
```

Der SOAP-Antworttext enthält die folgenden Elemente:
  
- [MarkAsJunkResponse](markasjunkresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MarkAsJunkResponseMessage](markasjunkresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [MovedItemId](moveditemid.md)
    
## <a name="markasjunk-operation-request-example-remove-a-sender-from-the-blocked-sender-list"></a>Beispiel für eine MarkAsJunk-Vorgangsanforderung: Entfernen eines Absenders aus der Liste der blockierten Absender

Das folgende Beispiel einer **MarkAsJunk-Vorgangsanforderung** zeigt, wie der Absender einer E-Mail-Nachricht aus der Liste der blockierten Absender entfernt und die E-Mail-Nachricht in den Ordner Posteingang verschoben wird. Sie müssen eine vom blockierten Absender gesendete E-Mail-Nachricht beibehalten, um den Absender aus der Liste der blockierten Absender zu entfernen. Die E-Mail-Adresse des Absenders ist E-Mail-Nachrichten zugeordnet, die vom Absender gesendet wurden. Das Entfernen eines Absenders aus der Liste der blockierten Absender ist nicht erfolgreich, wenn die Referenz-E-Mail-Nachricht im Postfach des Benutzers nicht mehr vorhanden ist. Der Elementbezeichner, der zum Zuordnen einer E-Mail-Nachricht zu seinem Absender verwendet wird, muss einem Element zugeordnet sein, das im Exchange Postfach vorhanden ist. Es wird empfohlen, einen ausgeblendeten Ordner zum Speichern von Elementen zu erstellen, die von zuvor blockierten Absendern gesendet wurden, damit die Blockierung der Absender von der Clientanwendung aufgehoben werden kann. Für den Fall, dass ein Element aus dem Exchange Postfach entfernt wurde, muss ein Administrator die Exchange-Verwaltungskonsole verwenden, um auf die Liste blockierter Absender zuzugreifen, um einen Absender aus der Liste zu entfernen. Informationen zum Aufheben der Blockierung eines Benutzers mithilfe der Exchange-Verwaltungskonsole finden Sie unter [Konfigurieren der Einstellungen für sichere und blockierte Absender in Office 365](https://support.microsoft.com/kb/2545137).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
    </soap:Header>
    <soap:Body>
      <m:MarkAsJunk IsJunk="false" MoveItem="true">
        <m:ItemIds>
          <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYu" />
        </m:ItemIds>
      </m:MarkAsJunk>
    </soap:Body>
 </soap:Envelope>

```

Eine erfolgreiche Antwort zum Entfernen eines Absenders aus der Liste der blockierten Absender entspricht der Antwort für das Hinzufügen eines Absenders zur Liste der blockierten Absender.
  
Der SOAP-Anforderungstext enthält die folgenden Elemente:
  
- [MarkAsJunk](markasjunk.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="markasjunk-operation-error-response"></a>Fehlerantwort des MarkAsJunk-Vorgangs

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **MarkAsJunk-Vorgangsanforderung.** Dies ist eine Antwort auf eine Anforderung zum Hinzufügen oder Entfernen eines Absenders aus der Liste blockierter Absender, wenn die durch den Elementbezeichner angegebene E-Mail-Nachricht nicht mehr im Postfach vorhanden ist. 
  
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
    <m:MarkAsJunkResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:MarkAsJunkResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:MarkAsJunkResponseMessage>
      </m:ResponseMessages>
    </m:MarkAsJunkResponse>
  </s:Body>
</s:Envelope>
```

Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:
  
- [MarkAsJunkResponse](markasjunkresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MarkAsJunkResponseMessage](markasjunkresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
    
- [GetItem-Vorgang](getitem-operation.md) GetItem-Vorgang 
    
- [FindItem-Vorgang](finditem-operation.md)
    

