---
title: Abrufen einer Liste von e-Mail-Benutzer mithilfe der Exchange-Verwaltungsshell
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b790dc8-5c4f-4acf-bbe7-63523395fbe7
description: In diesem Artikel erfahren Sie, wie Sie mithilfe von Exchange-Verwaltungsshell-Cmdlets ein Tool erstellen, das eine Liste von Exchange-Postfachbenutzern zurückgibt.
ms.openlocfilehash: 6f64330a11e372bffbea2fcd88bcfa0231ec0f28
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757140"
---
# <a name="get-a-list-of-mail-users-by-using-the-exchange-management-shell"></a>Abrufen einer Liste von e-Mail-Benutzer mithilfe der Exchange-Verwaltungsshell

In diesem Artikel erfahren Sie, wie Sie mithilfe von Exchange-Verwaltungsshell-Cmdlets ein Tool erstellen, das eine Liste von Exchange-Postfachbenutzern zurückgibt.
  
**Gilt für:** Exchange Online | Exchange Server 2013 | Office 365 
  
Abrufen einer Liste von Benutzern von Exchange Online, gliedert sich Exchange Online als Teil von Office 365 oder eine Version von Exchange, beginnend mit Exchange 2013 mithilfe eines verwalteten Tools, das ein Exchange-Verwaltungsshell-Cmdlet aufruft. Zuerst bestimmen Sie einen remote-Runspace auf einem Exchange-Server; Führen Sie dann das Cmdlet, um die Benutzerinformationen in den remote-Runspace abgerufen. 

Zum Verbinden mit dem remote-Runspace müssen Sie mit dem Exchange-Server mithilfe des Authentifizierungsschemas, das die Sicherheit Ihrer Organisation erfüllt authentifizieren. 

Dieser Artikel enthält Codebeispiele, die Sie verwenden können, um eine remote-Runspace einrichten und Ausführen einer Exchange-Verwaltungsshell-Cmdlet zum Abrufen einer Liste von Benutzern von einem Exchange-Server.

<a name="bk_prerequisites"> </a>

## <a name="prerequisites-for-getting-a-list-of-mailbox-users"></a>Voraussetzungen für das Abrufen einer Liste von Postfachbenutzern

Um diese Aufgabe auszuführen, benötigen Sie einen Verweis auf die folgenden Namespaces:
  
- **System.Collections.ObjectModel**
- **System.Management.Automation**
- **System.Management.Automation.Remoting**
- **System.Management.Automation.Runspaces**
    
> [!NOTE]
>  Wenn Sie Visual Studio zum Erstellen einer Anwendung verwenden, müssen Sie dem Projekt einen Verweis auf die Assembly "System.Management.Automation.dll" hinzufügen. Die Assembly finden Sie an einem der folgenden Speicherorte:
> - Für die Betriebssysteme Windows XP und Windows Vista im Windows PowerShell-Installationsverzeichnis ($PSHOME)
> - Für die Betriebssysteme Windows 7 und Windows 8 im folgenden Ordner: Windows\assembly\GAC_MSIL\System.Management.Automation 
  
Nicht Laden der Exchange 2013-Verwaltungs-Snap-in in den Runspace auf Computern, die eine Anwendung ausgeführt werden, die Exchange-Verwaltungsshell-Cmdlets zu automatisieren. Die Anwendung sollte stattdessen einen remote-Runspace erstellen, wie weiter unten in diesem Artikel beschrieben.

<a name="bk_gettinglistmailbox"> </a>

## <a name="connect-to-a-remote-runspace-on-an-exchange-server"></a>Herstellen einer Verbindung mit einem Remoterunspace auf einem Exchange-Server

Die Methode zum Herstellen einer Verbindung mit einem Remoterunspace zur Verwendung eines Exchange-Verwaltungsshell-Cmdlets ist je nach verwendetem Authentifizierungsschema verschieden. Die Codebeispiele in diesem Abschnitt zeigen, wie Sie eine Verbindung mit einem Remoterunspace herstellen, wenn Sie eine der in der folgenden Tabelle aufgeführten Authentifizierungsmethoden verwenden.
  
