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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757140"
---
# <a name="get-a-list-of-mail-users-by-using-the-exchange-management-shell"></a><span data-ttu-id="e28d4-103">Abrufen einer Liste von e-Mail-Benutzer mithilfe der Exchange-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="e28d4-103">Get a list of mail users by using the Exchange Management Shell</span></span>

<span data-ttu-id="e28d4-104">In diesem Artikel erfahren Sie, wie Sie mithilfe von Exchange-Verwaltungsshell-Cmdlets ein Tool erstellen, das eine Liste von Exchange-Postfachbenutzern zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e28d4-104">Learn how to use Exchange Management Shell cmdlets to create a tool that returns a list of Exchange mailbox users.</span></span>
  
<span data-ttu-id="e28d4-105">**Gilt für:** Exchange Online | Exchange Server 2013 | Office 365</span><span class="sxs-lookup"><span data-stu-id="e28d4-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span> 
  
<span data-ttu-id="e28d4-106">Abrufen einer Liste von Benutzern von Exchange Online, gliedert sich Exchange Online als Teil von Office 365 oder eine Version von Exchange, beginnend mit Exchange 2013 mithilfe eines verwalteten Tools, das ein Exchange-Verwaltungsshell-Cmdlet aufruft.</span><span class="sxs-lookup"><span data-stu-id="e28d4-106">Getting a list of users from Exchange Online, Exchange Online as part of Office 365, or a version of Exchange starting with Exchange 2013 by using a managed tool that calls an Exchange Management Shell cmdlet is a two-step process.</span></span> <span data-ttu-id="e28d4-107">Zuerst bestimmen Sie einen remote-Runspace auf einem Exchange-Server; Führen Sie dann das Cmdlet, um die Benutzerinformationen in den remote-Runspace abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e28d4-107">First, you establish a remote runspace on an Exchange server; then, you run the cmdlet to retrieve the user information in the remote runspace.</span></span> 

<span data-ttu-id="e28d4-108">Zum Verbinden mit dem remote-Runspace müssen Sie mit dem Exchange-Server mithilfe des Authentifizierungsschemas, das die Sicherheit Ihrer Organisation erfüllt authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="e28d4-108">To connect to the remote runspace, you have to authenticate with the Exchange server by using the authentication scheme that meets the security requirements of your organization.</span></span> 

<span data-ttu-id="e28d4-109">Dieser Artikel enthält Codebeispiele, die Sie verwenden können, um eine remote-Runspace einrichten und Ausführen einer Exchange-Verwaltungsshell-Cmdlet zum Abrufen einer Liste von Benutzern von einem Exchange-Server.</span><span class="sxs-lookup"><span data-stu-id="e28d4-109">This article provides code examples that you can use to set up a remote runspace and run an Exchange Management Shell cmdlet to get a list of users from an Exchange server.</span></span>

<span data-ttu-id="e28d4-110"><a name="bk_prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="e28d4-110"></span></span>

## <a name="prerequisites-for-getting-a-list-of-mailbox-users"></a><span data-ttu-id="e28d4-111">Voraussetzungen für das Abrufen einer Liste von Postfachbenutzern</span><span class="sxs-lookup"><span data-stu-id="e28d4-111">Prerequisites for getting a list of mailbox users</span></span>

<span data-ttu-id="e28d4-112">Um diese Aufgabe auszuführen, benötigen Sie einen Verweis auf die folgenden Namespaces:</span><span class="sxs-lookup"><span data-stu-id="e28d4-112">To perform this task, you need a reference to the following namespaces:</span></span>
  
- <span data-ttu-id="e28d4-113">**System.Collections.ObjectModel**</span><span class="sxs-lookup"><span data-stu-id="e28d4-113">**System.Collections.ObjectModel**</span></span>
- <span data-ttu-id="e28d4-114">**System.Management.Automation**</span><span class="sxs-lookup"><span data-stu-id="e28d4-114">**System.Management.Automation**</span></span>
- <span data-ttu-id="e28d4-115">**System.Management.Automation.Remoting**</span><span class="sxs-lookup"><span data-stu-id="e28d4-115">**System.Management.Automation.Remoting**</span></span>
- <span data-ttu-id="e28d4-116">**System.Management.Automation.Runspaces**</span><span class="sxs-lookup"><span data-stu-id="e28d4-116">**System.Management.Automation.Runspaces**</span></span>
    
