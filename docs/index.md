# Citrix Provisioning 1906 PowerShell with Objects Programmer’s Guide

<p>Use Provisioning programming interfaces to manage your implementation from a command line or from scripts. Only users with correct administrative privileges can use programming commands.Non-administrators, that do not have elevated privileges and attempt to use these commands, will receive the ‘Invalid access’ message.</p>

<p>Four different programming interfaces exist:</p>

- Management Command Line Interface (MCLI) 
- Simple Object Access Protocol (SOAP) Server Programmer Interface  
- PowerShell Programmer Interface with Objects 
- PowerShell Programmer Interface (Deprecated) 

<p>This document provides the information needed to use this interface.</p>

## Using the PowerShell Programmer Interface withObjects<a name="_Toc464196015"></a>

<p>Use the information that follows to manage a ProvisioningService’s implementation from the PowerShell Interface with Objects.</p>

#Installation of PowerShell Snap-In<a name="_Toc464196016"></a>

<p>The PowerShell snap-in (Citrix.PVS.SnapIn.dll) can be installed using the Provisioning Server Console install.</p>

##Registration of McliPSSnapIn.dll usingImport-Module<a name="_Toc464196017"></a>

<p>If the snap-in later needs to be registered in PowerShell,this can be manually done by running one of the following command inPowerShell. The path where the Citrix.PVS.SnapIn.dll is installed needs to be used.</p>

<p>Import-Module “path\Citrix.PVS.SnapIn.dll”</p>

##Registration of Citrix.PVS.SnapIn.dll usingAdd-PSSnapin<a name="_Toc464196018"></a>

<p>If the snap-in later needs to be registered in PowerShell,this can be manually done by running one of the following commands at the DOS command prompt. After the command is run and PowerShell is started, the snap-in needs to be added using the command “Add-PSSnapin -Name Citrix.PVS.SnapIn”.</p>

###64-bit Registration<a name="_Toc464196019"></a>

<p><span style="font-size:10.0pt;font-family:"Courier New"">%systemroot%\Microsoft.NET\Framework64\v4.0.30319\installutil.exeCitrix.PVS.SnapIn.dll</span></p>

###32-bit Registration<a name="_Toc464196020"></a>

<p><span style="font-size:10.0pt;font-family:"Courier New"">%systemroot%\Microsoft.NET\Framework\v4.0.30319\installutil.exeCitrix.PVS.SnapIn.dll</span></p>

##Alternative Registration of Citrix.PVS.SnapIn.dllin PowerShell<a name="_Toc464196021"></a>

<p>Another way to register is by running one of the following commands at the PowerShell command prompt:</p>

###64-bit Registration in PowerShell<a name="_Toc464196022"></a>

<p><span style="font-size:10.0pt;font-family:"Courier New"">$installutil= $env:systemroot + '\Microsoft.NET\Framework64\v4.0.30319\installutil.exe'</span></p>

<p><span style="font-size:10.0pt;font-family:"Courier New"">;$installutilCitrix.PVS.SnapIn.dll</span></p>

<p><span style="font-size:10.0pt;font-family:"Courier New"">Add-PSSnapin-Name Citrix.PVS.SnapIn</span></p>

###32-bit Registration in PowerShell<a name="_Toc464196023"></a>

<p><span style="font-size:10.0pt;font-family:"Courier New"">$installutil= $env:systemroot + '\Microsoft.NET\Framework32\v4.0.30319\installutil.exe'</span></p>

<p><span style="font-size:10.0pt;font-family:"Courier New"">;$installutilCitrix.PVS.SnapIn.dll</span></p>

<p><span style="font-size:10.0pt;font-family:"Courier New"">Add-PSSnapin-Name Citrix.PVS.SnapIn</span></p>

#Uninstall of PowerShell Snap-In<a name="_Toc464196024"></a>

<p>The PowerShell snap-in (Citrix.PVS.SnapIn.dll) can beuninstalled using the Provisioning Server Console install.</p>

##Unregister of Citrix.PVS.SnapIn.dll<a name="_Toc464196025"></a>

<p>The snap-in needs to be unregistered from PowerShell, thiscan be manually done by running one of the following commands at the DOScommand prompt:</p>

###64-bit Unregister<a name="_Toc464196026"></a>

<p>%systemroot%\Microsoft.NET\Framework64\v4.0.30319\installutil.exe-u Citrix.PVS.SnapIn.dll</p>

###32-bit Unregister<a name="_Toc464196027"></a>

<p>%systemroot%\Microsoft.NET\Framework\v4.0.30319\installutil.exe-u Citrix.PVS.SnapIn.dll</p>

