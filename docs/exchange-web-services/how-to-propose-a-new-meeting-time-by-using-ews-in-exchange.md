---
title: Vorschlagen einer neuen Besprechungszeit mithilfe der EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d5ac8e5b-3876-4f20-b4d3-44505e066042
description: Erfahren Sie, wie in der Exchange-Clientanwendung Besprechungszeiten vorschlagen mithilfe der EWS in Exchange.
ms.openlocfilehash: f9edd8511332474a728635a6aa369a772da24786
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756981"
---
# <a name="propose-a-new-meeting-time-by-using-ews-in-exchange"></a>Vorschlagen einer neuen Besprechungszeit mithilfe der EWS in Exchange

Erfahren Sie, wie in der Exchange-Clientanwendung Besprechungszeiten vorschlagen mithilfe der EWS in Exchange.
  
Das neue Feature Zeit für vorschlagen ermöglicht es den Teilnehmern Besprechungszeiten Organisator der Besprechung als Teil des Exchange-Kalender Workflows vorschlagen. Wenn ein Teilnehmer eine neue Besprechung vorschlägt, kann der Organisator verwenden der vorgeschlagene neue Besprechungszeit zum Aktualisieren der Besprechung und Aktualisierungen an alle Teilnehmer senden. Bevor Sie Teilnehmer Besprechungszeiten vorschlagen aktivieren können, müssen Sie bestimmen, ob der Organisator für Vorschläge für neue Zeit zulässt. In diesem Artikel wird beschrieben, wie um festzustellen, ob Sie ein neues vorschlagen können Zeit- und wie Sie EWS verwenden, um eine neue Zeit vorschlagen.
  
> [!NOTE]
> [!HINWEIS] Die verwaltete EWS-API implementiert diese Funktion nicht. 
  
## <a name="determine-whether-you-can-propose-a-new-time-for-a-meeting-by-using-ews"></a>Bestimmen Sie, ob Sie eine neue Zeit für eine Besprechung vorschlagen können mithilfe der Exchange-Webdienste
<a name="bk_Determine"> </a>

Bevor Sie eine neue Zeit für eine Besprechung vorschlagen können, müssen Sie hier finden einen Verweis auf diese Besprechung und festzustellen, ob der Organisator der Besprechung die Besprechung zur Unterstützung von neue Zeit Vorschläge konfiguriert. Sie können einen Verweis auf eine Besprechung erhalten, indem Sie eines der folgenden: 
  
- Suchen nach der Besprechungsanfrage im Posteingang
    
- Suchen den Termin im Kalender
    
Gehen Sie folgendermaßen vor, um einen Verweis Besprechung zu erhalten:
  
