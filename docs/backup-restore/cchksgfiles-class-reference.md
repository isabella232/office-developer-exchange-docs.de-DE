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
# <a name="cchksgfiles-class-reference"></a><span data-ttu-id="272fe-103">CChkSGFiles-Klassenreferenz</span><span class="sxs-lookup"><span data-stu-id="272fe-103">CChkSGFiles class reference</span></span>

<span data-ttu-id="272fe-104">Hier finden Sie Referenzinformationen für die CHKSGFILES-API in Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="272fe-104">Find reference information for the CHKSGFILES API in Exchange 2013.</span></span>
  
<span data-ttu-id="272fe-105">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="272fe-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="272fe-106">Mit der CHKSGFILES-API können Sicherungs-und Wiederherstellungsanwendungen programmgesteuert die Integrität von Exchange Server 2013 Transaktionsprotokolldateien und-Datenbankenüber prüfen.</span><span class="sxs-lookup"><span data-stu-id="272fe-106">The CHKSGFILES API enables backup and restore applications to verify the integrity of Exchange Server 2013 transaction log files and databases programmatically.</span></span> <span data-ttu-id="272fe-107">Sie können diese API in Sicherungs-und Wiederherstellungsanwendungen verwenden, die den Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) verwenden.</span><span class="sxs-lookup"><span data-stu-id="272fe-107">You can use this API in backup and restore applications that use the Volume Shadow Copy Service (VSS).</span></span>
  
> [!NOTE]
> <span data-ttu-id="272fe-108">Speichergruppen stehen in Exchange 2013 nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="272fe-108">Storage groups are not available in Exchange 2013.</span></span> <span data-ttu-id="272fe-109">Die Unterstützung für Speichergruppen wurde aus Exchange-Versionen, beginnend mit Exchange Server 2010, entfernt.</span><span class="sxs-lookup"><span data-stu-id="272fe-109">Support for storage groups was removed from versions of Exchange starting with Exchange Server 2010.</span></span> <span data-ttu-id="272fe-110">Aus Gründen der Abwärtskompatibilität mit Datenbanken und Speichergruppen in Exchange-Versionen, die älter als Exchange 2010 sind, können Sie mit der CHKSGFILES-API Speichergruppen angeben.</span><span class="sxs-lookup"><span data-stu-id="272fe-110">For backward compatibility with databases and storage groups in versions of Exchange earlier than Exchange 2010, the CHKSGFILES API enables you to specify storage groups.</span></span> <span data-ttu-id="272fe-111">Wenn Sie CHKSGFILES für Exchange 2013 Datenbanken ausführen, sollten Sie Parameter festlegen, die einen Speichergruppen Bezeichner in eine leere Zeichenfolge angeben.</span><span class="sxs-lookup"><span data-stu-id="272fe-111">When you run CHKSGFILES against Exchange 2013 databases, you should set parameters that specify a storage group identifier to an empty string.</span></span> 
  
## <a name="file-location"></a><span data-ttu-id="272fe-112">Dateispeicherort</span><span class="sxs-lookup"><span data-stu-id="272fe-112">File location</span></span>
<span data-ttu-id="272fe-113"><a name="bk_fileslocation"> </a></span><span class="sxs-lookup"><span data-stu-id="272fe-113"><a name="bk_fileslocation"> </a></span></span>

<span data-ttu-id="272fe-114">Die CHKSGFILES-API wird im Rahmen von Exchange 2013 ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="272fe-114">The CHKSGFILES API ships as part of Exchange 2013.</span></span> <span data-ttu-id="272fe-115">Sie können diese API auf einem Computer verwenden, auf dem die Postfachserverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="272fe-115">You can use this API on a computer that has the Mailbox server role installed.</span></span> 
  
<span data-ttu-id="272fe-116">Standardmäßig wird die CHKSGFILES-dll im Verzeichnis C:\Program Files\Microsoft\Exchange\V15\Bin installiert.</span><span class="sxs-lookup"><span data-stu-id="272fe-116">By default, the CHKSGFILES DLL is installed in the C:\Program Files\Microsoft\Exchange\V15\Bin directory.</span></span>
  
<span data-ttu-id="272fe-117">Exchange 2013 enthält nur eine 64-Bit-Version (amd64) der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="272fe-117">Exchange 2013 includes only a 64-bit (amd64) version of the CHKSGFILES API.</span></span> 
  
<span data-ttu-id="272fe-118">Sie können eine ZIP-Datei herunterladen, die die CHKSGFILE. lib-Bibliothek und CHKSGFILES. hxx-Headerdateien zur Verwendung in Ihrer benutzerdefinierten Anwendung aus dem [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=36802)enthält.</span><span class="sxs-lookup"><span data-stu-id="272fe-118">You can download a .zip file that includes the CHKSGFILE.lib library and CHKSGFILES.hxx header files for use in your custom application from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=36802).</span></span>
  
## <a name="development-languages"></a><span data-ttu-id="272fe-119">Entwicklungssprachen</span><span class="sxs-lookup"><span data-stu-id="272fe-119">Development languages</span></span>
<span data-ttu-id="272fe-120"><a name="bk_developmentlanguages"> </a></span><span class="sxs-lookup"><span data-stu-id="272fe-120"><a name="bk_developmentlanguages"> </a></span></span>

