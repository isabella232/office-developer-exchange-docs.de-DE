---
title: UpdateItem-Vorgang (Aufgabe)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: b0a7f114-d040-40eb-a8f3-05ea6489e472
description: Der UpdateItem-Vorgang wird verwendet, um die Eigenschaften von Aufgabenelementen im Exchange Speicher zu aktualisieren.
ms.openlocfilehash: a268b4b281f149f14bc6c48a774fc9071093ebb5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510750"
---
# <a name="updateitem-operation-task"></a>UpdateItem-Vorgang (Aufgabe)

Der UpdateItem-Vorgang wird verwendet, um die Eigenschaften von Aufgabenelementen im Exchange Speicher zu aktualisieren.
  
## <a name="remarks"></a>HinwBemerkungeneise

Sie können Exchange Webdienste nicht zum Senden von Aufgabenanforderungen verwenden. Exchange Webdienste können Aufgabenanforderungen zurückgeben, die von MicrosoftOfficeOutlook erstellt werden. Wenn bereits eine Aufgabenanforderung gesendet wurde, gibt eine Anforderung zum Aktualisieren der Aufgabe einen Fehler zurück.
  
## <a name="updating-the-current-occurrence-of-a-recurring-task"></a>Aktualisieren des aktuellen Vorkommens einer Wiederkehrenden Aufgabe

Das Ergebnis eines UpdateItem-Vorgangs für wiederkehrende Vorgänge unterscheidet sich vom Ergebnis des UpdateItem-Vorgangs für einen einzelnen, nicht wiederkehrenden Vorgang. Änderungen an einem Vorkommen einer Wiederkehrenden Aufgabe führen dazu, dass einmalige Vorgänge generiert werden, wenn die folgenden Aktualisierungen vorgenommen werden:
  
1. Die Statuseigenschaft eines erneuten oder nicht erneut generierten wiederkehrenden Vorgangs wird auf **Abgeschlossen** festgelegt.
    
2. Das Start- oder Enddatum eines nicht erneut generierten wiederkehrenden Vorgangs wird geändert.
    
Wenn beispielsweise eine **UpdateItem-Anforderung** den Wert "Completed" einer Terminserie auf **"true"** festlegt, enthält **updateItemResponse** eine neue ID und einen neuen ChangeKey, die einen neu erstellten einmaligen Vorgang darstellen. Die ID, die in der Anforderung enthalten war, ist weiterhin gültig, und die wiederkehrende Aufgabe, die durch diese ID dargestellt wird, wurde aktualisiert, um das nächste Vorkommen darzustellen. Der ChangeKey, der in der Anforderung enthalten war, ist nicht mehr gültig, da die Wiederkehrende Aufgabe aktualisiert wurde. 
  
Sie können den [GetItem-Vorgang](getitem-operation.md) verwenden, um den neuesten **ChangeKey** für die Wiederkehrende Aufgabe abzurufen. 
  
Bei nicht wiederkehrenden Vorgängen oder für das letzte Vorkommen einer wiederkehrenden Aufgabe gibt die UpdateItem-Antwort die gleiche **ID** zurück, die an sie übergeben wurde, und gibt den zugeordneten aktualisierten **ChangeKey** zurück.
  
## <a name="see-also"></a>Siehe auch



[UpdateItem-Vorgang](updateitem-operation.md)