##Alternative Unregister of Citrix.PVS.SnapIn.dll inPowerShell<a name="_Toc464196028"></a>

<p>Another way to unregister is by running one of the followingcommands at the PowerShell command prompt:</p>

###64-bit Unregister in PowerShell<a name="_Toc464196029"></a>

<p><span style="font-size:10.0pt;font-family:"Courier New"">$installutil= $env:systemroot + '\Microsoft.NET\Framework64\v4.0.30319\installutil.exe'</span></p>

<p><span style="font-size:10.0pt;font-family:"Courier New"">;$installutil-u Citrix.PVS.SnapIn.dll</span></p>

###32-bit Unregister in PowerShell<a name="_Toc464196030"></a>

<p><span style="font-size:10.0pt;font-family:"Courier New"">$installutil= $env:systemroot + '\Microsoft.NET\Framework32\v4.0.30319\installutil.exe'</span></p>

<p><span style="font-size:10.0pt;font-family:"Courier New"">;$installutil-u Citrix.PVS.SnapIn.dll</span></p>

#Setup of the SOAP Server Communication<a name="_Toc464196031"></a>

<p>Unless the defaults are fine, use this command to set thevalues for the SOAP Server connection:</p>

##Set-PvsConnection<a name="_Toc464196032"></a>

<p style="margin-left:.4in;text-indent:-.2in"><span style="font-size:10.0pt;font-family:"Courier New"">Set the SoapServer connection, and if -Persist isspecified the connection settings are saved in the registry. A PvsConnectionobject can be used as the parameter.</span></p>

<p style="margin-left:.7in;text-indent:-.2in"><span style="font-size:10.0pt;font-family:"Courier New"">Required</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">PvsConnection Connection: PvsConnection object withchanged property value(s) to be set. The object can come from a pileline.</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">These values are in the PvsConnection object, andonly will be set if the value has changed.</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">string Name or Server: Name or IP of the Server toconnect to. Default=localhost</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">string Port: The Port to use to connect.Default=54321</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">string User: User name to use for Authentication. Ifit has a value, it will be *****. Default=""</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">string Domain: Domain name to use forAuthentication. If it has a value, it will be *****. Default=""</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">string Password: Password to use for Authentication.If it has a value, it will be *****. Default=""</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">string Persist: True when the connection settingsshould be, for Set, or have been, for Get, saved to the registry.</span></p>

<p style="margin-left:.7in;text-indent:-.2in"><span style="font-size:10.0pt;font-family:"Courier New"">PvsConnection can be created or modified usingmethods below:</span></p>

<p style="margin-left:.8in;text-indent:-.2in"><span style="font-size:10.0pt;font-family:"Courier New"">New-Object Citrix.PVS.SnapIn.PvsConnection: Createsdefault Server=localhost, Port=54321, and no authentication.</span></p>

<p style="margin-left:.8in;text-indent:-.2in"><span style="font-size:10.0pt;font-family:"Courier New"">New-ObjectCitrix.PVS.SnapIn.PvsConnection(Citrix.PVS.SnapIn copyFrom): Creates withsettings of the copyFrom Citrix.PVS.SnapIn.</span></p>

<p style="margin-left:.8in;text-indent:-.2in"><span style="font-size:10.0pt;font-family:"Courier New"">SetServerToLocalHostDefaultSettings:Server=localhost, Port=54321, and no authentication.</span></p>

<p style="margin-left:.8in;text-indent:-.2in"><span style="font-size:10.0pt;font-family:"Courier New"">Copy(Citrix.PVS.SnapIn copyFrom): Modifies thesettings to match the copyFrom Citrix.PVS.SnapIn.</span></p>

<p style="margin-left:.8in;text-indent:-.2in"><span style="font-size:10.0pt;font-family:"Courier New"">Equals(Citrix.PVS.SnapIn compareTo): Returns truewhen the settings match what is in the compareTo.</span></p>

<p></p>

<p style="margin-left:.7in;text-indent:-.2in"><span style="font-size:10.0pt;font-family:"Courier New"">When Connection is not passed, the parameters beloware used:</span></p>

<p style="margin-left:.7in;text-indent:-.2in"><span style="font-size:10.0pt;font-family:"Courier New"">Optional field values to set:</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">string Name or Server: Name or IP of the Server toconnect to. Default=localhost</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">string Port: The Port to use to connect.Default=54321</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">string User: User name to use for Authentication. Ifit has a value, it will be *****. Default=""</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">string Domain: Domain name to use forAuthentication. If it has a value, it will be *****. Default=""</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">string Password: Password to use for Authentication.If it has a value, it will be *****. Default=""</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">string Persist: True when the connection settingsshould be, for Set, or have been, for Get, saved to the registry.</span></p>

