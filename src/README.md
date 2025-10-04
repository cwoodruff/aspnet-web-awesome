# ASPNET-Web-Awesome

A sample ASP.NET Core Razor Pages application demonstrating integration with Web Awesome (Font Awesome) web components.

## Prerequisites

- .NET 9.0 SDK or later
- LibMan CLI (for installing Font Awesome)

## Getting Started

### 1. Restore NuGet packages

```bash
cd src
dotnet restore
```

### 2. Install Font Awesome (Web Awesome) using LibMan

```bash
cd src/ASPNET-Web-Awesome
libman restore
```

If you don't have LibMan CLI installed, install it first:

```bash
dotnet tool install -g Microsoft.Web.LibraryManager.Cli
```

### 3. Build and run the application

```bash
cd src
dotnet build
dotnet run --project ASPNET-Web-Awesome
```

The application will be available at `https://localhost:5001` or `http://localhost:5000`.

## Web Awesome Integration

This project integrates Font Awesome (also known as Web Awesome) for icon support. The integration is configured in:

- **Layout**: `Pages/Shared/_Layout.cshtml` - includes Font Awesome CSS
- **LibMan**: `libman.json` - manages Font Awesome library installation
- **Demo**: `Pages/Index.cshtml` - demonstrates Font Awesome icon usage

### Manual Installation (Alternative)

If `libman restore` doesn't work due to network restrictions, you can manually download Font Awesome:

1. Download Font Awesome from https://fontawesome.com/download
2. Extract the zip file
3. Copy the contents to `wwwroot/lib/font-awesome/`

The directory structure should be:
```
wwwroot/lib/font-awesome/
├── css/
│   └── all.min.css
└── webfonts/
    ├── fa-brands-400.woff2
    ├── fa-brands-400.ttf
    ├── fa-regular-400.woff2
    ├── fa-regular-400.ttf
    ├── fa-solid-900.woff2
    └── fa-solid-900.ttf
```

## Project Structure

```
ASPNET-Web-Awesome/
├── Pages/
│   ├── Shared/
│   │   └── _Layout.cshtml
│   ├── Index.cshtml
│   ├── Privacy.cshtml
│   └── Error.cshtml
├── wwwroot/
│   ├── css/
│   ├── js/
│   └── lib/
│       └── font-awesome/
├── libman.json
├── appsettings.json
└── Program.cs
```

## License

MIT License - See LICENSE file for details.
