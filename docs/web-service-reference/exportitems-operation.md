---
title: ExportItems-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExportItems
api_type:
- schema
ms.assetid: e2846abb-0b16-4732-bbd8-038a674672f6
description: Der Export Items-Vorgang exportiert Elemente aus einem Postfach.
ms.openlocfilehash: 547a490a27d2414d2eda1d89cdac036a34eddccd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526046"
---
# <a name="exportitems-operation"></a>ExportItems-Vorgang

Der **Export Items** -Vorgang exportiert Elemente aus einem Postfach. 
  
## <a name="exportitems-request-example"></a>Export Items-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer **Export Items** -Anforderung wird gezeigt, wie Sie eine Anforderung zum Abrufen von drei aus einem Postfach exportierten Elementen erstellen. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
      xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:ExportItems>
      <m:ItemIds>
        <t:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89GAAA="/>
        <t:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89FAAA="/>
        <t:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY87NAAA="/>
      </m:ItemIds>
    </m:ExportItems>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a>Kommentar

Die Element-IDs im Beispiel wurden verkürzt, um die Lesbarkeit zu erhalten.
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [RequestServerVersion](requestserverversion.md)
    
- [ExportItems](exportitems.md)
    
- [Itemids (NonEmptyArrayOfItemIdsType)](itemids-nonemptyarrayofitemidstype.md)
    
- [ItemId](itemid.md)
    
## <a name="successful-exportitems-response-example"></a>Erfolgreiches Export Items-Antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **Export Items** -Anforderung. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <t:ServerVersionInfo MajorVersion="14"
    MinorVersion="1"
    MajorBuildNumber="139"
    MinorBuildNumber="0"
    Version="Exchange2010_SP1"
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
    xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ExportItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ExportItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89GAAA=" ChangeKey="FwAAAA=="/>
          <m:Data>
            AQAAAAgAAAAAAAAALgBlAHgAdABlAHMAdAAuAG0AaQBjAHIAbwBzAG8AZgB0AC4A
            YwBvAG0AAABTAE0AVABQAAAAVQBzAGUAcgAyAEAAYQB1AGoAaQBuAGcALQBkAG8AbQAuAGUA
            eAB0AGUAcwB0AC4AbQBpAGMAcgBvAHMAbwBmAHQALgBjAG8AbQAAALCE/jlMAAAAVQBzAGUA
            cgAyAEAAYQB1AGoAaQBuAGcALQBkAG8AbQAuAGUAeAB0AGUAcwB0AC4AbQBpAGMAcgBvAHMA
            bwBmAHQALgBjAG8AbQAAAAMAADkAAAAAAwD+DwYAAAADAARAAwACQAMADkA=
          </m:Data>
        </m:ExportItemsResponseMessage>
        <m:ExportItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89FAAA=" ChangeKey="FwAAAA=="/>
          <m:Data>
            AQAAAAgAAAAAAAAAAQAAAAMAAAAYAAAAAQAAAAcDAgAAAAAAwAAAAAAAAEYAJACA
            QAAyAAAh9SpR08oBAwAEQAMAFkANABMOAwAAQAMAIQ4AAAAAsIQSN0oAAAAyAGEAYgAxADYA
            MQA2ADYALQBhAGUANQBkAC0ANAAyAGUAZgAtAGEANQA1ADkALQBjADgAOQAwADgANwBkADIA
            MwBkADgANAAAAAMACzf/////AwAgDmQEAAADAPcPAAAAAEAABzBPMXstUdPKAUAACDBPMXst
            UdPKAQMABTcFAAAAsIQONx4AAABtAGUAcwBzAGEAZwBlAC8AcgBmAGMAOAAyADIAAACwhAEw
            IgAAAE0AbwBzAHQAIABmAGEAcwBjAGkAbgBhAHQAaQBuAGcAAAACAfkPBAAAAAAAAAADAAFA
            FABKZ3QrAAAAZF2mAwAXAAEAAACwhBoAEgAAAEkAUABNAC4ATgBvAHQAZQAAAAMANgAAAAAA
            sIQ3ACIAAABNAG8AcwB0ACAAZgBhAHMAYwBpAG4AYQB0AGkAbgBnAAAAQAA5AACq+za80coB
            AgE7AGUAAABFWDovTz1GSVJTVCBPUkdBTklaQVRJT04vT1U9RVhDSEFOR0UgQURNSU5JU1RS
            QVRJVkUgR1JPVVAgKEZZRElCT0hGMjNTUERMVCkvQ049UkVDSVBJRU5UUy9DTj1VU0VST05F
            ALCEPQACAAAAAAACAUEAfgAAAAAAAADcp0DIwEIQGrS5CAArL+GCAQAAAAAAAAAvTz1GSVJT
            VCBPUkdBTklaQVRJT04vT1U9RVhDSEFOR0UgQURNSU5JU1RSQVRJVkUgR1JPVVAgKEZZRElC
            T0hGMjNTUERMVCkvQ049UkVDSVBJRU5UUy9DTj1VU0VST05FALCEQgAQAAAAVQB
          </m:Data>
        </m:ExportItemsResponseMessage>
        <m:ExportItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY87NAAA=" ChangeKey="CQAAAA=="/>
          <m:Data>
            AQAAAAgAAAAAAAAAAQAAAAMAAAAYAAAAAQAAAAcDAgAAAAAAwAAAAAAAAEYAJACA
            BAAAAAYAAAABDouAAAACAAAAEiAAAOSECEBbAAAAL089RklSU1QgT1JHQU5JWkFUSU9OL09V
            PUVYQ0hBTkdFIEFETUlOSVNUUkFUSVZFIEdST1VQIChGWURJQk9IRjIzU1BETFQpL0NOPVJF
            Q0lQSUVOVFMvQ049AAMAFwABAAAAsIQaABIAAABJAFAATQAuAE4AbwB0AGUAAAALACMAAAAL
            ACkAAAADADYAAAAAALCENwAyAAAASQBuAHQAZQByAGUAcwB0AGkAbgBnACAALQAgAGYAcgBv
            AG0AIABFAFcAUwBNAEEAAABAADkAAHZeFxfRygECATsAZQAAAEVYOi9PPUZJUlNUIE9SR0FO
            SVpBVElPTi9PVT1FWENIQU5HRSBBRE1JTklTVFJBVElWRSBHUk9VUCAoRllESUJPSEYyM1NQ
            RExUKS9DTj1SRUNJUElFTlRTL0NOPVVTRVJPTkUAsIQ9AAIAAAAAAAIBPwB+AAAAAAAAANyn
            QMjAQhAatLkIACsv4YIBAAAAAAAAAC9PPUZJUlNUIE9SR0FOSVpBVElPTi9PVT1FWENIQU5H
          </m:Data>
        </m:ExportItemsResponseMessage>
      </m:ResponseMessages>
    </m:ExportItemsResponse>
  </s:Body>
