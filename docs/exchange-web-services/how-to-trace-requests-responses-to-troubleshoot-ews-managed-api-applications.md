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
# <a name="trace-requests-and-responses-to-troubleshoot-ews-managed-api-apps"></a><span data-ttu-id="9712d-103">Ablaufverfolgungsanforderungen und-Antworten zur Problembehandlung bei verwaltete EWS-API apps</span><span class="sxs-lookup"><span data-stu-id="9712d-103">Trace requests and responses to troubleshoot EWS Managed API apps</span></span>

<span data-ttu-id="9712d-104">Erfahren Sie, wie Sie EWS-Anforderungen und-Antworten zur Problembehandlung bei Fehlern in ihrer verwaltete EWS-API Anwendung verfolgen.</span><span class="sxs-lookup"><span data-stu-id="9712d-104">Find out how to trace EWS requests and responses to troubleshoot errors in your EWS Managed API application.</span></span>
  
<span data-ttu-id="9712d-105">Das Debugging einer auf dem Webdienst basierenden Anwendung kann schwierig sein, da ein Teil der Verarbeitung auf einem Remotecomputer ausgeführt wird, auf den Sie möglicherweise keinen Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="9712d-105">Debugging a web service-based application can be difficult because part of the processing is performed on a remote computer that you might not have access to.</span></span> <span data-ttu-id="9712d-106">Da Sie den Code auf dem Server nicht durchlaufen können, kann es hilfreich sein, die XML-Anforderungen und-Antworten anzuzeigen, die zwischen dem Client und dem Server gesendet werden, um zu bestimmen, welcher Teil der Anwendung einen Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="9712d-106">Because you cannot step through the code on the server, it can be helpful to see the XML requests and responses that are sent between the client and the server to determine which part of the application is causing an error.</span></span> 
  
<span data-ttu-id="9712d-107">Wenn Sie EWS verwenden, haben Sie bereits Zugriff auf die XML-Anforderung und-Antwort; Sie können einen Unterbrechungspunkt in Ihrem Code platzieren, um die Antwort des Servers auf Ihre Anforderung zu überprüfen, um ein Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="9712d-107">If you are using EWS, you already have access to the XML request and response; you can put a break point in your code to review the server's response to your request in order to troubleshoot an issue.</span></span> <span data-ttu-id="9712d-108">Wenn Sie die verwaltete EWS-API verwenden, haben Sie keinen direkten Zugriff auf die EWS-Anforderung und-Antwort.</span><span class="sxs-lookup"><span data-stu-id="9712d-108">If you're using the EWS Managed API, you don't have direct access to the EWS request and response.</span></span> <span data-ttu-id="9712d-109">Sie können jedoch Ablaufverfolgungsmethoden für das [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt verwenden, um die XML-Anforderung und-Antwort zu erfassen, und Sie können dann mithilfe der XML-Datei ermitteln, warum der Code nicht funktioniert.</span><span class="sxs-lookup"><span data-stu-id="9712d-109">However, you can use tracing methods on the [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object to capture the XML request and response, and you can then use the XML to determine why your code is not working.</span></span> 

<span data-ttu-id="9712d-110">Wenn Sie beispielsweise eine Eigenschaft nicht ordnungsgemäß festgelegt haben, erhalten Sie möglicherweise eine unerwartete Antwort, und Sie können die Ablaufverfolgungsausgabe verwenden, um sich die XML-Anforderung und die Antwort zur Identifizierung des Fehlers anzusehen.</span><span class="sxs-lookup"><span data-stu-id="9712d-110">For example, if you did not set a property correctly, you might get an unexpected response, and you can use the trace output to look at the XML request and response to identify the error.</span></span> <span data-ttu-id="9712d-111">Die Ablaufverfolgungsausgabe des verwaltete EWS-API kann Sie auch beim manuellen Erstellen der XML-Anforderung zum Erstellen Ihrer EWS-Anwendung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9712d-111">The trace output from the EWS Managed API can also help you manually build the XML request to create your EWS application.</span></span> <span data-ttu-id="9712d-112">Wenn Sie EWS verwenden, können Sie eine kleine Anwendung erstellen, indem Sie verwaltete EWS-API verwenden, nachverfolgen und dann die XML-Anforderungsinformationen verwenden, um Sie bei der Erstellung Ihrer EWS-Anforderung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9712d-112">If you are using EWS, you can create a small application by using EWS Managed API, trace it, and then use the XML request information to help you build your EWS request.</span></span> 
  
