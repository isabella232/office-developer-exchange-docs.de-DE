---
title: Verwenden der Antwort des Exchange-Verwaltungsshell-Cmdlets
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dac8e526-11c6-4c2e-b9a2-f016b1fc738a
description: Hier erfahren Sie, wie Sie die Antwort von einem Exchange-Verwaltungsshell-Cmdlet in Ihrer verwalteten Exchange-Anwendung verwenden.
ms.openlocfilehash: c1b81356ab5dc288ab08287d47581871c36beb05
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44435702"
---
# <a name="use-the-exchange-management-shell-cmdlet-response"></a>Verwenden der Antwort des Exchange-Verwaltungsshell-Cmdlets

Hier erfahren Sie, wie Sie die Antwort von einem Exchange-Verwaltungsshell-Cmdlet in Ihrer verwalteten Exchange-Anwendung verwenden.
  
**Gilt für:** Exchange Online | Exchange Server 2013 | Office 365
  
Jedes Exchange-Verwaltungsshell-Cmdlet gibt eine oder mehrere [PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx) -Instanzen zurück, die eine konsistente Ansicht eines beliebigen Objekts in der Exchange-Verwaltungsshell-Umgebung bereitstellen. Dieser Artikel enthält Informationen zum Verwenden der Eigenschaften einer **PSObject** -Instanz, um die Eigenschaftswerte des zugrunde liegenden Exchange Server 2013-API-Objekts zurückzugeben. 
  
## <a name="prerequisites-for-using-cmdlet-responses"></a>Voraussetzungen für die Verwendung von Cmdlet-Antworten
<a name="prerequisites_bk"> </a>

Um Cmdlet-Antworten verwenden zu können, benötigen Sie einen Verweis auf den **System. Automation. Management** -Namespace. 
  
> [!NOTE]
>  Wenn Sie Visual Studio verwenden, um eine Anwendung zu erstellen, müssen Sie dem Projekt einen Verweis auf die Assembly System. Mangagement. Automation. dll hinzufügen. Sie können die Assembly in einem der folgenden Speicherorte finden: 
> - Für die Betriebssysteme Windows XP und Windows Vista im Windows PowerShell-Installationsverzeichnis ($PSHOME) 
> - Für die Betriebssysteme Windows 7 und Windows 8 im folgenden Ordner: Windows\assembly\GAC_MSIL\System.Management.Automation 
  
## <a name="windows-powershell-remote-runspace"></a>Windows PowerShell Remote Remoterunspace
<a name="usingremoterunspace_bk"> </a>

Der Exchange-Verwaltungsshell verwendet Remote Windows PowerShell Funktionen für alle Befehle, sogar für Befehle, die auf dem lokalen Server ausgeführt werden. Daher werden alle Antworten von Exchange-Verwaltungsshell-Cmdlets serialisiert. Dies bedeutet, dass das Response-Objekt nicht in den Exchange-Objekttyp umgewandelt werden kann, obwohl das Response-Objekt den Exchange-Objekttyp angibt, der zum Generieren der Antwort verwendet wurde. Stattdessen müssen Sie den Eigenschaftenbehälter verwenden, der vom Response-Objekt verfügbar gemacht wird, um die Werte aus dem Exchange-Objekttyp zu erhalten.
  
Der Eigenschaftenbehälter im Response-Objekt enthält ein Schlüssel/Wert-Paar für jede öffentliche Eigenschaft oder Methode im Exchange-Objekttyp. Das Response-Objekt enthält den Namen des zugrunde liegenden Exchange-Objekttyps; Sie können diesen Namen verwenden, um den Exchange-Objekttyp zu ermitteln, der durch das Response-Objekt dargestellt wird, sodass Sie die entsprechende Eigenschaft extrahieren können. Jeder Wert im Eigenschaftenbehälter enthält auch Typinformationen, sodass Sie den Eigenschaftswert in den entsprechenden verwalteten Typ umwandeln können.
  
## <a name="use-the-cmdlet-response"></a>Verwenden der Cmdlet-Antwort
<a name="usingPSObject_bk"> </a>

Die [PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx) -Klasse macht die folgenden drei öffentlichen Eigenschaften verfügbar, die die Werte des zugrunde liegenden Exchange 2013-API-Objekts enthalten: [Properties](https://msdn.microsoft.com/library/system.management.automation.psobject.properties%28VS.85%29.aspx), [Methods](https://msdn.microsoft.com/library/system.management.automation.psobject.methods%28VS.85%29.aspx)und [Members](https://msdn.microsoft.com/library/system.management.automation.psobject.members%28VS.85%29.aspx). Jede Eigenschaft, die vom Exchange 2013-API-Objekt verfügbar gemacht wird, verfügt über ein entsprechendes Schlüssel/Wert-Paar in den Eigenschaften **Properties** und **Members** . Ihre Anwendung kann die **Properties** -Auflistung nach dem Namen einer Eigenschaft indizieren, um den Wert der Eigenschaft abzurufen. 
  
Sie können die **typeNames** -Eigenschaft der **PSObject** -Instanz verwenden, um den Typ des zugrunde liegenden Exchange-Objekts zu ermitteln, das von der **PSObject** -Instanz gekapselt wird. Die **typeNames** -Eigenschaft ist eine Auflistung von Zeichenfolgen, die die Objekthierarchie des dargestellten Typs enthält. Sie können diese Namen verwenden, um das Objekt zu bestimmen, das durch die **PSObject** -Instanz dargestellt wird, sodass Sie die entsprechende Eigenschaft extrahieren können. 
  
Im folgenden Codebeispiel wird die Cmdlet-Antwort verwendet, um den Inhalt der **Properties** -Auflistung einer **PSObject** -Instanz in der Konsole zu drucken. Für das Codebeispiel ist ein Verweis auf den **System. Automation. Management** -Namespace erforderlich. 
  
```cs
foreach (PSPropertyInfo propertyInfo in psObject.Properties)
{
    Console.WriteLine(string.Format("{0}: {1}",
        propertyInfo.Name, propertyInfo.Value);
}
```

<br/>

```vb
For Each PropertyInfo As PSProperty In ObjectInfo.Properties
    Console.WriteLine(String.Format("{0}: {1}", PropertyInfo.Name, PropertyInfo.Value))
Next

```

## <a name="see-also"></a>Siehe auch

- [Erstellen von Exchange-Verwaltungsshell Tools](create-exchange-management-shell-tools.md)   
- [Abrufen einer Liste von e-Mail-Benutzern mithilfe der Exchange-Verwaltungsshell](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
    