<span data-ttu-id="272fe-121">Die CHKSGFILES-API ist für die Verwendung mit Versionen von Visual Studio vorgesehen, die mit Visual Studio 2005 in systemeigenem C/C++ beginnen.</span><span class="sxs-lookup"><span data-stu-id="272fe-121">The CHKSGFILES API is intended for use with versions of Visual Studio starting with Visual Studio 2005 in native C/C++.</span></span> <span data-ttu-id="272fe-122">Die CHKSGFILES-API ist nicht für die Verwendung in verwaltetem Code vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="272fe-122">The CHKSGFILES API is not intended for use in managed code.</span></span> <span data-ttu-id="272fe-123">Sie können zwar eine COM-Interop-Assembly mit CHKSGFILES erstellen, es wird jedoch keine unterstützte COM-Interop-Assembly mit Exchange 2013 ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="272fe-123">Although you can create a COM Interop assembly with CHKSGFILES, we do not ship a supported COM Interop assembly with Exchange 2013.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="272fe-124">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="272fe-124">In this section</span></span>
<span data-ttu-id="272fe-125"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="272fe-125"><a name="bk_inthissection"> </a></span></span>

- [<span data-ttu-id="272fe-126">CChkSGFiles. CMaxDbPerSG-Funktion</span><span class="sxs-lookup"><span data-stu-id="272fe-126">CChkSGFiles.CMaxDbPerSG function</span></span>](cchksgfiles-cmaxdbpersg-function.md)
    
- [<span data-ttu-id="272fe-127">CChkSGFiles. Delete-Funktion</span><span class="sxs-lookup"><span data-stu-id="272fe-127">CChkSGFiles.Delete function</span></span>](cchksgfiles-delete-function.md)
    
- [<span data-ttu-id="272fe-128">CChkSGFiles. err-Aufzählung</span><span class="sxs-lookup"><span data-stu-id="272fe-128">CChkSGFiles.ERR enumeration</span></span>](cchksgfiles-err-enumeration.md)
    
- [<span data-ttu-id="272fe-129">CChkSGFiles. ErrCheckDbHeaders-Funktion</span><span class="sxs-lookup"><span data-stu-id="272fe-129">CChkSGFiles.ErrCheckDbHeaders function</span></span>](cchksgfiles-errcheckdbheaders-function.md)
    
- [<span data-ttu-id="272fe-130">CChkSGFiles. ErrCheckDbPages-Funktion</span><span class="sxs-lookup"><span data-stu-id="272fe-130">CChkSGFiles.ErrCheckDbPages function</span></span>](cchksgfiles-errcheckdbpages-function.md)
    
- [<span data-ttu-id="272fe-131">CChkSGFiles. ErrCheckLogs-Funktion</span><span class="sxs-lookup"><span data-stu-id="272fe-131">CChkSGFiles.ErrCheckLogs function</span></span>](cchksgfiles-errchecklogs-function.md)
    
- [<span data-ttu-id="272fe-132">CChkSGFiles. ErrGetHeader-Funktion (reserviert)</span><span class="sxs-lookup"><span data-stu-id="272fe-132">CChkSGFiles.ErrGetHeader function (reserved)</span></span>](cchksgfiles-errgetheader-function-reserved.md)
    
- [<span data-ttu-id="272fe-133">CChkSGFiles. ErrInit-Funktion</span><span class="sxs-lookup"><span data-stu-id="272fe-133">CChkSGFiles.ErrInit function</span></span>](cchksgfiles-errinit-function.md)
    
- [<span data-ttu-id="272fe-134">CChkSGFiles. ErrTerm-Funktion</span><span class="sxs-lookup"><span data-stu-id="272fe-134">CChkSGFiles.ErrTerm function</span></span>](cchksgfiles-errterm-function.md)
    
- [<span data-ttu-id="272fe-135">CChkSGFiles. iDbInvalid-Aufzählung</span><span class="sxs-lookup"><span data-stu-id="272fe-135">CChkSGFiles.iDbInvalid enumeration</span></span>](cchksgfiles-idbinvalid-enumeration.md)
    
- [<span data-ttu-id="272fe-136">CChkSGFiles. New-Funktion</span><span class="sxs-lookup"><span data-stu-id="272fe-136">CChkSGFiles.New function</span></span>](cchksgfiles-new-function.md)
    
- [<span data-ttu-id="272fe-137">CChkSGFiles. NO_FLAGS-Aufzählung</span><span class="sxs-lookup"><span data-stu-id="272fe-137">CChkSGFiles.NO_FLAGS enumeration</span></span>](cchksgfiles-no_flags-enumeration.md)
    
- [<span data-ttu-id="272fe-138">CChkSGFiles. PAGE_INFO-Struktur</span><span class="sxs-lookup"><span data-stu-id="272fe-138">CChkSGFiles.PAGE_INFO struct</span></span>](cchksgfiles-page_info-struct.md)
    
- [<span data-ttu-id="272fe-139">CChkSGFiles. PgnoFromFileOffset-Funktion</span><span class="sxs-lookup"><span data-stu-id="272fe-139">CChkSGFiles.PgnoFromFileOffset function</span></span>](cchksgfiles-pgnofromfileoffset-function.md)
    
## <a name="see-also"></a><span data-ttu-id="272fe-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="272fe-140">See also</span></span>

- [<span data-ttu-id="272fe-141">Exchange Online- und Exchange-Entwicklung</span><span class="sxs-lookup"><span data-stu-id="272fe-141">Exchange Online and Exchange development</span></span>](../exchange-server-development.md)
- [<span data-ttu-id="272fe-142">Sicherung, Wiederherstellung und Notfallwiederherstellung</span><span class="sxs-lookup"><span data-stu-id="272fe-142">Backup, Restore, and Disaster Recovery</span></span>](https://technet.microsoft.com/library/dd876874)
    

