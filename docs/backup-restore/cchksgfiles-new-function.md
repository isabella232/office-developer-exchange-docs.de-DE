---
title: CChkSGFiles. New-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- New
api_type:
- dllExport
ms.assetid: 588d8c74-c9ce-4d5e-8a79-a2a68676e858
description: 'Letzte Änderung: 22. Februar 2013'
ms.openlocfilehash: d18d3ef20890012a1d8c193ec87bdca10a1ed451
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455233"
---
# <a name="cchksgfilesnew-function"></a>CChkSGFiles. New-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Erstellt eine neue Instanz der **CChkSGFiles** -Klasse. Sie müssen diese Funktion aufrufen, bevor Sie die zu überprüfende Speichergruppe und Datenbanken angeben können. 
  
```cs
Static CCheckSGFiles  * __stdcall New  ();

```

## <a name="parameters"></a>Parameter

Keine.
  
## <a name="return-value"></a>Return value

Ein Verweis (Zeiger) auf das neu erstellte Objekt.
  
## <a name="remarks"></a>Bemerkungen

Die **neue** Funktion erstellt ein **CCheckSGFiles** -Objekt und gibt dem Aufrufer einen Verweis (Zeiger) auf dieses Objekt zurück. Sie müssen diese Funktion aufrufen, bevor Sie eine der anderen Funktionen in der **CCheckSGFiles** -Klasse aufruft. 
  
Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, müssen Sie die **neue** Funktion im Single-Thread-Teil der Anwendung aufrufen, und Sie können Sie nur einmal für jedes **CCheckSGFiles** -Objekt aufrufen. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung betrieben wird, muss über Lesezugriffsberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.
  

