---
title: MarkAsJunk-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1f71f04d-56a9-4fee-a4e7-d1034438329e
description: Hier finden Sie Informationen zum MarkAsJunk-EWS-Vorgang.
ms.openlocfilehash: 25d6b01dfff64c4e45f3382223311219d349c165
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468572"
---
# <a name="markasjunk-operation"></a>MarkAsJunk-Vorgang

Hier finden Sie Informationen zum **MarkAsJunk** -EWS-Vorgang. 
  
Mit dem **MarkAsJunk** -Vorgang werden Benutzer aus der Liste blockierter e-Mails hinzugefügt und entfernt und e-Mail-Nachrichten in den Ordner Junk-e-Mail verschoben 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-markasjunk-operation"></a>Verwenden des MarkAsJunk-Vorgangs

Der **MarkAsJunk** -Vorgang enthält zwei boolesche Optionen, um anzugeben, ob ein e-Mail-Absender zur Liste blockierter Absender hinzugefügt werden soll und ob die Ziel-e-Mail in den standardmäßigen Junk-e-Mail-Ordner oder in den Ordner Posteingang verschoben werden soll. Die Aktionen werden durch die Werte der Attribute **isjunk** und **MoveItem** bestimmt. Im folgenden sind die möglichen Aktionen basierend auf den Wertkombinationen für die Attribute **isjunk** und **MoveItem** aufgeführt: 
  
- Wenn das **isjunk** -Attribut auf **true**festgelegt ist und das **MoveItem** -Attribut auf **true**festgelegt ist, wird der Absender der Ziel-e-Mail-Nachricht zur Liste blockierter Absender hinzugefügt, und die e-Mail-Nachricht wird in den Ordner Junk-dmail verschoben.
    
- Wenn das **isjunk** -Attribut auf **true**festgelegt ist und das **MoveItem** -Attribut auf **false**festgelegt ist, wird der Absender der Ziel-e-Mail-Nachricht zur Liste blockierter Absender hinzugefügt, und die e-Mail-Nachricht wird nicht aus dem Ordner verschoben.
    
- Wenn das **isjunk** -Attribut auf **false**festgelegt ist und das **MoveItem** -Attribut auf **true**festgelegt ist, wird der Absender der Ziel-e-Mail-Nachricht aus der Liste blockierter Absender entfernt, und die e-Mail-Nachricht wird in den Ordner Posteingang verschoben.
    
- Wenn das **isjunk** -Attribut auf **false**festgelegt ist und das **MoveItem** -Attribut auf **false**festgelegt ist, wird der Absender der Ziel-e-Mail-Nachricht aus der Liste blockierter Absender entfernt, und die e-Mail-Nachricht wird nicht aus dem Ordner verschoben.
    
> [!IMPORTANT]
> Der Inhalt der Liste blockierter Absender ist nicht von EWS auffindbar. Wenn der Liste blockierter Absender ein Absender hinzugefügt wird, müssen Sie eine Kopie einer vom blockierten Absender gesendeten e-Mail-Nachricht behalten, um den Absender zukünftig aufzuheben. 
  
### <a name="markasjunk-operation-soap-headers"></a>SOAP-Header des MarkAsJunk-Vorgangs

Der **MarkAsJunk** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="markasjunk-operation-request-example-add-a-sender-to-the-blocked-sender-list"></a>MarkAsJunk-Vorgangs Anforderungs Beispiel: Hinzufügen eines Absenders zur Liste blockierter Absender

Im folgenden Beispiel einer **MarkAsJunk** -Vorgangsanforderung wird gezeigt, wie der Absender einer e-Mail zur Liste blockierter Absender hinzugefügt und die e-Mail in den Junk-e-Mail-Ordner verschiebt wird. Der **MarkAsJunk** -Vorgang akzeptiert die eindeutige ID der e-Mail-Nachricht, um die e-Mail zu identifizieren, die zum Verweisen auf den Absender verwendet wird, der der Liste blockierter Absender hinzugefügt wurde. 
  
> [!NOTE]
> Alle Element-IDs und Änderungsschlüssel in diesem Artikel wurden verkürzt, um die Lesbarkeit zu erhalten. 
  
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

Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:
  
- [MarkAsJunk](markasjunk.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="successful-markasjunk-operation-response"></a>Erfolgreiche Reaktion des MarkAsJunk-Vorgangs

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **MarkAsJunk** -Vorgangsanforderung zum Hinzufügen eines Absenders zur Liste blockierter Absender und zum Verlegen der e-Mail-Nachricht in den Junk-e-Mail-Ordner. 
  
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

Der SOAP-Antworttext Körper enthält die folgenden Elemente:
  
- [MarkAsJunkResponse](markasjunkresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MarkAsJunkResponseMessage](markasjunkresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [MovedItemId](moveditemid.md)
    
## <a name="markasjunk-operation-request-example-remove-a-sender-from-the-blocked-sender-list"></a>MarkAsJunk-Vorgangs Anforderungs Beispiel: Entfernen eines Absenders aus der Liste blockierter Absender

Im folgenden Beispiel einer **MarkAsJunk** -Vorgangsanforderung wird gezeigt, wie der Absender einer e-Mail-Nachricht aus der Liste blockierter Absender entfernt und die e-Mail-Nachricht in den Ordner Posteingang verschoben wird. Sie müssen eine vom blockierten Absender gesendete e-Mail-Nachricht beibehalten, um den Absender aus der Liste blockierter Absender zu entfernen. Die e-Mail-Adresse des Absenders ist e-Mail-Nachrichten zugeordnet, die vom Absender gesendet wurden. Das Entfernen eines Absenders aus der Liste blockierter Absender ist nicht erfolgreich, wenn die Referenz-e-Mail-Nachricht nicht mehr im Postfach des Benutzers vorhanden ist. Die Element-ID, die zum Zuordnen einer e-Mail-Nachricht zu ihrem Absender verwendet wird, muss einem Element zugeordnet sein, das im Exchange-Postfach vorhanden ist. Es wird empfohlen, einen ausgeblendeten Ordner zum Speichern von Elementen zu erstellen, die von zuvor blockierten Absendern gesendet wurden, sodass die Blockierung der Absender von der Clientanwendung aufgehoben werden kann. Für den Fall, dass ein Element aus dem Exchange-Postfach entfernt wurde, muss ein Administrator die Exchange-Verwaltungskonsole verwenden, um auf die Liste blockierter Absender zuzugreifen, um einen Absender aus der Liste zu entfernen. Informationen zum Aufheben der Blockierung eines Benutzers mithilfe der Exchange-Verwaltungskonsole finden Sie unter [Konfigurieren der Einstellungen für sichere Absender und blockierte Absender in Office 365](https://support.microsoft.com/kb/2545137).
  
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

Eine erfolgreiche Antwort zum Entfernen eines Absenders aus der Liste blockierter Absender ist identisch mit der Antwort zum Hinzufügen eines Absenders zur Liste blockierter Absender.
  
Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:
  
- [MarkAsJunk](markasjunk.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="markasjunk-operation-error-response"></a>Fehlerantwort des MarkAsJunk-Vorgangs

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **MarkAsJunk** -Vorgangsanforderung. Dies ist eine Antwort auf eine Anforderung zum Hinzufügen oder Entfernen eines Absenders aus der Liste blockierter Absender, wenn die durch die Element-ID angegebene e-Mail-Nachricht nicht mehr im Postfach vorhanden ist. 
  
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
    