<p></p>

<p style="margin-left:.7in;text-indent:-.2in"><span style="font-size:10.0pt;font-family:"Courier New"">Optional</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">SwitchParameter PassThru: If -PassThru is specified,the resulting PvsConnection object is returned.</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">SwitchParameter Confirm: The impact of thisoperation is "low". If -Confirm is specified, the operation will beconfirmed. $ConfirmPreference can be set to "low" to haveconfirmation without the Confirm parameter.</span></p>

####EXAMPLE 1: Set PvsConnection for Individual Fields

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">Get the PvsConnection into a $o variable. Change the$o field values and then Set the PvsConnection with the result.</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">$o = Get-PvsConnection -Fields Port</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">$o.Port = 54322</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">Set-PvsConnection $o</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">The -Fields parameter with only the needed fieldsspecified makes the Get work faster because only those fields are retrieved.</span></p>

####EXAMPLE 2: Set PvsConnection for a Field Using Pipe

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">Get the PvsConnection into a $o variable for thefield that has the wrong value. Change the $o field to the correct value and thenSet the PvsConnection with the result.</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">Get-PvsConnection -Fields Port | Where-Object{$_.Port -ne 54322} | foreach { $o = $_; $o.Port = 54322; $o } |Set-PvsConnection</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">The -Fields parameter with only the needed fieldsspecified makes the Get work faster because only those fields are retrieved.</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">The "foreach { $o = $_; $o.X = Y; $o }"sets the field X to value Y and returns the object again so it can be piped tothe Set command for update.</span></p>

####EXAMPLE 3: Set PvsConnection Port with Parameter

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">Set the PvsConnection Port using the Port parameterinstead of a PvsConnection object.</span></p>

<p style="margin-left:2.0in;text-indent:-1.4in"><span style="font-size:10.0pt;font-family:"Courier New"">Set-PvsConnection -Port 54322</span></p>

<p style="margin-left:2.8in;text-indent:-2.2in"><span style="font-size:10.0pt;font-family:"Courier New"">This is the only Set command that has fieldparameters.</span></p>

#Command Specific Help<a name="_Toc464196033"></a>

<p>All of the documentation for specific commands is includedin the command-line help by calling Get-Help and the name of the command, forexample “Get-Help Get-PvsDevice”. The documentation for the specific commandincludes information about the object that is may get or set. The documentationof all of the objects is included in the “Objects, in the Citrix.PVS.SnapInNamespace” section.</p>

#Error Handling<a name="_Toc464196034"></a>

<p>For the Citrix.PVS.SnapIn, if an error occurs, aPvsException will be in the Exception member of the $error. The “Error codes”information is included in this document.</p>

<p>The members of a PvsException are:</p>

<p style="margin-left:99.0pt;text-indent:-85.5pt">InnerException:The exception that occured. This exception maybe an EAException or otherstandard Exception.</p>

<p style="margin-left:99.0pt;text-indent:-85.5pt">ToString():Has the formatted full Message of the InnerException.</p>

<p style="margin-left:99.0pt;text-indent:-85.5pt">If theInnerException GetType().Name equals "EAException", then The membersof it are:</p>

<p style="margin-left:99.0pt;text-indent:-85.5pt"> returnCode: The number, as shown below in the Error codes. The name of theerror, for example "NotImplemented", is not included in theEAException.</p>

<p style="margin-left:99.0pt;text-indent:-85.5pt"> Message: The message, as shown below in the Error codes. The [v1], [v2], [v3],[v4], and [v5] will be replaced with values as required.</p>

<p style="margin-left:99.0pt;text-indent:-85.5pt"> Details: Has the Details for the EAException if there are any. OtherException,ManagementInterfaceError and PvsStatusException will have Details.</p>

<p style="margin-left:99.0pt;text-indent:-85.5pt"> ToString(): Has the Message as shown below in the Error codes. If there isDetails, it will be returned or included, and if partialReturn, they will beincluded.</p>

<p style="margin-left:99.0pt;text-indent:-85.5pt"> partialReturn: Might have a list of EAException objects if any of the itemsprocessed during the command had any issues.</p>

<p style="margin-left:99.0pt;text-indent:-85.5pt"> Severity: Can have the values Critical, Error, Warning or Duplicate.</p>

<p style="margin-left:99.0pt;text-indent:-85.5pt"> Source: Has the value that is displayed in the Console as a Title or Type forthe error.</p>

<p style="margin-left:99.0pt;text-indent:-85.5pt"></p>