> [!NOTE]
>  <span data-ttu-id="e28d4-p102">Wenn Sie Visual Studio zum Erstellen einer Anwendung verwenden, müssen Sie dem Projekt einen Verweis auf die Assembly "System.Management.Automation.dll" hinzufügen. Die Assembly finden Sie an einem der folgenden Speicherorte:</span><span class="sxs-lookup"><span data-stu-id="e28d4-p102">When you are using Visual Studio to create an application, you must add a reference to the System.Management.Automation.dll assembly to the project. The assembly can be found in one of the following locations:</span></span>
> - <span data-ttu-id="e28d4-119">Für die Betriebssysteme Windows XP und Windows Vista im Windows PowerShell-Installationsverzeichnis ($PSHOME)</span><span class="sxs-lookup"><span data-stu-id="e28d4-119">For Windows XP and Windows Vista operating systems, the Windows PowerShell installation directory ($PSHOME).</span></span>
> - <span data-ttu-id="e28d4-120">Für die Betriebssysteme Windows 7 und Windows 8 im folgenden Ordner: Windows\assembly\GAC_MSIL\System.Management.Automation</span><span class="sxs-lookup"><span data-stu-id="e28d4-120">For the Windows 7 and Windows 8 operating systems, the following folder: Windows\assembly\GAC_MSIL\System.Management.Automation.</span></span> 
  
<span data-ttu-id="e28d4-121">Nicht Laden der Exchange 2013-Verwaltungs-Snap-in in den Runspace auf Computern, die eine Anwendung ausgeführt werden, die Exchange-Verwaltungsshell-Cmdlets zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="e28d4-121">Do not load the Exchange 2013 Management snap-in into the runspace on computers that are running applications that automate Exchange Management Shell cmdlets.</span></span> <span data-ttu-id="e28d4-122">Die Anwendung sollte stattdessen einen remote-Runspace erstellen, wie weiter unten in diesem Artikel beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e28d4-122">The application should instead create a remote runspace, as described later in this article.</span></span>

<span data-ttu-id="e28d4-123"><a name="bk_gettinglistmailbox"> </a></span><span class="sxs-lookup"><span data-stu-id="e28d4-123"></span></span>

## <a name="connect-to-a-remote-runspace-on-an-exchange-server"></a><span data-ttu-id="e28d4-124">Herstellen einer Verbindung mit einem Remoterunspace auf einem Exchange-Server</span><span class="sxs-lookup"><span data-stu-id="e28d4-124">Connect to a remote runspace on an Exchange server</span></span>

<span data-ttu-id="e28d4-p104">Die Methode zum Herstellen einer Verbindung mit einem Remoterunspace zur Verwendung eines Exchange-Verwaltungsshell-Cmdlets ist je nach verwendetem Authentifizierungsschema verschieden. Die Codebeispiele in diesem Abschnitt zeigen, wie Sie eine Verbindung mit einem Remoterunspace herstellen, wenn Sie eine der in der folgenden Tabelle aufgeführten Authentifizierungsmethoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="e28d4-p104">The method that you use to connect to a remote runspace to use an Exchange Management Shell cmdlet varies based on the authentication scheme that you are using. This section provides code examples that show how to connect to a remote runspace when you are using an authentication method listed in the following table.</span></span>
  