</s:Envelope>
```

### <a name="comment"></a>Kommentar

Die Element-IDs und Änderungsschlüssel im Beispiel wurden verkürzt, um die Lesbarkeit zu erhalten.
  
### <a name="response-elements"></a>Response-Elemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ExportItemsResponse](exportitemsresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ExportItemsResponseMessage](exportitemsresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [ItemId](itemid.md)
    
- [Data (base64Binary)](data-base64binary.md)
    
## <a name="exportitems-error-response-example"></a>Export Items-Fehlerantwort Beispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Antwort auf die **Export Items** -Anforderung, die zwei Fehler und ein erfolgreich exportiertes Element enthält. Das erste Element im Beispiel wird erfolgreich exportiert. Das zweite Element enthält einen falschen Änderungsschlüssel. Das dritte Element stellt einen Versuch dar, ein Element aus dem falschen Postfach zu exportieren. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="164" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ExportItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                           xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ExportItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ItemId Id="AAMkADhhOGU0oMf0GPIQeAAAAUC8iAABseAAAAUFZ7AAA=" ChangeKey="CQAAAA=="/>
          <m:Data>
            AQAAAAgAAAAAAAAALgBlAHgAdABlAHMAdAAuAG0AaQBjAHIAbwBzAG8AZgB0AC4A
            YwBvAG0AAABTAE0AVABQAAAAVQBzAGUAcgAyAEAAYQB1AGoAaQBuAGcALQBkAG8AbQAuAGUA
            eAB0AGUAcwB0AC4AbQBpAGMAcgBvAHMAbwBmAHQALgBjAG8AbQAAALCE/jlMAAAAVQBzAGUA
            cgAyAEAAYQB1AGoAaQBuAGcALQBkAG8AbQAuAGUAeAB0AGUAcwB0AC4AbQBpAGMAcgBvAHMA
            bwBmAHQALgBjAG8AbQAAAAMAADkAAAAAAwD+DwYAAAADAARAAwACQAMADkA=
          </m:Data>
        </m:ExportItemsResponseMessage>
        <m:ExportItemsResponseMessage ResponseClass="Error">
          <m:MessageText>The change key is invalid.</m:MessageText>
          <m:ResponseCode>ErrorInvalidChangeKey</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ExportItemsResponseMessage>
        <m:ExportItemsResponseMessage ResponseClass="Error">
          <m:MessageText>No mailbox with such guid.</m:MessageText>
          <m:ResponseCode>ErrorNonExistentMailbox</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:MessageXml>
            <t:Value Name="MailboxGuid">f3f6f699-2254-40ce-9994-388d9d98419e</t:Value>
          </m:MessageXml>
        </m:ExportItemsResponseMessage>
      </m:ResponseMessages>
    </m:ExportItemsResponse>
  </s:Body>
</s:Envelope>

```

### <a name="comments"></a>Comments

Die Element-IDs, Änderungsschlüssel und Daten im Beispiel wurden verkürzt, um die Lesbarkeit zu erhalten.
  
### <a name="error-response-elements"></a>Fehlerantwortelemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ExportItemsResponse](exportitemsresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ExportItemsResponseMessage](exportitemsresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [ItemId](itemid.md)
    
- [Data (base64Binary)](data-base64binary.md)
    
- [MessageText](messagetext.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Messagexml verwendet](messagexml.md)
    
- **Wert**
    
> [!NOTE]
> Das **value** -Element ist im Schema nicht vorhanden. Dieses Element ist gültig, da das [messagexml verwendet](messagexml.md) -Element, in dem das **value** -Instanzelement auftritt, alle wohlgeformten XML-Daten enthalten kann. 
  
## <a name="see-also"></a>Siehe auch



[UploadItems-Vorgang](uploaditems-operation.md)


[EWS-Operationen in Exchange](ews-operations-in-exchange.md)
  
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

