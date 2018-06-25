---
title: UpdateItem-Vorgang (Aufgabe)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: b0a7f114-d040-40eb-a8f3-05ea6489e472
description: Der Vorgang UpdateItem wird verwendet, um Eigenschaften für Aufgabenelemente im Exchange-Speicher zu aktualisieren.
ms.openlocfilehash: d6f966fa663300b476383a136d30cf611d6bfb9b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839376"
---
# <a name="updateitem-operation-task"></a>UpdateItem-Vorgang (Aufgabe)

Der Vorgang UpdateItem wird verwendet, um Eigenschaften für Aufgabenelemente im Exchange-Speicher zu aktualisieren.
  
## <a name="remarks"></a>Hinweise

Sie können Exchange-Webdienste Aufgabenanfragen senden. Exchange-Webdienste können Aufgabenanfragen zurückzugeben, die vom MicrosoftOfficeOutlook erstellt werden. Wenn bereits eine Aufgabenanfrage gesendet wurde, wird eine Anforderung zum Aktualisieren der Aufgabe einen Fehler zurück.
  
## <a name="updating-the-current-occurrence-of-a-recurring-task"></a>Aktualisieren das aktuelle Vorkommen einer wiederkehrenden Aufgabe

Das Ergebnis einer UpdateItem Operation für wiederkehrende Aufgaben unterscheidet sich von das Ergebnis des Vorgangs UpdateItem für einen einzelnen, einer einmaligen Vorgang. Änderungen an einem Vorkommen einer Aufgabenserie verursachen einmalige Aufgaben generiert werden soll, wenn die folgenden Updates vorgenommen werden:
  
1. Die Statuseigenschaft des einer wiederkehrenden Aufgabe erzeugt oder nonregenerating wird auf **abgeschlossen**festgelegt.
    
2. Das Start- oder Enddatum des einer nonregenerating wiederkehrenden Aufgabe geändert wird.
    
Beispielsweise, wenn eine Anforderung **UpdateItem** den abgeschlossen-Wert, der einen sich wiederholenden Vorgang auf **true**festgelegt wird, muss die **UpdateItemResponse** enthalten, eine neue-Id und ChangeKey, die einen neu erstellten einmaligen Vorgang darstellen. Die Id, die in der Anforderung enthalten war noch gültig ist, und die Aufgabenserie, die durch diese Id dargestellt ist wurde aktualisiert, um das nächste Vorkommen darstellen. Die ChangeKey, die in der Anforderung enthalten war ist nicht mehr gültig, da sich wiederholenden Vorgang aktualisiert wurde. 
  
Die [GetItem-Vorgang](getitem-operation.md) können Sie um die neuesten **ChangeKey** für die sich wiederholenden Vorgang zu erhalten. 
  
Für einen einzelnen Aufgaben oder für das letzte Vorkommen einer Aufgabenserie, gibt die Antwort UpdateItem dieselbe **Id** , die es übergeben wurde, und gibt Sie zurück, dass der zugeordnete **ChangeKey**aktualisiert.
  
## <a name="see-also"></a>Siehe auch



[UpdateItem Operation](updateitem-operation.md)

