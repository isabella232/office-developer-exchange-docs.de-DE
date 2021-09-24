---
title: Vorschlagen einer neuen Besprechungszeit mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: d5ac8e5b-3876-4f20-b4d3-44505e066042
description: Erfahren Sie, wie Sie neue Besprechungszeiten aus Ihrer Exchange-Clientanwendung mithilfe von EWS in Exchange vorschlagen.
ms.openlocfilehash: a6406aaef2005e74165e647510af891d2a59503e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522229"
---
# <a name="propose-a-new-meeting-time-by-using-ews-in-exchange"></a>Vorschlagen einer neuen Besprechungszeit mithilfe von EWS in Exchange

Erfahren Sie, wie Sie neue Besprechungszeiten aus Ihrer Exchange-Clientanwendung mithilfe von EWS in Exchange vorschlagen.
  
Die Funktion "Neue Uhrzeit vorschlagen" ermöglicht es Teilnehmern, dem Besprechungsorganisator im Rahmen des Exchange Kalenderworkflows neue Besprechungszeiten vorzuschlagen. Wenn ein Teilnehmer eine neue Besprechung vorschlägt, kann der Organisator die vorgeschlagene neue Besprechungszeit verwenden, um die Besprechung zu aktualisieren und Updates an alle Teilnehmer zu senden. Bevor Sie teilnehmern ermöglichen können, neue Besprechungszeiten vorzuschlagen, müssen Sie bestimmen, ob der Organisator neue Zeitvorschläge zulässt. In diesem Artikel wird beschrieben, wie Sie bestimmen können, ob Sie eine neue Zeit vorschlagen können, und wie Sie mithilfe von EWS eine neue Zeit vorschlagen können.
  
> [!NOTE]
> Die verwaltete EWS-API implementiert diese Funktion nicht. 
  
## <a name="determine-whether-you-can-propose-a-new-time-for-a-meeting-by-using-ews"></a>Bestimmen, ob Sie einen neuen Zeitpunkt für eine Besprechung mithilfe von EWS vorschlagen können
<a name="bk_Determine"> </a>

Bevor Sie eine neue Uhrzeit für eine Besprechung vorschlagen können, müssen Sie einen Verweis auf diese Besprechung finden und ermitteln, ob der Besprechungsorganisator die Besprechung so konfiguriert hat, dass neue Zeitvorschläge unterstützt werden. Sie können einen Verweis auf eine Besprechung erhalten, indem Sie eine der folgenden Aktionen ausführen: 
  
- Suchen der Besprechungsanfrage im Posteingang
    
- Suchen des Termins im Kalender
    
Führen Sie die folgenden Schritte aus, um eine Besprechungsreferenz zu finden:
  
