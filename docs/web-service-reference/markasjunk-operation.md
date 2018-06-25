---
title: MarkAsJunk Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1f71f04d-56a9-4fee-a4e7-d1034438329e
description: Hier finden Sie Informationen über die MarkAsJunk EWS Vorgang.
ms.openlocfilehash: b9d79e6fbec87ce41030b4981f3c16f2f9ce9507
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830353"
---
# <a name="markasjunk-operation"></a>MarkAsJunk Operation

Hier finden Sie Informationen zum **MarkAsJunk** EWS-Vorgang. 
  
Der Vorgang **MarkAsJunk** hinzugefügt und entfernt aus der Liste blockierter e-Mail-Benutzer und e-Mail-Nachrichten in den Junk-e-Mail-Ordner verschoben. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-markasjunk-operation"></a>Verwenden des MarkAsJunk-Vorgangs

Der Vorgang **MarkAsJunk** enthält zwei boolesche Optionen, um anzugeben, ob ein e-Mail-Absender zur Liste blockierter Absender hinzugefügt werden soll, und gibt an, ob die Ziel-e-Mail-Nachricht in den Junk-e-Mail-Standardordner oder den Ordner Posteingang verschoben werden sollen. Die Aktionen werden durch die Werte der Attribute **IsJunk** und **MoveItem** bestimmt. Im folgenden sind die möglichen Aktionen basierend auf den Wertkombinationen für die Attribute **IsJunk** und **MoveItem** : 
  
- Wenn das **IsJunk** -Attribut auf **true**festgelegt ist und das **MoveItem** -Attribut auf **true**festgelegt ist, der Absender der e-Mail-Zielnachricht wird die Liste der blockierten Absender hinzugefügt, und die e-Mail-Nachricht in den Junk-e-Dmail Ordner verschoben wird.
    
- Wenn das **IsJunk** -Attribut auf **true**festgelegt ist und das **MoveItem** -Attribut auf **false**festgelegt ist, wird der Absender der e-Mail-Zielnachricht die Liste der blockierten Absender hinzugefügt, und die e-Mail-Nachricht wird nicht aus dem Ordner verschoben.
    
- Wenn das Attribut **IsJunk** festgelegt ist auf **false**und der **MoveItem** -Attribut auf **true fest,** den Absender der Ziel-e-Mail-Messageis aus der Liste blockierter Absender entfernt festgelegt ist und die e-Mail-Nachricht wird in den Ordner Posteingang verschoben.
    
- Wenn das **IsJunk** -Attribut auf **false**festgelegt ist und das **MoveItem** -Attribut auf **false**festgelegt ist, wird der Absender der e-Mail-Zielnachricht aus der Liste blockierter Absender entfernt und die e-Mail-Nachricht wird nicht aus dem Ordner verschoben.
    
> [!IMPORTANT]
> Der Inhalt der Liste blockierter Absender sind nicht von EWS sichtbar. Wenn ein Absender zur Liste blockierter Absender hinzugefügt wird, müssen Sie eine Kopie einer e-Mail-Nachricht, die von der blockierten Absender gesendet, um den Absender in der Zukunft Aufheben der Blockierung zu speichern. 
  
### <a name="markasjunk-operation-soap-headers"></a>MarkAsJunk Vorgang SOAP-Header

