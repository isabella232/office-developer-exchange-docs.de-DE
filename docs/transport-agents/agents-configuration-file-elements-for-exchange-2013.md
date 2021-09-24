---
title: Agents-Konfigurationsdateielemente für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Agents
api_type:
- schema
ms.assetid: 3047653b-d712-46c1-ae0a-73f3975f5e9d
description: Hier finden Sie Informationen zu den XML-Elementen in der agents.config- und fetagents.config-Konfigurationsdatei in Exchange 2013.
ms.openlocfilehash: bdf394130f7818c5b956e8b15eed86a6318b9698
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510421"
---
# <a name="agents-configuration-file-elements-for-exchange-2013"></a>Agents-Konfigurationsdateielemente für Exchange 2013

Hier finden Sie Informationen zu den XML-Elementen in der agents.config- und fetagents.config-Konfigurationsdatei in Exchange 2013.
  
**Gilt für:** Exchange Server 2013
  
Wenn Sie den Clientzugriff oder die Postfachserverrolle auf einem Exchange Server installieren, erstellt das Installationsprogramm eine XML-Datei, die Konfigurationsinformationen zu agents enthält, die auf dem Server installiert sind. Sie können nicht direkt in diese Datei schreiben. 
  
Der Front-End-Transport-Dienst wird auf Clientzugriffsservern ausgeführt und schreibt in eine Datei mit dem Namen fetagents.config. Der Transportdienst und der Postfachtransportdienst werden auf Postfachservern ausgeführt und schreiben in eine Datei mit dem Namen agents.config. Ein Computer mit der Clientzugriffsserverrolle und der Postfachserverrolle verfügt über eine fetagents.config und eine agents.config Datei. 
  
Die einzige unterstützte Möglichkeit zum Schreiben in diese Dateien ist die Verwendung der Transport-Agent-Cmdlets in der Exchange Verwaltungsshell. Informationen zu den Transport-Agent-Cmdlets finden Sie unter [Mail Flow Cmdlets](https://technet.microsoft.com/library/aa998553%28v=exchg.150%29.aspx) auf TechNet. 
  
> [!NOTE]
> Um zwischen Agents zu unterscheiden, die den Front-End-Transport-Dienst auf dem Clientzugriffsserver und den Transportdienst auf dem Postfachserver erweitern, verfügen Transport-Agent-Cmdlets über einen  _TransportService-Parameter_ mit dem Wert "Hub" für den Transportdienst und "FrontEnd" für den Front-End-Transport-Dienst. 
  
Sie können die datei agents.config oder fetagents.config lesen, um das Vorhandensein und die Konfigurationsinformationen für einen oder mehrere Agents auf dem Server zu ermitteln. Diese Dokumentation enthält eine Referenz, die Sie verwenden können, um die Informationen in der agents.config-Datei oder im fetagents.config zu lesen. Das Format für beide Dateien ist identisch. Diese Dokumentation enthält keine Informationen zum Schreiben in die Dateien.
  
> [!CAUTION]
> Wenn Sie nicht unterstützte Methoden zum Schreiben in die agents.config Datei oder fetagents.config verwenden, kann dies zu unerwarteten Ergebnissen führen, z. B. einem Ausfall des Transportdiensts oder der Transport-Agents oder beides. Schreiben Sie nicht direkt in eine dieser Dateien. Die einzige unterstützte Methode zum Schreiben in diese Dateien ist die Verwendung der Transport-Agent-Cmdlets Exchange Verwaltungsshell. 
  
## <a name="location-of-the-transport-agent-configuration-files"></a>Speicherort der Transport-Agent-Konfigurationsdateien
<a name="bk_ConfigLoc"> </a>

Wenn Sie Exchange 2013 installieren, erstellt das Installationsprogramm eine XML-Datei mit dem Namen agents.config.template oder fetagents.config.template, abhängig von der installierten Serverrolle, im \<ExchangeInstallFolder\> Ordner "\TransportRoles\Agents" (wo \<ExchangeInstallFolder\> sich der Ordner befindet, in dem Sie Exchange 2013 installiert haben). Wenn Sie die Clientzugriffsserverrolle installieren, kopiert Exchange 2013 die Datei fetagents.config.template in fetagents.config. Wenn Sie die Postfachserverrolle installieren, kopiert Exchange 2013 die Datei agents.config.template in agents.config. Exchange 2013 liest und schreibt diese Datei, wenn Sie die Transport-Agents-Konfiguration auf dem Server ändern.
  
## <a name="verifying-a-transport-agent-installation"></a>Überprüfen einer Transport-Agent-Installation
<a name="bk_verifyinstall"> </a>

Sie können die XML-Funktionen des .NET Framework verwenden, um die agents.config oder die fetagents.config XML-Datei zu lesen und zu überprüfen. Um die Installation und Konfiguration eines Transport-Agents zu überprüfen, [](agent.md) lesen Sie den XML-Code in der Konfigurationsdatei, und suchen Sie das Agent-Element, das dem Transport-Agent entspricht. Wenn kein **Agent-Element** für den bestimmten Transport-Agent vorhanden ist, wird der Transport-Agent nicht installiert. Wenn der Transport-Agent installiert ist, können Sie die Attribute des **Agent-Elements** lesen, um dessen Konfiguration zu ermitteln. 
  
## <a name="configuration-file-element-hierarchy"></a>Hierarchie der Konfigurationsdateielemente
<a name="bk_elementref"> </a>

Der folgende Code zeigt die Elementhierarchie in der XML-Konfigurationsdatei.
  
```XML
<configuration>
    <mexRuntime>
        <monitoring>
            <agentExecution/>
            <messageSnapshot/>
        </monitoring>
        <agentList>
            <agent/>
            <agent/>
            <agent />
        </agentList>
    </mexRuntim>
</configuration>
```

## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_elementreflist"> </a>

- [Agent](agent.md)
    
- [agentExecution](agentexecution.md)
    
- [agentList](agentlist.md)
    
- [Konfiguration](configuration.md)
    
- [messageSnapshot](messagesnapshot.md)
    
- [mexRuntime](mexruntime.md)
    
- [Überwachung](monitoring.md)
    
## <a name="see-also"></a>Siehe auch

- [Transport-Agents in Exchange](transport-agents-in-exchange-2013.md)
- [Transport-Agent-Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)
- [Transport-Agent-Namespaces in Exchange 2013](transport-agent-namespaces-in-exchange-2013.md)
- [Cmdlets für E-Mail-Flow](https://docs.microsoft.com/powershell/exchange/?view=exchange-ps)
    

