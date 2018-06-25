---
title: Erstellen eines SmtpReceiveAgent Transport-Agents für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cdc7c462-74a7-49d6-95b2-155d783840e9
description: Erfahren Sie, wie Sie einen benutzerdefinierten SmtpReceiveAgent Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
ms.openlocfilehash: a74d5baae6334c5e17acb6335206964b48f320e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757299"
---
# <a name="create-an-smtpreceiveagent-transport-agent-for-exchange-2013"></a>Erstellen eines SmtpReceiveAgent Transport-Agents für Exchange 2013

Erfahren Sie, wie Sie einen benutzerdefinierten SmtpReceiveAgent Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
  
**Gilt für:** Exchange Server 2013
  
Verwandte Codeabschnitte und Beispiel-apps:

- [Exchange 2013: Erstellen eines Stelle Konvertierung Transport-Agents](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)
  
Die Klassen [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) und [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) können Sie das Verhalten der Front-End-Transportdienst auf einem Client Access Server oder den Transportdienst auf einem Postfachserver zu erweitern. Diese Klassen können Sie um Transport-Agents zu implementieren, mit denen auf Nachrichten antworten, wie sie in Ihrer Organisation stammen. 
  
Die Klassen [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) und [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) enthalten, die in der folgenden Tabelle aufgeführten Ereignisse. 
  
**In Tabelle 1. SmtpReceiveAgent-Klassenereignisse**

|Document.SelectionChanged **-Ereignis**|**Beschreibung**|
|:-----|:-----|
|[OnAuthCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnAuthCommand.aspx) <br/> |Wird verwendet, wenn der Agent Informationen, die nur in den Befehl SMTP- **AUTH** bereitgestellt wird, erfordert wie ein Agent, der annimmt oder ablehnt versucht, eine Nachricht basierend auf den Typ der Authentifizierungsmethode übermitteln.  <br/> |
|[OnConnect](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnConnect.aspx) <br/> |Wird verwendet, wenn der Agent Informationen erforderlich, die bereitgestellt wird sind, nur, wenn eine Verbindung über SMTP auf den Front-End-Transport-Dienst, wie ein Agent geöffnet wird, das eine Aktion basierend auf dem Adresse oder die Domäne des SMTP-Remoteserver verwendet wird.  <br/> |
|[OnDataCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDataCommand.aspx) <br/> |Verwenden Sie dieses Ereignis, wenn der Agent Informationen erforderlich sind, die im SMTP- **DATA** -Befehl bereitgestellt wird.  <br/> |
|[OnDisconnect](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDisconnect.aspx) <br/> |Wird verwendet, wenn der Agent Informationen erforderlich, verfügbar zum Zeitpunkt der Trennung, wie etwa das aktuelle Datum und Uhrzeit sind, um Berechnungen Zeit ausführen zu können.  <br/> |
|[OnEhloCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEhloCommand.aspx) <br/> |Wird verwendet, wenn der Agent Informationen erforderlich sind, die in den SMTP- **EHLO** -Befehl bereitgestellt wird; Wenn beispielsweise der Agent akzeptiert oder lehnt Nachrichten auf Grundlage der Identität in den **EHLO** -Befehl bereitgestellt.  <br/> |
|[OnEndOfAuthentication](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfAuthentication.aspx) <br/> |Wird verwendet, wenn der Agent Informationen erforderlich, die sind nach der Remoteserver den Authentifizierungsprozess abgeschlossen ist; zum Beispiel für ein Agent, der eine Aktion für eine Nachricht basierend auf die von der remote-SMTP-Server oder Client bereitgestellten Authentifizierungsinformationen ausführt.  <br/> |
|["OnEndofData"](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) <br/> |Wird verwendet, wenn der Agent ausführen muss, eine Aktion basierend auf Daten, die in der Nachricht verfügbar ist. Dieses Ereignis wird nicht ausgelöst, auf den Front-End-Transport-Dienst. Wenn Ihre Transport-Agent muss dieses Ereignis verwendet werden, müssen Sie ihn auf einem Postfachserver zu installieren.  <br/> |
|["OnEndOfHeaders"](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) <br/> |Wird verwendet, wenn der Agent ausführen muss, eine Aktion basierend auf Informationen, die in den Kopfzeilen der gesendete Nachricht verfügbar ist.  <br/> |
   
## <a name="creating-a-custom-smtpreceiveagent-transport-agent"></a>Erstellen eines benutzerdefinierten SmtpReceiveAgent Transport-Agents

Das folgende Verfahren beschreibt, wie Sie einen benutzerdefinierten SmtpReceiveAgent Transport-Agent zu erstellen. 
  
### <a name="to-create-the-transport-agent"></a>So erstellen Sie den Transport-agent

1. Fügen Sie Verweise auf die Namespaces hinzu.
    
   ```cs
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Smtp;
      using Microsoft.Exchange.Data.Transport.Email;
      using Microsoft.Exchange.Data.TextConverters;
  
   ```

   Diese Namespaces finden Sie auf Ihrem Exchange 2013-Server. Wenn Sie einen Verweis auf die Namespaces hinzufügen, haben Sie Zugriff auf die Member [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) sowie andere Klassen in der [Exchange 2013: Erstellen Sie einen Textkörper Konvertierung Transport-Agent](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) Beispiel. 
    
2. Implementieren Sie die für die [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) -Klasse abgeleitete Klasse. 
    
   ```cs
      public class BodyConversionFactory : SmtpReceiveAgentFactory
      {
          /// <summary>
          /// Create a new BodyConversion
          /// </summary>
          /// <param name="server">Exchange server</param>
          /// <returns>A new BodyConversion</returns>
          public override SmtpReceiveAgent CreateAgent(SmtpServer server)
          {
              return new BodyConversion();
          }
      }
  
   ```

   Dieser Code abgeleitete Klasse instanziieren und überschreiben Sie die **Hilfe von CreateAgent** -Methode zum Erstellen einer Instanz des neuen benutzerdefinierten Agents. 
    
3. Definieren des Agents.
    
   ```cs
     public class BodyConversion : SmtpReceiveAgent
      {
          // Your custom code goes here
          /// <summary>
          /// The constructor registers an end of data event handler.
          /// </summary>
          public BodyConversion()
          {
              Debug.WriteLine("[BodyConversion] Agent constructor");
              this.OnEndOfData += new EndOfDataEventHandler(this.OnEndOfDataHandler);
          }
      }
  
   ```

   Nachdem Sie Ihre Agent-Klasse definiert haben, können Sie Ihre benutzerdefinierten Funktionalität hinzufügen. In diesem Beispiel wird das Ereignis ["OnEndofData"](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) an den benutzerdefinierten Ereignishandler umgeleitet. 
    
## <a name="see-also"></a>Siehe auch

- [Transport-Agent Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)    
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)    
- [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
    