1. Verwenden Sie [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS-Vorgangs (oder die [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=EXCHG.80%29.aspx) EWS Managed API-Methode) zum Suchen nach der-Ziel meeting Anforderung oder Kalenderelement. Alternativ können Sie [SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) EWS-Vorgangs verwenden, um den Bezeichner des Ziels meeting Anforderung oder Kalenderelement abzurufen. 
    
2. Analysieren Sie die Ergebnisse der **FindItem** -Vorgang (oder **Folder.FindItems** -Methode) zum Abrufen der Elementbezeichner des Besprechungselements. 
    
3. Verwenden Sie den [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) -EWS-Vorgang, um die Antwortobjekte für die Besprechung abzurufen. 
    
Das folgende XML zeigt, was gesendet wird, um die Antwortobjekte für ein Element anzufordern.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

**GetItem** Operation Antwort sieht ungefähr wie die folgende XML-Code, wenn Sie die Element-ID, die Besprechung starten und Endzeit, die Antwort objektauflistung anfordern und der Organisator vorgeschlagenen Änderungen an die Besprechungszeit ermöglicht. Die Antwort-Auflistung-Objekt, das durch das [ResponseObjects](http://msdn.microsoft.com/library/ad29e064-3f3d-4b7b-aa4c-9ec27326381d%28Office.15%29.aspx) -Element dargestellt wird, enthält den Satz von Antworten, die für das Kalenderelement gültig sind. Das **ProposeNewTime** -Element ist ein Antwortobjekt, der angibt, dass der Benutzer eine neue Zeit für die Besprechung vorschlagen kann. Die [AcceptItem](http://msdn.microsoft.com/library/05a15431-77e1-411a-a16b-5481d364d3cc%28Office.15%29.aspx) [TentativelyAcceptItem](http://msdn.microsoft.com/library/ce6f50ef-ad8a-47e4-915a-487b2ef7a2e0%28Office.15%29.aspx)und [DeclineItem](http://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) -Elemente darstellen, die Antwortobjekte, die Sie verwenden können, der Besprechungsorganisator eine neue Besprechungszeit vorschlagen. 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="propose-a-new-meeting-time-by-using-ews"></a>Vorschlagen einer neuen Besprechungszeit mithilfe der Exchange-Webdienste
<a name="bk_Propose"> </a>

Wenn Sie ein Antwortobjekt **ProposeNewTime** erhalten, wenn Sie die **GetItem** Operation verwendet, um ein Kalenderelement oder einer Besprechungsanfrage erhalten möchten, können Sie mit einer vorgeschlagenen neuen Besprechungszeit reagieren. Wenn Sie eine **ProposeNewTime** Response-Objekt nicht erhalten haben, werden Sie kann nicht als Teil des Workflows Kalender eine neue Besprechungszeit vorschlagen. Sie können jedoch auf der Organisator eine neuen Besprechungszeit anfordern antworten. Ein Antwortobjekt **ProposeNewTime** gemeldet werden, können Sie durch einen Verweis auf den Bezeichner für die Besprechung reagieren und vorschlagen eine neuen Besprechungszeit an den Organisator. Dies ist, in dem das Antwortobjekt **ProposeNewTime** dem normalen Reaktionszeit Objekt Muster unterscheidet, dass Sie nicht mit einem **ProposeNewTime** Antwortobjekt Antworten. Verwenden Sie eine der anderen meeting Antwortobjekte wie **AcceptItem**, **TentativelyAcceptItem**oder **DeclineItem**, eine neue Besprechung vorschlagen. In diesem Beispiel wird das **AcceptItem** Response-Objekt. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

Die Antwort auf diese Anforderung enthält die ID des Kalenderelements an, das Kalender des Teilnehmers hinzugefügt wurde, und eine Kopie der Besprechungsanfrage, die im Ordner für die Teilnehmer Gelöschte Objekte getätigt wurde. Die Response-Nachricht mit dem neuen Uhrzeit Vorschlag wurde auch im Ordner für die Teilnehmer gesendete Objekte gespeichert (müssen Sie die Besprechung suchen Antwortnachricht zu handhaben darauf).
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

Der Organisator erhalten eine [MeetingResponse](http://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx) -Nachricht, wenn der Teilnehmer mit einer vorgeschlagenen neuen Besprechungszeit antwortet. Die **MeetingResponse** -Nachricht enthält die vorgeschlagene neue Besprechung Startzeit und Endzeit und die ID des zugeordneten Kalenderelements im Kalender des Organisierer vorhanden. Der Organisator kann diese Informationen verwenden, um ihre vorhandene Kalenderelement für die Besprechung zu aktualisieren. Es folgt der Workflow für den Organisator Antworten auf eine **MeetingResponse** -Nachrichten, die eine neue Besprechungszeit vorgeschlagen: 
  
1. Bestimmen Sie, ob die **ProposedStart** oder **ProposedEnd** -Elemente in der **MeetingResponse**festgelegt wurden. Wenn dies der Fall ist, fahren Sie mit Schritt 2. Wenn dies nicht der Fall ist, wird die Nachricht **MeetingResponse** nur gibt an, ob der Teilnehmer hat akzeptiert, mit Vorbehalt angenommen oder die Besprechung wurde abgesagt. 
    
2. Rufen Sie vorhandene Kalenderelement der Organisator für die Besprechung, mithilfe des EWS-Bezeichners im **AssociatedCalendarItemId** Element zurückgegeben. 
    
3. Vergleichen Sie die ursprünglichen Start- und Endzeit mit vorgeschlagenen neuen Besprechungszeit. Wenn die vorgeschlagene neue Besprechungszeit an den Organisator akzeptabel ist, fahren Sie mit Schritt 4. Der Organisator der Besprechung Anderenfalls kann entweder ignorieren die Uhrzeit der vorgeschlagenen Besprechung oder senden eine e-Mail-Antwort an die Teilnehmer, die die neue Besprechungszeit vorgeschlagen.
    
4. (Optional) Führen Sie einen Anruf [GetUserAvailability](http://msdn.microsoft.com/library/8da17226-5d3a-4525-9ffa-d83730f47bb1%28Office.15%29.aspx) EWS-Vorgang, um herauszufinden, ob die vorgeschlagene Zeit für alle Teilnehmer, einschließlich der Postfächer Raum- und Ressource funktioniert. (Sie können die [ExchangeService.GetUserAvailability](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getuseravailability%28v=exchg.80%29.aspx) EWS Managed API-Methode auch verwenden, dazu.) 
    
5. Der Organisator kann dann aktualisieren Sie ihre Besprechung mit der vorgeschlagenen Besprechungszeiten und senden die Updates an alle Teilnehmer mithilfe der [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) EWS-Vorgang (oder die [Appointment.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) EWS Managed API-Methode). 
    
Die folgende Abbildung zeigt den Prozess, der zwischen der Organisator der Besprechung, die Teilnehmer und der Exchange-Server, der die EWS-Aufrufe behandelt.
  
**Abbildung 1. Prozess zum Vorschlagen einer neuen Besprechungszeit**

![In der Abbildung wird der Workflow zwischen dem Organisator, Exchange und einem Teilnehmer dargestellt, wenn eine neue Besprechungszeit vorgeschlagen wird. Wenn der Organisator neue Vorschläge für Besprechungen zulässt, kann ein Teilnehmer eine neue Besprechungszeit mit einem Antwortobjekt vorschlagen.](media/Ex_ProposeNewMeetingTime.png)
  
## <a name="version-differences"></a>Versionsunterschiede
<a name="bk_Behavior"> </a>

Das neue Feature Zeit für vorschlagen wurde in Exchange Buildversion 15.00.0800.007 eingeführt. In früheren Versionen von Exchange müssen Benutzer EWS-Anwendung senden eine separate e-Mail an den Organisator der Besprechung eine andere Besprechungszeit anfordern. 
  
## <a name="see-also"></a>Siehe auch


- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Löschen von Terminen und Abbrechen an Besprechungen mithilfe von EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

