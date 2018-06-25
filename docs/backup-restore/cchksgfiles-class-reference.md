---
title: Referenz für die CChkSGFiles
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9347d5f6-95bb-4045-9c86-0dc0ded24fe8
description: Referenzinformationen Sie für die CHKSGFILES-API in Exchange 2013.
ms.openlocfilehash: 583ac5e16ab60d119c3028bf81123e9f60a58ff4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756805"
---
# <a name="cchksgfiles-class-reference"></a>Referenz für die CChkSGFiles

Referenzinformationen Sie für die CHKSGFILES-API in Exchange 2013.
  
**Gilt für:** Exchange Server 2013 
  
Die CHKSGFILES-API ermöglicht die Sicherung und Wiederherstellung Applications, um die Integrität von Exchange Server 2013-Transaktionsprotokolldateien und Datenbanken programmgesteuert zu überprüfen. Sie können diese API in Sicherung verwenden und Wiederherstellen von Webanwendungen, die den Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) verwenden.
  
> [!NOTE]
> Speichergruppen sind nicht verfügbar in Exchange 2013. Unterstützung für Speichergruppen wurde aus Exchange beginnend mit Exchange Server 2010-Versionen entfernt. Für die Abwärtskompatibilität mit Datenbanken und Speichergruppen in früheren Versionen von Exchange als Exchange 2010 können mit der API für CHKSGFILES Speichergruppen angeben. Wenn Sie für CHKSGFILES in Exchange 2013-Datenbanken ausführen, sollten Sie Parameter festlegen, die einen Gruppenbezeichner Speicher auf eine leere Zeichenfolge angeben. 
  
## <a name="file-location"></a>Dateispeicherort
<a name="bk_fileslocation"> </a>

Die CHKSGFILES-API ist im Lieferumfang von Exchange 2013. Sie können diese API auf einem Computer verwenden, die die Postfach-Serverrolle installiert ist. 
  
Standardmäßig ist die CHKSGFILES-DLL im Verzeichnis C:\Program Files\Microsoft\Exchange\V15\Bin installiert.
  
Exchange 2013 umfasst nur eine 64-Bit-Version (amd64) Version der CHKSGFILES-API. 
  
Sie können eine ZIP-Datei, die die Bibliothek CHKSGFILE.lib enthält und CHKSGFILES.hxx-Header-Dateien für die Verwendung in Ihrer benutzerdefinierten Anwendung aus dem [Microsoft Download Center](http://www.microsoft.com/en-us/download/details.aspx?id=36802)herunterladen.
  
## <a name="development-languages"></a>Entwicklungssprachen
<a name="bk_developmentlanguages"> </a>

Die CHKSGFILES-API ist für die Verwendung mit Visual Studio beginnend mit Visual Studio 2005 im systemeigenen C/C++-Versionen vorgesehen. Die CHKSGFILES-API ist nicht für die Verwendung in verwaltetem Code vorgesehen. Obwohl Sie eine COM-Interop-Assembly mit CHKSGFILES erstellen können, werden wir eine unterstützte COM-Interop-Assembly mit Exchange 2013 nicht geliefert.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_inthissection"> </a>

- [CChkSGFiles.CMaxDbPerSG-Funktion](cchksgfiles-cmaxdbpersg-function.md)
    
- [CChkSGFiles.Delete-Funktion](cchksgfiles-delete-function.md)
    
- [CChkSGFiles.ERR-Aufzählung](cchksgfiles-err-enumeration.md)
    
- [CChkSGFiles.ErrCheckDbHeaders-Funktion](cchksgfiles-errcheckdbheaders-function.md)
    
- [CChkSGFiles.ErrCheckDbPages-Funktion](cchksgfiles-errcheckdbpages-function.md)
    
- [CChkSGFiles.ErrCheckLogs-Funktion](cchksgfiles-errchecklogs-function.md)
    
- [CChkSGFiles.ErrGetHeader-Funktion (reserviert)](cchksgfiles-errgetheader-function-reserved.md)
    
- [CChkSGFiles.ErrInit-Funktion](cchksgfiles-errinit-function.md)
    
- [CChkSGFiles.ErrTerm-Funktion](cchksgfiles-errterm-function.md)
    
- [CChkSGFiles.iDbInvalid-Aufzählung](cchksgfiles-idbinvalid-enumeration.md)
    
- [CChkSGFiles.New-Funktion](cchksgfiles-new-function.md)
    
- [CChkSGFiles.NO_FLAGS-Aufzählung](cchksgfiles-no_flags-enumeration.md)
    
- [CChkSGFiles.PAGE_INFO-Struktur](cchksgfiles-page_info-struct.md)
    
- [CChkSGFiles.PgnoFromFileOffset-Funktion](cchksgfiles-pgnofromfileoffset-function.md)
    
## <a name="see-also"></a>Siehe auch

- [Exchange Online und Exchange-Entwicklung](../exchange-server-development.md)
- [Sicherung, Wiederherstellung und Notfallwiederherstellung](http://technet.microsoft.com/en-us/library/dd876874)
    

