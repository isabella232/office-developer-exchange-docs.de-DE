---
title: Vorschlagen einer neuen Besprechungszeit mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d5ac8e5b-3876-4f20-b4d3-44505e066042
description: Erfahren Sie, wie Sie neue Besprechungszeiten in Ihrer Exchange-Clientanwendung mithilfe von EWS in Exchange vorschlagen.
ms.openlocfilehash: 4f001bb82d2325624b567412620283619b51f25b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456811"
---
# <a name="propose-a-new-meeting-time-by-using-ews-in-exchange"></a>Vorschlagen einer neuen Besprechungszeit mithilfe von EWS in Exchange

Erfahren Sie, wie Sie neue Besprechungszeiten in Ihrer Exchange-Clientanwendung mithilfe von EWS in Exchange vorschlagen.
  
Mit dem Feature neue Zeit vorschlagen können Teilnehmer dem Besprechungsorganisator neue Besprechungszeiten als Teil des Exchange-Kalender Workflows vorschlagen. Wenn ein Teilnehmer eine neue Besprechung vorschlägt, kann der Organisator die vorgeschlagene neue Besprechungszeit verwenden, um die Besprechung zu aktualisieren und Updates an alle Teilnehmer zu senden. Bevor Sie Teilnehmern die Möglichkeit geben, neue Besprechungszeiten vorzuschlagen, müssen Sie ermitteln, ob der Organisator neue Zeit Vorschläge zulässt. In diesem Artikel wird beschrieben, wie Sie bestimmen können, ob Sie eine neue Zeit vorschlagen und wie Sie EWS verwenden, um eine neue Zeit anzubieten.
  
> [!NOTE]
> Die verwaltete EWS-API implementiert diese Funktion nicht. 
  
## <a name="determine-whether-you-can-propose-a-new-time-for-a-meeting-by-using-ews"></a>Ermitteln, ob Sie eine neue Zeit für eine Besprechung mithilfe von EWS vorschlagen können
<a name="bk_Determine"> </a>

Bevor Sie eine neue Zeit für eine Besprechung vorschlagen können, müssen Sie einen Verweis auf diese Besprechung finden und bestimmen, ob der Besprechungsorganisator die Besprechung so konfiguriert hat, dass neue Zeit Vorschläge unterstützt werden. Sie können einen Verweis auf eine Besprechung erhalten, indem Sie einen der folgenden Schritte ausführen: 
  
- Suchen der Besprechungsanfrage im Posteingang
    
- Suchen des Termins im Kalender
    
Führen Sie die folgenden Schritte aus, um eine Besprechungs Referenz zu finden:
  
