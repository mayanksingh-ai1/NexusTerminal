# WPF Desktop Host — next stage

The current deliverable runs as a local browser prototype. The Windows-native host is intentionally not scaffolded with package references yet, to avoid presenting an untested WebView2 shell as complete. Next step: create a WPF .NET 8 project, add Microsoft.Web.WebView2, point the WebView to the local UI assets, and then move exchange/risk logic into C# services.
