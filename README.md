# MajdataEdit Neo

MajdataEdit Neo is a desktop editor for **maimai Simai charts**. It provides a text editor for chart data, chart metadata and timing controls, and tools for previewing a chart alongside its music.

## Requirements

- .NET 10 SDK
- A desktop environment supported by Avalonia
- MajdataPlay for the player connection and playback preview

The app currently connects to MajdataPlay at `ws://127.0.0.1:8083/majdata`.

## Build and run

From the repository root:

```sh
dotnet restore MajdataEdit-Neo.sln
dotnet build MajdataEdit-Neo.sln
dotnet run --project MajdataEdit-Neo.csproj
```

Open a chart by selecting its `maidata.txt` file. The app looks for the chart's music and optional background media in the same directory. For file names and integration details, see [log/info.md](log/info.md).

## Project layout

- `Views/`, `ViewModels/`, and `Controls/` contain the Avalonia user interface and its presentation logic.
- `Models/` contains chart, media, file, and player-connection logic.
- `Modules/AutoSave/` contains the reusable autosave module.
- `Assets/` contains application resources.

## License

See [LICENSE](LICENSE).