1. Verwenden Sie den [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -EWS-Vorgang (oder die [Folder. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=EXCHG.80%29.aspx) verwaltete EWS-API-Methode), um die Ziel-Besprechungsanfrage oder das Kalenderelement zu finden. Alternativ können Sie den [SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) -EWS-Vorgang verwenden, um den Bezeichner der Ziel-Besprechungsanfrage oder des Kalenderelements abzurufen. 
    
2. Analysieren Sie die Ergebnisse des **FindItem** -Vorgangs (oder der **Folder. FindItems** -Methode), um den Elementbezeichner des Besprechungselements abzurufen. 
    
3. Verwenden Sie den [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) -EWS-Vorgang, um die Response-Objekte für die Besprechung abzurufen. 
    
Der folgende XML-Code zeigt, was gesendet wird, um die Response-Objekte für ein Element anzufordern.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:MailboxCulture>en-US</t:MailboxCulture>
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:ResponseObjects"/>
          <t:FieldURI FieldURI="item:Subject"/>
          <t:FieldURI FieldURI="calendar:Start"/>
          <t:FieldURI FieldURI="calendar:End"/>
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkADEzOTExYjJkL1AAA=" ChangeKey="CwAAAB/G6X"/>
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

Die **GetItem** -Vorgangs Antwort sieht ähnlich wie beim folgenden XML-Code aus, wenn Sie die Element-ID, die Start-und Endzeit der Besprechung, die Auflistung der Antwortobjekte anfordern und die vorgeschlagene Änderung an der Besprechungszeit durch den Organisator ermöglicht wird. Die Response-Objektsammlung, die durch das [ResponseObjects](https://msdn.microsoft.com/library/ad29e064-3f3d-4b7b-aa4c-9ec27326381d%28Office.15%29.aspx) -Element dargestellt wird, enthält die Gruppe von Antworten, die für das Kalenderelement gültig sind. Das **ProposeNewTime** -Element ist ein Response-Objekt, das angibt, dass der Benutzer eine neue Zeit für die Besprechung vorschlagen kann. Die [AcceptItem](https://msdn.microsoft.com/library/05a15431-77e1-411a-a16b-5481d364d3cc%28Office.15%29.aspx)-, [TentativelyAcceptItem](https://msdn.microsoft.com/library/ce6f50ef-ad8a-47e4-915a-487b2ef7a2e0%28Office.15%29.aspx)-und [DeclineItem](https://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) -Elemente stellen die Response-Objekte dar, die Sie verwenden können, um dem Besprechungsorganisator eine neue Besprechungszeit vorzuschlagen. 
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:MeetingRequest>
              <t:ItemId Id="AAMkADEzOTExYjJkL1AAA=" ChangeKey="CwAAAB/G6X"/>
              <t:Subject>Competitive analysis: kick off meeting</t:Subject>
              <t:ResponseObjects>
                <t:AcceptItem/>
                <t:TentativelyAcceptItem/>
                <t:DeclineItem/>
                <t:ProposeNewTime/>
                <t:ReplyToItem/>
                <t:ReplyAllToItem/>
                <t:ForwardItem/>
              </t:ResponseObjects>
              <t:Start>2013-11-09T17:00:00Z</t:Start>
              <t:End>2013-11-09T17:30:00Z</t:End>
            </t:MeetingRequest>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="propose-a-new-meeting-time-by-using-ews"></a>Vorschlagen einer neuen Besprechungszeit mithilfe von EWS
<a name="bk_Propose"> </a>

Wenn Sie ein **ProposeNewTime** -Antwortobjekt erhalten haben, als Sie den **GetItem** -Vorgang zum Abrufen eines Kalenderelements oder einer Besprechungsanfrage verwendet haben, können Sie mit einer vorgeschlagenen neuen Besprechungszeit Antworten. Wenn Sie kein **ProposeNewTime** -Antwortobjekt erhalten haben, können Sie im Rahmen des Kalender Workflows keine neue Besprechungszeit vorschlagen. Sie können jedoch dem Organisator Antworten, um eine neue Besprechungszeit anzufordern. Wenn Sie ein **ProposeNewTime** -Antwortobjekt erhalten, können Sie auf die Besprechung Antworten, indem Sie auf Ihren Bezeichner verweisen, und dem Organisator eine neue Besprechungszeit vorschlagen. Hier unterscheidet sich das **ProposeNewTime** -Antwortobjekt von dem typischen Antwortobjekt Muster darin, dass Sie nicht mit einem **ProposeNewTime** -Antwortobjekt Antworten. Sie verwenden eines der anderen Besprechungsantwort Objekte wie **AcceptItem**, **TentativelyAcceptItem**oder **DeclineItem**, um eine neue Besprechung vorzuschlagen. In diesem Beispiel wird das **AcceptItem** -Antwortobjekt verwendet. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013"/>
  </soap:Header>
  <soap:Body>
    <m:CreateItem>
      <m:Items>
        <t:AcceptItem>
          <t:Body BodyType="Text">This time works better for the HiPPO.</t:Body>
          <t:ReferenceItemId Id="AAMkADEzOTExYjJkL1AAA=" ChangeKey="CwAAAB/G6X"/>
          <t:ProposedStart>2013-11-28T04:00:00Z</t:ProposedStart>
          <t:ProposedEnd>2013-11-28T04:30:00Z</t:ProposedEnd>
        </t:AcceptItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

Die Antwort auf diese Anforderung enthält den Bezeichner des Kalenderelements, das dem Kalender des Teilnehmers hinzugefügt wurde, und eine Kopie der Besprechungsanfrage, die im Ordner Gelöschte Elemente des Teilnehmers eingefügt wurde. Die Antwortnachricht mit dem neuen Zeitvorschlag wurde auch im Ordner "Gesendete Elemente" des Teilnehmers gespeichert (Sie müssen die Antwortnachricht für die Besprechung finden, damit ein Handle darauf abgerufen wird).
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkAGRmOWE2OWAAA=" ChangeKey="DwAAJsmU"/>
            </t:CalendarItem>
            <t:MeetingRequest>
              <t:ItemId Id="AAMkAGRmOWE2AAABB=" ChangeKey="AAAGJu1A"/>
            </t:MeetingRequest>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>
```

Der Organisator erhält eine [MeetingResponse](https://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx) -Nachricht, wenn der Teilnehmer mit einer vorgeschlagenen neuen Besprechungszeit antwortet. Die **MeetingResponse** -Nachricht enthält die vorgeschlagene neue Start Zeit für die Besprechung und die Endzeit sowie den Bezeichner des zugeordneten Kalenderelements im Kalender des Organisators. Der Organisator kann diese Informationen verwenden, um das vorhandene Kalenderelement für die Besprechung zu aktualisieren. Im folgenden finden Sie den Workflow für den Organisator, der auf eine **MeetingResponse** -Nachricht antwortet, die eine neue Besprechungszeit vorschlägt: 
  
1. Bestimmen Sie, ob die **ProposedStart** -oder **ProposedEnd** -Elemente in der **MeetingResponse**festgelegt wurden. Wenn dies der Fall ist, fahren Sie mit Schritt 2 fort. Wenn dies nicht der Fall ist, gibt die **MeetingResponse** -Nachricht nur an, ob der Teilnehmer die Besprechung akzeptiert, mit Vorbehalt angenommen oder abgelehnt hat. 
    
2. Abrufen des vorhandenen Kalenderelements des Organisators für die Besprechung mithilfe der EWS-ID, die im **AssociatedCalendarItemId** -Element zurückgegeben wird. 
    
3. Vergleichen Sie die ursprüngliche Anfangs-und Endzeit mit der vorgeschlagenen neuen Besprechungszeit. Wenn die vorgeschlagene neue Besprechungszeit für den Organisator akzeptabel ist, fahren Sie mit Schritt 4 fort. Andernfalls kann der Besprechungsorganisator entweder die vorgeschlagene Besprechungszeit ignorieren oder eine e-Mail-Antwort an den Teilnehmer senden, der die neue Besprechungszeit vorgeschlagen hat.
    
4. Optional Führen Sie einen [GetUserAvailability](https://msdn.microsoft.com/library/8da17226-5d3a-4525-9ffa-d83730f47bb1%28Office.15%29.aspx) -EWS-Vorgangsaufruf aus, um herauszufinden, ob die vorgeschlagene Zeit für alle Teilnehmer, einschließlich Raum-und Ressourcenpostfächern funktionieren soll. (Sie können dazu auch die verwaltete EWS-API-Methode [Datei "ExchangeService. GetUserAvailability](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getuseravailability%28v=exchg.80%29.aspx) verwenden.) 
    
5. Der Organisator kann dann seine Besprechung mit den neuen vorgeschlagenen Besprechungszeiten aktualisieren und die Updates an alle Teilnehmer mit dem [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) -EWS-Vorgang (oder der [Termin. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode) senden. 
    
In der folgenden Abbildung ist der Prozess dargestellt, der zwischen dem Besprechungsorganisator, dem Teilnehmer und dem Exchange-Server stattfindet, der die EWS-Anrufe verarbeitet hat.
  
**Abbildung 1. Prozess für das vorschlagen einer neuen Besprechungszeit**

![In der Abbildung wird der Workflow zwischen dem Organisator, Exchange und einem Teilnehmer dargestellt, wenn eine neue Besprechungszeit vorgeschlagen wird. Wenn der Organisator neue Vorschläge für Besprechungen zulässt, kann ein Teilnehmer eine neue Besprechungszeit mit einem Antwortobjekt vorschlagen.](media/Ex_ProposeNewMeetingTime.png)
  
## <a name="version-differences"></a>Versionsunterschiede
<a name="bk_Behavior"> </a>

Das Feature "neue Zeit vorschlagen" wurde in Exchange Build Version 15.00.0800.007 eingeführt. In früheren Versionen von Exchange müssen Benutzer von EWS-Anwendungen eine separate e-Mail an den Besprechungsorganisator senden, um eine andere Besprechungszeit anzufordern. 
  
## <a name="see-also"></a>Siehe auch


- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Löschen von Terminen und Absagen von Besprechungen mithilfe von EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

