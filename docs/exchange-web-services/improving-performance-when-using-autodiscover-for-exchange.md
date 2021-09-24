---
title: Verbessern der Leistung bei Verwendung der AutoErmittlung für Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: e65ff6b2-3810-43ad-9728-27308891b193
description: Informationen Sie über Möglichkeiten zur Verbesserung der Leistung von AutoErmittlung-Prozesses in der Anwendung.
ms.openlocfilehash: c0920f71c230f63658dfa8d29b34ca75bb796db0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520997"
---
# <a name="improving-performance-when-using-autodiscover-for-exchange"></a>Verbessern der Leistung bei Verwendung der AutoErmittlung für Exchange

Informationen Sie über Möglichkeiten zur Verbesserung der Leistung von AutoErmittlung-Prozesses in der Anwendung.
  
Es gibt viele Gründe für die AutoErmittlung wie folgt. Konfigurieren der Anwendung zum Verbinden mit Exchange ohne Benutzereingriff eignet! Wenn Sie in diesem Artikel lesen, wissen Sie wahrscheinlich bereits alle Gründe zum verwenden und Liebe AutoErmittlung, damit wir hier aufgelistet werden nicht. Stattdessen wird jetzt über einen Nachteil sprechen: Leistung.
  
AutoErmittlung ist grundsätzlich ein langsamer Vorgang nicht, aber es ist entweder nicht grundsätzlich schnell. Der [AutoErmittlung-Prozesses](autodiscover-for-exchange.md) umfasst zahlreiche Netzwerkaktivität, und das viele mögliche Verzögerungen führt. AutoErmittlung-Prozesses hat drei Phasen. alle drei haben Auswirkungen auf Leistung haben: 
  
- Definieren des kandidatenpools der AutoErmittlung-Endpunkt - für Anwendungen, die auf die Domäne eingebundener Computer ausgeführt, kann dies umfassen, [SCP-Lookups](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md), die bei der Kommunikation mit Active Directory-Domänendienste (AD DS) umfasst.
    
- Versuchen jede Candidate - dies erfordert eine HTTP-Anforderung und Antwort an jeden Endpunkt Candidate.
    
- Ausprobieren anderer alternativen - Wenn die Kandidaten in Ihrem AutoErmittlung Endpunkt Candidate Pool nicht Ergebnisse liefern, möglich, eine nicht authentifizierte GET-Anforderung (HTTP-Anforderung/Antwort) und eine DNS-Suche.
    
Auf der Oberfläche mag dies nicht wie viel. Was ist ein Szenario, in dem der AutoErmittlung Endpunkt Candidate Pool ist mehr als eine oder zwei URLs und nicht finden Sie eine funktionsfähige, jedoch eine, bis die letzte URL in Ihrem Pool. Die Verzögerung kann etwas deutlicher werden. Ja, was tun Sie?
  
## <a name="consider-the-need-for-scp-lookup"></a>Berücksichtigen Sie die Notwendigkeit für SCP-Suche

Wenn SCP-Objekte vorhanden und gut konfiguriert haben, können sie die AutoErmittlung beschleunigen. In anderen Fällen können jedoch sie verlangsamen. Wenn SCP nicht in Ihrer Umgebung verwendet wird, überspringen Sie den gesamten SCP-Lookup-Teil des AutoErmittlung-Prozesses Zeit sparen.
  
Die EWS Managed API ist das einfach: Legen Sie die [ExchangeService.EnableScpLookup](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.enablescplookup%28v=exchg.80%29.aspx) -Eigenschaft nur auf **false**, vor dem Aufrufen der [ExchangeService.AutodiscoverUrl](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.autodiscoverurl%28v=exchg.80%29.aspx) -Methode. Wenn Sie die [AutodiscoverService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice%28v=exchg.80%29.aspx) -Klasse verwenden, legen Sie die [AutodiscoverService.EnableScpLookup](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.enablescplookup%28v=exchg.80%29.aspx) -Eigenschaft auf **false** vor dem Aufruf einer der Methoden. 
  
## <a name="use-autodiscover-less-often"></a>AutoErmittlung weniger häufig verwenden

AutoErmittlung ist nicht für die Verwendung vorgesehen häufig von Anwendungen verwenden. Die Absicht hinter AutoErmittlung ist für eine Anwendung zu verwenden, um Konfigurationsinformationen zu ermitteln, und klicken Sie dann zwischenspeichern, die betreffenden Informationen für einen gewissen Zeitraum. Wenn Sie Konfigurationsinformationen-Zwischenspeicherung werden nicht sinnvoll, Zwischenspeicherung in Ihrer Anwendung, wie oft verringern Sie AutoErmittlung verwenden.
  
Auch wenn Sie bereits zwischenspeichern, ausgewertet werden soll, wie lange Sie Konfigurationsinformationen Zwischenspeichern. Standardmäßig wird zum [Aktualisieren von autoermittlungsinformationen alle 24 Stunden](how-to-refresh-configuration-information-by-using-autodiscover.md), aber möglicherweise zu diesem Zeitpunkt erweitern können. Mit Ihrer Zielumgebungen testen und für die Konfiguration, die für Sie arbeitet mit einer "Time-to-live" ergeben.
  
## <a name="minimize-requested-data"></a>Minimieren Sie die angeforderte Daten

Bei Verwendung die **AutodiscoverService** -Klasse in die EWS Managed API oder des Vorgangs [GetUserSettings-Vorgang (SOAP)](https://msdn.microsoft.com/library/758d965c-ef63-4de4-9120-e293abf14ff8%28Office.15%29.aspx) mittels SOAP müssen Sie direkte Kontrolle darüber, welche Einstellungen in der Antwort zurückgegeben werden. Obwohl Sie ein paar Einstellungen anfordern können, sind wahrscheinlich, dass die Anwendung nur wenige von ihnen benötigt. Jede Einstellung, die Sie anfordern erfordert eine weitere Verarbeitung auf dem Server, d. h. mehr Zeit für eine Antwort wartet. Bewerten Sie die Einstellungen, die Sie anfordern, und zu vermeiden Sie, die Sie nicht benötigen. 
  
Wenn Sie die **ExchangeService.AutodiscoverUrl** -Methode in die EWS Managed API verwenden, können nicht Sie die Einstellungen ändern können. Diese Methode ist jedoch bereits relativ effiziente. Es werden nur die Einstellungen der **ExternalEwsUrl** und **InternalEwsUrl** aus der [UserSettingName-Enumeration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.usersettingname%28v=exchg.80%29.aspx)angefordert.
  
Wenn Sie den POX AutoErmittlungsdienst, [Sie können keine bestimmte Eigenschaften anfordern](autodiscover-for-exchange.md#bk_Options)verwenden.
  
## <a name="see-also"></a>Siehe auch


- [AutoErmittlung für Exchange](autodiscover-for-exchange.md)
    
- [Suchen nach AutoErmittlungs-Endpunkten mit der SCP-Suche in Exchange](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [Aktualisieren von Konfigurationsinformationen mithilfe der AutoErmittlung](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [ExchangeService-Klasse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)
    
- [AutodiscoverService-Klasse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice%28v=exchg.80%29.aspx)
    

