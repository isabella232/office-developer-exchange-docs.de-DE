---
title: CChkSGFiles. CMaxDbPerSG-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CMaxDbPerSG
api_type:
- dllExport
ms.assetid: 5871988b-a5d7-42cc-9b83-8fededb5072f
description: 'Letzte Änderung: 22. Februar 2013'
ms.openlocfilehash: b7c3517779eb07ef053c1dd4fa25544310fb3343
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455261"
---
# <a name="cchksgfilescmaxdbpersg-function"></a>CChkSGFiles. CMaxDbPerSG-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Gibt die maximale Anzahl von Datenbanken zurück, die in einer einzelnen Exchange Server-Speichergruppe zulässig sind.
  
```cs
Static ULONG  __stdcall CMaxDbPerSG  ();

```

## <a name="parameters"></a>Parameter

Keine.
  
## <a name="return-value"></a>Return value

Die maximale Anzahl von Datenbanken, die der angegebene Exchange-Server pro Speichergruppe zulässt. Da Speichergruppen nicht Teil Exchange 2013 sind, gibt diese Funktion den Wert 1 zurück.
  
## <a name="remarks"></a>Bemerkungen

Mit dem **CCheckSGFiles** -Objekt können Sie Datenbanken (und Transaktionsprotokolldateien) nur in einer Speichergruppe validieren, sodass der von der **CMaxDbPerSG** -Funktion zurückgegebene Wert auch die maximale Anzahl von Datenbanken darstellt, die Sie überprüfen können, indem Sie eine Instanz der **CCheckSGFiles** -Klasse verwenden. 
  
Beachten Sie, dass Exchange Server 2003 und Exchange Server 2007 standardmäßig maximal fünf Datenbanken pro Speichergruppe zulassen.
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung betrieben wird, muss über Lesezugriffsberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.
  