1. Verwenden Sie den [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS-Vorgang (oder die verwaltete EWS-API-Methode [Folder.FindItems),](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=EXCHG.80%29.aspx) um die Zielbesprechungsanfrage oder das Kalenderelement zu suchen. Alternativ können Sie den [SyncFolderItems-EWS-Vorgang](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) verwenden, um den Bezeichner der Zielbesprechungsanfrage oder des Kalenderelements abzurufen. 
    
2. Analysieren Sie die Ergebnisse des **FindItem-Vorgangs** (oder der **Folder.FindItems-Methode),** um den Elementbezeichner des Besprechungselements abzurufen. 
    
3. Verwenden Sie den [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) EWS-Vorgang, um die Antwortobjekte für die Besprechung abzurufen. 
    
Der folgende XML-Code zeigt, was gesendet wird, um die Antwortobjekte für ein Element anzufordern.
  
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

Die **GetItem-Vorgangsantwort** sieht ähnlich wie die folgende XML aus, wenn Sie den Elementbezeichner, die Start- und Endzeit der Besprechung, die Antwortobjektsammlung und wenn der Organisator vorgeschlagene Änderungen an der Besprechungszeit zulässt. Die Antwortobjektsammlung, die durch das [ResponseObjects-Element](https://msdn.microsoft.com/library/ad29e064-3f3d-4b7b-aa4c-9ec27326381d%28Office.15%29.aspx) dargestellt wird, enthält den Satz von Antworten, die für das Kalenderelement gültig sind. Das **"ProposeNewTime"-Element** ist ein Antwortobjekt, das angibt, dass der Benutzer eine neue Uhrzeit für die Besprechung vorschlagen kann. Die Elemente [AcceptItem,](https://msdn.microsoft.com/library/05a15431-77e1-411a-a16b-5481d364d3cc%28Office.15%29.aspx) [TentativelyAcceptItem](https://msdn.microsoft.com/library/ce6f50ef-ad8a-47e4-915a-487b2ef7a2e0%28Office.15%29.aspx)und [DeclineItem](https://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) stellen die Antwortobjekte dar, mit denen Sie dem Besprechungsorganisator eine neue Besprechungszeit vorschlagen können. 
  
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

Wenn Sie ein **ProposedNewTime-Antwortobjekt** erhalten haben, als Sie den **GetItem-Vorgang** zum Abrufen eines Kalenderelements oder einer Besprechungsanfrage verwendet haben, können Sie mit einer vorgeschlagenen neuen Besprechungszeit antworten. Wenn Sie kein **"ProposeNewTime"-Antwortobjekt** erhalten haben, können Sie im Rahmen des Kalenderworkflows keine neue Besprechungszeit vorschlagen. Sie können dem Organisator jedoch antworten, um eine neue Besprechungszeit anzufordern. Wenn Sie ein **"ProposeNewTime"-Antwortobjekt** erhalten, können Sie auf die Besprechung antworten, indem Sie auf den Bezeichner verweisen und dem Organisator eine neue Besprechungszeit vorschlagen. Hier unterscheidet sich das **"ProposeNewTime"-Antwortobjekt** vom typischen Antwortobjektmuster, da Sie nicht mit einem **"ProposeNewTime"-Antwortobjekt** antworten. Sie verwenden eines der anderen Besprechungsantwortobjekte, z. **B. AcceptItem,** **TentativelyAcceptItem** oder **DeclineItem,** um eine neue Besprechung vorzuschlagen. In diesem Beispiel wird das **AcceptItem-Antwortobjekt** verwendet. 
  
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

Die Antwort auf diese Anforderung enthält den Bezeichner des Kalenderelements, das dem Kalender des Teilnehmers hinzugefügt wurde, und eine Kopie der Besprechungsanfrage, die im Ordner "Gelöschte Elemente" des Teilnehmers abgelegt wurde. Die Antwortnachricht mit dem neuen Zeitvorschlag wurde auch im Ordner "Gesendete Elemente" des Teilnehmers gespeichert (Sie müssen die Besprechungsantwortnachricht finden, um ein Handle dafür zu erhalten).
  
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

Der Organisator erhält eine [MeetingResponse-Nachricht,](https://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx) wenn der Teilnehmer mit einer vorgeschlagenen neuen Besprechungszeit antwortet. Die **MeetingResponse-Nachricht** enthält die vorgeschlagene neue Start- und Endzeit der Besprechung sowie den Bezeichner des zugeordneten Kalenderelements im Kalender des Organisators. Der Organisator kann diese Informationen verwenden, um sein vorhandenes Kalenderelement für die Besprechung zu aktualisieren. Es folgt der Workflow für den Organisator, um auf eine **MeetingResponse-Nachricht** zu antworten, die eine neue Besprechungszeit vorschlägt: 
  
1. Bestimmen Sie, ob die **ProposedStart-** oder **ProposedEnd-Elemente** in **MeetingResponse** festgelegt wurden. Wenn ja, fahren Sie mit Schritt 2 fort. Andernfalls gibt die **MeetingResponse-Nachricht** nur an, ob der Teilnehmer die Besprechung angenommen, mit Vorbehalt angenommen oder abgelehnt hat. 
    
2. Rufen Sie das vorhandene Kalenderelement des Organisators für die Besprechung mithilfe des EWS-Bezeichners ab, der im **AssociatedCalendarItemId-Element** zurückgegeben wird. 
    
3. Vergleichen Sie die ursprüngliche Start- und Endzeit mit der vorgeschlagenen neuen Besprechungszeit. Wenn die vorgeschlagene neue Besprechungszeit für den Organisator akzeptabel ist, fahren Sie mit Schritt 4 fort. Andernfalls kann der Besprechungsorganisator entweder die vorgeschlagene Besprechungszeit ignorieren oder eine E-Mail-Antwort an den Teilnehmer senden, der die neue Besprechungszeit vorgeschlagen hat.
    
4. (Optional) Führen Sie einen [GetUserAvailability](https://msdn.microsoft.com/library/8da17226-5d3a-4525-9ffa-d83730f47bb1%28Office.15%29.aspx) EWS-Vorgangsaufruf aus, um herauszufinden, ob die vorgeschlagene Zeit für alle Teilnehmer funktioniert, einschließlich Raum- und Ressourcenpostfächern. (Dazu können Sie auch die verwaltete EWS-API-Methode [ExchangeService.GetUserAvailability](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getuseravailability%28v=exchg.80%29.aspx) verwenden.) 
    
5. Der Organisator kann dann seine Besprechung mit den neuen vorgeschlagenen Besprechungszeiten aktualisieren und die Updates mithilfe des [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) EWS-Vorgangs (oder der verwalteten EWS-API-Methode von [Appointment.Update)](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) an alle Teilnehmer senden. 
    
Die folgende Abbildung zeigt den Prozess, der zwischen dem Besprechungsorganisator, dem Teilnehmer und dem Exchange Server stattfindet, der die EWS-Anrufe verarbeitet hat.
  
**Abbildung 1. Prozess zum Vorschlagen einer neuen Besprechungszeit**

![In der Abbildung wird der Workflow zwischen dem Organisator, Exchange und einem Teilnehmer dargestellt, wenn eine neue Besprechungszeit vorgeschlagen wird. Wenn der Organisator neue Vorschläge für Besprechungen zulässt, kann ein Teilnehmer eine neue Besprechungszeit mit einem Antwortobjekt vorschlagen.](media/Ex_ProposeNewMeetingTime.png)
  
## <a name="version-differences"></a>Versionsunterschiede
<a name="bk_Behavior"> </a>

Das Feature "Neue Uhrzeit vorschlagen" wurde in Exchange Buildversion 15.00.0800.007 eingeführt. In früheren Versionen von Exchange müssen EWS-Anwendungsbenutzer eine separate E-Mail an den Besprechungsorganisator senden, um eine andere Besprechungszeit anzufordern. 
  
## <a name="see-also"></a>Siehe auch


- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Löschen von Terminen und Absagen von Besprechungen mithilfe von EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