|**Authentifizierungsmethode**|**Betrifft**|**URI**|
|:-----|:-----|:-----|
|[Verbinden Sie mit einer remote-Runspace auf Exchange Online mithilfe von Standardauthentifizierung](#bk_basic) <br/> |Exchange Online-Server  <br/> |`https://outlook.office365.com/PowerShell-LiveID`<br/><br/>`https://<server>/PowerShell-LiveID`  <br/> |
|[Verbinden Sie mit einer remote-Runspace mithilfe von Zertifikatauthentifizierung](#bk_cert) <br/> |Exchange Online- und Exchange lokal-Server  <br/> |`https://outlook.office365.com/PowerShell`<br/><br/>`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |
|[Verbinden Sie mit einer remote-Runspace auf einem Exchange-Server mithilfe von Kerberos-Authentifizierung](#bk_Kerberos) <br/> |Exchange Online- und Exchange lokal-Server  <br/> |`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |

<a name="bk_basic"> </a>

### <a name="connect-to-a-remote-runspace-on-exchange-online-by-using-basic-authentication"></a>Herstellen einer Verbindung mit einem Remoterunspace in Exchange Online mithilfe der Standardauthentifizierung

Im folgenden Codebeispiel wird definiert die **GetUsersUsingBasicAuth** -Methode, die ein Exchange-Verwaltungsshell-Runspace auf einem Remoteserver Exchange Online erstellt, mithilfe der Standardauthentifizierung. Anschließend ruft die Methode die **GetUserInformation** -Methode, wie im Abschnitt [Abrufen einer Liste von Postfachbenutzern aus einer remote-Runspace](#bk_remote), definiert, um eine Liste der Benutzer auf dem Remoteserver zurückzugeben.
  
This method requires the following parameters:
  
-  **liveIDConnectionUri** &ndash; Eine Zeichenfolge, die den URI des Exchange Online-Servers enthält, die die Anwendung zu authentifizieren. Wenn Exchange Online in Office 365 ausgeführt wird, ist der URI https://outlook.office365.com/PowerShell-LiveID; Andernfalls ist der URI https://\<Servername\>/PowerShell-LiveID. 
    
-  **schemaUri** &ndash; Eine Zeichenfolge, die den URI des Schemadokuments enthält, die das Exchange-Verwaltungsshell-Schema definiert. Das Schema-URI ist http://schemas.microsoft.com/powershell/Microsoft.Exchange. 
    
-  **Anmeldeinformationen** &ndash; Ein [PSCredential](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx) -Objekt, das die Anmeldeinformationen des Benutzers enthält, die die Anwendung ausgeführt wird. 
    
-  **Count** &ndash; Die Anzahl der Exchange-Postfachbenutzer zurückgegeben. 
    
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

Im folgenden Codebeispiel wird definiert die **GetUsersUsingCertificate** -Methode, die ein Exchange-Verwaltungsshell-Runspace auf einem Remoteserver erstellt, mit einem Zertifikat. Anschließend ruft die Methode die **GetUserInformation** -Methode, wie im Abschnitt [Abrufen einer Liste von Postfachbenutzern aus einer remote-Runspace](#bk_remote), definiert, um eine Liste der Benutzer auf dem Remoteserver zurückzugeben.
  
This method requires the following parameters:
  
-  **Fingerabdruck** &ndash; Eine Zeichenfolge, die den Fingerabdruck des Zertifikats enthält, mit dem die Anwendung zu authentifizieren. 
    
-  **certConnectionUri** &ndash; Eine Zeichenfolge, die den URI des Servers enthält, die das Zertifikat authentifizieren. Der URI wird einer der in der folgenden Tabelle aufgeführten entsprechen. 
    
    **In Tabelle 1. CertConnectionUri URIs**

    |**Server**|**URI**|
    |:-----|:-----|
    |Exchange-Server ohne SSL  <br/> |`http://<servername>/PowerShell`  <br/> |
    |Exchange-Server mit SSL  <br/> |`https://<servername>/PowerShell`  <br/> |
    |Exchange Online als Teil von Office 365  <br/> |`https://outlook.office365.com/PowerShell`  <br/> |
   
- **schemaUri** &ndash; Eine Zeichenfolge, die den URI des Schemadokuments enthält, die das Exchange-Verwaltungsshell-Schema definiert. Das Schema-URI ist http://schemas.microsoft.com/powershell/Microsoft.Exchange. 
    
- **Count** &ndash; Die Anzahl der Exchange-Postfachbenutzer zurückgegeben. 
    
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

Im folgenden Codebeispiel wird definiert die **GetUsersUsingKerberos** -Methode, die ein Exchange-Verwaltungsshell-Runspace auf einem Remoteserver erstellt, mithilfe der Kerberos-Authentifizierung. Anschließend ruft die Methode die **GetUserInformation** -Methode, wie im Abschnitt [Abrufen einer Liste von Postfachbenutzern aus einer remote-Runspace](#bk_remote), definiert, um eine Liste der Benutzer auf dem Remoteserver zurückzugeben.
  
This method requires the following parameters:
  
- **kerberosUri** &ndash; Eine Zeichenfolge, die den URI des Kerberos-Servers enthält, die die Anwendung zu authentifizieren. Der URI wird einer der in der folgenden Tabelle aufgeführten entsprechen. 
    
    **In Tabelle 2. KerberosUri URIs**

    |**Server**|**URI**|
    |:-----|:-----|
    |Exchange-Server ohne SSL  <br/> |`http://<servername>/PowerShell`  <br/> |
    |Exchange-Server mit SSL  <br/> |`https://<servername>/PowerShell`  <br/> |
   
- **schemaUri** &ndash; Eine Zeichenfolge, die den URI des Schemadokuments enthält, die das Exchange-Verwaltungsshell-Schema definiert. Das Schema-URI ist http://schemas.microsoft.com/powershell/Microsoft.Exchange. 
    
- **Anmeldeinformationen** &ndash; Ein [PSCredential](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx) -Objekt, das die Anmeldeinformationen des Benutzers enthält, die die Anwendung ausgeführt wird. 
    
- **Count** &ndash; Die Anzahl der Exchange-Postfachbenutzer zurückgegeben. 
    
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

Im folgenden Codebeispiel wird definiert die **GetUserInformation** -Methode, die eine Sammlung von [PSObject](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx) zurückgibt, die Exchange-Postfachbenutzer darstellen. Diese Methode wird von den Methoden **GetUsersUsingBasicAuth**, **GetUsersUsingCertificate**und **GetUsersUsingKerberos** , um die Liste der Benutzer aus dem Remoteserver zurückzugeben aufgerufen. 
  
This method requires the following parameters:
  
- **Count** &ndash; Die Anzahl der Exchange-Postfachbenutzer zurückgegeben. 
    
- **Runspace** &ndash; Der remote-Runspace, die für den Exchange-Remoteserver eingerichtet ist. 
    
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

Die **GetUserInformation** -Methode wird nicht mehr als _Count_ Postfachbenutzer zurück. Zur Vereinfachung des Codes für die in diesem Beispiel wird die Methode nicht filtern oder anderweitig einschränken, die Postfachbenutzer, die zurückgegeben werden. 
  
## <a name="see-also"></a>Siehe auch

- [Erstellen von Exchange-Verwaltungsshell-tools](create-exchange-management-shell-tools.md)   
- [Verwenden Sie die Exchange-Verwaltungsshell-Cmdlet-Antwort](how-to-use-the-exchange-management-shell-cmdlet-response.md)
    

