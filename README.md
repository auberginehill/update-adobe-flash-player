<!-- Visual Studio Code: For a more comfortable reading experience, use the key combination Ctrl + Shift + V

  _    _           _       _                        _       _          ______ _           _     _____  _
 | |  | |         | |     | |              /\      | |     | |        |  ____| |         | |   |  __ \| |
 | |  | |_ __   __| | __ _| |_ ___ ______ /  \   __| | ___ | |__   ___| |__  | | __ _ ___| |__ | |__) | | __ _ _   _  ___ _ __
 | |  | | '_ \ / _` |/ _` | __/ _ \______/ /\ \ / _` |/ _ \| '_ \ / _ \  __| | |/ _` / __| '_ \|  ___/| |/ _` | | | |/ _ \ '__|
 | |__| | |_) | (_| | (_| | ||  __/     / ____ \ (_| | (_) | |_) |  __/ |    | | (_| \__ \ | | | |    | | (_| | |_| |  __/ |
  \____/| .__/ \__,_|\__,_|\__\___|    /_/    \_\__,_|\___/|_.__/ \___|_|    |_|\__,_|___/_| |_|_|    |_|\__,_|\__, |\___|_|
        | |                                                                                                     __/ |
        |_|                                                                                                    |___/               -->


## Update-AdobeFlashPlayer.ps1

<table>
   <tr>
      <td style="padding:6px"><strong>OS:</strong></td>
      <td style="padding:6px">Windows</td>
   </tr>
   <tr>
      <td style="padding:6px"><strong>Type:</strong></td>
      <td style="padding:6px">A Windows PowerShell script</td>
   </tr>
   <tr>
      <td style="padding:6px"><strong>Language:</strong></td>
      <td style="padding:6px">Windows PowerShell</td>
   </tr>
   <tr>
      <td style="padding:6px"><strong>Description:</strong></td>
      <td style="padding:6px">Update-AdobeFlashPlayer downloads a list of the most recent Flash version numbers against which it compares the Flash version numbers found on the system and displays, weather a Flash update is needed or not. If a working Internet connection is not found, Update-AdobeFlashPlayer will exit at an early stage without displaying any info apart from what is found on the system. The actual update process naturally needs elevated rights, but if, however, all detected Flash Players seem to be up-to-date, Update-AdobeFlashPlayer will exit before checking, weather it is run elevated or not. Thus, if Update-AdobeFlashPlayer is run in a up-to-date machine in a "normal" PowerShell window, Update-AdobeFlashPlayer will just check that everything is OK and leave without further ceremony.
      <br />
      <br />If Update-AdobeFlashPlayer is run without elevated rights (but with a working Internet connection) in a machine with old Flash versions, it will be shown that a Flash update is needed, but Update-AdobeFlashPlayer will exit with a fail before actually downloading any files or making any changes to the system. To perform an update with Update-AdobeFlashPlayer, PowerShell has to be run in an elevated window (run as an administrator).
      <br />
      <br />If Update-AdobeFlashPlayer is run in an elevated PowerShell window and no Flash is detected, the script offers the option to install one specific version of Flash in two steps in the "Admin Corner", where, in contrary to the main autonomous nature of Update-AdobeFlashPlayer, an end-user input is required.
      <br />
      <br />In the update procedure (if old Flash has been found and Update-AdobeFlashPlayer is run with administrative rights) Update-AdobeFlashPlayer downloads the Flash uninstaller from Adobe and (a) full Flash installer(s) for the type(s) of Flash Player(s) from Adobe, which it has deemed to be outdated and after stopping several Flash-related processes uninstalls the outdated Flash version(s) and installs the downloaded Flash Player(s). Adobe Flash Player is configured by creating a backup of the exisiting configuration file (mms.cfg) and overwriting new settings to the configuration file. After the installation a web page in the default browser is opened for verifying that the Flash Player has been installed correctly. The downloaded files are purged from the hard drive after a while. This script is based on Bob Ross' PowerShell script "<a href="http://powershell.com/cs/forums/t/6128.aspx">Automated Adobe Flash Player Maintenance PowerScript for Public Computing Environment</a>".</td>
   </tr>
   <tr>
      <td style="padding:6px"><strong>Homepage:</strong></td>
      <td style="padding:6px"><a href="https://github.com/auberginehill/update-adobe-flash-player">https://github.com/auberginehill/update-adobe-flash-player</a></td>
   </tr>
   <tr>
      <td style="padding:6px"><strong>Version:</strong></td>
      <td style="padding:6px">1.1</td>
   </tr>
   <tr>
        <td style="padding:6px"><strong>Sources:</strong></td>
        <td style="padding:6px">
            <table>
                <tr>
                    <td style="padding:6px">Emojis:</td>
                    <td style="padding:6px"><a href="https://api.github.com/emojis">https://api.github.com/emojis</a></td>
                </tr>
                <tr>
                    <td style="padding:6px">Bob Ross:</td>
                    <td style="padding:6px"><a href="http://powershell.com/cs/forums/t/6128.aspx">Automated Adobe Flash Player Maintenance PowerScript for Public Computing Environment</a></td>
                </tr>
                <tr>
                    <td style="padding:6px">ps1:</td> 
                    <td style="padding:6px"><a href="http://powershell.com/cs/blogs/tips/archive/2011/05/04/test-internet-connection.aspx">Test Internet connection</a></td>
                </tr>
                <tr>
                    <td style="padding:6px">Tobias Weltner:</td> 
                    <td style="padding:6px"><a href="http://powershell.com/cs/PowerTips_Monthly_Volume_8.pdf#IDERA-1702_PS-PowerShellMonthlyTipsVol8-jan2014">PowerTips Monthly vol 8 January 2014</a></td>
                </tr>
                <tr>
                    <td style="padding:6px">alejandro5042:</td> 
                    <td style="padding:6px"><a href="http://stackoverflow.com/questions/29266622/how-to-run-exe-with-without-elevated-privileges-from-powershell?rq=1">How to run exe with/without elevated privileges from PowerShell</a></td>
                </tr>
                <tr>
                    <td style="padding:6px">Raven Hunter:</td> 
                    <td style="padding:6px"><a href="https://community.spiceworks.com/topic/487699-a-little-powershell-help-flash-version-query">A little powershell help, Flash Version Query</a></td>
                </tr>
                <tr>
                    <td style="padding:6px">Kreloc:</td> 
                    <td style="padding:6px"><a href="https://www.reddit.com/r/PowerShell/comments/3tgr2m/get_current_versions_of_adobe_products/">Get current versions of Adobe Products</a></td>
                </tr>
                <tr>
                    <td style="padding:6px">chocolatey:</td> 
                    <td style="padding:6px"><a href="https://chocolatey.org/packages/flashplayerplugin">Flash Player Plugin</a></td>
                </tr>
                <tr>
                    <td style="padding:6px">JaredPar and Matthew Pirocchi:</td> 
                    <td style="padding:6px"><a href="http://stackoverflow.com/questions/5466329/whats-the-best-way-to-determine-the-location-of-the-current-powershell-script?noredirect=1&lq=1">What's the best way to determine the location of the current PowerShell script?</a></td>
                </tr>
                <tr>
                    <td style="padding:6px">lamaar75:</td> 
                    <td style="padding:6px"><a href="http://powershell.com/cs/forums/t/9685.aspx">Creating a Menu</a></td>
                </tr>
            </table>
        </td>
   </tr>
   <tr>
      <td style="padding:6px"><strong>Downloads:</strong></td>
      <td style="padding:6px">For instance <a href="https://raw.githubusercontent.com/auberginehill/update-adobe-flash-player/master/Update-AdobeFlashPlayer.ps1">Update-AdobeFlashPlayer.ps1</a>. Or <a href="https://github.com/auberginehill/update-adobe-flash-player/archive/master.zip">everything as a .zip-file</a>.</td>
   </tr>
</table>




#### Outputs

<table>
    <tr>
        <th>:arrow_right:</th>
        <td style="padding:6px">
            <ul>
                <li>Displays Flash related information in console. Tries to update outdated Adobe Flash Player(s) to its/their latest version(s), if old Flash Player(s) is/are found and if Update-AdobeFlashPlayer is run in an elevated Powershell window. In addition to that, if such an update procedure is initiated... </li>
            </ul>
        </td>
    </tr>
    <tr>
        <th></th>
        <td style="padding:6px">
            <ul>
                <p>
                    <li>the Flash Player configuration file (mms.cfg) is overwritten with new parameters and the following backups are made:</li>
                </p>
                <ol>
                    <p><strong>Configuration file:</strong></p>
                    <p>
                        <table>
                            <tr>
                                <td style="padding:6px"><strong>System</strong></td>
                                <td style="padding:6px"><strong>File</strong></td>
                            </tr>
                            <tr>
                                <td style="padding:6px">32-bit Windows</a></td>
                                <td style="padding:6px"><code>%WINDIR%\System32\Macromed\Flash\mms.cfg</code></td>
                            </tr>
                            <tr>
                                <td style="padding:6px">64-bit Windows</a></td>
                                <td style="padding:6px"><code>%WINDIR%\SysWow64\Macromed\Flash\mms.cfg</code></td>
                            </tr>
                        </table>
                    </p>
                    <p><strong>"Original" file</strong>, which is created when the script tries to update something for the first time:</p>
                    <p>
                        <table>
                            <tr>
                                <td style="padding:6px"><strong>System</strong></td>
                                <td style="padding:6px"><strong>File</strong></td>
                            </tr>
                            <tr>
                                <td style="padding:6px">32-bit Windows</a></td>
                                <td style="padding:6px"><code>%WINDIR%\System32\Macromed\Flash\mms_original.cfg</code></td>
                            </tr>
                            <tr>
                                <td style="padding:6px">64-bit Windows</a></td>
                                <td style="padding:6px"><code>%WINDIR%\SysWow64\Macromed\Flash\mms_original.cfg</code></td>
                            </tr>
                        </table>
                    </p>
                    <p><strong>"Backup" file</strong>, which is created when the script tries to update something for the second time and which gets overwritten in each successive update cycle:</p>
                    <p>
                        <table>
                            <tr>
                                <td style="padding:6px"><strong>System</strong></td>
                                <td style="padding:6px"><strong>File</strong></td>
                            </tr>
                            <tr>
                                <td style="padding:6px">32-bit Windows</a></td>
                                <td style="padding:6px"><code>%WINDIR%\System32\Macromed\Flash\mms_backup.cfg</code></td>
                            </tr>
                            <tr>
                                <td style="padding:6px">64-bit Windows</a></td>
                                <td style="padding:6px"><code>%WINDIR%\SysWow64\Macromed\Flash\mms_backup.cfg</code></td>
                            </tr>
                        </table>
                    </p>
                    <p>The <code>%WINDIR%</code> location represents the Windows system directory, such as <code>C:\Windows</code> and may be displayed in PowerShell with the <code>$env:windir</code> variable.</p>
                </ol>
                <p>
                    <li>To see the actual values that are being written, please see the Step 6 in the <a href="https://raw.githubusercontent.com/auberginehill/update-adobe-flash-player/master/Update-AdobeFlashPlayer.ps1">script</a> itself, where the original settings are overwritten with the following values:</li>
                </p>
                <ol>
                    <p>
                        <table>
                            <tr>
                                <td style="padding:6px"><strong>Value</strong></td>
                                <td style="padding:6px"><strong>Description</strong></td>
                            </tr>
                            <tr>
                                <td style="padding:6px"><code>AssetCacheSize = 0</code></td>
                                <td style="padding:6px">Disables storing the common Flash components</a></td>
                            </tr>
                            <tr>
                                <td style="padding:6px"><code>AutoUpdateDisable = 1</code></td>
                                <td style="padding:6px">Disables the Automatic Flash Update</a></td>
                            </tr>
                            <tr>
                                <td style="padding:6px"><code>LegacyDomainMatching = 0</code></td>
                                <td style="padding:6px">Denies Flash Player 6 and earlier superdomain rules</a></td>
                            </tr>
                            <tr>
                                <td style="padding:6px"><code>LocalFileLegacyAction = 0</code></td>
                                <td style="padding:6px">Denies Flash Player 7 and earlier local-trusted sandbox</a></td>
                            </tr>
                            <tr>
                                <td style="padding:6px"><code>LocalStorageLimit = 1</code></td>
                                <td style="padding:6px">Disables persistent shared objects</a></td>
                            </tr>
                            <tr>
                                <td style="padding:6px"><code>SilentAutoUpdateEnable = 0</code></td>
                                <td style="padding:6px">Disables background updates</a></td>
                            </tr>
                            <tr>
                                <td style="padding:6px"><code>ThirdPartyStorage = 0</code></td>
                                <td style="padding:6px">Denies third-party locally persistent shared objects</a></td>
                            </tr>
                        </table>
                        <p>Most of the settings above may render some web pages broken.</p>
                    </p>
                    <p>For a comprehensive list of available settings and a more detailed description of the values above, please see the <a href="http://www.adobe.com/devnet/flashplayer/articles/flash_player_admin_guide.html">Adobe Flash Player Administration Guide</a>.</p>
                </ol>
                <p>
                    <li>To open these file locations in a Resource Manager Window, for instance a command
                        <br />
                        <br /><code>Invoke-Item $env:windir\System32\Macromed\Flash\</code>
                        <br />
                        <br />or
                        <br />
                        <br /><code>Invoke-Item $env:windir\SysWOW64\Macromed\Flash\</code>
                        <br />
                        <br />may be used at the PowerShell prompt window <code>[PS>]</code>.
                    </li>
                </p>
            </ul>
        </td>
    </tr>
</table>




#### Notes

<table>
    <tr>
        <th>:warning:</th>
        <td style="padding:6px">
            <ul>
                <li>Requires a working Internet connection for downloading a list of the most recent Flash version numbers.</li>
            </ul>
        </td>
    </tr>
    <tr>
        <th></th>
        <td style="padding:6px">
            <ul>
                <p>
                    <li>Also requires a working Internet connection for downloading a Flash uninstaller and a complete Flash installer(s) from Adobe (but this procedure is not initiated, if the system is deemed up-to-date).</li>
                </p>


                <p>
                    <li>For performing any actual updates with Update-AdobeFlashPlayer, it's mandatory to run this script in an elevated PowerShell window (where PowerShell has been started with the "run as an administrator" option). The elevated rights are needed for uninstalling Flash, installing Flash and for writing the mms.cfg file.</li>
                </p>
                <p>
                    <li>Please also notice that during the actual update phase Update-AdobeFlashPlayer closes a bunch of processes without any further notice in Step 3 and in Step 6 Update-AdobeFlashPlayer alters the Flash configuration file (mms.cfg) so, that for instance, the automatic Flash updates are turned off.</li>
                </p>
                <p>
                    <li>The Flash Player ActiveX control on Windows 8.1 and above is a component of Internet Explorer and Edge and is updated via Windows Update. By using the Flash Player ActiveX installer, Flash Player ActiveX control cannot be installed on Windows 8.1 and above systems. Also, the Flash Player uninstaller doesn't uninstall the ActiveX control on Windows 8.1 and above systems.</li>
                </p>
                <p>
                    <li>Please note that when run in an elevated PowerShell window and old Flash Player(s) is/are detected, Update-AdobeFlashPlayer will automatically try to download files from the Internet without prompting the end-user beforehand or without asking any confirmations (in Step 1 and Step 2).</li>
                </p>
                <p>
                    <li>Please note that the downloaded files are temporarily placed in a directory, which is specified with the <code>$path</code> variable (at line 41).</li>
                </p>
                <p>
                    <li>The <code>$env:temp</code> variable points to the current temp folder. The default value of the <code>$env:temp</code> variable is <code>C:\Users\&lt;username&gt;\AppData\Local\Temp</code> (i.e. each user account has their own separate temp folder at path <code>%USERPROFILE%\AppData\Local\Temp</code>). To see the current temp path, for instance a command
                    <br />
                    <br /><code>[System.IO.Path]::GetTempPath()</code>
                    <br />
                    <br />may be used at the PowerShell prompt window <code>[PS>]</code>. To change the temp folder for instance to <code>C:\Temp</code>, please, for example, follow the instructions at <a href="http://www.eightforums.com/tutorials/23500-temporary-files-folder-change-location-windows.html">Temporary Files Folder - Change Location in Windows</a>, which in essence are something along the lines:
                        <ol>
                           <li>Right click on Computer and click on Properties (Or select Start → Control Panel → System). In the resulting window with the basic information about the computer...</li>
                           <li>Click on Advanced system settings on the left panel and select Advanced tab on the resulting pop-up window.</li>
                           <li>Click on the button near the bottom labeled Environment Variables.</li>
                           <li>In the topmost section labeled User variables both TMP and TEMP may be seen listed. Each different login account is assigned its own temporary locations. These values can be changed by double clicking a value or by highlighting a value and selecting Edit. The specified path will be used by Windows and many other programs for temporary files. It's advisable to set the same value (a directory path) for both TMP and TEMP.</li>
                           <li>Any running programs need to be restarted for the new values to take effect. In fact, probably also Windows itself needs to be restarted for it to begin using the new values for its own temporary files.</li>
                        </ol>
                    </li>
                </p>
            </ul>
        </td>
    </tr>
</table>




#### Examples

<table>
    <tr>
        <th>:book:</th>
        <td style="padding:6px">To open this code in Windows PowerShell, for instance:</td>
   </tr>
   <tr>
        <th></th>
        <td style="padding:6px">
            <ol>
                <p>
                    <li><code>./Update-AdobeFlashPlayer</code><br />
                    Run the script. Please notice to insert <code>./</code> or <code>.\</code> before the script name.</li>
                </p>
                <p>
                    <li><code>help ./Update-AdobeFlashPlayer -Full</code><br />
                    Display the help file.</li>
                </p>
                <p>
                    <li><p><code>Set-ExecutionPolicy remotesigned</code><br />
                    This command is altering the Windows PowerShell rights to enable script execution. Windows PowerShell has to be run with elevated rights (run as an administrator) to actually be able to change the script execution properties. The default value is "<code>Set-ExecutionPolicy restricted</code>".</p>
                        <p>Parameters:
                                <ol>
                                    <table>
                                        <tr>
                                            <td style="padding:6px"><code>Restricted</code></td>
                                            <td style="padding:6px">Does not load configuration files or run scripts. Restricted is the default execution policy.</td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>AllSigned</code></td>
                                            <td style="padding:6px">Requires that all scripts and configuration files be signed by a trusted publisher, including scripts that you write on the local computer.</td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>RemoteSigned</code></td>
                                            <td style="padding:6px">Requires that all scripts and configuration files downloaded from the Internet be signed by a trusted publisher.</td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>Unrestricted</code></td>
                                            <td style="padding:6px">Loads all configuration files and runs all scripts. If you run an unsigned script that was downloaded from the Internet, you are prompted for permission before it runs.</td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>Bypass</code></td>
                                            <td style="padding:6px">Nothing is blocked and there are no warnings or prompts.</td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>Undefined</code></td>
                                            <td style="padding:6px">Removes the currently assigned execution policy from the current scope. This parameter will not remove an execution policy that is set in a Group Policy scope.</td>
                                        </tr>
                                    </table>
                                </ol>
                        </p>
                    <p>For more information, type "<code>help Set-ExecutionPolicy -Full</code>" or visit <a href="https://technet.microsoft.com/en-us/library/hh849812.aspx">Set-ExecutionPolicy</a>.</p>
                    </li>
                </p>
                <p>
                    <li><code>New-Item -ItemType File -Path C:\Temp\Update-AdobeFlashPlayer.ps1</code><br />
                    Creates an empty ps1-file to the <code>C:\Temp</code> directory. The <code>New-Item</code> cmdlet has an inherent <code>-NoClobber</code> mode built into it, so that the procedure will halt, if overwriting (replacing the contents) of an existing file is about to happen. Overwriting a file with the <code>New-Item</code> cmdlet requires using the <code>Force</code>.<br />
                    For more information, please type "<code>help New-Item -Full</code>".</li>
                </p>
            </ol>
        </td>
    </tr>
</table>




#### Contributing

<p>Find a bug? Have a feature request? Here is how you can contribute to this project:</p>

 <table>
   <tr>
      <th><img class="emoji" title="contributing" alt="contributing" height="28" width="28" align="absmiddle" src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f33f.png"></th>
      <td style="padding:6px"><strong>Bugs:</strong></td>
      <td style="padding:6px"><a href="https://github.com/auberginehill/update-adobe-flash-player/issues">Submit bugs</a> and help us verify fixes.</td>
   </tr>
   <tr>
      <th rowspan="2"></th>
      <td style="padding:6px"><strong>Feature Requests:</strong></td>
      <td style="padding:6px">Feature request can be submitted by <a href="https://github.com/auberginehill/update-adobe-flash-player/issues">creating an Issue</a>.</td>
   </tr>
   <tr>
      <td style="padding:6px"><strong>Edit Source Files:</strong></td>
      <td style="padding:6px"><a href="https://github.com/auberginehill/update-adobe-flash-player/pulls">Submit pull requests</a> for bug fixes and features and discuss existing proposals.</td>
   </tr>
 </table>




#### www

<table>
    <tr>
        <th><img class="emoji" title="www" alt="www" height="28" width="28" align="absmiddle" src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f310.png"></th>
        <td style="padding:6px"><a href="https://github.com/auberginehill/update-adobe-flash-player">Script Homepage</a></td>
    </tr>
    <tr>
        <th rowspan="12"></th>
        <td style="padding:6px">Bob Ross: <a href="http://powershell.com/cs/forums/t/6128.aspx">Automated Adobe Flash Player Maintenance PowerScript for Public Computing Environment</a></td>
    </tr>
    <tr>
        <td style="padding:6px">ps1: <a href="http://powershell.com/cs/blogs/tips/archive/2011/05/04/test-internet-connection.aspx">Test Internet connection</a></td>
    </tr>
    <tr>
        <td style="padding:6px">Tobias Weltner: <a href="http://powershell.com/cs/PowerTips_Monthly_Volume_8.pdf#IDERA-1702_PS-PowerShellMonthlyTipsVol8-jan2014">PowerTips Monthly vol 8 January 2014</a></td>
    </tr>
    <tr>
        <td style="padding:6px">alejandro5042: <a href="http://stackoverflow.com/questions/29266622/how-to-run-exe-with-without-elevated-privileges-from-powershell?rq=1">How to run exe with/without elevated privileges from PowerShell</a></td>
    </tr>
    <tr>
        <td style="padding:6px">Raven Hunter: <a href="https://community.spiceworks.com/topic/487699-a-little-powershell-help-flash-version-query">A little powershell help, Flash Version Query</a></td>
    </tr>
    <tr>
        <td style="padding:6px">Kreloc: <a href="https://www.reddit.com/r/PowerShell/comments/3tgr2m/get_current_versions_of_adobe_products/">Get current versions of Adobe Products</a></td>
    </tr>
    <tr>
        <td style="padding:6px">chocolatey: <a href="https://chocolatey.org/packages/flashplayerplugin">Flash Player Plugin</a></td>
    </tr>
    <tr>
        <td style="padding:6px">JaredPar and Matthew Pirocchi: <a href="http://stackoverflow.com/questions/5466329/whats-the-best-way-to-determine-the-location-of-the-current-powershell-script?noredirect=1&lq=1">What's the best way to determine the location of the current PowerShell script?</a></td>
    </tr>
    <tr>
        <td style="padding:6px">lamaar75: <a href="http://powershell.com/cs/forums/t/9685.aspx">Creating a Menu</a></td>
    </tr>
    <tr>
        <td style="padding:6px"><a href="https://www.credera.com/blog/technology-insights/perfect-progress-bars-for-powershell/">Perfect Progress Bars for PowerShell</a></td>
    </tr>    
    <tr>
        <td style="padding:6px"><a href="https://technet.microsoft.com/en-us/library/ff730939.aspx">Adding a Simple Menu to a Windows PowerShell Script</a></td>
    </tr>
    <tr>
        <td style="padding:6px"><a href="https://msdn.microsoft.com/en-us/library/aa393941(v=vs.85).aspx">Uninstall method of the Win32_Product class</a></td>
    </tr> 
    <tr>
        <td style="padding:6px">ASCII Art: <a href="http://www.figlet.org/">http://www.figlet.org/</a> and <a href="http://www.network-science.de/ascii/">ASCII Art Text Generator</a></td>
    </tr>
</table>




#### Related scripts

 <table>
    <tr>
        <th><img class="emoji" title="www" alt="www" height="28" width="28" align="absmiddle" src="https://assets-cdn.github.com/images/icons/emoji/unicode/0023-20e3.png"></th>
        <td style="padding:6px"><a href="https://github.com/auberginehill/get-battery-info">Get-BatteryInfo</a></td>
    </tr>
    <tr>
        <th rowspan="6"></th>
        <td style="padding:6px"><a href="https://github.com/auberginehill/get-computer-info">Get-ComputerInfo</a></td>
    </tr>
    <tr>
        <td style="padding:6px"><a href="https://github.com/auberginehill/get-installed-windows-updates">Get-InstalledWindowsUpdates</a></td>
    </tr>
    <tr>
        <td style="padding:6px"><a href="https://github.com/auberginehill/get-ram-info">Get-RAMInfo</a></td>
    </tr>
    <tr>
        <td style="padding:6px"><a href="https://gist.github.com/auberginehill/eb07d0c781c09ea868123bf519374ee8">Get-TimeDifference</a></td>
    </tr>
    <tr>
        <td style="padding:6px"><a href="https://github.com/auberginehill/get-unused-drive-letters">Get-UnusedDriveLetters</a></td>
    </tr>
    <tr>
        <td style="padding:6px"></td>
    </tr>
</table>
