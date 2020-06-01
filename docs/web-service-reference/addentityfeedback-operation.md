---
title: AddEntityFeedback-Vorgang
manager: luken
ms.date: 4/18/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 00e40197-5794-4268-b937-bd65aa044890
description: Der AddEntityFeedback-Vorgang gibt Fehlerinformationen zurück, die serverseitigen Problemen entsprechen.
ms.openlocfilehash: a1027a0a1ee06cf3e83833b1d84c13d77b07c0b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458439"
---
# <a name="addentityfeedback-operation"></a>AddEntityFeedback-Vorgang

Der **AddEntityFeedback** -Vorgang gibt Fehlerinformationen zurück, die serverseitigen Problemen entsprechen. 
  
Dieser Vorgang basiert auf dem Typ des protokollierten Ereignisses. Eines der wichtigsten Ereignisse ist **EntityAdded**, das einer Entität entspricht, die ausgewählt wird. Dieser Vorgang ist Batch, sodass er zum Protokollieren von Batches von Einträgen in einer einzelnen Anforderung verwendet werden kann. 
  
## <a name="findpeople-request-examples"></a>FindPeople-Anforderungs Beispiele

Der **AddEntityFeedback** -Vorgang bietet Clients die Möglichkeit, Details zur Interaktion mit vom Dienst zurückgegebenen Entitäten zu protokollieren. Dies kann als Signal verwendet werden, um die Relevanz hinter den Kulissen für jeden Client zu verbessern. Beispielsweise können Clients diesen Vorgang verwenden, um Feedback zu Personen Entitäten bereitzustellen, die von **FindPeople**zurückgegeben werden.
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
                             xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                             xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:AddEntityFeedback>
            <m:EntityFeedbackEntries>
                  <t:EntityFeedbackEntry>
                        <t:ClientEventTimeUTC> 2015-07-05T22:16:18+00:00</t:ClientEventTimeUTC>
                        <t:ClientEventTimeLocal> 2015-07-05T22:16:18+00:00</t:ClientEventTimeLocal>
                        <t:ClientSessionId>00000000-0000-0000-0000-000000000012</t:ClientSessionId>
                        <t:ClientVersion>15.01.0101.01</t:ClientVersion>
                        <t:ClientId>Web</t:ClientId>
                        <t:TransactionId>123456789</t:TransactionId>
                        <t:EventType>EntityAdded</t:EventType>
                        <t:TargetEntityList>["a","b","c"]</t:TargetEntityList>
                        <t:SourceOfEntityAdded></t:SourceOfEntityAdded>
                        <t:JSONPropertyBag></t:JSONPropertyBag>
                  </t:EntityFeedbackEntry>
                  <t:EntityFeedbackEntry>
                  …
                  </t:EntityFeedbackEntry>
            </m:EntityFeedbackEntries>
      </m:AddEntityFeedback>
   </soap:Body>
</soap:Envelope>

```

### <a name="the-request-soap-body-contents"></a>Der Inhalt des SOAP-Anforderungstexts

Die SOAP-Anforderung enthält ein einzelnes Element **EntityFeedbackEntries**. Dies wiederum enthält ein Array von **EntityFeedbackEntry** -Objekten. Jeder Eintrag im Array kann die folgenden Elemente enthalten: 
  
|**Anforderungsparameter**|**Erforderlich**|**Beschreibung**|**Typ**|
|:-----|:-----|:-----|:-----|
|**ClientEventTimeUtc** <br/> |Ja  <br/> |Die UTC-Zeit, zu der das Ereignis auf Clientseite aufgetreten ist.  <br/> |DateTime  <br/> |
|**ClientEventTimeLocal** <br/> |Ja  <br/> |Die lokale Zeit, zu der das Ereignis auf der Clientseite aufgetreten ist.  <br/> |DateTime  <br/> |
|**ClientID** <br/> |Ja  <br/> |Typ des Clients (beispielsweise Outlook, OWA usw.).  <br/> |ClientIDType-Aufzählung  <br/> |
|**ClientSessionId** <br/> |Ja  <br/> |GUID, die die Sitzungs-ID identifiziert. Auf dem Client generiert.  <br/> |GUID  <br/> |
|**ClientVersion** <br/> |Ja  <br/> |Version des Clients (beispielsweise 15.01.0101.000).  <br/> |Zeichenfolge  <br/> |
|**EntityAddSource** <br/> |Nein  <br/> |Quelle für EntityAded (E.g., EntityRelevanceAPI, types, pasted).  <br/> |EntityAddSource-Aufzählung  <br/> |
|**EntrySequenceNumber** <br/> |Ja  <br/> |Eine inkrementelle ganze Zahl pro Clientsitzung. Wird zum Erkennen von Datenverlusten verwendet.  <br/> |Int  <br/> |
|**EventType** <br/> |Ja  <br/> |Typ des Ereignisses (z.b. Entität hinzugefügt, Entität entfernt).  <br/> |Zeichenfolge  <br/> |
|**JSONPropertyBag** <br/> |Nein  <br/> |Zusätzliche Eigenschaften, die dem Ereignis zugeordnet sind (JSON-BLOB von Schlüssel/Wert-Paaren).  <br/> |JSON-BLOB  <br/> |
|**TargetEntityList** <br/> |Nein  <br/> |Liste der Entitäten, die dem Ereignis zugeordnet sind.  <br/> |JSON-Zeichenfolge  <br/> |
|**TransactionId** <br/> |Nein  <br/> |ID (GUID) korrelieren der ID in Abfrageprotokollen.  <br/> |Zeichenfolge  <br/> |
   
### <a name="successful-addentityfeedback-operation-response"></a>Erfolgreiche Reaktion des AddEntityFeedback-Vorgangs

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                                MinorVersion="1" 
                                MajorBuildNumber="228" 
                                MinorBuildNumber="0" 
                                Version="V2_49" 
                                xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                                xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" 
                                                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                                              xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                                              xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope> 

```

