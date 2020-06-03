---
title: Pullbenachrichtigungen in Exchange für Postfachereignisse im Zusammenhang mit Löschungen in EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 83511eea-e0b5-4ef0-83b1-0c5434e6d3ab
description: Ermitteln Sie, welche Post Fach Ereignisse ausgelöst werden, wenn Sie Elemente mithilfe von EWS in Exchange löschen.
ms.openlocfilehash: c3d98ff798e3d0f6d214111d51da2c81278fd17d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457655"
---
# <a name="pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange"></a>Pullbenachrichtigungen in Exchange für Postfachereignisse im Zusammenhang mit Löschungen in EWS

Ermitteln Sie, welche Post Fach Ereignisse ausgelöst werden, wenn Sie Elemente mithilfe von EWS in Exchange löschen.
  
Wenn Sie [Elemente und Ordner aus einem Postfach löschen](deleting-items-by-using-ews-in-exchange.md), wird ein Post Fach Ereignis ausgelöst. In verschiedenen Versionen von Exchange werden unterschiedliche Post Fach Ereignisse als Reaktion auf Änderungen an Elementen und Ordnern in einem Postfach zurückgegeben. In der folgenden Tabelle sind die Post Fach Ereignisse aufgeführt, die für Löschungen zurückgegeben werden, wenn Sie Pull-Benachrichtigungen zum Abonnieren von Post Fach Ereignissen verwenden. 
  
**Tabelle 1: Lösch bezogene Post Fach Ereignisse für Pull-Benachrichtigungen**

|**Der Typ des Löschvorgangs und der EWS-Vorgang**|**Exchange 2010 Benachrichtigung, wenn Sie jeden Ordner Bezeichner angeben**|**Exchange 2010 Benachrichtigung, wenn Sie alle Ordner angeben**|**Exchange Online und Exchange 2013 Benachrichtigung, wenn Sie jeden Ordner Bezeichner angeben**|**Exchange Online und Exchange 2013, wenn Sie alle Ordner angeben**|
|:-----|:-----|:-----|:-----|:-----|
|Weiche Löschung über den [DeleteItem-Vorgang](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |DeletedEvent für das Element.  <br/> ModifiedEvent für den übergeordneten Ordner des Elements.  <br/> |DeletedEvent für das Element.  <br/> ModifiedEvent für den übergeordneten Ordner des Elements.  <br/> |MovedEvent für das Element. Dies gibt sowohl den alten als auch den neuen übergeordneten Ordner Bezeichner an. Das Element wird in den Ordner für die gelöschten Elemente im Dumpster verschoben.   <br/> ModifiedEvent für den übergeordneten Ordner des Elements.  <br/> |DeletedEvent für das Element.  <br/> DeletedEvent für das Element aus dem standardmäßigen Suchordner AllItems.  <br/> ModifiedEvent für den übergeordneten Ordner des Elements.  <br/> |
|Hartes löschen über den [DeleteItem-Vorgang](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |DeletedEvent für das Element.  <br/> ModifiedEvent für den übergeordneten Ordner des Elements.  <br/> |DeletedEvent für das Element.  <br/> ModifiedEvent für den übergeordneten Ordner des Elements.  <br/> |DeletedEvent für das Element.  <br/> ModifiedEvent für den übergeordneten Ordner des Elements.  <br/> |DeletedEvent für das Element.  <br/> DeletedEvent für das Element aus dem standardmäßigen Suchordner AllItems.  <br/> ModifiedEvent für den übergeordneten Ordner des Elements.  <br/> |
|Navigieren in den Ordner "Gelöschte Elemente" über den [DeleteItem-Vorgang](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |MovedEvent für das Element. Dies gibt sowohl den alten als auch den neuen übergeordneten Ordner Bezeichner an.  <br/> ModifiedEvent für den alten übergeordneten Ordner des Elements.  <br/> ModifiedEvent für den neuen übergeordneten Ordner des Elements, bei dem es sich um den Ordner "Gelöschte Elemente" handelt.  <br/> |MovedEvent für das Element. Dies gibt sowohl den alten als auch den neuen übergeordneten Ordner Bezeichner an.  <br/> ModifiedEvent für den alten übergeordneten Ordner des Elements.  <br/> ModifiedEvent für den neuen übergeordneten Ordner des Elements, bei dem es sich um den Ordner "Gelöschte Elemente" handelt.  <br/> |MovedEvent für das Element. Dies gibt sowohl den alten als auch den neuen übergeordneten Ordner Bezeichner an.  <br/> ModifiedEvent für den alten übergeordneten Ordner des Elements.  <br/> ModifiedEvent für den neuen übergeordneten Ordner des Elements, bei dem es sich um den Ordner "Gelöschte Elemente" handelt.  <br/> |DeletedEvent aus dem standardmäßigen Suchordner von AllItems.  <br/> CreatedEvent für das Element im Ordner AllItems.  <br/> ModifiedEvent für den ursprünglichen übergeordneten Ordner des Elements.  <br/> ModifiedEvent für den Ordner "Gelöschte Elemente".  <br/> |
|Weiche Löschung über den [DeleteFolder-Vorgang](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den übergeordneten Ordner des Ordners.  <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den übergeordneten Ordner des Ordners.  <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den übergeordneten Ordner des Ordners.  <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den übergeordneten Ordner des Ordners.  <br/> |
|Hartes löschen über den [DeleteFolder-Vorgang](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den übergeordneten Ordner des Ordners.  <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den übergeordneten Ordner des Ordners.  <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den übergeordneten Ordner des Ordners.  <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den übergeordneten Ordner des Ordners.  <br/> |
|Navigieren in den Ordner "Gelöschte Elemente" über den [DeleteFolder-Vorgang](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |MovedEvent für den Ordner. Dies gibt sowohl den alten als auch den neuen übergeordneten Ordner Bezeichner an.  <br/> ModifiedEvent für den alten übergeordneten Ordner des Ordners.  <br/> ModifiedEvent für den neuen übergeordneten Ordner des Ordners, bei dem es sich um den Ordner "Gelöschte Elemente" handelt.  <br/> |MovedEvent für den Ordner. Dies gibt sowohl den alten als auch den neuen übergeordneten Ordner Bezeichner an.  <br/> ModifiedEvent für den alten übergeordneten Ordner des Ordners.  <br/> ModifiedEvent für den neuen übergeordneten Ordner des Ordners, bei dem es sich um den Ordner "Gelöschte Elemente" handelt.  <br/> |MovedEvent für den Ordner. Dies gibt sowohl den alten als auch den neuen übergeordneten Ordner Bezeichner an.  <br/> ModifiedEvent für den alten übergeordneten Ordner des Ordners.  <br/> ModifiedEvent für den neuen übergeordneten Ordner des Ordners, bei dem es sich um den Ordner "Gelöschte Elemente" handelt.  <br/> |ModifiedEvent für den alten übergeordneten Ordner des Ordners.  <br/> ModifiedEvent für den neuen übergeordneten Ordner des Ordners, bei dem es sich um den Ordner "Gelöschte Elemente" handelt.  <br/> |
   
## <a name="see-also"></a>Siehe auch


- [Benachrichtigungsabonnements, Postfachereignisse und EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [Löschen von Elementen mithilfe von EWS in Exchange](deleting-items-by-using-ews-in-exchange.md)
    
- [Umgang mit Fehlern in Exchange im Zusammenhang mit Löschungen in EWS](handling-deletion-related-errors-in-ews-in-exchange.md)
    

