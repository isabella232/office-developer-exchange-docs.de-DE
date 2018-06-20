---
title: Generieren Sie eine Liste von Endpunkten für die AutoErmittlung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 82394d3c-9fc7-4b3c-b48d-1fe983c198f7
description: Erfahren Sie, wie Sie eine Priorität für die AutoErmittlung Endpunkte erstellen.
ms.openlocfilehash: ccecacc9c8beef464727efbc9d1fced7a81f9b7c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756900"
---
# <a name="generate-a-list-of-autodiscover-endpoints"></a>Generieren Sie eine Liste von Endpunkten für die AutoErmittlung

Erfahren Sie, wie Sie eine Priorität für die AutoErmittlung Endpunkte erstellen.
  
Die erste Aufgabe in der [AutoErmittlung-Prozesses](autodiscover-for-exchange.md) wird zum Erstellen der Liste der AutoErmittlung-Endpunkte für die Anwendung zu testen. Diese Endpunkte AutoErmittlung können stammen aus einer [SCP-Suche](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) oder die e-Mail-Adresse des Benutzers abgeleitet werden können. Schließlich können Sie eine große Anzahl von Endpunkten am Ende. Sehen wir uns an, wie Sie sie nach Priorität sortieren können. 
  
## <a name="start-with-scp-lookup"></a>Beginnen Sie mit SCP-Suche
<a name="bk_StartWithScp"> </a>

AutoErmittlung-Endpunkte, die keinen [SCP-Suche](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) stammen sollte die höchste Priorität in der Liste verfügen. Administratoren können konfigurieren SCP-Objekten so, dass Ihr Client an den Endpunkt engsten oder am effizientesten AutoErmittlung weitergeleitet, daher es ratsam ist, diese Endpunkte zu starten. Da die SCP-Suchprozess Priorisierung Schema verfügt, sind die Ergebnisse der SCP-Suche bereits, wie folgt priorisiert: 
  
1. AutoErmittlung-Endpunkten von SCP-Objekten, die mit einem Bereich für die Active Directory-Standort, zu dem der Client-Computer gehört.
    
2. AutoErmittlung-Endpunkten von SCP-Objekten, die nicht mit einem Bereich für alle Active Directory-Standort.
    
3. AutoErmittlung-Endpunkten von SCP-Objekten bezogen auf einem anderen Active Directory-Standort als die Website, der der Clientcomputer gehört.
    
Nachdem Sie die Ergebnisse der SCP-Suchprozess haben, können Sie Endpunkte hinzufügen, die von e-Mail-Adresse des Benutzers abgeleitet werden. Diese können dienen als eine standardmäßige Endpunkte und Fallback festgelegt, falls es keine Ergebnisse SCP gibt oder die Endpunkte von SCP-Suche zurückgegebenen nicht ausreichend sind.
  
## <a name="add-endpoints-derived-from-the-users-email-address"></a>Hinzufügen von e-Mail-Adresse des Benutzers abgeleitete Endpunkte
<a name="bk_AddDerivedEndpoints"> </a>

Wenn SCP-Suche funktioniert nicht oder nicht die SCP-Suche zurückgegebenen Endpunkte eine erfolgreiche Antwort zurückzugeben, können die e-Mail-Adresse des Benutzers einen Satz von AutoErmittlung Standardendpunkte abgeleitet werden. Diese Endpunkte sollte eine niedrigere Priorität als die SCP-Suche stammen, jedoch möglicherweise benötigt werden, wenn die SCP-Suche nicht erfolgreich war.
  
### <a name="to-derive-autodiscover-endpoints"></a>AutoErmittlung Endpunkte abgeleitet werden.

1. Extrahieren Sie den Domänennamen aus e-Mail-Adresse des Benutzers an. Angenommen, wenn die e-Mail-Adresse des Benutzers Sadie.Daniels@contoso.com ist, wäre der Domänennamen "contoso.com".
    
