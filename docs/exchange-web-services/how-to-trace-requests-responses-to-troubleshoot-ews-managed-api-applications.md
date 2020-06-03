---
title: Ablaufverfolgungsanforderungen und-Antworten zur Problembehandlung bei verwaltete EWS-API apps
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 186c1d1d-b8dc-4914-b3cd-6fada7ecd877
description: Erfahren Sie, wie Sie EWS-Anforderungen und-Antworten zur Problembehandlung bei Fehlern in ihrer verwaltete EWS-API Anwendung verfolgen.
localization_priority: Priority
ms.openlocfilehash: dd225030d62a2e8211b7063ee78a59fd1a070263
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455856"
---
# <a name="trace-requests-and-responses-to-troubleshoot-ews-managed-api-apps"></a>Ablaufverfolgungsanforderungen und-Antworten zur Problembehandlung bei verwaltete EWS-API apps

Erfahren Sie, wie Sie EWS-Anforderungen und-Antworten zur Problembehandlung bei Fehlern in ihrer verwaltete EWS-API Anwendung verfolgen.
  
Das Debugging einer auf dem Webdienst basierenden Anwendung kann schwierig sein, da ein Teil der Verarbeitung auf einem Remotecomputer ausgeführt wird, auf den Sie möglicherweise keinen Zugriff haben. Da Sie den Code auf dem Server nicht durchlaufen können, kann es hilfreich sein, die XML-Anforderungen und-Antworten anzuzeigen, die zwischen dem Client und dem Server gesendet werden, um zu bestimmen, welcher Teil der Anwendung einen Fehler verursacht. 
  
Wenn Sie EWS verwenden, haben Sie bereits Zugriff auf die XML-Anforderung und-Antwort; Sie können einen Unterbrechungspunkt in Ihrem Code platzieren, um die Antwort des Servers auf Ihre Anforderung zu überprüfen, um ein Problem zu beheben. Wenn Sie die verwaltete EWS-API verwenden, haben Sie keinen direkten Zugriff auf die EWS-Anforderung und-Antwort. Sie können jedoch Ablaufverfolgungsmethoden für das [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt verwenden, um die XML-Anforderung und-Antwort zu erfassen, und Sie können dann mithilfe der XML-Datei ermitteln, warum der Code nicht funktioniert. 

Wenn Sie beispielsweise eine Eigenschaft nicht ordnungsgemäß festgelegt haben, erhalten Sie möglicherweise eine unerwartete Antwort, und Sie können die Ablaufverfolgungsausgabe verwenden, um sich die XML-Anforderung und die Antwort zur Identifizierung des Fehlers anzusehen. Die Ablaufverfolgungsausgabe des verwaltete EWS-API kann Sie auch beim manuellen Erstellen der XML-Anforderung zum Erstellen Ihrer EWS-Anwendung unterstützen. Wenn Sie EWS verwenden, können Sie eine kleine Anwendung erstellen, indem Sie verwaltete EWS-API verwenden, nachverfolgen und dann die XML-Anforderungsinformationen verwenden, um Sie bei der Erstellung Ihrer EWS-Anforderung zu unterstützen. 
  
## <a name="enabling-tracing-on-the-exchangeservice-object"></a>Aktivieren der Ablaufverfolgung für das Datei "ExchangeService-Objekt
<a name="bk_EnableTracing"> </a>

Erstellen Sie zum Aktivieren der Ablaufverfolgung ein [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für Ihre Anwendung, und legen Sie die Eigenschaften der Ablaufverfolgung wie im folgenden Beispiel gezeigt fest. 
  
```cs
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2010);
service.TraceListener = ITraceListenerInstance;
// Optional flags to indicate the requests and responses to trace.
service.TraceFlags = TraceFlags.EwsRequest | TraceFlags.EwsResponse
service.TraceEnabled = true;

```

Nachdem Sie die [TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) -Eigenschaft auf **true**festgelegt haben, werden alle Anforderungen, die mit den Ablaufverfolgungsflags übereinstimmen, an den angegebenen Ablauf Verfolgungs Listener gesendet. Sie können ein einzelnes Ablaufverfolgungsflag angeben, oder Sie können mehrere Ablaufverfolgungskennzeichen angeben, indem Sie Sie mit einem logischen **or**kombinieren. Sie können die [TraceFlags-Aufzählung](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx) verwenden, um Werte für EWS und für Auto Ermittlungsanforderungen und-Antworten anzugeben. 
  
## <a name="implementing-a-tracelistener-object"></a>Implementieren eines TraceListener-Objekts
<a name="bk_traceListener"> </a>

Sie können die [TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) -Eigenschaft auf **true** festlegen, um die XML-Anforderungen und-Antworten an Ihre Anwendung (beispielsweise ein Konsolenfenster) auszugeben. Wenn Sie die Ablaufverfolgungsausgabe Steuern und in einer Datei speichern möchten, wird empfohlen, ein [TraceListener-Klassen](https://msdn.microsoft.com/library/system.diagnostics.tracelistener.aspx) Objekt zu implementieren. Das folgende Codebeispiel zeigt ein einfaches Objekt, das die [ITraceListener](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx) -Schnittstelle implementiert und die nachverfolgten Anforderungen und Antworten in XML-oder Textdateien speichert. 
  
```cs
class TraceListener : ITraceListener
{
    #region ITraceListener Members
    public void Trace(string traceType, string traceMessage)
    {
      CreateXMLTextFile(traceType, traceMessage.ToString());
    }
    #endregion
    private void CreateXMLTextFile(string fileName, string traceContent)
    {
      // Create a new XML file for the trace information.
      try
      {
        // If the trace data is valid XML, create an XmlDocument object and save.
        XmlDocument xmlDoc = new XmlDocument();
        xmlDoc.Load(traceContent);
        xmlDoc.Save(fileName + ".xml");
      }
      catch
      {
        // If the trace data is not valid XML, save it as a text document.
        System.IO.File.WriteAllText(fileName + ".txt", traceContent);
      }
    }
}

```

## <a name="see-also"></a>Siehe auch

- [Verwenden von Webdiensten in Exchange](start-using-web-services-in-exchange.md)
- [Behandeln von AutoErmittlungs-Fehlermeldungen](handling-autodiscover-error-messages.md)    
- [Verweisen auf die EWS-verwaltete API-Assembly](how-to-reference-the-ews-managed-api-assembly.md)    
- [Kommunizieren mit EWS unter Verwendung der verwalteten EWS-API](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

