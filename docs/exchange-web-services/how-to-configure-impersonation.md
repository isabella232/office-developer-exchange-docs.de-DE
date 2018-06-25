---
title: Konfigurieren des Identitätswechsels
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: efcef39f-e26d-4eed-95ac-36a5bf8c089f
description: Erfahren Sie, wie Sie einem Dienstkonto mithilfe der Exchange-Verwaltungsshell die Identitätswechselrolle gewähren können.
ms.openlocfilehash: 57ccef48a7553bcc06e3b3ae940b376b8555ef84
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756875"
---
# <a name="configure-impersonation"></a>Konfigurieren des Identitätswechsels

Erfahren Sie, wie Sie einem Dienstkonto mithilfe der Exchange-Verwaltungsshell die Identitätswechselrolle gewähren können. 
  
Durch den Identitätswechsel kann ein Aufrufer wie eine Dienstanwendung ein Benutzerkonto imitieren. Der Aufrufer kann Vorgänge mithilfe der Berechtigungen durchführen, die dem imitierten Konto zugewiesen sind, statt die dem Aufruferkonto zugewiesenen Berechtigungen zu verwenden.
  
Exchange Online, Exchange Online als Teil von Office 365 und Versionen von Exchange ab Exchange 2013 verwenden die rollenbasierte Zugriffssteuerung (RBAC), um Konten Berechtigungen zu gewähren. Ihr Exchange-Serveradministrator muss den Dienstkonten die **ApplicationImpersonation**-Rolle mithilfe des [New-ManagementRoleAssignment](http://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx)-Cmdlets gewähren, die andere Benutzer imitieren. 
  
## <a name="configuring-the-applicationimpersonation-role"></a>Konfigurieren der ApplicationImpersonation-Rolle

Verwenden Sie oder Ihr Exchange-Serveradministrator beim Zuweisen der **ApplicationImpersonation**-Rolle folgende Parameter des **New-ManagementRoleAssignment**-Cmdlets: 
  
-  _Name_ &ndash; Den Anzeigenamen der rollenzuweisung. Beim Zuweisen einer Rolle erfolgt ein Eintrag in der RBAC-Rollenliste. Sie können Rollenzuweisungen mithilfe des [Get-ManagementRoleAssignment](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx)-Cmdlets verifizieren. 
    
-  _Rolle_ &ndash; Der RBAC-Rolle zuweisen. Beim Einrichten des Identitätswechsels weisen Sie die **ApplicationImpersonation**-Rolle zu. 
    
-  _Benutzer_ &ndash; Das Dienstkonto. 
    
-  _CustomRecipientScope_ &ndash; Des Umfangs der Benutzer, die das Dienstkonto imitieren kann. Das Dienstkonto kann nur Benutzer innerhalb des angegebenen Umfangs imitieren. Wenn kein Umfang angegeben ist, wird dem Dienstkonto die **ApplicationImpersonation**-Rolle für alle Benutzer in einem Unternehmen gewährt. Sie können benutzerdefinierte Verwaltungsbereiche mithilfe des [New-ManagementScope](http://msdn.microsoft.com/library/1ea1f474-69d6-48c0-9beb-bfa4442c5dab.aspx)-Cmdlets angeben. 
    
Bevor Sie den Identitätswechsel konfigurieren, benötigen Sie Folgendes:
  
- Administratoranmeldeinformationen für den Exchange-Server
    
- Domänenadministrator-Anmeldeinformationen oder andere Anmeldeinformationen mit der Berechtigung zum Erstellen und Zuweisen von Rollen und Bereichen
    
- Exchange-Verwaltungstools. Sie werden auf dem Computer installiert, über den Sie die Befehle ausführen.
    
### <a name="to-configure-impersonation-for-all-users-in-an-organization"></a>So konfigurieren Sie den Identitätswechsel für alle Benutzer in einem Unternehmen

1. Öffnen Sie die Exchange-Verwaltungsshell. Wählen Sie im Startmenü **Alle Programme** > **Microsoft Exchange Server 2013**. 
    
2. Führen Sie das **New-ManagementRoleAssignment**-Cmdlet aus, um die Identitätswechselberechtigung für den angegebenen Benutzer hinzuzufügen. Im folgenden Beispiel wird veranschaulicht, wie man den Identitätswechsel konfigurieren muss, damit ein Dienstkonto alle anderen Benutzer in einem Unternehmen imitieren kann. 
    
   ```powershell
   New-ManagementRoleAssignment -name:impersonationAssignmentName -Role:ApplicationImpersonation -User:serviceAccount 
   ```

### <a name="to-configure-impersonation-for-specific-users-or-groups-of-users"></a>So konfigurieren Sie den Identitätswechsel für bestimmte Benutzer oder Benutzergruppen

1. Öffnen Sie die Exchange-Verwaltungsshell. Wählen Sie im Startmenü **Alle Programme** > **Microsoft Exchange Server 2013**. 
    
2. Führen Sie das **New-ManagementScope**-Cmdlet aus, um einen Bereich zu erstellen, dem die Identitätswechselrolle zugewiesen werden kann. Wenn ein vorhandener Bereich verfügbar ist, können Sie diesen Schritt überspringen. Im folgenden Beispiel wird veranschaulicht, wie ein Verwaltungsbereich für eine bestimmte Gruppe erstellt werden kann. 
    
   ```powershell
    New-ManagementScope -Name:scopeName -RecipientRestrictionFilter:recipientFilter
   ```

   Der Parameter _RecipientRestrictionFilter_ des Cmdlets **New-ManagementScope** definiert die Member des Bereichs. Sie können die Eigenschaften des **Identity**-Objekts verwenden, um den Filter zu erstellen. Das folgende Beispiel ist ein Filter, der das Ergebnis auf einen einzelnen Benutzer mit dem Benutzernamen „John" begrenzt. 
    
   ```powershell
   Name -eq "john"
   ```

3. Führen Sie das **New-ManagementRoleAssignment**-Cmdlet aus, um die Berechtigung zum Imitieren der Elemente des angegebenen Bereichs hinzuzufügen. Im folgenden Beispiel wird veranschaulicht, wie ein Dienstkonto zum Imitieren aller Benutzer in einem Bereich konfiguriert werden muss. 
    
   ```powershell
    New-ManagementRoleAssignment -Name:impersonationAssignmentName -Role:ApplicationImpersonation -User:serviceAccount -CustomRecipientWriteScope:scopeName
    
   ```


Nachdem der Administrator die Identitätswechsel-Berechtigungen gewährt hat, können Sie das Dienstkonto verwenden, um Aufrufe zu anderen Benutzerkonten auszuführen. Sie können die Rollenzuweisungen mithilfe des [Get-ManagementRoleAssignment](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx)-Cmdlets verifizieren. 
  
## <a name="see-also"></a>Siehe auch

- [Identitätswechsel und EWS in Exchange](impersonation-and-ews-in-exchange.md)
- [ApplicationImpersonation-Rolle](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx)   
- [New-ManagementRoleAssignment](http://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx)    
- [Get-ManagementRoleAssignment](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx)
    

