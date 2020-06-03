---
title: Abrufen einer Liste von e-Mail-Benutzern mithilfe der Exchange-Verwaltungsshell
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.assetid: 8b790dc8-5c4f-4acf-bbe7-63523395fbe7
description: In diesem Artikel erfahren Sie, wie Sie mithilfe von Exchange-Verwaltungsshell-Cmdlets ein Tool erstellen, das eine Liste von Exchange-Postfachbenutzern zurückgibt.
localization_priority: Priority
ms.openlocfilehash: 817d92ef1bb88017f471681b448c052ecaa54e7e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44435709"
---
# <a name="get-a-list-of-mail-users-by-using-the-exchange-management-shell"></a>Abrufen einer Liste von e-Mail-Benutzern mithilfe der Exchange-Verwaltungsshell

In diesem Artikel erfahren Sie, wie Sie mithilfe von Exchange-Verwaltungsshell-Cmdlets ein Tool erstellen, das eine Liste von Exchange-Postfachbenutzern zurückgibt.
  
**Gilt für:** Exchange Online | Exchange Server 2013 | Office 365 
  
Zum Abrufen einer Liste von Benutzern aus Exchange Online, Exchange Online als Teil von Office 365 oder einer Exchange-Version ab Exchange 2013 mithilfe eines verwalteten Tools, das ein Exchange-Verwaltungsshell-Cmdlet aufruft, müssen zwei Schritte ausgeführt werden. Zuerst bestimmen Sie einen Remoterunspace auf einem Exchange-Server, dann führen Sie das Cmdlet aus, um Benutzerinformationen aus dem Remoterunspace abzurufen. 

Zum Herstellen einer Verbindung mit dem Remoterunspace müssen Sie sich unter Verwendung des Authentifizierungsschemas, das die Sicherheitsanforderungen Ihrer Organisation erfüllt, beim Exchange-Server authentifizieren. 

Dieser Artikel enthält Codebeispiele, die Sie verwenden können, um einen Remoterunspace einzurichten und ein Exchange-Verwaltungsshell-Cmdlet zum Abrufen einer Liste von Benutzern von einem Exchange-Server auszuführen.

<a name="bk_prerequisites"> </a>

## <a name="prerequisites-for-getting-a-list-of-mailbox-users"></a>Voraussetzungen für das Abrufen einer Liste von Postfachbenutzern

Um diese Aufgabe auszuführen, benötigen Sie einen Verweis auf die folgenden Namespaces:
  
- **System. Collections. ObjectModel**
- **System. Management. Automation**
- **System. Management. Automation. Remoting**
- **System. Management. Automation. Runspaces**
    
> [!NOTE]
>  Wenn Sie Visual Studio zum Erstellen einer Anwendung verwenden, müssen Sie dem Projekt einen Verweis auf die Assembly "System.Management.Automation.dll" hinzufügen. Die Assembly finden Sie an einem der folgenden Speicherorte:
> - Für die Betriebssysteme Windows XP und Windows Vista im Windows PowerShell-Installationsverzeichnis ($PSHOME)
> - Für die Betriebssysteme Windows 7 und Windows 8 im folgenden Ordner: Windows\assembly\GAC_MSIL\System.Management.Automation 
  
Laden Sie das Exchange 2013-Verwaltungs-Snap-in nicht in das Remoterunspace auf Computern mit Anwendungen, die Exchange-Verwaltungsshell-Cmdlets automatisieren. Stattdessen muss die Anwendung einen Remoterunspace erstellen, wie an späterer Stelle in diesem Artikel beschrieben.

<a name="bk_gettinglistmailbox"> </a>

## <a name="connect-to-a-remote-runspace-on-an-exchange-server"></a>Herstellen einer Verbindung mit einem Remoterunspace auf einem Exchange-Server

Die Methode zum Herstellen einer Verbindung mit einem Remoterunspace zur Verwendung eines Exchange-Verwaltungsshell-Cmdlets ist je nach verwendetem Authentifizierungsschema verschieden. Die Codebeispiele in diesem Abschnitt zeigen, wie Sie eine Verbindung mit einem Remoterunspace herstellen, wenn Sie eine der in der folgenden Tabelle aufgeführten Authentifizierungsmethoden verwenden.
  
