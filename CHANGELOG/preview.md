# Current preview release

## [7.1.0-preview.5] - 2020-07-06

### Engine Updates and Fixes

- Ensure assemblies listed in the module manifest `FileList` field are not loaded (#12968)

### Code Cleanup

<details>

<summary>

<p>We thank the following contributors!</p>
<p>@xtqqczze</p>

</summary>

<ul>
<li>Code performance fixes (#12956) (Thanks @xtqqczze!)</li>
</ul>

</details>

### Tools

- Add missing `.editorconfig` settings present in `dotnet/runtime` (#12871) (Thanks @xtqqczze!)

### Tests

- Add new test for `Format-Custom` to avoid data loss (#11393) (Thanks @iSazonov!)

### Build and Packaging Improvements

<details>
<summary>

<p>Fixed upgrade code in MSI package.</p>

</summary>
<ul>
<li>Change log for v7.1.0-preview.5 (Internal 11880)</li>
<li>Fix Path for the Preview MSI (#13070)</li>
<li>Correct stable and preview upgrade codes for <code>MSI</code> (#13036)</li>
<li>Changelog for `v7.1.0-preview.4` (Internal 11841)</li>
<li>Fix NuGet package compliance issues (#13045)</li>
<li>Bump <code>xunit.runner.visualstudio</code> from <code>2.4.1</code> to<code> 2.4.2</code> (#12874)</li>
<li>Bump NJsonSchema from `10.1.21` to `10.1.23` (#13032) (#13022)</li>
</ul>

</details>

### Documentation and Help Content

- Fix links for MSI packages to point to `7.1.0-preview.3` (#13056)
- Add update `packages.microsoft.com` step to distribution request template. (#13008)
- Update `windows-core.md` (#13053) (Thanks @xtqqczze!)
- Add `@rjmholt` to maintainers list (#13033)
- Update docs for `v7.1.0-preview.4` release (#13028)

## [7.1.0-preview.4] - 2020-06-25

### Breaking Changes

- Make the switch parameter `-Qualifier` not positional for `Split-Path` (#12960) (Thanks @yecril71pl!)
- Resolve the working directory as literal path for `Start-Process` when it's not specified (#11946) (Thanks @NoMoreFood!)
- Make `-OutFile` parameter in web cmdlets to work like `-LiteralPath` (#11701) (Thanks @iSazonov!)

### Engine Updates and Fixes

- Ensure null-coalescing LHS is evaluated only once (#12667)
- Fix path handling bug in `PSTask` (#12554) (Thanks @IISResetMe!)
- Remove extra line before formatting group (#12163) (Thanks @iSazonov!)
- Make module formatting not generate error with strict mode (#11943)
- Adding more ETW logs to WSMan plugin (#12798) (Thanks @krishnayalavarthi!)
- Restrict loading of `amsi.dll` to `system32` folder (#12730)

### General Cmdlet Updates and Fixes

- Fix `NullReferenceException` in `CommandSearcher.GetNextCmdlet` (#12659) (Thanks @powercode!)
- Prevent `NullReferenceException` in Unix computer cmdlets with test hooks active (#12651) (Thanks @vexx32!)
- Fix issue in `Select-Object` where `Hashtable` members (e.g. `Keys`) cannot be used with `-Property` or `-ExpandProperty` (#11097) (Thanks @vexx32!)
- Fix conflicting shorthand switch `-w` for pwsh (#12945)
- Rename the `CimCmdlet` resource file (#12955) (Thanks @iSazonov!)
- Remove use of `Test-Path` in `ConciseView` (#12778)
- Flag `default` switch statement condition clause as keyword (#10487) (Thanks @msftrncs!)
- Add parameter `SchemaFile` to `Test-Json` cmdlet (#11934) (Thanks @beatcracker!)
- Bring back Certificate provider parameters (#10622) (Thanks @iSazonov!)
- Fix `New-Item` to create symbolic link to relative path target (#12797) (Thanks @iSazonov!)
- Add `CommandLine` property to Process (#12288) (Thanks @iSazonov!)
- Adds `-MaskInput` parameter to `Read-Host` (#10908) (Thanks @davinci26!)
- Change `CimCmdlets` to use `AliasAttribute` (#12617) (Thanks @thlac!)

### Code Cleanup

<details>

<summary>

<p>We thank the following contributors!</p>
<p>@xtqqczze, @sethvs, @romero126, @kvprasoon, @powercode</p>

</summary>

<ul>
<li>Use <code>nameof</code> operator (#12716) (Thanks @xtqqczze!)</li>
<li>Fix comments in Mshexpression.cs (#12711) (Thanks @sethvs!)</li>
<li>Formatting: remove duplicate semicolons (#12666) (Thanks @xtqqczze!)</li>
<li>Replace <code>SortedList</code> with <code>Generic.SortedList&lt;TKey,TValue&gt;</code> (#12954) (Thanks @xtqqczze!)</li>
<li>Use HashSet instead of Hashtable with null values (#12958) (Thanks @xtqqczze!)</li>
<li>Rename <code>CopyItem.Tests.ps1</code> to <code>Copy-Item.Tests.ps1</code> to match other tests (#10701) (Thanks @romero126!)</li>
<li>Fix <code>RCS1114: Remove redundant delegate creation</code> (#12917) (Thanks @xtqqczze!)</li>
<li>Code redundancy fixes (#12916) (Thanks @xtqqczze!)</li>
<li>Update the PowerShell modules to use the new Help URI (#12686)</li>
<li>Reorder modifiers according to preferred order (#12864) (Thanks @xtqqczze!)</li>
<li>Expand numberOfPowershellRefAssemblies list capacity (#12840) (Thanks @xtqqczze!)</li>
<li>Add readonly modifier to internal static members (#11777) (Thanks @xtqqczze!)</li>
<li>cleanup: Use coalesce expression (#12829) (Thanks @xtqqczze!)</li>
<li>Add missing assessibility modifiers (#12820) (Thanks @xtqqczze!)</li>
<li>Use <code>t_</code> naming convention for ThreadStatic members (#12826) (Thanks @xtqqczze!)</li>
<li>Formatting: Add empty line between declarations (#12824) (Thanks @xtqqczze!)</li>
<li>Clarify defaultRefAssemblies list capacity in AddType.cs (#12520) (Thanks @xtqqczze!)</li>
<li>Fixing &quot;Double &quot;period&quot; (..) in message for System.InvalidOperationException&quot; (#12758) (Thanks @kvprasoon!)</li>
<li>Rethrow to preserve stack details for better maintainability (#12723) (Thanks @xtqqczze!)</li>
<li>Delete license.rtf (#12738) (Thanks @xtqqczze!)</li>
<li>Nullable annotations for CommandSearcher (#12733) (Thanks @powercode!)</li>
<li>Redundancy: Remove 'partial' modifier from type with a single part (#12725) (Thanks @xtqqczze!)</li>
<li>Remove phrase 'All rights reserved' from Microsoft copyright statements (#12722) (Thanks @xtqqczze!)</li>
<li>IDictionary -&gt; IDictionary&lt;string, FunctionInfo&gt; for FunctionTable (#12658) (Thanks @powercode!)</li>
</ul>

</details>

### Tools

- Use correct isError parameter with Write-Log (#12989)
- Disable `NonPrivateReadonlyFieldsMustBeginWithUpperCaseLetter` rule in `StyleCop` (#12855) (Thanks @xtqqczze!)
- Add @TylerLeonhardt to PowerShell team list to correct changelog generation (#12927)
- Enable the upload of `ETW` traces to `CLR CAP` in Windows daily build (#12890)
- Prevent GitHub workflow for daily dotnet build updates from running in forks (#12763) (Thanks @bergmeister!)
- Add GitHub action for PR creation and `Wix` file generation logic (#12748)

### Tests

- Remove duplicate tests from `Measure-Object.Tests.ps1` (#12683) (Thanks @sethvs!)
- Fix tests to not write errors to console (#13010)
- Make sure tabcompletion tests run (#12981)
- Remove dependency on DNS for `Test-Connection` tests on macOS (#12943)
- Restore `markdownlint` tests (#12549) (Thanks @xtqqczze!)
- Wrap tests in pester blocks (#12700) (Thanks @xtqqczze!)

### Build and Packaging Improvements

<details>

<summary>

<p>We thank the following contributors!</p>
<p>@iSazonov, @kvprasoon, @Saancreed, @heaths, @xtqqczze</p>

</summary>

<ul>
<li>Update Distribution_Request.md</li>
<li>Bump NJsonSchema from 10.1.15 to 10.1.16 (#12685)</li>
<li>Disable uploading Symbols package (#12687)</li>
<li>Update .NET SDK version from <code>5.0.100-preview.5.20279.10</code> to <code>5.0.100-preview.6.20318.15</code> (#13018)</li>
<li>Remove component ref when re-generating the wix file (#13019)</li>
<li>Make sure icons are added to MSI staging folder (#12983)</li>
<li>Update <code>DotnetRutimeMetadata.json</code> to point to preview 6 (#12972)</li>
<li>Bump PSReadLine from <code>2.0.1</code> to <code>2.0.2</code> (#12909)</li>
<li>Bump <code>NJsonSchema</code> from 10.1.18 to 10.1.21 (#12944)</li>
<li>Check if Azure Blob exists before overwriting (#12921)</li>
<li>Enable skipped tests (#12894) (Thanks @iSazonov!)</li>
<li>Fix break in package build by pinning <code>ffi</code> version to <code>1.12</code> (#12889)</li>
<li>Upgrade <code>APIScan</code> version (#12876)</li>
<li>Make contributors unique in Release notes (#12878) (Thanks @kvprasoon!)</li>
<li>Update Linux daily CI to run in a single agent &amp; collect traces (#12866)</li>
<li>Update .NET SDK version from <code>5.0.100-preview.5.20278.13</code> to <code>5.0.100-preview.5.20279.10</code> (#12844) (Thanks @github-actions[bot]!)</li>
<li>Sign the <code>MSIX</code> files for the store (#12582)</li>
<li>Update the CI builds (#12830)</li>
<li>Update .NET SDK version from <code>5.0.100-preview.5.20272.6</code> to <code>5.0.100-preview.5.20278.13</code> (#12772) (Thanks @github-actions[bot]!)</li>
<li>Allow use of build module on unknown Linux distros (#11146) (Thanks @Saancreed!)</li>
<li>Fix MSI upgrade and shortcut issues (#12792) (Thanks @heaths!)</li>
<li>Bump NJsonSchema from 10.1.17 to 10.1.18 (#12812)</li>
<li>Update .NET SDK version from <code>5.0.100-preview.5.20269.29</code> to <code>5.0.100-preview.5.20272.6</code> (#12759) (Thanks @github-actions[bot]!)</li>
<li>Bump NJsonSchema from 10.1.16 to 10.1.17 (#12761)</li>
<li>Update to dotnet SDK 5.0.0-preview.5.20268.9 (#12740)</li>
<li>Remove <code>assets\license.rtf</code> (#12721) (Thanks @xtqqczze!)</li>
<li>Bump <code>Microsoft.CodeAnalysis.CSharp</code> from <code>3.5.0</code> to <code>3.6.0</code> (#12731)</li>
</ul>

</details>

### Documentation and Help Content

- Update `README` and `metadata` files for next release (#12717)
- Update `README.md` removing experimental status of `Arm` builds, but `Win-Arm64` is still preview for Stable release. (#12707)
- Add link to Github compare in changelog (#12713) (Thanks @xtqqczze!)
- Added missing changelog for v7.1.0-preview.2 (#12665)
- Update required Visual Studio version in build docs (#12628) (Thanks @xtqqczze!)
- minor update to Distribution_Request.md (#12705) (Thanks @kilasuit!)
- Update docs.microsoft.com links (#12653) (Thanks @xtqqczze!)
- Update change log for `6.2.5` release (#12670)
- Update `README.md` and `metadata.json` for next release (#12668)
- Merge 7.0.1 change log (#12669)
- Remove markdown unused definitions (#12656) (Thanks @xtqqczze!)
- Add HoloLens to list of PowerShell adopters (#12940) (Thanks @reynoldsbd!)
- Update `README.md` and `metadata.json` for next releases (#12939)
- Fix broken link in `README.md` (#12887) (Thanks @xtqqczze!)
- Minor typo corrections in Distribution Request Issue Templates (#12744) (Thanks @corbob!)
- Correct 'review-for-comments' in `Governance.md` (#11035) (Thanks @MarvTheRobot!)
- Fix markdown ordered lists (#12657) (Thanks @xtqqczze!)
- Fix broken `docs.microsoft.com` link (#12776) (Thanks @xtqqczze!)
- Replace link to Slack with link to PowerShell Virtual User Group (#12786) (Thanks @xtqqczze!)
- Update `LICENSE.txt` so that it's recognized as MIT (#12729)

## [7.1.0-preview.3] - 2020-05-14

### Breaking Changes

- Fix string parameter binding for `BigInteger` numeric literals (#11634) (Thanks @vexx32!)

### Engine Updates and Fixes

- Set correct `PSProvider` full name at module load time (#11813) (Thanks @iSazonov!)

### Experimental Features

- Support passing `PSPath` to native commands (#12386)

### General Cmdlet Updates and Fixes

- Fix incorrect index in format string in ParameterBinderBase (#12630) (Thanks @powercode!)
- Copy the `CommandInfo` property in `Command.Clone()` (#12301) (Thanks @TylerLeonhardt!)
- Apply `-IncludeEqual` in `Compa-Object` when `-ExcludeDifferent` is specified (#12317) (Thanks @davidseibel!)
- Change `Get-FileHash` to close file handles before writing output (#12474) (Thanks @HumanEquivalentUnit!)
- Fix inconsistent exception message in `-replace` operator (#12388) (Thanks @jackdcasey!)

### Code Cleanup

<details>

<summary>

<p>We thank the following contributors!</p>
<p>@xtqqczze, @RDIL, @powercode, @xtqqczze, @xtqqczze</p>

</summary>

<ul>
<li>Replace Unicode <code>non-breaking space</code> character with space (#12576) (Thanks @xtqqczze!)</li>
<li>Remove unused <code>New-DockerTestBuild.ps1</code> (#12610) (Thanks @RDIL!)</li>
<li>Annotate <code>Assert</code> methods for better code analysis (#12618) (Thanks @powercode!)</li>
<li>Use correct casing for cmdlet names and parameters in *.ps1 files throughout the codebase (#12584) (Thanks @xtqqczze!)</li>
<li>Document why <code>PackageVersion</code> is used in <code>PowerShell.Common.props</code> (#12523) (Thanks @xtqqczze!)</li>
</ul>

</details>

### Tools

- Update `@PoshChan` config to include `SSH` (#12526) (Thanks @vexx32!)
- Update log message in `Start-PSBootstrap` (#12573) (Thanks @xtqqczze!)
- Add the `.NET SDK` installation path to the current process path in `tools/UpdateDotnetRuntime.ps1` (#12525)

### Tests

- Make CIM tab completion test case insensitive (#12636)
- Mark ping tests as Pending due to stability issues in macOS (#12504)

### Build and Packaging Improvements

<details>

<summary>

<p>We thank the following contributors!</p>
<p>@jcotton42, @iSazonov, @iSazonov, @iSazonov</p>

</summary>

<ul>
<li>Update build to use the new .NET SDK <code>5.0.100-preview.4.20258.7</code> (#12637)</li>
<li>Bump NJsonSchema from 10.1.14 to 10.1.15 (#12608)</li>
<li>Bump NJsonSchema from 10.1.13 to 10.1.14 (#12598)</li>
<li>Bump NJsonSchema from 10.1.12 to 10.1.13 (#12583)</li>
<li>Update the build to sign any unsigned files as 3rd party Dlls (#12581)</li>
<li>Update .NET SDK to <code>5.0.100-preview.4.20229.10</code> (#12538)</li>
<li>Add ability to <code>Install-Dotnet</code> to specify directory (#12469)</li>
<li>Allow <code>/</code> in relative paths for <code>using module</code> (#7424) (#12492) (Thanks @jcotton42!)</li>
<li>Update dotnet metadata for next channel for automated updates (#12502)</li>
<li>Bump .NET to 5.0.0-preview.4 (#12507)</li>
<li>Bump <code>Microsoft.ApplicationInsights</code> from <code>2.13.1</code> to <code>2.14.0</code> (#12479)</li>
<li>Bump PackageManagement from 1.4.6 to 1.4.7 in /src/Modules (#12506)</li>
<li>Bump <code>Xunit.SkippableFact</code> from <code>1.3.12</code> to <code>1.4.8</code> (#12480)</li>
<li>Fix quotes to allow variable expansion (#12512)</li>
<li>Use new <code>TargetFramework</code> as <code>net5.0</code> in packaging scripts (#12503) (Thanks @iSazonov!)</li>
<li>Use new value for <code>TargetFramework</code> as <code>net5.0</code> instead of <code>netcoreapp5.0</code> (#12486) (Thanks @iSazonov!)</li>
<li>Disable <code>PublishReadyToRun</code> for framework dependent packages (#12450)</li>
<li>Add <code>dependabot</code> rules to ignore updates from .NET (#12466)</li>
<li>Update <code>README.md</code> and <code>metadata.json</code> for upcoming release (#12441)</li>
<li>Turn on <code>ReadyToRun</code> (#12361) (Thanks @iSazonov!)</li>
<li>Add summary to compressed sections of change log (#12429)</li>
</ul>

</details>

### Documentation and Help Content

- Add link to life cycle doc to distribution request template (#12638)
- Update TFM reference in build docs (#12514) (Thanks @xtqqczze!)
- Fix broken link for blogs in documents (#12471)

## [7.1.0-preview.2] - 2020-04-23

### Breaking Changes

- On Windows, `Start-Process` creates a process environment with
  all the environment variables from current session,
  using `-UseNewEnvironment` creates a new default process environment (#10830) (Thanks @iSazonov!)
- Do not wrap return result to `PSObject` when converting ScriptBlock to delegate (#10619)

### Engine Updates and Fixes

- Allow case insensitive paths for determining `PSModulePath` (#12192)
- Add PowerShell version 7.0 to compatible version list (#12184)
- Discover assemblies loaded by `Assembly.Load(byte[])` and `Assembly.LoadFile` (#12203)

### General Cmdlet Updates and Fixes

- Fix `WinCompat` module loading to treat PowerShell 7 modules with higher priority (#12269)
- Implement `ForEach-Object -Parallel` runspace reuse (#12122)
- Fix `Get-Service` to not modify collection while enumerating it (#11851) (Thanks @NextTurn!)
- Clean up the IPC named pipe on PowerShell exit (#12187)
- Fix `<img />` detection regex in web cmdlets (#12099) (Thanks @vexx32!)
- Allow shorter signed hex literals with appropriate type suffixes (#11844) (Thanks @vexx32!)
- Update `UseNewEnvironment` parameter behavior of `Start-Process` cmdlet on Windows (#10830) (Thanks @iSazonov!)
- Add `-Shuffle` switch to `Get-Random` command (#11093) (Thanks @eugenesmlv!)
- Make `GetWindowsPowerShellModulePath` compatible with multiple PS installations (#12280)
- Fix `Start-Job` to work on systems that don't have Windows PowerShell registered as default shell (#12296)
- Specifying an alias and `-Syntax` to `Get-Command` returns the aliased commands syntax (#10784) (Thanks @ChrisLGardner!)
- Make CSV cmdlets work when using `-AsNeeded` and there is an incomplete row (#12281) (Thanks @iSazonov!)
- In local invocations, do not require `-PowerShellVersion 5.1` for `Get-FormatData` in order to see all format data. (#11270) (Thanks @mklement0!)
- Added Support For Big Endian `UTF-32` (#11947) (Thanks @NoMoreFood!)
- Fix possible race that leaks PowerShell object dispose in `ForEach-Object -Parallel` (#12227)
- Add `-FromUnixTime` to `Get-Date` to allow Unix time input (#12179) (Thanks @jackdcasey!)
- Change default progress foreground and background colors to provide improved contrast (#11455) (Thanks @rkeithhill!)
- Fix `foreach -parallel` when current drive is not available (#12197)
- Do not wrap return result to `PSObject` when converting `ScriptBlock` to `delegate` (#10619)
- Don't write DNS resolution errors on `Test-Connection -Quiet` (#12204) (Thanks @vexx32!)
- Use dedicated threads to read the redirected output and error streams from the child process for out-of-proc jobs (#11713)

### Code Cleanup

<details>

<summary>

<p>We thank the following contributors!</p>
<p>@ShaydeNofziger, @RDIL</p>

</summary>

<ul>
<li>Fix erroneous comment in <code>tokenizer.cs</code> (#12206) (Thanks @ShaydeNofziger!)</li>
<li>Fix terms checker issues (#12189)</li>
<li>Update copyright notice to latest guidance (#12190)</li>
<li>CodeFactor cleanup (#12251) (Thanks @RDIL!)</li>
</ul>

</details>

### Tools

- Update .NET dependency update script to include test `csproj` files (#12372)
- Scripts to update to .NET prerelease version (#12284)

### Tests

- Pin major Pester version to 4 to prevent breaking changes caused by upcoming release of v5 (#12262) (Thanks @bergmeister!)

### Build and Packaging Improvements

<details>

<summary>

<p>We thank the following contributors!</p>
<p>@rkitover, @bergmeister</p>

</summary>

<ul>
<li>Add the <code>nuget.config</code> from root to the temporary build folder (#12394)</li>
<li>Bump System.IO.Packaging (#12365)</li>
<li>Bump Markdig.Signed from 0.18.3 to 0.20.0 (#12379)</li>
<li>Bump to .NET 5 Preview 3 pre-release (#12353)</li>
<li>Bump PowerShellGet from 2.2.3 to 2.2.4 (#12342)</li>
<li>Linux: Initial support for Gentoo installations. (#11429) (Thanks @rkitover!)</li>
<li>Upgrade to .NET 5 Preview 2 (#12250) (Thanks @bergmeister!)</li>
<li>Fix the <code>Sync PSGalleryModules to Artifacts</code> build (#12277)</li>
<li>Bump PSReadLine from 2.0.0 to 2.0.1 (#12243)</li>
<li>Bump <code>NJsonSchema</code> from <code>10.1.11</code> to <code>10.1.12</code> (#12230)</li>
<li>Update change log generation script to support collapsible sections (#12214)</li>
</ul>

</details>

### Documentation and Help Content

- Add documentation for `WebResponseObject` and `BasicHtmlWebResponseObject` properties (#11876) (Thanks @kevinoid!)
- Add Windows 10 IoT Core reference in `Adopters.md` (#12266) (Thanks @parameshbabu!)
- Update `README.md` and `metadata.json` for `7.1.0-preview.1` (#12211)

## [7.1.0-preview.1] - 2020-03-26

### Breaking Changes

- Use invariant culture string conversion for `-replace` operator (#10954) (Thanks @iSazonov!)

### Engine Updates and Fixes

- Revert the PRs that made `DBNull.Value` and `NullString.Value` treated as `$null` (#11648)

### Experimental Features

- Use invariant culture string conversion for `-replace` operator (#10954) (Thanks @iSazonov!)

### General Cmdlet Updates and Fixes

- Fix an operator preference order issue in binder code (#12075) (Thanks @DamirAinullin!)
- Fix `NullReferenceException` when binding common parameters of type `ActionPreference` (#12124)
- Fix default formatting for deserialized `MatchInfo` (#11728) (Thanks @iSazonov!)
- Use asynchronous streams in `Invoke-RestMethod` (#11095) (Thanks @iSazonov!)
- Address UTF-8 Detection In `Get-Content -Tail` (#11899) (Thanks @NoMoreFood!)
- Handle the `IOException` in `Get-FileHash` (#11944) (Thanks @iSazonov!)
- Change `PowerShell Core` to `PowerShell` in a resource string (#11928) (Thanks @alexandair!)
- Bring back `MainWindowTitle` in `PSHostProcessInfo` (#11885) (Thanks @iSazonov!)
- Miscellaneous minor updates to Windows Compatibility (#11980)
- Fix `ConciseView` to split `PositionMessage` using `[Environment]::NewLine` (#12010)
- Remove network hop restriction for interactive sessions (#11920)
- Fix `NullReferenceException` in `SuspendStoppingPipeline()` and `RestoreStoppingPipeline()` (#11870) (Thanks @iSazonov!)
- Generate GUID for `FormatViewDefinition` `InstanceId` if not provided (#11896)
- Fix `ConciseView` where error message is wider than window width and doesn't have whitespace (#11880)
- Allow cross-platform `CAPI-compatible` remote key exchange (#11185) (Thanks @silijon!)
- Fix error message (#11862) (Thanks @NextTurn!)
- Fix `ConciseView` to handle case where there isn't a console to obtain the width (#11784)
- Update `CmsCommands` to use Store vs certificate provider (#11643) (Thanks @mikeTWC1984!)
- Enable `pwsh` to work on Windows systems where `mpr.dll` and STA is not available (#11748)
- Refactor and implement `Restart-Computer` for `Un*x` and macOS (#11319)
- Add an implementation of `Stop-Computer` for Linux and macOS (#11151)
- Fix `help` function to check if `less` is available before using (#11737)
- Update `PSPath` in `certificate_format_ps1.xml` (#11603) (Thanks @xtqqczze!)
- Change regular expression to match relation-types without quotes in Link header (#11711) (Thanks @Marusyk!)
- Fix error message during symbolic link deletion (#11331)
- Add custom `Selected.*` type to `PSCustomObject` in `Select-Object` only once (#11548) (Thanks @iSazonov!)
- Add `-AsUTC` to the `Get-Date` cmdlet (#11611)
- Fix grouping behavior with Boolean values in `Format-Hex` (#11587) (Thanks @vexx32!)
- Make `Test-Connection` always use the default synchronization context for sending ping requests (#11517)
- Correct startup error messages (#11473) (Thanks @iSazonov!)
- Ignore headers with null values in web cmdlets (#11424) (Thanks @iSazonov!)
- Re-add check for `Invoke-Command` job dispose. (#11388)
- Revert "Update formatter to not write newlines if content is empty (#11193)" (#11342) (Thanks @iSazonov!)
- Allow `CompleteInput` to return results from `ArgumentCompleter` when `AST` or Script has matching function definition (#10574) (Thanks @M1kep!)
- Update formatter to not write new lines if content is empty (#11193)

### Code Cleanup

<details>

<ul>
<li>Use span-based overloads (#11884) (Thanks @iSazonov!)</li>
<li>Use new <code>string.Split()</code> overloads (#11867) (Thanks @iSazonov!)</li>
<li>Remove unreachable DSC code (#12076) (Thanks @DamirAinullin!)</li>
<li>Remove old dead code from FullCLR (#11886) (Thanks @iSazonov!)</li>
<li>Use <code>Dictionary.TryAdd()</code> where possible (#11767) (Thanks @iSazonov!)</li>
<li>Use <code>Environment.NewLine</code> instead of hard-coded linefeed in <code>ParseError.ToString</code> (#11746)</li>
<li>Fix <code>FileSystem</code> provider error message (#11741) (Thanks @iSazonov!)</li>
<li>Reformat code according to <code>EditorConfig</code> rules (#11681) (Thanks @xtqqczze!)</li>
<li>Replace use of throw <code>GetExceptionForHR</code> with <code>ThrowExceptionForHR</code> (#11640) (Thanks @xtqqczze!)</li>
<li>Refactor delegate types to lambda expressions (#11690) (Thanks @xtqqczze!)</li>
<li>Remove Unicode BOM from text files (#11546) (Thanks @xtqqczze!)</li>
<li>Fix Typo in <code>Get-ComputerInfo</code> cmdlet description (#11321) (Thanks @doctordns!)</li>
<li>Fix typo in description for <code>Get-ExperimentalFeature</code> <code>PSWindowsPowerShellCompatibility</code> (#11282) (Thanks @alvarodelvalle!)</li>
<li>Cleanups in command discovery (#10815) (Thanks @iSazonov!)</li>
<li>Review <code>CurrentCulture</code> (#11044) (Thanks @iSazonov!)</li>
</ul>

</details>

### Tools

- Change recommended VS Code extension name from `ms-vscode.csharp` to `ms-dotnettools.csharp` (#12083) (Thanks @devlead!)
- Specify `csharp_preferred_modifier_order` in `EditorConfig` (#11775) (Thanks @xtqqczze!)
- Update `.editorconfig` (#11675) (Thanks @xtqqczze!)
- Enable `EditorConfig` support in `OmniSharp` (#11627) (Thanks @xtqqczze!)
- Specify charset in `.editorconfig` as `utf-8` (no BOM) (#11654) (Thanks @xtqqczze!)
- Configure the issue label bot (#11527)
- Avoid variable names that conflict with automatic variables (#11392) (Thanks @xtqqczze!)

### Tests

- Add empty `preview.md` file to fix broken link (#12041)
- Add helper functions for SSH remoting tests (#11955)
- Add new tests for `Get-ChildItem` for `FileSystemProvider` (#11602) (Thanks @iSazonov!)
- Ensure that types referenced by `PowerShellStandard` are present (#10634)
- Check state and report reason if it's not "opened" (#11574)
- Fixes for running tests on Raspbian (#11661)
- Unify pester test syntax for the arguments of `-BeOfType`  (#11558) (Thanks @xtqqczze!)
- Correct casing for automatic variables (#11568) (Thanks @iSazonov!)
- Avoid variable names that conflict with automatic variables part 2 (#11559) (Thanks @xtqqczze!)
- Update pester syntax to v4 (#11544) (Thanks @xtqqczze!)
- Allow error 504 (Gateway Timeout) in `markdown-link` tests (#11439) (Thanks @xtqqczze!)
- Re-balance CI tests (#11420) (Thanks @iSazonov!)
- Include URL in the markdown-links test error message (#11438) (Thanks @xtqqczze!)
- Use CIM cmdlets instead of WMI cmdlets in tests (#11423) (Thanks @xtqqczze!)

### Build and Packaging Improvements

<details>

<ul>
<li>Put symbols in separate package (#12169)</li>
<li>Disable <code>x86</code> PDB generation (#12167)</li>
<li>Bump <code>NJsonSchema</code> from <code>10.1.5</code> to <code>10.1.11</code> (#12050) (#12088) (#12166)</li>
<li>Create <code>crossgen</code> symbols for Windows <code>x64</code> and <code>x86</code> (#12157)</li>
<li>Move to <code>.NET 5 preview.1</code> (#12140)</li>
<li>Bump <code>Microsoft.CodeAnalysis.CSharp</code> from <code>3.4.0</code> to <code>3.5.0</code> (#12136)</li>
<li>Move to standard internal pool for building (#12119)</li>
<li>Fix package syncing to private Module Feed  (#11841)</li>
<li>Add Ubuntu SSH remoting tests CI (#12033)</li>
<li>Bump <code>Markdig.Signed</code> from <code>0.18.1</code> to <code>0.18.3</code> (#12078)</li>
<li>Fix MSIX packaging to determine if a Preview release by inspecting the semantic version string (#11991)</li>
<li>Ignore last exit code in the build step as <code>dotnet</code> may return error when SDK is not installed (#11972)</li>
<li>Fix daily package build (#11882)</li>
<li>Fix package sorting for syncing to private Module Feed (#11838)</li>
<li>Set <code>StrictMode</code> version <code>3.0</code> (#11563) (Thanks @xtqqczze!)</li>
<li>Bump <code>.devcontainer</code> version to dotnet <code>3.1.101</code> (#11707) (Thanks @Jawz84!)</li>
<li>Move to version 3 of <code>AzFileCopy</code> (#11697)</li>
<li>Update <code>README.md</code> and <code>metadata.json</code> for next release (#11664)</li>
<li>Code Cleanup for environment data gathering in <code>build.psm1</code> (#11572) (Thanks @xtqqczze!)</li>
<li>Update Debian Install Script To Support Debian 10 (#11540) (Thanks @RandomNoun7!)</li>
<li>Update <code>ADOPTERS.md</code> (#11261) (Thanks @edyoung!)</li>
<li>Change back to use powershell.exe in 'SetVersionVariables.yml' to unblock daily build (#11207)</li>
<li>Change to use pwsh to have consistent JSON conversion for <code>DateTime</code> (#11126)</li>
</ul>

</details>

### Documentation and Help Content

- Replace `VSCode` link in `CONTRIBUTING.md` (#11475) (Thanks @stevend811!)
- Remove the version number of PowerShell from LICENSE (#12019)
- Add the 7.0 change log link to `CHANGELOG/README.md` (#12062) (Thanks @LabhanshAgrawal!)
- Improvements to the contribution guide (#12086) (Thanks @ShaydeNofziger!)
- Update the doc about debugging dotnet core in VSCode (#11969)
- Update `README.md` and `metadata.json` for the next release (#11918) (#11992)
- Update `Adopters.md` to include info on Azure Pipelines and GitHub Actions (#11888) (Thanks @alepauly!)
- Add information about how Amazon AWS uses PowerShell. (#11365) (Thanks @bpayette!)
- Add link to .NET CLI version in build documentation (#11725) (Thanks @joeltankam!)
- Added info about `DeploymentScripts` in `ADOPTERS.md` (#11703)
- Update `CHANGELOG.md` for `6.2.4` release (#11699)
- Update `README.md` and `metadata.json` for next release (#11597)
- Update the breaking change definition (#11516)
- Adding System Frontier to the PowerShell Core adopters list `ADOPTERS.md` (#11480) (Thanks @OneScripter!)
- Update `ChangeLog`, `README.md` and `metadata.json` for `7.0.0-rc.1` release (#11363)
- Add `AzFunctions` to `ADOPTERS.md` (#11311) (Thanks @Francisco-Gamino!)
- Add `Universal Dashboard` to `ADOPTERS.md` (#11283) (Thanks @adamdriscoll!)
- Add `config.yml` for `ISSUE_TEMPLATE` so that Doc, Security, Support, and Windows PowerShell issues go to URLs (#11153)
- Add `Adopters.md` file (#11256)
- Update `Readme.md` for `preview.6` release (#11108)
- Update `SUPPORT.md` (#11101) (Thanks @mklement0!)
- Update `README.md` (#11100) (Thanks @mklement0!)

[7.1.0-preview.5]: https://github.com/PowerShell/PowerShell/compare/v7.1.0-preview.4...v7.1.0-preview.5
[7.1.0-preview.4]: https://github.com/PowerShell/PowerShell/compare/v7.1.0-preview.3...v7.1.0-preview.4
[7.1.0-preview.3]: https://github.com/PowerShell/PowerShell/compare/v7.1.0-preview.2...v7.1.0-preview.3
[7.1.0-preview.2]: https://github.com/PowerShell/PowerShell/compare/v7.1.0-preview.1...v7.1.0-preview.2
[7.1.0-preview.1]: https://github.com/PowerShell/PowerShell/compare/v7.0.0-preview.6...v7.1.0-preview.1