## <a name="enabling-tracing-on-the-exchangeservice-object"></a><span data-ttu-id="9712d-113">Aktivieren der Ablaufverfolgung für das Datei "ExchangeService-Objekt</span><span class="sxs-lookup"><span data-stu-id="9712d-113">Enabling tracing on the ExchangeService object</span></span>
<span data-ttu-id="9712d-114"><a name="bk_EnableTracing"> </a></span><span class="sxs-lookup"><span data-stu-id="9712d-114"><a name="bk_EnableTracing"> </a></span></span>

<span data-ttu-id="9712d-115">Erstellen Sie zum Aktivieren der Ablaufverfolgung ein [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für Ihre Anwendung, und legen Sie die Eigenschaften der Ablaufverfolgung wie im folgenden Beispiel gezeigt fest.</span><span class="sxs-lookup"><span data-stu-id="9712d-115">To enable tracing, create an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for your application, and set the tracing properties as shown in the following example.</span></span> 
  
```cs
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2010);
service.TraceListener = ITraceListenerInstance;
// Optional flags to indicate the requests and responses to trace.
service.TraceFlags = TraceFlags.EwsRequest | TraceFlags.EwsResponse
service.TraceEnabled = true;

```

<span data-ttu-id="9712d-116">Nachdem Sie die [TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) -Eigenschaft auf **true**festgelegt haben, werden alle Anforderungen, die mit den Ablaufverfolgungsflags übereinstimmen, an den angegebenen Ablauf Verfolgungs Listener gesendet.</span><span class="sxs-lookup"><span data-stu-id="9712d-116">After you set the [TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) property to **true**, all requests that match the trace flags will be sent to the specified trace listener.</span></span> <span data-ttu-id="9712d-117">Sie können ein einzelnes Ablaufverfolgungsflag angeben, oder Sie können mehrere Ablaufverfolgungskennzeichen angeben, indem Sie Sie mit einem logischen **or**kombinieren.</span><span class="sxs-lookup"><span data-stu-id="9712d-117">You can specify a single trace flag, or you can specify multiple trace flags by combining them with a logical **OR**.</span></span> <span data-ttu-id="9712d-118">Sie können die [TraceFlags-Aufzählung](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx) verwenden, um Werte für EWS und für Auto Ermittlungsanforderungen und-Antworten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9712d-118">You can use the [TraceFlags enumeration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx) to specify values for EWS and for Autodiscover requests and responses.</span></span> 
  
## <a name="implementing-a-tracelistener-object"></a><span data-ttu-id="9712d-119">Implementieren eines TraceListener-Objekts</span><span class="sxs-lookup"><span data-stu-id="9712d-119">Implementing a TraceListener object</span></span>
<span data-ttu-id="9712d-120"><a name="bk_traceListener"> </a></span><span class="sxs-lookup"><span data-stu-id="9712d-120"><a name="bk_traceListener"> </a></span></span>

<span data-ttu-id="9712d-121">Sie können die [TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) -Eigenschaft auf **true** festlegen, um die XML-Anforderungen und-Antworten an Ihre Anwendung (beispielsweise ein Konsolenfenster) auszugeben.</span><span class="sxs-lookup"><span data-stu-id="9712d-121">You can set the [TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) property to **true** to output the XML requests and responses to your application, such as a console window.</span></span> <span data-ttu-id="9712d-122">Wenn Sie die Ablaufverfolgungsausgabe Steuern und in einer Datei speichern möchten, wird empfohlen, ein [TraceListener-Klassen](https://msdn.microsoft.com/library/system.diagnostics.tracelistener.aspx) Objekt zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="9712d-122">If you want to control the trace output and save it to a file, we recommend that you implement a [TraceListener class](https://msdn.microsoft.com/library/system.diagnostics.tracelistener.aspx) object.</span></span> <span data-ttu-id="9712d-123">Das folgende Codebeispiel zeigt ein einfaches Objekt, das die [ITraceListener](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx) -Schnittstelle implementiert und die nachverfolgten Anforderungen und Antworten in XML-oder Textdateien speichert.</span><span class="sxs-lookup"><span data-stu-id="9712d-123">The following code example shows a simple object that implements the [ITraceListener](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx) interface and stores the traced requests and responses in XML or text files.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="9712d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9712d-124">See also</span></span>

- [<span data-ttu-id="9712d-125">Verwenden von Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="9712d-125">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
- [<span data-ttu-id="9712d-126">Behandeln von AutoErmittlungs-Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="9712d-126">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)    
- [<span data-ttu-id="9712d-127">Verweisen auf die EWS-verwaltete API-Assembly</span><span class="sxs-lookup"><span data-stu-id="9712d-127">Reference the EWS Managed API assembly</span></span>](how-to-reference-the-ews-managed-api-assembly.md)    
- [<span data-ttu-id="9712d-128">Kommunizieren mit EWS unter Verwendung der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="9712d-128">Communicate with EWS by using the EWS Managed API</span></span>](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