|<span data-ttu-id="e28d4-127">**Authentifizierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="e28d4-127">**Authentication method**</span></span>|<span data-ttu-id="e28d4-128">**Betrifft**</span><span class="sxs-lookup"><span data-stu-id="e28d4-128">**Applies to**</span></span>|<span data-ttu-id="e28d4-129">**URI**</span><span class="sxs-lookup"><span data-stu-id="e28d4-129">**URI**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e28d4-130">Verbinden Sie mit einer remote-Runspace auf Exchange Online mithilfe von Standardauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="e28d4-130">Connect to a remote runspace on Exchange Online by using basic authentication</span></span>](#bk_basic) <br/> |<span data-ttu-id="e28d4-131">Exchange Online-Server</span><span class="sxs-lookup"><span data-stu-id="e28d4-131">Exchange Online servers</span></span>  <br/> |`https://outlook.office365.com/PowerShell-LiveID`<br/><br/>`https://<server>/PowerShell-LiveID`  <br/> |
|[<span data-ttu-id="e28d4-132">Verbinden Sie mit einer remote-Runspace mithilfe von Zertifikatauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="e28d4-132">Connect to a remote runspace by using certificate authentication</span></span>](#bk_cert) <br/> |<span data-ttu-id="e28d4-133">Exchange Online- und Exchange lokal-Server</span><span class="sxs-lookup"><span data-stu-id="e28d4-133">Exchange Online and Exchange on-premises servers</span></span>  <br/> |`https://outlook.office365.com/PowerShell`<br/><br/>`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |
|[<span data-ttu-id="e28d4-134">Verbinden Sie mit einer remote-Runspace auf einem Exchange-Server mithilfe von Kerberos-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="e28d4-134">Connect to a remote runspace on an Exchange server by using Kerberos authentication</span></span>](#bk_Kerberos) <br/> |<span data-ttu-id="e28d4-135">Exchange Online- und Exchange lokal-Server</span><span class="sxs-lookup"><span data-stu-id="e28d4-135">Exchange Online and Exchange on-premises servers</span></span>  <br/> |`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |

<span data-ttu-id="e28d4-136"><a name="bk_basic"> </a></span><span class="sxs-lookup"><span data-stu-id="e28d4-136"></span></span>

### <a name="connect-to-a-remote-runspace-on-exchange-online-by-using-basic-authentication"></a><span data-ttu-id="e28d4-137">Herstellen einer Verbindung mit einem Remoterunspace in Exchange Online mithilfe der Standardauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="e28d4-137">Connect to a remote runspace on Exchange Online by using basic authentication</span></span>

<span data-ttu-id="e28d4-138">Im folgenden Codebeispiel wird definiert die **GetUsersUsingBasicAuth** -Methode, die ein Exchange-Verwaltungsshell-Runspace auf einem Remoteserver Exchange Online erstellt, mithilfe der Standardauthentifizierung.</span><span class="sxs-lookup"><span data-stu-id="e28d4-138">The following code example defines the **GetUsersUsingBasicAuth** method, which creates an Exchange Management Shell runspace on a remote Exchange Online server by using basic authentication.</span></span> <span data-ttu-id="e28d4-139">Anschließend ruft die Methode die **GetUserInformation** -Methode, wie im Abschnitt [Abrufen einer Liste von Postfachbenutzern aus einer remote-Runspace](#bk_remote), definiert, um eine Liste der Benutzer auf dem Remoteserver zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="e28d4-139">The method then calls the **GetUserInformation** method, as defined in the section [Get a list of mailbox users from a remote runspace](#bk_remote), to return a list of users on the remote server.</span></span>
  
<span data-ttu-id="e28d4-140">This method requires the following parameters:</span><span class="sxs-lookup"><span data-stu-id="e28d4-140">This method requires the following parameters:</span></span>
  
-  <span data-ttu-id="e28d4-141">**liveIDConnectionUri** &ndash; Eine Zeichenfolge, die den URI des Exchange Online-Servers enthält, die die Anwendung zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="e28d4-141">**liveIDConnectionUri** &ndash; A string that contains the URI of the Exchange Online server that will authenticate the application.</span></span> <span data-ttu-id="e28d4-142">Wenn Exchange Online in Office 365 ausgeführt wird, ist der URI https://outlook.office365.com/PowerShell-LiveID; Andernfalls ist der URI https://\<Servername\>/PowerShell-LiveID.</span><span class="sxs-lookup"><span data-stu-id="e28d4-142">If Exchange Online is running in Office 365, the URI is https://outlook.office365.com/PowerShell-LiveID; otherwise, the URI is https://\<servername\>/PowerShell-LiveID.</span></span> 
    
-  <span data-ttu-id="e28d4-143">**schemaUri** &ndash; Eine Zeichenfolge, die den URI des Schemadokuments enthält, die das Exchange-Verwaltungsshell-Schema definiert.</span><span class="sxs-lookup"><span data-stu-id="e28d4-143">**schemaUri** &ndash; A string that contains the URI of the schema document that defines the Exchange Management Shell schema.</span></span> <span data-ttu-id="e28d4-144">Das Schema-URI ist http://schemas.microsoft.com/powershell/Microsoft.Exchange.</span><span class="sxs-lookup"><span data-stu-id="e28d4-144">The schema URI is http://schemas.microsoft.com/powershell/Microsoft.Exchange.</span></span> 
    
-  <span data-ttu-id="e28d4-145">**Anmeldeinformationen** &ndash; Ein [PSCredential](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx) -Objekt, das die Anmeldeinformationen des Benutzers enthält, die die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e28d4-145">**credentials** &ndash; A [PSCredential](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx) object that contains the credentials of the user who is running the application.</span></span> 
    
-  <span data-ttu-id="e28d4-146">**Count** &ndash; Die Anzahl der Exchange-Postfachbenutzer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e28d4-146">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
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

<span data-ttu-id="e28d4-147"><a name="bk_cert"> </a></span><span class="sxs-lookup"><span data-stu-id="e28d4-147"></span></span>

### <a name="connect-to-a-remote-runspace-by-using-certificate-authentication"></a><span data-ttu-id="e28d4-148">Herstellen einer Verbindung mit einem Remoterunspace mithilfe der Zertifikatauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="e28d4-148">Connect to a remote runspace by using certificate authentication</span></span>

<span data-ttu-id="e28d4-149">Im folgenden Codebeispiel wird definiert die **GetUsersUsingCertificate** -Methode, die ein Exchange-Verwaltungsshell-Runspace auf einem Remoteserver erstellt, mit einem Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="e28d4-149">The following code example defines the **GetUsersUsingCertificate** method, which creates an Exchange Management Shell runspace on a remote server by using a certificate.</span></span> <span data-ttu-id="e28d4-150">Anschließend ruft die Methode die **GetUserInformation** -Methode, wie im Abschnitt [Abrufen einer Liste von Postfachbenutzern aus einer remote-Runspace](#bk_remote), definiert, um eine Liste der Benutzer auf dem Remoteserver zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="e28d4-150">The method then calls the **GetUserInformation** method, as defined in the section [Get a list of mailbox users from a remote runspace](#bk_remote), to return a list of users on the remote server.</span></span>
  
<span data-ttu-id="e28d4-151">This method requires the following parameters:</span><span class="sxs-lookup"><span data-stu-id="e28d4-151">This method requires the following parameters:</span></span>
  
-  <span data-ttu-id="e28d4-152">**Fingerabdruck** &ndash; Eine Zeichenfolge, die den Fingerabdruck des Zertifikats enthält, mit dem die Anwendung zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="e28d4-152">**thumbprint** &ndash; A string that contains the thumbprint of the certificate that is used to authenticate the application.</span></span> 
    
-  <span data-ttu-id="e28d4-153">**certConnectionUri** &ndash; Eine Zeichenfolge, die den URI des Servers enthält, die das Zertifikat authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="e28d4-153">**certConnectionUri** &ndash; A string that contains the URI of the server that will authenticate the certificate.</span></span> <span data-ttu-id="e28d4-154">Der URI wird einer der in der folgenden Tabelle aufgeführten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e28d4-154">The URI will be one of those listed in the following table.</span></span> 
    
    <span data-ttu-id="e28d4-155">**In Tabelle 1. CertConnectionUri URIs**</span><span class="sxs-lookup"><span data-stu-id="e28d4-155">**Table 1. certConnectionUri URIs**</span></span>

    |<span data-ttu-id="e28d4-156">**Server**</span><span class="sxs-lookup"><span data-stu-id="e28d4-156">**Server**</span></span>|<span data-ttu-id="e28d4-157">**URI**</span><span class="sxs-lookup"><span data-stu-id="e28d4-157">**URI**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="e28d4-158">Exchange-Server ohne SSL</span><span class="sxs-lookup"><span data-stu-id="e28d4-158">Exchange server without using SSL</span></span>  <br/> |`http://<servername>/PowerShell`  <br/> |
    |<span data-ttu-id="e28d4-159">Exchange-Server mit SSL</span><span class="sxs-lookup"><span data-stu-id="e28d4-159">Exchange server using SSL</span></span>  <br/> |`https://<servername>/PowerShell`  <br/> |
    |<span data-ttu-id="e28d4-160">Exchange Online als Teil von Office 365</span><span class="sxs-lookup"><span data-stu-id="e28d4-160">Exchange Online as part of Office 365</span></span>  <br/> |`https://outlook.office365.com/PowerShell`  <br/> |
   
- <span data-ttu-id="e28d4-161">**schemaUri** &ndash; Eine Zeichenfolge, die den URI des Schemadokuments enthält, die das Exchange-Verwaltungsshell-Schema definiert.</span><span class="sxs-lookup"><span data-stu-id="e28d4-161">**schemaUri** &ndash; A string that contains the URI of the schema document that defines the Exchange Management Shell schema.</span></span> <span data-ttu-id="e28d4-162">Das Schema-URI ist http://schemas.microsoft.com/powershell/Microsoft.Exchange.</span><span class="sxs-lookup"><span data-stu-id="e28d4-162">The schema URI is http://schemas.microsoft.com/powershell/Microsoft.Exchange.</span></span> 
    
- <span data-ttu-id="e28d4-163">**Count** &ndash; Die Anzahl der Exchange-Postfachbenutzer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e28d4-163">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
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

<span data-ttu-id="e28d4-164"><a name="bk_Kerberos"> </a></span><span class="sxs-lookup"><span data-stu-id="e28d4-164"></span></span>

### <a name="connect-to-a-remote-runspace-on-an-exchange-server-by-using-kerberos-authentication"></a><span data-ttu-id="e28d4-165">Herstellen einer Verbindung mit einem Remoterunspace auf einem Exchange-Server mithilfe der Kerberos-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="e28d4-165">Connect to a remote runspace on an Exchange server by using Kerberos authentication</span></span>

<span data-ttu-id="e28d4-166">Im folgenden Codebeispiel wird definiert die **GetUsersUsingKerberos** -Methode, die ein Exchange-Verwaltungsshell-Runspace auf einem Remoteserver erstellt, mithilfe der Kerberos-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="e28d4-166">The following code example defines the **GetUsersUsingKerberos** method, which creates an Exchange Management Shell runspace on a remote server by using Kerberos authentication.</span></span> <span data-ttu-id="e28d4-167">Anschließend ruft die Methode die **GetUserInformation** -Methode, wie im Abschnitt [Abrufen einer Liste von Postfachbenutzern aus einer remote-Runspace](#bk_remote), definiert, um eine Liste der Benutzer auf dem Remoteserver zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="e28d4-167">The method then calls the **GetUserInformation** method, as defined in the section [Get a list of mailbox users from a remote runspace](#bk_remote), to return a list of users on the remote server.</span></span>
  
<span data-ttu-id="e28d4-168">This method requires the following parameters:</span><span class="sxs-lookup"><span data-stu-id="e28d4-168">This method requires the following parameters:</span></span>
  
- <span data-ttu-id="e28d4-169">**kerberosUri** &ndash; Eine Zeichenfolge, die den URI des Kerberos-Servers enthält, die die Anwendung zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="e28d4-169">**kerberosUri** &ndash; A string that contains the URI of the Kerberos server that will authenticate the application.</span></span> <span data-ttu-id="e28d4-170">Der URI wird einer der in der folgenden Tabelle aufgeführten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e28d4-170">The URI will be one of those listed in the following table.</span></span> 
    
    <span data-ttu-id="e28d4-171">**In Tabelle 2. KerberosUri URIs**</span><span class="sxs-lookup"><span data-stu-id="e28d4-171">**Table 2. kerberosUri URIs**</span></span>

    |<span data-ttu-id="e28d4-172">**Server**</span><span class="sxs-lookup"><span data-stu-id="e28d4-172">**Server**</span></span>|<span data-ttu-id="e28d4-173">**URI**</span><span class="sxs-lookup"><span data-stu-id="e28d4-173">**URI**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="e28d4-174">Exchange-Server ohne SSL</span><span class="sxs-lookup"><span data-stu-id="e28d4-174">Exchange server without using SSL</span></span>  <br/> |`http://<servername>/PowerShell`  <br/> |
    |<span data-ttu-id="e28d4-175">Exchange-Server mit SSL</span><span class="sxs-lookup"><span data-stu-id="e28d4-175">Exchange server using SSL</span></span>  <br/> |`https://<servername>/PowerShell`  <br/> |
   
- <span data-ttu-id="e28d4-176">**schemaUri** &ndash; Eine Zeichenfolge, die den URI des Schemadokuments enthält, die das Exchange-Verwaltungsshell-Schema definiert.</span><span class="sxs-lookup"><span data-stu-id="e28d4-176">**schemaUri** &ndash; A string that contains the URI of the schema document that defines the Exchange Management Shell schema.</span></span> <span data-ttu-id="e28d4-177">Das Schema-URI ist http://schemas.microsoft.com/powershell/Microsoft.Exchange.</span><span class="sxs-lookup"><span data-stu-id="e28d4-177">The schema URI is http://schemas.microsoft.com/powershell/Microsoft.Exchange.</span></span> 
    
- <span data-ttu-id="e28d4-178">**Anmeldeinformationen** &ndash; Ein [PSCredential](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx) -Objekt, das die Anmeldeinformationen des Benutzers enthält, die die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e28d4-178">**credentials** &ndash; A [PSCredential](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx) object that contains the credentials of the user who is running the application.</span></span> 
    
- <span data-ttu-id="e28d4-179">**Count** &ndash; Die Anzahl der Exchange-Postfachbenutzer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e28d4-179">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
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

<span data-ttu-id="e28d4-180"><a name="bk_remote"> </a></span><span class="sxs-lookup"><span data-stu-id="e28d4-180"></span></span>

## <a name="get-a-list-of-mailbox-users-from-a-remote-runspace"></a><span data-ttu-id="e28d4-181">Get a list of mailbox users from a remote runspace</span><span class="sxs-lookup"><span data-stu-id="e28d4-181">Get a list of mailbox users from a remote runspace</span></span>

<span data-ttu-id="e28d4-182">Im folgenden Codebeispiel wird definiert die **GetUserInformation** -Methode, die eine Sammlung von [PSObject](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx) zurückgibt, die Exchange-Postfachbenutzer darstellen.</span><span class="sxs-lookup"><span data-stu-id="e28d4-182">The following code example defines the **GetUserInformation** method, which returns a collection of [PSObject](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx) instances that represent Exchange mailbox users.</span></span> <span data-ttu-id="e28d4-183">Diese Methode wird von den Methoden **GetUsersUsingBasicAuth**, **GetUsersUsingCertificate**und **GetUsersUsingKerberos** , um die Liste der Benutzer aus dem Remoteserver zurückzugeben aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e28d4-183">This method is called by the **GetUsersUsingBasicAuth**, **GetUsersUsingCertificate**, and **GetUsersUsingKerberos** methods to return the list of users from the remote server.</span></span> 
  
<span data-ttu-id="e28d4-184">This method requires the following parameters:</span><span class="sxs-lookup"><span data-stu-id="e28d4-184">This method requires the following parameters:</span></span>
  
- <span data-ttu-id="e28d4-185">**Count** &ndash; Die Anzahl der Exchange-Postfachbenutzer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e28d4-185">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
- <span data-ttu-id="e28d4-186">**Runspace** &ndash; Der remote-Runspace, die für den Exchange-Remoteserver eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="e28d4-186">**runspace** &ndash; The remote runspace that is established for the remote Exchange server.</span></span> 
    
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

<span data-ttu-id="e28d4-187">Die **GetUserInformation** -Methode wird nicht mehr als _Count_ Postfachbenutzer zurück.</span><span class="sxs-lookup"><span data-stu-id="e28d4-187">The **GetUserInformation** method will return no more than  _count_ mailbox users.</span></span> <span data-ttu-id="e28d4-188">Zur Vereinfachung des Codes für die in diesem Beispiel wird die Methode nicht filtern oder anderweitig einschränken, die Postfachbenutzer, die zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e28d4-188">To simplify the code for this example, the method does not filter or otherwise limit the mailbox users that are returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e28d4-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e28d4-189">See also</span></span>

- [<span data-ttu-id="e28d4-190">Erstellen von Exchange-Verwaltungsshell-tools</span><span class="sxs-lookup"><span data-stu-id="e28d4-190">Create Exchange Management Shell tools</span></span>](create-exchange-management-shell-tools.md)   
- [<span data-ttu-id="e28d4-191">Verwenden Sie die Exchange-Verwaltungsshell-Cmdlet-Antwort</span><span class="sxs-lookup"><span data-stu-id="e28d4-191">Use the Exchange Management Shell cmdlet response</span></span>](how-to-use-the-exchange-management-shell-cmdlet-response.md)
    