### <a name="the-response-soap-body-contains-the-following-elements"></a>Der SOAP-Antworttext Körper enthält die folgenden Elemente:

#### <a name="errors"></a>Fehler 
  
Die API kann einen Batch von Feedback Einträgen protokollieren, wir protokollieren alles, was wir können. Dieses Feld stellt die Anzahl der Fehlereinträge dar, die nicht protokolliert wurden.
    
#### <a name="errordetails"></a>ErrorDetails
  
Details zu den oben aufgeführten Fehlern werden durch getrennt `;` .
    
### <a name="currently-supported-values"></a>Derzeit unterstützte Werte

|**ClientIdType-Aufzählung**|
|:-----|
|Desktop  <br/> |
|Exchange  <br/> |
|IMAP4  <br/> |
|Lync  <br/> |
|MacMail  <br/> |
|MacOutlook  <br/> |
|Mobil  <br/> |
|Andere  <br/> |
|Outlook  <br/> |
|Outlook Service  <br/> |
|POP3  <br/> |
|Tablet  <br/> |
|Web  <br/> |
   
|**EntityAddSource-Aufzählung**|
|:-----|
|ActiveDirectory  <br/> |
|EntityRelevanceApi  <br/> |
|EntityRelevanceApiCache  <br/> |
|ExplicitTyping  <br/> |
|LocalCache  <br/> |
|LocalCacheAndEntityRelevanceAPI  <br/> |
|Keine  <br/> |
|Andere  <br/> |
|Einfügen  <br/> |
   
### <a name="addentityfeedback-operation-error-response"></a>Fehlerantwort des AddEntityFeedback-Vorgangs

Informationen zu Fehlercodes, die für EWS allgemein sind, finden Sie unter [Response Code](responsecode.md).
  
### <a name="example-of-addentityfeedback-in-conjunction-with-findpeople"></a>Beispiel für AddEntityFeedback in Verbindung mit FindPeople

#### <a name="findpeople-request"></a>FindPeople-Anforderung
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
<soap:Body >
    <m:FindPeople>
      <m:IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="100" Offset="0"/>
      <m:QueryString>user1</m:QueryString>
      <m:SearchPeopleSuggestionIndex>true</m:SearchPeopleSuggestionIndex>
    </m:FindPeople>
  </soap:Body>
</soap:Envelope>    
    
```

#### <a name="findpeople-response"></a>FindPeople-Antwort

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <FindPeopleResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <People>
                <Persona xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                    <PersonaId Id="AAUQAFjZ4UxX8SZCqSPFsmh0cSo=" />
                    <PersonaType>Person</PersonaType>
                    <CreationTime>2015-10-02T23:25:42</CreationTime>
                    <DisplayName>user2</DisplayName>
…
                  </Persona>
            </People>
            <TotalNumberOfPeopleInView>0</TotalNumberOfPeopleInView>
            <FirstMatchingRowIndex>0</FirstMatchingRowIndex>
            <FirstLoadedRowIndex>0</FirstLoadedRowIndex>
            <TransactionId>b56ad16e-5d5a-4574-90f8-b8dd57382be6</TransactionId>
        </FindPeopleResponse>
    </s:Body>
</s:Envelope>

```

#### <a name="addentityfeedback-request"></a>AddEntityFeedback-Anforderung

```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:AddEntityFeedback>
<m:EntityFeedbackEntries>
<t:EntityFeedbackEntry>
         <t:ClientEventTimeUtc>2015-07-05T22:16:18+00:00</t:ClientEventTimeUtc>
         <t:ClientEventTimeLocal>2015-07-05T22:16:18+00:00</t:ClientEventTimeLocal>
         <t:ClientSessionId>00000000-0000-0000-0000-000000000012</t:ClientSessionId>
         <t:ClientVersion>15.01.0101.01</t:ClientVersion>
         <t:ClientId>Web</t:ClientId>
         <t:TransactionId>b56ad16e-5d5a-4574-90f8-b8dd57382be6</t:TransactionId>
         <t:EventType>EntityAdded</t:EventType>
         <t:TargetEntityList>["user1@ms7.com"]</t:TargetEntityList>
         <t:SourceOfEntityAdded>EntityRelevanceApi</t:SourceOfEntityAdded>
         <t:JSONPropertyBag></t:JSONPropertyBag>
</t:EntityFeedbackEntry>
</m:EntityFeedbackEntries>
      </m:AddEntityFeedback>
   </soap:Body>
</soap:Envelope>

```

> [!NOTE]
> Verwenden der FindPeople-Antwort Transaktions-ID als AddEntityFeedback-Anforderungs Transaktions-ID. 
  
#### <a name="addentityfeedback-response"></a>AddEntityFeedback-Antwort

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope>

```