|**Authentifizierungsmethode**|**Gilt für**|**uri**|
|:-----|:-----|:-----|
|[Herstellen einer Verbindung mit einem Remoterunspace in Exchange Online mithilfe der Standardauthentifizierung](#bk_basic) <br/> |Exchange Online-Server  <br/> |`https://outlook.office365.com/PowerShell-LiveID`<br/><br/>`https://<server>/PowerShell-LiveID`  <br/> |
|[Herstellen einer Verbindung mit einem Remoterunspace mithilfe der Zertifikatauthentifizierung](#bk_cert) <br/> |Exchange Online- und Exchange lokal-Server  <br/> |`https://outlook.office365.com/PowerShell`<br/><br/>`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |
|[Herstellen einer Verbindung mit einem Remoterunspace auf einem Exchange-Server mithilfe der Kerberos-Authentifizierung](#bk_Kerberos) <br/> |Exchange Online- und Exchange lokal-Server  <br/> |`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |

<a name="bk_basic"> </a>

### <a name="connect-to-a-remote-runspace-on-exchange-online-by-using-basic-authentication"></a>Herstellen einer Verbindung mit einem Remoterunspace in Exchange Online mithilfe der Standardauthentifizierung

Im folgenden Codebeispiel wird die **GetUsersUsingBasicAuth**-Methode definiert, die unter Verwendung der Standardauthentifizierung einen Exchange-Verwaltungsshell-Runspace auf einem Exchange Online-Remoteserver erstellt. Anschließend ruft die Methode die **GetUserInformation**-Methode auf, wie im Abschnitt [Abrufen einer Liste von Postfachbenutzern aus einem Remoterunspace](#bk_remote) definiert, um eine Liste der Benutzer auf dem Remoteserver zurückzugeben.
  
This method requires the following parameters:
  
-  **liveIDConnectionUri** &ndash; Eine Zeichenfolge, die den URI des Exchange Online Servers enthält, von dem die Anwendung authentifiziert wird. Wenn Exchange Online in Office 365 läuft, ist der URI `https://outlook.office365.com/PowerShell-LiveID` ; andernfalls ist der URI `https://<servername>/PowerShell-LiveID` . 
    
-  **schemaUri** &ndash; Eine Zeichenfolge, die den URI des Schemadokuments enthält, das das Exchange-Verwaltungsshell Schema definiert. Der Schema-URI ist `https://schemas.microsoft.com/powershell/Microsoft.Exchange` . 
    
-  **Anmeldeinformationen** &ndash; Ein [PSCredential](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx) -Objekt, das die Anmeldeinformationen des Benutzers enthält, der die Anwendung ausführt. 
    
-  **Anzahl** &ndash; Die Anzahl der zurückzugebenden Exchange-Postfachbenutzer. 
    
```cs
public Collection<PSObject> GetUsersUsingBasicAuth(
    string liveIDConnectionUri, string schemaUri, PSCredential credentials, int count)
{
    WSManConnectionInfo connectionInfo = new WSManConnectionInfo(
        new Uri(liveIDConnectionUri),
        schemaUri, credentials);
    connectionInfo.AuthenticationMechanism = AuthenticationMechanism.Basic;
    using (Runspace runspace = RunspaceFactory.CreateRunspace(connectionInfo))
    {
        return GetUserInformation(count, runspace);
    }
}
```


```vb
  Function GetUsersUsingBasicAuth( _
    ByVal LiveIDConnectionUri As String, ByVal ScehmaUri As String, _
    ByVal Credentials As PSCredential, ByVal Count As Integer) As Collection(Of PSObject)
    Dim ConnectionInfo As WSManConnectionInfo = _
        New WSManConnectionInfo(New Uri(LiveIDConnectionUri), ScehmaUri, Credentials)
    ConnectionInfo.AuthenticationMechanism = AuthenticationMechanism.Basic
    Dim RemoteRunspace As Runspace
    RemoteRunspace = RunspaceFactory.CreateRunspace(ConnectionInfo)
    Return GetUserInformation(Count, RemoteRunspace)
  End Function

```

<a name="bk_cert"> </a>

### <a name="connect-to-a-remote-runspace-by-using-certificate-authentication"></a>Herstellen einer Verbindung mit einem Remoterunspace mithilfe der Zertifikatauthentifizierung

Im folgenden Codebeispiel wird die **GetUsersUsingCertificate**-Methode definiert, die unter Verwendung einer Zertifikatauthentifizierung einen Exchange-Verwaltungsshell-Runspace auf einem Remoteserver erstellt. Anschließend ruft die Methode die **GetUserInformation**-Methode auf, wie im Abschnitt [Abrufen einer Liste von Postfachbenutzern aus einem Remoterunspace](#bk_remote) definiert, um eine Liste der Benutzer auf dem Remoteserver zurückzugeben.
  
This method requires the following parameters:
  
-  **Fingerabdruck** &ndash; Eine Zeichenfolge, die den Fingerabdruck des Zertifikats enthält, das zum Authentifizieren der Anwendung verwendet wird. 
    
-  **certConnectionUri** &ndash; Eine Zeichenfolge, die den URI des Servers enthält, von dem das Zertifikat authentifiziert wird. Die möglichen URIs sind in der folgenden Tabelle aufgeführt. 
    
    **Tabelle 1. certConnectionUri-URIs**

    |**Server**|**uri**|
    |:-----|:-----|
    |Exchange-Server ohne SSL  <br/> |`http://<servername>/PowerShell`  <br/> |
    |Exchange-Server mit SSL  <br/> |`https://<servername>/PowerShell`  <br/> |
    |Exchange Online als Teil von Office 365  <br/> |`https://outlook.office365.com/PowerShell`  <br/> |
   
- **schemaUri** &ndash; Eine Zeichenfolge, die den URI des Schemadokuments enthält, das das Exchange-Verwaltungsshell Schema definiert. Der Schema-URI ist https://schemas.microsoft.com/powershell/Microsoft.Exchange . 
    
- **Anzahl** &ndash; Die Anzahl der zurückzugebenden Exchange-Postfachbenutzer. 
    
```cs
public Collection<PSObject> GetUsersUsingCertificate(
    string thumbprint, string certConnectionUri, string schemaUri, int count)
{
    WSManConnectionInfo connectionInfo = new WSManConnectionInfo(
        new Uri(certConnectionUri),
        schemaUri,
        thumbprint)
    using (Runspace runspace = RunspaceFactory.CreateRunspace(connectionInfo))
    {
        return GetUserInformation(count, runspace);
    }
}
```


```vb
  Function GetUsersUsingCertificate( _
    ByVal Thumbprint As String, ByVal CertConnectionUri As String, _
    ByVal SchemaUri As String, ByVal Count As Integer) As Collection(Of PSObject)
    Dim ConnectionInfo As WSManConnectionInfo
    ConnectionInfo = New WSManConnectionInfo(New Uri(CertConnectionUri), SchemaUri, Thumbprint)
    Dim RemoteRunspace As Runspace
    RemoteRunspace = RunspaceFactory.CreateRunspace(ConnectionInfo)
    Return GetUserInformation(Count, RemoteRunspace)
  End Function

```

<a name="bk_Kerberos"> </a>

### <a name="connect-to-a-remote-runspace-on-an-exchange-server-by-using-kerberos-authentication"></a>Herstellen einer Verbindung mit einem Remoterunspace auf einem Exchange-Server mithilfe der Kerberos-Authentifizierung

Im folgenden Codebeispiel wird die **GetUsersUsingKerberos**-Methode definiert, die unter Verwendung der Kerberos-Authentifizierung einen Exchange-Verwaltungsshell-Runspace auf einem Remoteserver erstellt. Anschließend ruft die Methode die **GetUserInformation**-Methode auf, wie im Abschnitt [Abrufen einer Liste von Postfachbenutzern aus einem Remoterunspace](#bk_remote) definiert, um eine Liste der Benutzer auf dem Remoteserver zurückzugeben.
  
This method requires the following parameters:
  
- **kerberosUri** &ndash; Eine Zeichenfolge, die den URI des Kerberos-Servers enthält, von dem die Anwendung authentifiziert wird. Die möglichen URIs sind in der folgenden Tabelle aufgeführt. 
    
    **Tabelle 2. kerberosUri-URIs**

    |**Server**|**uri**|
    |:-----|:-----|
    |Exchange-Server ohne SSL  <br/> |`http://<servername>/PowerShell`  <br/> |
    |Exchange-Server mit SSL  <br/> |`https://<servername>/PowerShell`  <br/> |
   
- **schemaUri** &ndash; Eine Zeichenfolge, die den URI des Schemadokuments enthält, das das Exchange-Verwaltungsshell Schema definiert. Der Schema-URI ist https://schemas.microsoft.com/powershell/Microsoft.Exchange . 
    
- **Anmeldeinformationen** &ndash; Ein [PSCredential](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx) -Objekt, das die Anmeldeinformationen des Benutzers enthält, der die Anwendung ausführt. 
    
- **Anzahl** &ndash; Die Anzahl der zurückzugebenden Exchange-Postfachbenutzer. 
    
```cs
public Collection<PSObject> GetUsersUsingKerberos(
    string kerberosUri, string schemaUri, PSCredential credentials, int count)
{
    WSManConnectionInfo connectionInfo = new WSManConnectionInfo(
        new Uri(kerberosUri),
        schemaUri, credentials);
    connectionInfo.AuthenticationMechanism = AuthenticationMechanism.Kerberos;
    using (Runspace runspace = RunspaceFactory.CreateRunspace(connectionInfo))
    {
        return GetUserInformation(count, runspace);
    }
}
```

```vb
  Function GetUsersUsingKerberos( _
    ByVal KerberosUri As String, ByVal ScehmaUri As String, _
    ByVal Credentials As PSCredential, ByVal Count As Integer) As Collection(Of PSObject)
    Dim ConnectionInfo As WSManConnectionInfo = _
        New WSManConnectionInfo(New Uri(KerberosUri), ScehmaUri, Credentials)
    ConnectionInfo.AuthenticationMechanism = AuthenticationMechanism.Kerberos
    Dim RemoteRunspace As Runspace
    RemoteRunspace = RunspaceFactory.CreateRunspace(ConnectionInfo)
    Return GetUserInformation(Count, RemoteRunspace)
  End Function

```

<a name="bk_remote"> </a>

## <a name="get-a-list-of-mailbox-users-from-a-remote-runspace"></a>Get a list of mailbox users from a remote runspace

Im folgenden Codebeispiel wird die **GetUserInformation** -Methode definiert, die eine Auflistung von [PSObject](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx) -Instanzen zurückgibt, die Exchange-Postfachbenutzer darstellen. This method is called by the **GetUsersUsingBasicAuth**, **GetUsersUsingCertificate**, and **GetUsersUsingKerberos** methods to return the list of users from the remote server. 
  
This method requires the following parameters:
  
- **Anzahl** &ndash; Die Anzahl der zurückzugebenden Exchange-Postfachbenutzer. 
    
- **Remoterunspace** &ndash; Die Remote Remoterunspace, die für den Exchange-Remoteserver eingerichtet wurde. 
    
```cs
public Collection<PSObject> GetUserInformation(int count, Runspace runspace)
{
    using (PowerShell powershell = PowerShell.Create())
    {
        powershell.AddCommand("Get-Users");
        powershell.AddParameter("ResultSize", count);
        runspace.Open();
        powershell.Runspace = runspace;
        return powershell.Invoke();
    }
}
```

```vb
Function GetUserInformation(ByVal Count As Integer, ByVal RemoteRunspace As Runspace) As Collection(Of PSObject)
    Dim RemotePowerShell As PowerShell = PowerShell.Create
    RemotePowerShell.AddCommand("Get-Users")
    RemotePowerShell.AddParameter("ResultSize", Count)
    ' Open the remote runspace on the server.
    RemoteRunspace.Open()
    ' Associate the runspace with the Exchange Management Shell.
    RemotePowerShell.Runspace = RemoteRunspace
    ' Invoke the Exchange Management Shell to run the command.
    Return RemotePowerShell.Invoke
End Function

```

Die **GetUserInformation** -Methode gibt nicht mehr als _count_ -Postfachbenutzer zurück. To simplify the code for this example, the method does not filter or otherwise limit the mailbox users that are returned. 
  
## <a name="see-also"></a>Siehe auch

- [Erstellen von Exchange-Verwaltungsshell Tools](create-exchange-management-shell-tools.md)   
- [Verwenden der Antwort des Exchange-Verwaltungsshell-Cmdlets](how-to-use-the-exchange-management-shell-cmdlet-response.md)
    