2. Endpunkt-URLs ohne Dateierweiterungen in den folgenden Formaten zu erstellen:
    
  - "https://" + Domäne + "/ Autodiscover/AutoErmittlung"
    
  - "https://autodiscover." + Domäne + "/ Autodiscover/AutoErmittlung"
    
Nachdem Sie die Liste der Endpunkt-URLs kompiliert werden, die von SCP-Suche und die e-Mail-Adresse des Benutzers abgeleitet werden sollen, müssen Sie möglicherweise überarbeiten Dateinamenerweiterungen in diesen URLs, je nachdem, ob Sie die [AutoErmittlung SOAP-Webdienst](http://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx) oder die [POX verwenden AutoErmittlung-Webdienst](http://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx).
  
## <a name="add-or-replace-file-name-extensions-in-endpoint-urls"></a>Fügen Sie hinzu oder Ersetzen Sie Dateinamenerweiterungen Endpunkt-URLs
<a name="bk_FileExtensions"> </a>

Sie können den AutoErmittlungsdienst mithilfe der AutoErmittlung SOAP-Webdienst oder den Webdienst POX AutoErmittlung zugreifen. Jeder Dienst verwendet ähnliche Endpunkt-URLs mit der einzige Unterschied ist, die Dateinamenerweiterung an. Der AutoErmittlung SOAP-Webdienst verwendet die Erweiterung "svc" und der Webdienst POX AutoErmittlung verwendet die Erweiterung ".xml".
  
Standardmäßig sind der AutoErmittlung-Endpunkt-URLs von SCP-Suche zurückgegeben POX URLs. Jedoch bei Verwendung von SOAP-AutoErmittlung können einfach die Dateinamenerweiterung aus ".xml" an "svc" ändern und versuchen Sie es eine SOAP-Anforderung.
  
Für die abgeleiteten AutoErmittlung-Endpunkt-URLs die Erweiterung fehlt. Fügen Sie die entsprechende Erweiterung für die AutoErmittlung-Webdienst, den Sie arbeiten, bevor Sie versuchen, die URL hinzu.
  
## <a name="example-generating-a-list-of-autodiscover-endpoints"></a>Beispiel: Erstellen einer Liste von AutoErmittlung-Endpunkte
<a name="bk_Example"> </a>

Sehen wir uns an einem Beispiel. Sadie Daniels (Sadie.Daniels@contoso.com) ist eine Exchange-Webdienste (EWS)-Anwendung zum ersten Mal verwendet. Die Anwendung verwendet für die AutoErmittlung selbst konfigurieren. Sadies Computers ausführt, wird die Domäne "contoso.com" und "Redmond" Active Directory-Standort ist. Die Anwendung generiert eine Liste der AutoErmittlung-Endpunkte, die in Abbildung 1 dargestellt.
  
**Abbildung 1: Beispielliste AutoErmittlung**

![Eine Beispielliste mit Endpunkten für die AutoErmittlung, in der über die SCP-Suche abgerufene Endpunkte mit einer höheren Priorität angezeigt werden als abgeleitete Endpunkte](media/Ex15_Autodiscover_GenerateList_Example.png)
  
Die EWS-Anwendung in diesem Beispiel bevorzugt den AutoErmittlung für SOAP-Webdienst, damit es die Dateinamenerweiterung für die SCP-Ergebnisse "svc" geändert, vor dem Senden von SOAP-Anforderungen für diese.
  
## <a name="next-steps"></a>Nächste Schritte
<a name="bk_NextSteps"> </a>

Nachdem Sie eine Liste von Endpunkten AutoErmittlung generiert haben, testen Sie sie durch [Senden von Anforderungen an die Endpunkte](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).
  
## <a name="see-also"></a>Siehe auch


- [AutoErmittlung für Exchange](autodiscover-for-exchange.md)
    
- [Suchen Sie nach AutoErmittlung-Endpunkten mithilfe von SCP-Suche in Exchange](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [Behandeln von AutoErmittlungs-Fehlermeldungen](handling-autodiscover-error-messages.md)
    