Der Vorgang **MarkAsJunk** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |["ExchangeImpersonation"](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="markasjunk-operation-request-example-add-a-sender-to-the-blocked-sender-list"></a>MarkAsJunk Vorgang-anforderungsbeispiel: einen Absender zur Liste blockierter Absender hinzufügen

Im folgenden Beispiel wird eine **MarkAsJunk** Vorgang Anforderung veranschaulicht den Absender einer e-Mail aus der Liste blockierter Absender hinzufügen und die e-Mail-Nachricht in den Junk-e-Mailordner verschieben. Der **MarkAsJunk** -Vorgang akzeptiert den eigenen e-Mail-Nachrichtenbezeichner, um die e-Mail-Nachricht zu ermitteln, die verwendet wird, um den Absender verweisen, der die die Liste der blockierten Absender hinzugefügt wird. 
  
> [!NOTE]
> Bezeichner für alle Elemente aus, und Ändern von Schlüsseln in diesem Artikel wurde gekürzt, um die Lesbarkeit zu erhalten. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
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

Die Anforderung SOAP-Text enthält die folgenden Elemente:
  
- [MarkAsJunk](markasjunk.md)
    
- [Artikelnummern ein.](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="successful-markasjunk-operation-response"></a>Erfolgreiche MarkAsJunk Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **MarkAsJunk** Vorgang an einen Absender zur Liste blockierter Absender hinzufügen und die e-Mail-Nachricht in den Junk-e-Mail-Ordner verschieben. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                             MinorVersion="0" 
                             MajorBuildNumber="545" 
                             MinorBuildNumber="11" 
                             Version="Exchange2013" 
                             xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                             xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema">
        <m:MarkAsJunkResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

Die Antwort SOAP-Text enthält die folgenden Elemente:
  
- [MarkAsJunkResponse](markasjunkresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MarkAsJunkResponseMessage](markasjunkresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [MovedItemId](moveditemid.md)
    
## <a name="markasjunk-operation-request-example-remove-a-sender-from-the-blocked-sender-list"></a>MarkAsJunk Vorgang-anforderungsbeispiel: Entfernen von einem Absender aus der Liste blockierter Absender

Im folgenden Beispiel wird eine **MarkAsJunk** Vorgang Anforderung veranschaulicht den Absender einer e-Mail-Nachricht aus der Liste blockierter Absender entfernen und die e-Mail-Nachricht in den Ordner Posteingang zu verschieben. Sie müssen eine e-Mail-Nachricht, die von der blockierten Absender gesendet, um den Absender aus der Liste der blockierten Absender zu entfernen. Die e-Mail-Adresse des Absenders ist zugeordnet, mit der e-Mail-Nachrichten, die vom Absender gesendet wurden. Entfernen von einem Absender aus der Liste blockierter Absender erfolgreich nicht, wenn die Verweis e-Mail-Nachricht in das Postfach des Benutzers nicht mehr vorhanden ist. Die Element-ID verwendet, um den Absender eine e-Mail-Nachricht zuordnen muss ein Element zugeordnet werden, die in der Exchange-Postfach vorhanden ist. Es wird empfohlen, dass Sie Erstellen eines ausgeblendeten Ordners zum Speichern von Elementen, die von zuvor blockierten Absendern gesendet werden, sodass die Absender in der Clientanwendung aufgehoben werden können. Wenn ein Element aus dem Exchange-Postfach entfernt wurde, muss ein Administrator die Exchange-Verwaltungskonsole verwenden, um Zugriff auf die Liste der blockierten Absender, um einem Absender aus der Liste zu entfernen. Informationen zum Aufheben der Blockierung ein Benutzers mithilfe der Exchange-Verwaltungskonsole finden Sie unter [Gewusst wie: Konfigurieren des sicherer Absender und blockierter Absender Settings in Office 365](http://support.microsoft.com/kb/2545137).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
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

Eine erfolgreiche Antwort für das Entfernen von eines Absenders aus der Liste der blockierten Absender ist identisch mit der Antwort für das einen Absender zur Liste blockierter Absender hinzufügen.
  
Die Anforderung SOAP-Text enthält die folgenden Elemente:
  
- [MarkAsJunk](markasjunk.md)
    
- [Artikelnummern ein.](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="markasjunk-operation-error-response"></a>MarkAsJunk Vorgang Fehlerantwort

Das folgende Beispiel zeigt eine Fehlerantwort an eine **MarkAsJunk** Vorgang Anforderung. Dies ist eine Antwort auf eine Anforderung zum Hinzufügen oder Entfernen von einem Absender aus der Liste blockierter Absender bei die e-Mail-Nachricht durch den Bezeichner des Elements angegeben nicht mehr im Postfach vorhanden ist. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="545" 
                         MinorBuildNumber="11" 
                         Version="Exchange2013" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:MarkAsJunkResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:
  
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
    

