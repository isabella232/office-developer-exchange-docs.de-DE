---
title: CChkSGFiles-Klassenreferenz
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9347d5f6-95bb-4045-9c86-0dc0ded24fe8
description: Hier finden Sie Referenzinformationen für die CHKSGFILES-API in Exchange 2013.
ms.openlocfilehash: 38b1f2c900767c22594636f0c6ddf4855961aec4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526732"
---
# <a name="cchksgfiles-class-reference"></a>CChkSGFiles-Klassenreferenz

Hier finden Sie Referenzinformationen für die CHKSGFILES-API in Exchange 2013.
  
**Gilt für:** Exchange Server 2013 
  
Mit der CHKSGFILES-API können Sicherungs-und Wiederherstellungsanwendungen programmgesteuert die Integrität von Exchange Server 2013 Transaktionsprotokolldateien und-Datenbankenüber prüfen. Sie können diese API in Sicherungs-und Wiederherstellungsanwendungen verwenden, die den Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) verwenden.
  
> [!NOTE]
> Speichergruppen stehen in Exchange 2013 nicht zur Verfügung. Die Unterstützung für Speichergruppen wurde aus Exchange-Versionen, beginnend mit Exchange Server 2010, entfernt. Aus Gründen der Abwärtskompatibilität mit Datenbanken und Speichergruppen in Exchange-Versionen, die älter als Exchange 2010 sind, können Sie mit der CHKSGFILES-API Speichergruppen angeben. Wenn Sie CHKSGFILES für Exchange 2013 Datenbanken ausführen, sollten Sie Parameter festlegen, die einen Speichergruppen Bezeichner in eine leere Zeichenfolge angeben. 
  
## <a name="file-location"></a>Dateispeicherort
<a name="bk_fileslocation"> </a>

Die CHKSGFILES-API wird im Rahmen von Exchange 2013 ausgeliefert. Sie können diese API auf einem Computer verwenden, auf dem die Postfachserverrolle installiert ist. 
  
Standardmäßig wird die CHKSGFILES-dll im Verzeichnis C:\Program Files\Microsoft\Exchange\V15\Bin installiert.
  
Exchange 2013 enthält nur eine 64-Bit-Version (amd64) der CHKSGFILES-API. 
  
Sie können eine ZIP-Datei herunterladen, die die CHKSGFILE. lib-Bibliothek und CHKSGFILES. hxx-Headerdateien zur Verwendung in Ihrer benutzerdefinierten Anwendung aus dem [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=36802)enthält.
  
## <a name="development-languages"></a>Entwicklungssprachen
<a name="bk_developmentlanguages"> </a>

Die CHKSGFILES-API ist für die Verwendung mit Versionen von Visual Studio vorgesehen, die mit Visual Studio 2005 in systemeigenem C/C++ beginnen. Die CHKSGFILES-API ist nicht für die Verwendung in verwaltetem Code vorgesehen. Sie können zwar eine COM-Interop-Assembly mit CHKSGFILES erstellen, es wird jedoch keine unterstützte COM-Interop-Assembly mit Exchange 2013 ausgeliefert.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_inthissection"> </a>

- [CChkSGFiles. CMaxDbPerSG-Funktion](cchksgfiles-cmaxdbpersg-function.md)
    
- [CChkSGFiles. Delete-Funktion](cchksgfiles-delete-function.md)
    
- [CChkSGFiles. err-Aufzählung](cchksgfiles-err-enumeration.md)
    
- [CChkSGFiles. ErrCheckDbHeaders-Funktion](cchksgfiles-errcheckdbheaders-function.md)
    
- [CChkSGFiles. ErrCheckDbPages-Funktion](cchksgfiles-errcheckdbpages-function.md)
    
- [CChkSGFiles. ErrCheckLogs-Funktion](cchksgfiles-errchecklogs-function.md)
    
- [CChkSGFiles. ErrGetHeader-Funktion (reserviert)](cchksgfiles-errgetheader-function-reserved.md)
    
- [CChkSGFiles. ErrInit-Funktion](cchksgfiles-errinit-function.md)
    
- [CChkSGFiles. ErrTerm-Funktion](cchksgfiles-errterm-function.md)
    
- [CChkSGFiles. iDbInvalid-Aufzählung](cchksgfiles-idbinvalid-enumeration.md)
    
- [CChkSGFiles. New-Funktion](cchksgfiles-new-function.md)
    
- [CChkSGFiles. NO_FLAGS-Aufzählung](cchksgfiles-no_flags-enumeration.md)
    
- [CChkSGFiles. PAGE_INFO-Struktur](cchksgfiles-page_info-struct.md)
    
- [CChkSGFiles. PgnoFromFileOffset-Funktion](cchksgfiles-pgnofromfileoffset-function.md)
    
## <a name="see-also"></a>Siehe auch

- [Exchange Online- und Exchange-Entwicklung](../exchange-server-development.md)
- [Sicherung, Wiederherstellung und Notfallwiederherstellung](https://technet.microsoft.com/library/dd876874)
    

